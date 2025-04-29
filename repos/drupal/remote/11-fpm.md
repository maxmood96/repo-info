## `drupal:11-fpm`

```console
$ docker pull drupal@sha256:61acabd1864f5b97180120973d868327ec5334cba40f4d42209f5053c603e31d
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

### `drupal:11-fpm` - linux; amd64

```console
$ docker pull drupal@sha256:44981de578e2d7b2cc0aa910236c73b1daee6810556e1355f9abced1dea18ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195843139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1647df88edc49bb30dd502c2972171a3d7e18031486bb1dd1d1040c6ba070c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.3.20
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c87c15113d85f4c22b0e0eeb60c0133cec0a644c93df8ea4cce3b58914bdfa`  
		Last Modified: Mon, 28 Apr 2025 21:54:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7e72810f6381a4ac5bb94aee61b5b9fc04828ba83d6eefcfd482deabfa0666`  
		Last Modified: Mon, 28 Apr 2025 21:54:17 GMT  
		Size: 104.3 MB (104325257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e7b460a4bdc7bec868d0b694682988d6243690ad6c7b329d27be906b3e61af`  
		Last Modified: Mon, 28 Apr 2025 21:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7a2294186d6642bdd95b6404ca55391dac18a54b4d2830ba6ebf840b2a045d`  
		Last Modified: Mon, 28 Apr 2025 21:54:16 GMT  
		Size: 12.7 MB (12658348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c943d13d0aa4755204f8c40e039ec8110cf4247f8fad00ac543ae6726a413dca`  
		Last Modified: Mon, 28 Apr 2025 21:54:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91af39dbce2f5f4f1757db58e5a2e942af8660d05f4aa12a040d1c1cef3fb15`  
		Last Modified: Mon, 28 Apr 2025 21:54:16 GMT  
		Size: 27.8 MB (27827318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c70e19de0368362b4d1480aa3be64c8f2f39038507b3dfa6b9233fdd51266b`  
		Last Modified: Mon, 28 Apr 2025 21:54:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57731ba0321bd4651d6acfffc859db2480cd662ba770d8c87a7a4294806e48b4`  
		Last Modified: Mon, 28 Apr 2025 21:54:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa96857e26af97e6463cf9457893d3fb0b7652f2560c6eb93a65825690620ccd`  
		Last Modified: Mon, 28 Apr 2025 21:54:18 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52fa16298ace6a6898e126b4b026531d49448258ebe433a8de75d4a318c9817`  
		Last Modified: Mon, 28 Apr 2025 22:17:08 GMT  
		Size: 2.0 MB (1976757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a113b6db5f45341cc49752c089d1d9fe7fb3418a453b0e5d616295b9c33a3ff0`  
		Last Modified: Mon, 28 Apr 2025 22:17:07 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaf3d3b1c1783d565e95137483f4179e7f65d13281f34c78b63dd1bdd570eda`  
		Last Modified: Mon, 28 Apr 2025 22:17:08 GMT  
		Size: 750.6 KB (750624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b29637dc7404159e206e751af44ab570f4bce936e3f2dbfe898fd30a780578a`  
		Last Modified: Mon, 28 Apr 2025 22:17:07 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d071b44291fcc9a0c24712f9c250228559c01fca072e0951fb9665d058c0d63c`  
		Last Modified: Mon, 28 Apr 2025 22:17:10 GMT  
		Size: 20.1 MB (20063924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:d40b1f074b7da1dee50a4b291c7992dd352705f0bcdb6057cdf5d56f47b8f840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6380874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a743c2acef500f8159efaf2d6c379d1a6f8ca46c4a23f5b91397ed54229c5ad`

```dockerfile
```

-	Layers:
	-	`sha256:956beeecddbfc9a8b2605f75ddbaac11beafade38f05bde4d8b915039f6667e4`  
		Last Modified: Mon, 28 Apr 2025 22:17:08 GMT  
		Size: 6.3 MB (6343491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eab19563769f33e36d0cb67a55f3a6978421f46be8f0170ab3cad101276a265`  
		Last Modified: Mon, 28 Apr 2025 22:17:07 GMT  
		Size: 37.4 KB (37383 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ed265433bd4a43549eb13f9410edf0b9ff26d09b33fd20b0e2b5ef8b9fe20bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160323003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39a7b4167bb00c1f3afdf090dc1f336d56ce3b2ebee98081c180cdc8c4e1bc8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.3.20
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4b097a6bd1e1c6005148baf6fe5c3fc8f71c3806b0533176b9e71d30fae09`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b59a7abdeed6ca1e9edaa9c4d716d1e51f3acd76ac9b8a9593379251477a15`  
		Last Modified: Tue, 08 Apr 2025 02:06:14 GMT  
		Size: 76.2 MB (76162685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e77faae9141f2a82370cde20bb002409354ce3554b28663322cebbfd4d775`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95b007d63693a137d0530e05acff194ffbec67d707ffca14557868ca4200791`  
		Last Modified: Fri, 11 Apr 2025 18:10:14 GMT  
		Size: 12.7 MB (12656445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c0df582645b730071b5782f9ec1dbaedcb05431cd5bbee6c9a246f1c2dc79f`  
		Last Modified: Fri, 11 Apr 2025 18:10:13 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5dbce30b48b91803678f9e60f587c59fb00aed69f4d1334fccb7c1954d195d`  
		Last Modified: Fri, 11 Apr 2025 18:17:35 GMT  
		Size: 25.4 MB (25406826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88462611138e8d046e509465fd4dcd738d2299d77106d5ae0e5cc8dc11213d11`  
		Last Modified: Fri, 11 Apr 2025 18:17:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce177622e3597e6b7e63d8d92e154db4a9514921b2858e73c997b460e70884`  
		Last Modified: Fri, 11 Apr 2025 18:17:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077f263de673fcae80aa5866950cba9dfec979dab7306166a04c0cd07131290`  
		Last Modified: Fri, 11 Apr 2025 18:17:34 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fbd5c597f8be666e97880eccb840519f2763d384275ce7c7ada56644778e51`  
		Last Modified: Fri, 11 Apr 2025 20:30:43 GMT  
		Size: 1.3 MB (1331385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a327454dabe4c5b28b66839b68ddb3b0844c88f94808f2f76f6ff48b5242437d`  
		Last Modified: Fri, 11 Apr 2025 20:30:43 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4c54a03709d3e6c2f692f352d736a8650ef9f3548b4f7216a861170bce2293`  
		Last Modified: Fri, 11 Apr 2025 20:30:43 GMT  
		Size: 750.6 KB (750618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe0cc3694e8830fbac18824217b5bc5e22ac8d706ac1ccec2e5939c41edf338`  
		Last Modified: Fri, 11 Apr 2025 20:30:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02af7e07cff818879248969ac52149dc92ce13592c2ce78336542e4d985ac912`  
		Last Modified: Fri, 11 Apr 2025 20:30:45 GMT  
		Size: 20.1 MB (20063901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:ed9d768e740d0092bf212aef1df4ba5588f5da73e13e1d24c11a96c1be20582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6196106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b9c890c7dd57ec1eb734916a52d84336df40bf4494c82fe29010f427bc0e02`

```dockerfile
```

-	Layers:
	-	`sha256:277c39a1b1c8ddf733ebf6bd209cf3480df5fe1da648cde2715a6e6c6feadeb5`  
		Last Modified: Fri, 11 Apr 2025 20:30:43 GMT  
		Size: 6.2 MB (6158509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211dcad5d9b39b38af6e96797705b1fd8b71e63bc44cb88de8e1e64604f477f4`  
		Last Modified: Fri, 11 Apr 2025 20:30:42 GMT  
		Size: 37.6 KB (37597 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:29ebaf9caf93d9d8989c822df0be4a2230d9b5278ce841cd387a438952168680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.7 MB (189693228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34e65e02148b3c1a76403c4ac7537a0298b41635cb18757082401069669f3c4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.3.20
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c5f6dffca44b4205f0e945a57290bb8e3e1ae585f26eccc2c9828d7f9ccda`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc8e5730fe526cc83387586aee6b7883edb46c1cbf4028dd372d5e9cc4aa7ec`  
		Last Modified: Tue, 08 Apr 2025 02:20:36 GMT  
		Size: 98.1 MB (98130393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28e77e2da9013ba78046a81e9835f08797c66738b7838294afd4c12822ca8c`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1e173b3d4f7a6ecb666e5808530783144c61d44ff83b32c0b9c9a20678f392`  
		Last Modified: Fri, 11 Apr 2025 17:49:21 GMT  
		Size: 12.7 MB (12658206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19826dbe8767f2bbe44fdf3395133de0ce1092769d5bf24953f1b5037b6d0403`  
		Last Modified: Fri, 11 Apr 2025 17:49:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc05c4eec7dd263d6a85fcc12639896b5a0f2c8a5bca0a5b7458fa857beea224`  
		Last Modified: Fri, 11 Apr 2025 17:57:23 GMT  
		Size: 27.8 MB (27774292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4792428ab744b600142aca44e5d53aff9674a0fe632191f05880e6d5856778dd`  
		Last Modified: Fri, 11 Apr 2025 17:57:22 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6302b4d700562a8ff9210e6eb9be1229614b7d37a6c83a9afa3f88947339684b`  
		Last Modified: Fri, 11 Apr 2025 17:57:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56eb4d4954360998d6010785e062855d8dafe2903767dc9d50cf278ea189d4f0`  
		Last Modified: Fri, 11 Apr 2025 17:57:22 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bea2d8a6d0563ce3d91a4bd0b0848eddb0cf8b7120c4eef8689a8f42e7c5b0c`  
		Last Modified: Fri, 11 Apr 2025 20:38:28 GMT  
		Size: 2.2 MB (2236192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ab4956bfb452374f92b7c3b150d0c838a12398c7010b886a643edcead2c70d`  
		Last Modified: Fri, 11 Apr 2025 20:38:28 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b42f5851be82ac18813ee57b806e75937684c4e1dcdfb37b70958be5afb0c03`  
		Last Modified: Fri, 11 Apr 2025 20:38:28 GMT  
		Size: 750.6 KB (750627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6bfb53c551c6b62a0a50ea963ce84c2beb3998cfccd6eecbfd3745de51439`  
		Last Modified: Fri, 11 Apr 2025 20:38:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1c393c3cec3f8c3ed028e2ebd01dbbe12e0ffd3acd491e48bcb65efc73a158`  
		Last Modified: Fri, 11 Apr 2025 20:38:30 GMT  
		Size: 20.1 MB (20063923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:6f7fa34eb2a20d9a9c39fbd5edfcf403ab044b7010431ebd65f073ebf01dba07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6409712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0d4abf132e6bcdfdd521540870676e6708669e0b73ca9d2cc4c2166d06930`

```dockerfile
```

-	Layers:
	-	`sha256:5e8127fcb05c23770fe3ebb253b22d0246ac9d6b78eeb02a281ba075f46ae1a0`  
		Last Modified: Fri, 11 Apr 2025 20:38:28 GMT  
		Size: 6.4 MB (6372031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1777916080fc3773577c430b447d7c0298025c2eb94b2764280357fc667a19e9`  
		Last Modified: Fri, 11 Apr 2025 20:38:28 GMT  
		Size: 37.7 KB (37681 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm` - linux; 386

```console
$ docker pull drupal@sha256:c73a14952c5729688baa3e7135a0d1c0dd215fce96f96d16df0c60edaa299312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194569508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ab52496eaf20409164608096c60676834bbe260b72eb5a18d11283d1fbdc8c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.3.20
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970756f9d5e9421bb8ba6cf4a1a57d005de52fe95a1e5e5b9049b57fb2a0d5f8`  
		Last Modified: Mon, 28 Apr 2025 21:49:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ca131f467b963a08c53ae9b038b6ffd45ce77dfceb12b35745b7f3c6cd263`  
		Last Modified: Mon, 28 Apr 2025 21:49:37 GMT  
		Size: 101.5 MB (101507837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c67a6e63575a3a9b70b4bb403c8fdf254eb73bf2f33662957047fd6c869aac`  
		Last Modified: Mon, 28 Apr 2025 21:48:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a06fc871d30304dbe17248bd963d2c3e67da28fb98a582cb0ab0af592f501`  
		Last Modified: Mon, 28 Apr 2025 21:49:35 GMT  
		Size: 12.7 MB (12657514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8394ff2b118213cb53b39595529e5758c1ecacb8151adb9660a237861bd94d04`  
		Last Modified: Mon, 28 Apr 2025 21:49:34 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd0e604590824917c76061efb460c2be87e09340c959e1aaa722933de7cacdc`  
		Last Modified: Mon, 28 Apr 2025 21:49:35 GMT  
		Size: 28.3 MB (28337005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c9034314622e4b48ad323c51d5b419b0c27756db4ee9cb1f77bb261c78b6c`  
		Last Modified: Mon, 28 Apr 2025 21:49:35 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a933bb29844ff7fc27c7a42395eeb9cab280881badfda2493c275c82e4df20`  
		Last Modified: Mon, 28 Apr 2025 21:49:36 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85ca21a0f8c243fa1e536922da0633fc9ed6103fff9925fae88cca36f72f4d5`  
		Last Modified: Mon, 28 Apr 2025 21:49:36 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14915b4b87fbe676f02f4b3c5d0f8a4a84216f309fde25baf739f64b3307edbb`  
		Last Modified: Mon, 28 Apr 2025 22:16:57 GMT  
		Size: 2.0 MB (2028988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1fa202a38b77b2fe4bba89b9d5122a073348608a5e74e023c1a2d300b3b499`  
		Last Modified: Mon, 28 Apr 2025 22:16:56 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e0179ba7eb9b8da68ddd0ed524a7954087baaa682e6e1c0a26a2c46b5bb4c5`  
		Last Modified: Mon, 28 Apr 2025 22:16:56 GMT  
		Size: 750.6 KB (750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e417ab6860daca427bbdc249014ea01b1d3db89de6e17df91e0bb9671ba9e485`  
		Last Modified: Mon, 28 Apr 2025 22:16:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6590ee8308da8b2cb79699fdac3da078c023b7cd4a91412b2b5dff44a51da`  
		Last Modified: Mon, 28 Apr 2025 22:16:58 GMT  
		Size: 20.1 MB (20063407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:0a88203c4514e8f6d0645382ff204bbee745b4c192203422d244dee7e9e6385f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6361022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8904faa5fa7c4b7debaab1cfd9e46a2e38b9344608f8ff866dc0f3a173f421a2`

```dockerfile
```

-	Layers:
	-	`sha256:bfeb532b217ea41a4a91b4c01964aee7a2e0602b24ef344a24ac89e141b909da`  
		Last Modified: Mon, 28 Apr 2025 22:16:57 GMT  
		Size: 6.3 MB (6323742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec9b6ed8cf7bfe0e7c2afb802f74b7d1d081795b61b8b8cbf0331ba829dccc2`  
		Last Modified: Mon, 28 Apr 2025 22:16:56 GMT  
		Size: 37.3 KB (37280 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm` - linux; ppc64le

```console
$ docker pull drupal@sha256:656e6dd601de54f7a918f902e30d4a27b98405e174ce04b4378cd278cf37e90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199594058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1e1be62901429fce3393e21b7dc3ab90a1fa4aa3102dd29a6cd4adb49b8495`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.3.20
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0826c2c78ee871653d0f57d9c44ce65866504115c48a8494edbe4acb9069b52`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18cc47752cabbb3e0f444ea51014859eeb381a04a9b84e453b349ceeecfef1`  
		Last Modified: Mon, 28 Apr 2025 22:29:46 GMT  
		Size: 103.3 MB (103313187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72914eeea8bb18897afc016693b242383396e76406f7363c6ba1a9be152145bc`  
		Last Modified: Mon, 28 Apr 2025 22:29:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e70c452b8a47aaea723e2d87fa1e974976830227416f4ba3824b8f5be54f91b`  
		Last Modified: Mon, 28 Apr 2025 23:18:53 GMT  
		Size: 12.7 MB (12657808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a86abd65230c6d4e22f405f76f78450f9243ba2658e2d5b0e8b0c6475d215f`  
		Last Modified: Mon, 28 Apr 2025 23:18:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fe1323e71951c61dd0ad622b4a8349d3611d042c677857f3b4d257076d54b9`  
		Last Modified: Mon, 28 Apr 2025 23:26:54 GMT  
		Size: 28.9 MB (28893864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d45df797a877d01bdb2225b87ffcb554dab447e304f79ee25ee2d628eb6cf9f`  
		Last Modified: Mon, 28 Apr 2025 23:26:53 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113cb292dc3dcae1c0d9d20804e8cd483ee832f2d204487f69c42f408dbdda30`  
		Last Modified: Mon, 28 Apr 2025 23:26:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7b623ec3b7c654ec2e3eac83427ec526b912fdf6ae446919d3f1cf36725713`  
		Last Modified: Mon, 28 Apr 2025 23:26:53 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621b0d4e8464a1e72f592dc4f5fe481022c4ff92eea8097666d5ce2bbc4fe6`  
		Last Modified: Tue, 29 Apr 2025 04:46:09 GMT  
		Size: 1.8 MB (1832810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799a1f9a6baa87686a98498b416e224856bf30f2290d0344b1bb179b24551875`  
		Last Modified: Tue, 29 Apr 2025 04:46:08 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e130cd2100169174d5b42dea0470aa7895e4f3150fa5e16525785d0baa172f36`  
		Last Modified: Tue, 29 Apr 2025 04:46:09 GMT  
		Size: 750.6 KB (750626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bde87e5424d078e2e9d6ddbcdda8522fab0866b089a69b14fc2496b11517308`  
		Last Modified: Tue, 29 Apr 2025 04:46:08 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b1bcbbeb4630209e5d7a441eeaf6f3d9b1ff164414be369e19460650e28f8a`  
		Last Modified: Tue, 29 Apr 2025 04:46:10 GMT  
		Size: 20.1 MB (20064051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:123c4bca68cce9091a8edb1ce7e58bfa9f78fe577fe1f3663264cfb49547c911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6357994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9657ccb29d57d8f4ae0c82d9aef95a1d50692e472c5081eec9f19c5e19f9bcdd`

```dockerfile
```

-	Layers:
	-	`sha256:cf46bdbfb4e4b8e154fe4c5b98ca62d8d6b8add9fd4498136b89018637378b4a`  
		Last Modified: Tue, 29 Apr 2025 04:46:09 GMT  
		Size: 6.3 MB (6320481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79cbd22fb94574d1c8adf314fb82c83e38c89e99e3720c744911c228e1cd9353`  
		Last Modified: Tue, 29 Apr 2025 04:46:08 GMT  
		Size: 37.5 KB (37513 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm` - linux; s390x

```console
$ docker pull drupal@sha256:eee14c59fee711603cf5ac53b30e18eba8d16318252c0d4c2247d555df27d768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169646578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25c36d8b77679e369b9dec97e9ed2dbc468d285dc1d0988600c589228f32a5b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 02 Apr 2025 21:27:31 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Apr 2025 21:27:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_VERSION=8.3.20
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /var/www/html
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Apr 2025 21:27:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 02 Apr 2025 21:27:31 GMT
CMD ["php-fpm"]
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV DRUPAL_VERSION=11.1.6
# Wed, 02 Apr 2025 21:27:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 02 Apr 2025 21:27:31 GMT
WORKDIR /opt/drupal
# Wed, 02 Apr 2025 21:27:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 02 Apr 2025 21:27:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b23990f9b2f689c0958e401e12177302f3c3909b95265780e0ffa1d83f07b08`  
		Last Modified: Mon, 28 Apr 2025 22:11:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7157d5c3015139f8692f9d1c1ed18e722446a58364395c431f006376ad7d71`  
		Last Modified: Mon, 28 Apr 2025 22:11:19 GMT  
		Size: 80.8 MB (80819034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3c86053dceabe42d2b50d7dce807078de19abd3debede2d77be6e7dfc238f8`  
		Last Modified: Mon, 28 Apr 2025 22:11:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85f221a3cdb2f654131d662641239a3b95afdf6a9a74e5ac2eb9a46ff5b835e`  
		Last Modified: Mon, 28 Apr 2025 22:54:50 GMT  
		Size: 12.7 MB (12656946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e94188f4e08cfd91eb37ee94923d65a023bc35ff3352d1c54f8cf128e14f03`  
		Last Modified: Mon, 28 Apr 2025 22:54:49 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55028210a0709a8cfaca21fb347ed5854e8470230356f52b354ca4ae4938b134`  
		Last Modified: Mon, 28 Apr 2025 23:01:37 GMT  
		Size: 26.9 MB (26927637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922074808654bc6286b653ebe471a41af2be30466ed20c0c4d1cbde1421c91d6`  
		Last Modified: Mon, 28 Apr 2025 23:01:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83c646880f181cf291ce1da613baf5054a420685b82e9b9f58870c47c4bbde9`  
		Last Modified: Mon, 28 Apr 2025 23:01:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6480c6309b34a00a777c2512647063c39739bdce5a40fc96eefd201fa163d5c6`  
		Last Modified: Mon, 28 Apr 2025 23:01:37 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a373bf1fb7b8cf791e6561e0871cd317895d58da2d671e6b0f12632cb115e6`  
		Last Modified: Tue, 29 Apr 2025 03:05:46 GMT  
		Size: 1.5 MB (1530242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde53347c82fa004aed2d718a62a3be273a8cdc00d924aaee7e19e49c32297e6`  
		Last Modified: Tue, 29 Apr 2025 03:05:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3597fff2fc17f4e0c2e8aaea81906988f13434632dbe6a33fe0f98ee677403d8`  
		Last Modified: Tue, 29 Apr 2025 03:05:46 GMT  
		Size: 750.6 KB (750626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169b9e49504d7936836d99a059dd2c6d4ace88a5034f9c6dea596c730b6ea35`  
		Last Modified: Tue, 29 Apr 2025 03:05:46 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4183658010966b0bca705de2bd531932d1dfd7ccfd0292d3c5d381ffa16def`  
		Last Modified: Tue, 29 Apr 2025 03:05:47 GMT  
		Size: 20.1 MB (20063954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:99b61d4bda761719aa4007d91eae8ef34dde4f7025f52054ff5c9523bad3160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f3aa8f8aa8f27833f3dc07faf462ece484cd51e526d83cb6e2d8345cdff7c6`

```dockerfile
```

-	Layers:
	-	`sha256:1721844092014bdab1e7e414c7f928be0671812f8733400ae2b9111589079efa`  
		Last Modified: Tue, 29 Apr 2025 03:05:46 GMT  
		Size: 6.2 MB (6184931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d35624c5adfc40a9437c9238188a44120c5b104a4f6c24165a309a611c5d229d`  
		Last Modified: Tue, 29 Apr 2025 03:05:46 GMT  
		Size: 37.4 KB (37377 bytes)  
		MIME: application/vnd.in-toto+json
