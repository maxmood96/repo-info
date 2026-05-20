## `drupal:11-fpm-bookworm`

```console
$ docker pull drupal@sha256:817c201a121d5719da32728b1c7570e9f6e39d5c8c6a2211cb65e30da105860d
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

### `drupal:11-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:6c4ed6a0d6f4b4b305c0c108d3838acf4bfd6a55849d6d7b40758b6bfeef40fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199867939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f481fc6bc9d0552123895b2938334bba89955d8883d73ba0b2b9aa66ad597b4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:06:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:06:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:06:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:06:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:06:32 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:10:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:12:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:12:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:12:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:12:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:12:35 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:12:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:12:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:12:36 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:12:36 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:27:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:27:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 May 2026 00:27:14 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:27:14 GMT
ENV DRUPAL_VERSION=11.3.9
# Wed, 20 May 2026 00:27:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 May 2026 00:27:14 GMT
WORKDIR /opt/drupal
# Wed, 20 May 2026 00:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 May 2026 00:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e15364525168f1adf5295d94dd034153649798b42c53855141532044d7048d`  
		Last Modified: Tue, 19 May 2026 23:09:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5fb1bab77757190c5fe3c03c6bf18ee4499fbd115160f6b1ed7532af1e8b80`  
		Last Modified: Tue, 19 May 2026 23:09:46 GMT  
		Size: 104.3 MB (104341748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49702752ec0e2e51d12e2bf1cec5c0c90a166200c21ad4466145ad3536672b0`  
		Last Modified: Tue, 19 May 2026 23:09:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512756286a1b2e60c9cdd3fe197f3b4c1d997767712b0be4462b00852008e1f1`  
		Last Modified: Tue, 19 May 2026 23:12:47 GMT  
		Size: 13.8 MB (13828949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abf602cf1db5069cc1a9d972adb99d560a450be7d3b9f193980f4846010a5b4`  
		Last Modified: Tue, 19 May 2026 23:12:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f7c8a60c6d06fd9620fd358c074a9594be92c08a8627267d852c37fa342da`  
		Last Modified: Tue, 19 May 2026 23:12:48 GMT  
		Size: 29.8 MB (29756029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e175abde60898d0ec2836327e0df77f856c8e81f9172016a46679732c1e8b1`  
		Last Modified: Tue, 19 May 2026 23:12:47 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239dbb2360b1a0c69508045a057f7c8aec77dbada60fe80274edfbeb88baea37`  
		Last Modified: Tue, 19 May 2026 23:12:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38022994c38d0c388eee25c060af172edf2c986a6231aa4bfcdb452a171ae7a4`  
		Last Modified: Tue, 19 May 2026 23:12:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb1bea9d0aa5ff3b3aba5f76928270fc54757cbd858e5d21795354d87902507`  
		Last Modified: Tue, 19 May 2026 23:12:49 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247a15aadf1b2bc712044d370d98e9f49fb7397506bc6209266dd3f10df9d1d5`  
		Last Modified: Wed, 20 May 2026 00:27:36 GMT  
		Size: 1.6 MB (1552133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5654b3994960cc26402cd457630cc22e8202c3ee6560a97ef025b049055acc6`  
		Last Modified: Wed, 20 May 2026 00:27:36 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791baf20a4c72b4cedf30069b87f136497a5e322e0075072558a91cf2bf3ec46`  
		Last Modified: Wed, 20 May 2026 00:27:36 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a458efe37642882a462e51e4581ac5252a2007424eff77e8a0cc81838cee648`  
		Last Modified: Wed, 20 May 2026 00:27:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af16d06a7e81a6c5d31c4f6b45198b06b281d023b37404296f9ddbf077002b0`  
		Last Modified: Wed, 20 May 2026 00:27:38 GMT  
		Size: 21.4 MB (21351152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:fd80346014103e1d7951ac11744bd395c7bdb20bac80d07400a82d0e193cb555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f02508b711f405fa1bfaa1e6e5779ae664ae3a69b01342ebdd1f9841215c79`

```dockerfile
```

-	Layers:
	-	`sha256:890c53cea0d00015f7408190e3b9caf5b1c659c827d407dde4f1566f40f234f7`  
		Last Modified: Wed, 20 May 2026 00:27:36 GMT  
		Size: 6.5 MB (6524337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1ca1346ebd86f0f68fb6129e484fef994a05b8ec9a9388baa26b31214ce5e2`  
		Last Modified: Wed, 20 May 2026 00:27:36 GMT  
		Size: 35.7 KB (35743 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:08e451e3dcc4a0e602eaf78398a63085690ead32c2e635debcecb35bffb25047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164334734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714005296324e09a37b5cc54ae7276b868e765532bde296ea37da43ba721ed4d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:16:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:16:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:16:21 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:16:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:19:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:19:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:19:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:19:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:19:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:19:05 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:19:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:19:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:19:05 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:19:05 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 01:35:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:35:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 May 2026 01:35:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 May 2026 01:35:28 GMT
ENV DRUPAL_VERSION=11.3.9
# Wed, 20 May 2026 01:35:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 May 2026 01:35:28 GMT
WORKDIR /opt/drupal
# Wed, 20 May 2026 01:35:40 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 May 2026 01:35:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9393384d65473db806ca651fad428698288320221b702f417d746fd77a4a2387`  
		Last Modified: Tue, 19 May 2026 23:19:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d39edbe009964c663a393ef5475f0ab7863ff6ad2e2f7542d42b58931160f6`  
		Last Modified: Tue, 19 May 2026 23:19:24 GMT  
		Size: 76.2 MB (76155456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556ceb8d96455388f9bb888951413a29ac5bfa5a52d6c838b2918238cb0ec32a`  
		Last Modified: Tue, 19 May 2026 23:19:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e484e2fe088bb737e56b9e65d9af3c91aac5c2d9e2a09ff70f12d17fe20b434f`  
		Last Modified: Tue, 19 May 2026 23:19:22 GMT  
		Size: 13.8 MB (13826800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d6d3aa813eb640d9ae6b5f313ed2e0ed1237fc1d5440dfadbf2ebfaaba63c`  
		Last Modified: Tue, 19 May 2026 23:19:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b30039fc43789e8dab1fac11b589f97ba2f2e0fa4eaeb366a3273659a90309`  
		Last Modified: Tue, 19 May 2026 23:19:23 GMT  
		Size: 27.0 MB (26983444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05f06e9f31d356e32d16b8a86f8d61b467ee43604ff7454526930c6c4162b57`  
		Last Modified: Tue, 19 May 2026 23:19:23 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eae914e7940e53222bec4d8df133319bfec48b2de827cdd5a1c3eaa06bee7d9`  
		Last Modified: Tue, 19 May 2026 23:19:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a42a1d051748d928ba6990a0badde9d866dbed9b09a4d2afe597c16bc72d4ae`  
		Last Modified: Tue, 19 May 2026 23:19:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4026daf3475cd01a4bfbf4590de7b4a8e57966d454ab6992be4eac95fb538629`  
		Last Modified: Tue, 19 May 2026 23:19:25 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b6260752c17171da5147fc3100c202537f648b5d3d4e4b86b5d3643d97be4b`  
		Last Modified: Wed, 20 May 2026 01:35:56 GMT  
		Size: 1.3 MB (1272179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a860b60806a526c89ed9c8d7bb0d01ac9475a853fae4a2924679407799bd06d1`  
		Last Modified: Wed, 20 May 2026 01:35:56 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1681276ef79e81af739fb4e545bb1edd8563cdfd24a2fbf8ee7bf4fd6a79703e`  
		Last Modified: Wed, 20 May 2026 01:35:56 GMT  
		Size: 790.8 KB (790769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c566cab74bcee16cf179d3467406d399f470a930b896901a9eefdcb478445b`  
		Last Modified: Wed, 20 May 2026 01:35:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008b7187ff275ad7436f8041f0f2582e2ff23007f775b737709c21b5466d090e`  
		Last Modified: Wed, 20 May 2026 01:35:58 GMT  
		Size: 21.4 MB (21350823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:c272ae8bc808826e42b861366e7bccad0700e25dc3a4759e92a717aa0a77da3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6373556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cc4ea32149fb76350730a7135f3205d21a811e1a02f6b987034d33375ca3c6`

```dockerfile
```

-	Layers:
	-	`sha256:12cbb8a3a8c46277cab3289acb74f6a830f7ffa037a0bff0be193ef7927caefd`  
		Last Modified: Wed, 20 May 2026 01:35:56 GMT  
		Size: 6.3 MB (6337657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481d8ed4da1df74116a1097e5b8a63d1413e99bed1e14dc499aa309af4f543b6`  
		Last Modified: Wed, 20 May 2026 01:35:55 GMT  
		Size: 35.9 KB (35899 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:0ca312b285ff65d45a70f297615e813a757bd19fd887af63112bdc980efb4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193191359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38490701b2ed7ab10beb4b82d0a956ced4ffbac842f82dd386244569744ae6b2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:09:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:10:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:10:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:10:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:10:03 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:10:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:13:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:13:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:13:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:13:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:13:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:13:00 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:13:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:13:00 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:13:00 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:13:00 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 00:28:58 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:28:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 May 2026 00:28:58 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:28:58 GMT
ENV DRUPAL_VERSION=11.3.9
# Wed, 20 May 2026 00:28:58 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 May 2026 00:28:58 GMT
WORKDIR /opt/drupal
# Wed, 20 May 2026 00:29:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 May 2026 00:29:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b154186e8017430dae9ba870851fa2d050c5573ba00c1bf0ab4911f02dde898`  
		Last Modified: Tue, 19 May 2026 23:13:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e05ba90d32871730a709441b61fe8d9981b02f35cd5439296a7d3251ec965`  
		Last Modified: Tue, 19 May 2026 23:13:24 GMT  
		Size: 98.2 MB (98174136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ea4d05f02b2a8ff6ac8324322d721fdfad9438affd26b5f8128f29d6c0edd`  
		Last Modified: Tue, 19 May 2026 23:13:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ad13f7d3b6c64937c297e7c38a439c28a4b108c1036899722ac0973c05f8d3`  
		Last Modified: Tue, 19 May 2026 23:13:22 GMT  
		Size: 13.8 MB (13828718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a1ec111923b17d1d1fd4c3bd573d742992bd8788edc2a11151ddcac135f24f`  
		Last Modified: Tue, 19 May 2026 23:13:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a0f96ab58f19553ffb698e086b8b4e26748232ad27efa73867a95be0c65bd1`  
		Last Modified: Tue, 19 May 2026 23:13:24 GMT  
		Size: 29.4 MB (29378166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e76a7fc7873e860d920ba261dbf8b3516e9b6d1785a1dbc1bcea341596d32b3`  
		Last Modified: Tue, 19 May 2026 23:13:23 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5cde71ed55e66c405d76df9c30cc1685ed09de59cfbd4f8f116cd74b9068d`  
		Last Modified: Tue, 19 May 2026 23:13:24 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447340a5de65acff9dc19cec6c34eda7a1a7b9721638b8838a57015bd417b983`  
		Last Modified: Tue, 19 May 2026 23:13:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8173a6da131ff5d9bf96c532e40d81b9f4e5fd771a8e9ecc3f50045949e8493`  
		Last Modified: Tue, 19 May 2026 23:13:25 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3ce10e0fed5f767d7e4f68f45b42f070ece7e76c6ea6828fad14a97d7e75b5`  
		Last Modified: Wed, 20 May 2026 00:29:27 GMT  
		Size: 1.5 MB (1540291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824280b52de4d359eaad11eeb6879ba0c725da8bf6264f3c00b268873f74093e`  
		Last Modified: Wed, 20 May 2026 00:29:27 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a6a9e4793d8d11bc6408b9237b455ce6f1bc80005d9730bf1c126d5fc5ff4`  
		Last Modified: Wed, 20 May 2026 00:29:27 GMT  
		Size: 790.8 KB (790763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7334d851a35cb213a0b48fac2ed39ec48b41e5685fd28580495375a0c18a289`  
		Last Modified: Wed, 20 May 2026 00:29:27 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fc0302bcf9450a4c304cb95bdd7b67558d104e40b2c40577f482126f8102d8`  
		Last Modified: Wed, 20 May 2026 00:29:29 GMT  
		Size: 21.4 MB (21350623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:858f0342794570c615ce975bea58e0d390c706d6f30762d767954450c5c4d2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6588729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1709ddbe84ecbf44140d7b43977f2e6cedde3135601146b72e7cf65c8c40bba`

```dockerfile
```

-	Layers:
	-	`sha256:3c57916ef009153f84a1ea8bfa943ad83cf120985f670160b81d0f26c85b5465`  
		Last Modified: Wed, 20 May 2026 00:29:27 GMT  
		Size: 6.6 MB (6552782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef236395e5cf732d9541947bcaeda6c69d1fea83425acc70391d061985aaf83f`  
		Last Modified: Wed, 20 May 2026 00:29:27 GMT  
		Size: 35.9 KB (35947 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:73350dfe02aa203c83ba57425b24a52b5b41e8a9e292c2d81df28ffd3832d64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198708398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e458a2f57520fa6a6f6e98bdcf8e237870351ee7b6007ff094df88f21770c21`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:04:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:04:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:04:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:04:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:04:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:04:58 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:05:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:05:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:08:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:08:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:08:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:08:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:08:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:08:01 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:08:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:08:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:08:01 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:08:01 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 02:47:03 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:47:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 May 2026 02:47:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 May 2026 02:47:03 GMT
ENV DRUPAL_VERSION=11.3.9
# Wed, 20 May 2026 02:47:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 May 2026 02:47:03 GMT
WORKDIR /opt/drupal
# Wed, 20 May 2026 02:47:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 May 2026 02:47:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099471d6cadad367234f2d465406a6578bda1756bc8605e71195d3350cf8a7f7`  
		Last Modified: Tue, 19 May 2026 23:08:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9232129f71102dafe427d0a5f799b6eec131b390c2bfed49f48c836f4e8900`  
		Last Modified: Tue, 19 May 2026 23:08:24 GMT  
		Size: 101.5 MB (101536227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bff40134fd75977a86f4f573005594d5cbb77bbcc713bce13d1f3c2b01ed6b`  
		Last Modified: Tue, 19 May 2026 23:08:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177ae33f4a73c062ce14d130f8f421d40065eea61ff08acf76c7b9582ce4539f`  
		Last Modified: Tue, 19 May 2026 23:08:22 GMT  
		Size: 13.8 MB (13828120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fb6c09ad7ceb017efae4820f2def1d5cffbb422f2e1ef25d672e42b10bb69c`  
		Last Modified: Tue, 19 May 2026 23:08:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea67d8ccd2471c5a26fd6e14c91353821539804cb288a13e0547444989abbce`  
		Last Modified: Tue, 19 May 2026 23:08:24 GMT  
		Size: 30.3 MB (30345449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd16c74c92857ac31828573637222f0bc60c780691c5fc3b194aa2f18bfb9923`  
		Last Modified: Tue, 19 May 2026 23:08:23 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3d602ff20433adb4722ede172be85605bfc74b62c7f086ce0c0e5ba83969d9`  
		Last Modified: Tue, 19 May 2026 23:08:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c341494331980f44a11e5d7013c2bf803b046a8c59dd4e5ef9379d68ee351496`  
		Last Modified: Tue, 19 May 2026 23:08:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8263d1fae1d34cca692f0b9831993d9f8d5c828189ee898721d8fb045cd18`  
		Last Modified: Tue, 19 May 2026 23:08:25 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590c27e0e89416e8a653e7463b66ab78e480824b11b3c9c558091836c90297e2`  
		Last Modified: Wed, 20 May 2026 02:47:27 GMT  
		Size: 1.6 MB (1624631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677ff1fe88921a8158ab7fb067728898db4197719f8c067be3ea4ce4a1e15200`  
		Last Modified: Wed, 20 May 2026 02:47:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c1e343d357636353c86cceed947f0bd6a2b2910cb2b1ac15c259d29897546`  
		Last Modified: Wed, 20 May 2026 02:47:26 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca33e5be2f217cafb72acde5a0f8a3a7a8f43fec52541c5ecd47c481b7b93344`  
		Last Modified: Wed, 20 May 2026 02:47:26 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332924f222d83bb4116fa33d1c7c2d2a4359c66a005743e125fabbc18d29b123`  
		Last Modified: Wed, 20 May 2026 02:47:28 GMT  
		Size: 21.4 MB (21350988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:3f7dd280f1df078ee819f0c7d8d012b0d9e94c29e51f9d1d61f01f25f6283c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6539779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159632c029e571a0c6484fe576f26c2d12b1ab5092d484b36f2acc42c58c9c1a`

```dockerfile
```

-	Layers:
	-	`sha256:2ef37bb052b39713634bc4ca4df768c91e1f128fa15d125abae70ff7e2c641dd`  
		Last Modified: Wed, 20 May 2026 02:47:27 GMT  
		Size: 6.5 MB (6504097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ad8219f41b08935d0576090dd4da28bc00db8e0596583967f95071f60081fd`  
		Last Modified: Wed, 20 May 2026 02:47:26 GMT  
		Size: 35.7 KB (35682 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:4516a0dba8cc5ef161a31800fa743edbbd84ea200b6fba2a134ea40dbc2f0d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203972398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b446a350d63787d0ad1a62cada8c8a12a5246e494276ae6b2c1817b4dec6e604`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 21:00:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 21:01:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 21:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 21:01:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 21:01:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_VERSION=8.4.21
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Fri, 08 May 2026 21:01:04 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Fri, 08 May 2026 21:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 21:20:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:29:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 21:29:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 21:29:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 May 2026 21:29:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 21:29:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 21:29:10 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 21:29:10 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 21:29:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 21:29:10 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 21:29:10 GMT
CMD ["php-fpm"]
# Sat, 09 May 2026 03:37:41 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:37:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 14 May 2026 17:14:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 14 May 2026 17:14:02 GMT
ENV DRUPAL_VERSION=11.3.9
# Thu, 14 May 2026 17:14:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 May 2026 17:14:02 GMT
WORKDIR /opt/drupal
# Thu, 14 May 2026 17:14:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 14 May 2026 17:14:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea44eee5548ca8945b41eb561771174ff26bc54855cbc4f5ec5dd7fa4bc661d0`  
		Last Modified: Fri, 08 May 2026 21:05:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2976e7c369fddfd6ed2963aa00ea268b2439b009bb799f4238b2642dea19fc7`  
		Last Modified: Fri, 08 May 2026 21:05:56 GMT  
		Size: 103.3 MB (103331724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525931355248740bacfd8381bc07129c8272589a2c71d53d3831f54c32d56be`  
		Last Modified: Fri, 08 May 2026 21:05:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d320aafda41c0f975c0d9e98c56d450a163fd73b0e77c01cd94ae3b51acdd20c`  
		Last Modified: Fri, 08 May 2026 21:25:06 GMT  
		Size: 13.8 MB (13828338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1807afe4fb7e10110bc95c28438ecf52323ed29dfc0bff54cf07ac43511561e`  
		Last Modified: Fri, 08 May 2026 21:25:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc77d0e0d6603f695c613c87c98ef019bdc57bdb497ec91c1f43bb4c496c6484`  
		Last Modified: Fri, 08 May 2026 21:29:33 GMT  
		Size: 30.8 MB (30823972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6301c6c8d32ae5cb6a59e63357a1318f4a0435bd7deabe86aedf59dd8694f179`  
		Last Modified: Fri, 08 May 2026 21:29:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052bfe37bc60026e72084d2ed016f92c8f0c617b2cb97893235fe3d9acd290b1`  
		Last Modified: Fri, 08 May 2026 21:29:32 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e958f2455a5d02b2cb4efe3791d965c38d1b10ad26551454644eebc97f3d9d9`  
		Last Modified: Fri, 08 May 2026 21:29:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2362b8cfd62a667acb9bfd56e7254d1a2d01d518dae498911e9b590c197feec`  
		Last Modified: Fri, 08 May 2026 21:29:33 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1ab2fd5a9d6ab69af576e06ab9b863911cc79810f36d804db2e50b98afeacf`  
		Last Modified: Sat, 09 May 2026 03:38:35 GMT  
		Size: 1.8 MB (1754459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef76aeda48382600ff74761ac4edbb40c8333ec1b944a413aeb5478ee5c06f6d`  
		Last Modified: Sat, 09 May 2026 03:38:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef1986c9cb4025c237f62a8fb249385169d75cbb9ce04abf95bf035ba03e99`  
		Last Modified: Thu, 14 May 2026 17:14:57 GMT  
		Size: 790.8 KB (790765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc6de5485d9a872ae39b02918f548e9400bdf15091f2c04bc9120889cb8411d`  
		Last Modified: Thu, 14 May 2026 17:14:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c4340b683fa7c7032edc9661697504fcee14f033d23badcaef7ab775978f86`  
		Last Modified: Thu, 14 May 2026 17:14:58 GMT  
		Size: 21.4 MB (21351070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2306845f7e9d5fb5207075fe0b8e3a812cffcaba617c1673382bdb24c8948448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6536894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80926f8e2b56edcafb056883b0e4de4cbac93b52c86ffd726ccdad49e5c80c7`

```dockerfile
```

-	Layers:
	-	`sha256:737604fe8393939832f657b9184f2de6f3a0b646b22a232916491c0840c1a833`  
		Last Modified: Thu, 14 May 2026 17:14:57 GMT  
		Size: 6.5 MB (6501067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c615e18f412eeda359f105217c969cacabddb3abbdddbcdf8ec85d6f044271d`  
		Last Modified: Thu, 14 May 2026 17:14:57 GMT  
		Size: 35.8 KB (35827 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:70918a9b66912ff7d5b8d786b87f5d83aff01e90726030e44b9b4e5b0f08cc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173864746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418a4cddc5e6259f3eec57a212ad62f93f038b5dc979a82b99fd8f69043506f7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:10:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:10:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:10:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:10:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:10:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_VERSION=8.4.21
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Tue, 19 May 2026 23:10:28 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Tue, 19 May 2026 23:21:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 May 2026 23:21:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:25:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 May 2026 23:25:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:25:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 May 2026 23:25:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 May 2026 23:25:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 May 2026 23:25:17 GMT
WORKDIR /var/www/html
# Tue, 19 May 2026 23:25:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 May 2026 23:25:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:25:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 May 2026 23:25:17 GMT
CMD ["php-fpm"]
# Wed, 20 May 2026 02:08:45 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:08:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 May 2026 02:08:45 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 May 2026 02:08:45 GMT
ENV DRUPAL_VERSION=11.3.9
# Wed, 20 May 2026 02:08:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 May 2026 02:08:45 GMT
WORKDIR /opt/drupal
# Wed, 20 May 2026 02:08:52 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 May 2026 02:08:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ef3f197bfaac386157838c8b884dcf5d1a8f665a6438bf5ba96e0770ce4335`  
		Last Modified: Tue, 19 May 2026 23:15:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e7c6f1adb9eba80437e67eb04dd4c5e13162193e24c779758e72facca28269`  
		Last Modified: Tue, 19 May 2026 23:15:18 GMT  
		Size: 80.8 MB (80829888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6ece8af35bbb5e15d994b9c90ba748a6895224d39eecf02bc093a1678a4b0`  
		Last Modified: Tue, 19 May 2026 23:15:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c753221d8525b73cdaa2c4da24d98aa56a1167ac42fa0156a63aee7eededd5`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 13.8 MB (13827296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a1c4a4635f0c4894b188674e5bc1f138adeb65fc3ada22a4b15ce0ed5e7483`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37096dc0597dba5a04c34902c22a25b90e1c1702d1d33b123367f34276c61117`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 28.7 MB (28700246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f97bb2ad2574f395c9c664ea7ff406a846383fe00a311c42f46837efd24af8d`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da3bb144fc0adfc6fc95dc6643ec43d48d69126aae84e1787dc92a5dae0833f`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60f1b40a80363831ffc2a198ed160a214d4616a4697785e7dcfff447fd59e1c`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49210e15c3b3d05d9f69d9b4c8f374b4109c5c65fa8f999a11b258064ae72a57`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f63f3c177a047e47b52d949ffa65ac8c3f6a5c0897e05c6989772eff0648a9`  
		Last Modified: Wed, 20 May 2026 02:09:18 GMT  
		Size: 1.5 MB (1463198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b073862a35c8373b7fc115dd9385573adf8ae75cd79eb6d19ad373e84c5fd553`  
		Last Modified: Wed, 20 May 2026 02:09:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966228f4d89297bcc51a4f981fad7dcd0a754734ab3cfecf71a911177b9aa45b`  
		Last Modified: Wed, 20 May 2026 02:09:18 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181296c5fbfc4ed020733d28fced28d90f8336c79abe139609fe46eb23181585`  
		Last Modified: Wed, 20 May 2026 02:09:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff85668309596dd2f197caba6a7bb676954c1f6fb0c6b685f859934ec7fa073`  
		Last Modified: Wed, 20 May 2026 02:09:20 GMT  
		Size: 21.4 MB (21351137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2a76c4338b0ec67b8687d5a59352aa051e166e8e0dfadbc388cafb666ef2c803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce3aa974fcd554baf8bfb904c8e061e951f98f2ed6d81b509b04d6b9bac9b01`

```dockerfile
```

-	Layers:
	-	`sha256:8c2ac7126ebbddd5cb5986879fc2b96dc1af455dcac83205b5643907924ae85f`  
		Last Modified: Wed, 20 May 2026 02:09:18 GMT  
		Size: 6.4 MB (6361555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f3eaeadcfd51189e546162e21758fb78283b2dd3dc49dddb8922e60e20ab98`  
		Last Modified: Wed, 20 May 2026 02:09:18 GMT  
		Size: 35.7 KB (35739 bytes)  
		MIME: application/vnd.in-toto+json
