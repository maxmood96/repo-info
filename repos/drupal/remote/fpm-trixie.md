## `drupal:fpm-trixie`

```console
$ docker pull drupal@sha256:0a105102a92ddd69b0bbf7cfb8618770e3dc2dd486f75ae27e092fee5ef34d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:fpm-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:c897993ff90e13d7c36791499d3a40d248e6a51506c4bd9dadf5d7b540f150ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198139710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285f15558dfb6bb50845336ab150c2ce73fd06f3e2b7d57d04464899ac84f502`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:38:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 04:38:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 04:38:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 04:38:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 04:38:29 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 04:38:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 04:38:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 04:41:20 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 04:41:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 04:41:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 04:41:20 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 04:41:20 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 06:40:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:40:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 06:40:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 06:40:28 GMT
ENV DRUPAL_VERSION=11.2.8
# Tue, 18 Nov 2025 06:40:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 06:40:28 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 06:40:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 06:40:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7988844412cfdac063c91a36a7210df05e34ae43443f3e058db8424a62b44f62`  
		Last Modified: Tue, 18 Nov 2025 04:41:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8c61cdd11feb3e2c406532cc731b25a367fee2d7623fa510ad58b57766ed3`  
		Last Modified: Tue, 18 Nov 2025 04:42:05 GMT  
		Size: 117.8 MB (117837540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3525b2ddcef0c74cb8bd5e676639e076de6d9bd6c0a95d163aebb003dc2eefd6`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6d570e6664a4cf136e1fca464b1bd8cef951bcab61cca20e70a69cea098dc3`  
		Last Modified: Tue, 18 Nov 2025 04:41:52 GMT  
		Size: 13.8 MB (13791599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3f2381ffbc21f30d253dc73e77f676131bbeff6f67caf0520e8a2b5b303574`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92a8ef726859bc9e47098dd57fb2819a21dad873fa0fdcaf19131737bc30699`  
		Last Modified: Tue, 18 Nov 2025 04:41:53 GMT  
		Size: 13.7 MB (13660971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04461d72c9464d73f46a506ad00f47f78902047fab10b6b24ffaea87d00b64c`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce195a6c827079b359e583ccf91e0331a878877bf625c67c95ae59a273052c8`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74a52a0f3a4543c0c456056dbdae94dbcdbdf47a9eddea673db94e41cef0b5`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57aa505f5bbef6d819b22368c1e7c4e98f127ba6b89db6d73b17ad3f9c1dded`  
		Last Modified: Tue, 18 Nov 2025 04:41:51 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f9f461b22f7bb03af799aef43da465a1ec4a306a53763004a9b06ce892b87c`  
		Last Modified: Tue, 18 Nov 2025 06:40:59 GMT  
		Size: 1.6 MB (1632747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a309cf0272be7435ca8116b37748e379c97e36cb49bfe3b2f56093a80c2f9dae`  
		Last Modified: Tue, 18 Nov 2025 06:40:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eddfc1cc8960bd9c7208f0207fa768524a183493bc8eedd2ca422bb4c82e5b`  
		Last Modified: Tue, 18 Nov 2025 06:40:59 GMT  
		Size: 772.1 KB (772147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e88057498482007193ad4cbfa0d45a0d17844ea7e0fe517ae90b26af3a3ec6`  
		Last Modified: Tue, 18 Nov 2025 06:40:59 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885492081af25077a69ce7adcce403807b7dbae493a8eacc0419b9e278299cb8`  
		Last Modified: Tue, 18 Nov 2025 06:41:01 GMT  
		Size: 20.7 MB (20654677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:0dd2656d9f4df458f0fc2663e15e724a64fa3191b2b49391674e3b77c5ac015c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6851262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a083b828aa47983dd574ca8ad8a0c2d2e538a36b06bcc71c6c70bda69089bc2`

```dockerfile
```

-	Layers:
	-	`sha256:0d1adf36648d4447183a846bb2181cad6c35f708ef0d1f6f9992c5ed5ba1faf9`  
		Last Modified: Tue, 18 Nov 2025 09:08:16 GMT  
		Size: 6.8 MB (6812953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c908149c2549fcc5a63767cc97fbb6585971b8bfc5ee2c3a40f8a24a12212f`  
		Last Modified: Tue, 18 Nov 2025 09:08:16 GMT  
		Size: 38.3 KB (38309 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d3ac40f17e570e02aa130695892cd45654ea6068ab9d62cfcab2f666b1e90cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160594555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40da58460ab32724df4511b7236045528396cdfb2370577556d99f1716736080`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:40:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:40:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:40:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:40:46 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:40:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:40:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:43:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:43:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:43:41 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:43:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:43:41 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:43:41 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:43:41 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 05:30:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:30:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 05:30:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:30:18 GMT
ENV DRUPAL_VERSION=11.2.8
# Tue, 18 Nov 2025 05:30:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 05:30:18 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 05:30:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 05:30:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e15b2702538d58ad41d73933a9ca7ed75636e7a9193fcfd3938af3e225614`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dc9c49daa937d4630adbfaea0671b63469bb895e99d2e511e0872b530c2f60`  
		Last Modified: Tue, 18 Nov 2025 02:44:15 GMT  
		Size: 86.2 MB (86246052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04dbb2611276383b057bfc6e2807539484105c24203e1c4d0a1f897e60d45d1`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b031b724edc0959a77dc39a18b4309aaaae9cc31abbb6c10ae1c361dd6af8b94`  
		Last Modified: Tue, 18 Nov 2025 02:44:07 GMT  
		Size: 13.8 MB (13789453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6b083293147ca1e207c8b696f3464c3ee9a01191e2db74976ccea920d79b89`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe4e832dadf3287aefb07662280cda13534dcc237bf59e156218457ac0e059`  
		Last Modified: Tue, 18 Nov 2025 02:44:07 GMT  
		Size: 11.6 MB (11561877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7855992240f1e7a219f3dfbd8f347dff0b5263e06a3e52134026725e7f13c3`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b87d105eafbfaff24df97557e7181e93917b7ae8093733732d6c2af68ce271`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f138682af93afa35dd82c8b6bae0fe6a61df98e4b4d9c42496e4097d8b5b4`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1add8c45825d681aef55eb4d850cf454f52fbfbf3bd93dd2c02282632ffa4b`  
		Last Modified: Tue, 18 Nov 2025 02:44:06 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa095af1ca27f54c8505408ac6f0095d4c73c2e16278cc0f9f619c3f56c55b`  
		Last Modified: Tue, 18 Nov 2025 05:30:49 GMT  
		Size: 1.3 MB (1346583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c43985f5661f44996af99ebaa6b1eefaad9d4b6c35b78a6172fb6f91897cdb`  
		Last Modified: Tue, 18 Nov 2025 05:30:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038317a987160de51eeeb6621cc9dec1e894b8adefcb800bcfd2765cd918048d`  
		Last Modified: Tue, 18 Nov 2025 05:30:49 GMT  
		Size: 772.1 KB (772147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eede858f96ef2c62a970873696d03b6421ecc80552c2ed104b842b662f559df0`  
		Last Modified: Tue, 18 Nov 2025 05:30:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98c353be8edd2ecef21b4781ca0adc6b112b00e15895966a58164b6d9e4f36e`  
		Last Modified: Tue, 18 Nov 2025 05:30:50 GMT  
		Size: 20.7 MB (20654939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:2abe7544d8e5a2ededc1bb3cdcebbd3bb623157644b2f9c14ec24d5ba2d6c692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6655378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ca3005377ad3fd35f597f3f3b769edbb99ae0f5f4608dc94b496b65e5bc559`

```dockerfile
```

-	Layers:
	-	`sha256:d673120352dd2adf3c2ff43eb0ce85e6c2e471e3a7d46dd7d3e0d243b916f0f9`  
		Last Modified: Tue, 18 Nov 2025 09:08:22 GMT  
		Size: 6.6 MB (6616850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3234e18d252ff65b090ca0144c04e0cb34a8bbc2d617a4d5d064a897fb2c555`  
		Last Modified: Tue, 18 Nov 2025 09:08:23 GMT  
		Size: 38.5 KB (38528 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5a83cd8167090a112552cdf315cb3f949ceac29949aed1e0a2fd1c6068f0b29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190450352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82260b16dc8b804dcffd70f037c0fe6d66f3843c2ffba1686360c3d83a81861`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:22:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:22:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:22:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:22:16 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:31:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:31:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:34:14 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:34:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:34:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:34:14 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:34:14 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 05:40:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:40:31 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 05:40:31 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:40:31 GMT
ENV DRUPAL_VERSION=11.2.8
# Tue, 18 Nov 2025 05:40:31 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 05:40:31 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 05:43:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 05:43:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707c1ebb57f901cb38bf6cf05ed313102f4997f868fe3cfcd5aa0c08a6cd121e`  
		Last Modified: Tue, 18 Nov 2025 02:26:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58514a97ad93e9d6f1994b026483165586a50876b5ed65353eba4fbcbc8387b7`  
		Last Modified: Tue, 18 Nov 2025 02:26:14 GMT  
		Size: 110.2 MB (110162500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70512b0537613eec104ea2b47f21deea93930ca7aac239756a3cf274a7b8fd4b`  
		Last Modified: Tue, 18 Nov 2025 02:26:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2096b1be0b634bd16905d4a216926b8e929116281bf83591a70d003833767fe`  
		Last Modified: Tue, 18 Nov 2025 02:34:35 GMT  
		Size: 13.8 MB (13791291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a35899f4485dff0ee9bd6659a0ccd068973d0b4b523d185f822b0a841b0a4`  
		Last Modified: Tue, 18 Nov 2025 02:34:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b007cf57197326ddaf4aaf98c821711216b2e45a60a3bbbb7c89cef86e558a7a`  
		Last Modified: Tue, 18 Nov 2025 02:34:34 GMT  
		Size: 13.3 MB (13328293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c28e818fdba84235a26b1468589ca017964cdaeb22d448a82845f02b48485bd`  
		Last Modified: Tue, 18 Nov 2025 02:34:33 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c78c2cf0204b122400b78fdcf121b5fc0c6ccc6b50829c699ca5194f5b86d`  
		Last Modified: Tue, 18 Nov 2025 02:34:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5281a7db138889dea51bca47f4ac405ef107912b8d5408748d0dae0c9c6cf60`  
		Last Modified: Tue, 18 Nov 2025 02:34:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625127e538e46e10a6579f32b633a51d0468f5b2ccb803a25ff680f862035056`  
		Last Modified: Tue, 18 Nov 2025 02:34:32 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78700e79349f40dcb36f72a9f5d57fe7d59b5b44d238558b8caddc05ed33a55`  
		Last Modified: Tue, 18 Nov 2025 05:41:03 GMT  
		Size: 1.6 MB (1590134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e994a9ab9ffe4ee6848723046bd47f23b5c5e14f166c861fa54c2bfb38399978`  
		Last Modified: Tue, 18 Nov 2025 05:41:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13338c4cd56fb0dd91fed6571fced2acb894bade8c73460c9fdd48a33e36de9`  
		Last Modified: Tue, 18 Nov 2025 05:41:03 GMT  
		Size: 772.1 KB (772148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c51bcd8476e314000d1981cda29f0f5811b63bbccd2a2c2e980fbb413ea5d84`  
		Last Modified: Tue, 18 Nov 2025 05:41:03 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588c0018422d3fe7f51342788b084d8d47e29f41b0aec40f16ae48c58a8ffc6`  
		Last Modified: Tue, 18 Nov 2025 05:43:46 GMT  
		Size: 20.7 MB (20653833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:f5f26b8aa35e288fdcf87ca40680fceea7c8e1bd1590810e9c5949bac00840f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21b051a96996cd62a955ba02ff647626da57a8930f9b0367b7c02445a3ab9a8`

```dockerfile
```

-	Layers:
	-	`sha256:b61ee1f749f35c5bc445627afda2cfde71bdb8dfd9b7c6710031ac6fd59a6b01`  
		Last Modified: Tue, 18 Nov 2025 09:08:29 GMT  
		Size: 6.9 MB (6910383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4ddb9818e180177b36b54291be2c0cdc65b4f1cb7c35cce306bf890e5be5a7`  
		Last Modified: Tue, 18 Nov 2025 09:08:30 GMT  
		Size: 38.6 KB (38612 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; 386

```console
$ docker pull drupal@sha256:fcdd3229b6e25dcb78b9b3b5ffb20c7340c8db9f8bf22318e85795a2de54c020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198333876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f27035eb4b474c9f7eb08be868ed46c88192e5eaf83ae5f6300a7347e037481`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:22:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:22:25 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:26:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:28:52 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:28:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:28:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:28:52 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:28:52 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 04:17:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:17:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 04:17:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:17:20 GMT
ENV DRUPAL_VERSION=11.2.8
# Tue, 18 Nov 2025 04:17:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 04:17:20 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 04:17:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 04:17:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9ed2cdd021787dec191a45b5dd2cc0df86560b7c37ca01983bcc3b524e1091`  
		Last Modified: Tue, 18 Nov 2025 02:25:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4432538c5a560d91f94280046a687b78b8c8276eea739476a31d69f05e9b04`  
		Last Modified: Tue, 18 Nov 2025 02:25:52 GMT  
		Size: 116.1 MB (116138468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ed3ea53aa36deec3d875de1e4f17d1d65241896416d4af8f1d7b3365ea593`  
		Last Modified: Tue, 18 Nov 2025 02:25:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efcd8f720b0f8f8259983646155f29d2ac2bbe72b57768e859ff2afb371116f`  
		Last Modified: Tue, 18 Nov 2025 02:29:10 GMT  
		Size: 13.8 MB (13790763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbfc6e61acc96c9ec7ce4b6dba0f3f4608f6a1b5f1e26bb84f7d22628502b2d`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e4dfa1c11a3ae29a7109811ba49fc3f7fd94bd7cb1a986341f75d6ec08af6f`  
		Last Modified: Tue, 18 Nov 2025 02:29:10 GMT  
		Size: 14.0 MB (13957220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3639992346e7fae3d13af805a0d4e39ae958e3e410659f23cf43038a1ab0b861`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea91c416c37479df4b1215afdd60417af1f220196c9196a979ca9663ba3420f2`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580c0c32ca496e98ccd516b5d052c30af173008b01c2771b6f89f6d798450f9`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0a4941e2a48ee6a3c4cf7761f072ffde4250e79f09a30276621ec6293c1c6`  
		Last Modified: Tue, 18 Nov 2025 02:29:09 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bc33785dd3362718a04e98dee1c6c3d7e7a7233d8b770d5b30b8268713c9c3`  
		Last Modified: Tue, 18 Nov 2025 04:17:51 GMT  
		Size: 1.7 MB (1713295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b2c64d38a615cd201027caf2ab690ff49f19bf3f5f766895977ef0b4768259`  
		Last Modified: Tue, 18 Nov 2025 04:17:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64eaca56502396586c7220e8be565edae64f8521cb0dd9639fe92ed3cd69265`  
		Last Modified: Tue, 18 Nov 2025 04:17:51 GMT  
		Size: 772.1 KB (772140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb2d159e7a2d6e21f522e5c613146dd7ad6a82fb6e8c812df57f9592e2558a1`  
		Last Modified: Tue, 18 Nov 2025 04:17:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f504b151cd58492daeb9db73ea322ecd6fb82eb2bce9bb70ce19af5566006b75`  
		Last Modified: Tue, 18 Nov 2025 04:17:53 GMT  
		Size: 20.7 MB (20655375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:7a2440bf8cb9a7a9a9a3e8386e06e7b36f19a5339d2c43fc659b0f8faf707f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6824985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2107440fb3d0de2b1c77174c2f5d69be13559c162c5920cd26ee343757ce7e6`

```dockerfile
```

-	Layers:
	-	`sha256:2282a1c097bdb9560ffdf78628f0638d58175a4123eb8256719ae402fe46ab1e`  
		Last Modified: Tue, 18 Nov 2025 09:08:36 GMT  
		Size: 6.8 MB (6786777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca518ad6355ab956c4210b154fbe46996f2f9e2a0e7103ca020fb9da997ec600`  
		Last Modified: Tue, 18 Nov 2025 09:08:37 GMT  
		Size: 38.2 KB (38208 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:8b33c6853143c75013a768d4bebeb4712bbe852e8634ba53f8d1f39b501bdc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194462749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57ecf80c9ee70cc838cca776dc537a3203588ec3cda900f4532ef5505c25819`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:13:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:13:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:13:57 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 02:13:57 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 03:00:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 03:00:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:14:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 03:15:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:15:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 03:15:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 03:15:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 03:15:56 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 03:16:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 03:16:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 03:16:06 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 03:16:06 GMT
CMD ["php-fpm"]
# Thu, 13 Nov 2025 19:17:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 19:17:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Nov 2025 19:17:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 19:17:48 GMT
ENV DRUPAL_VERSION=11.2.8
# Thu, 13 Nov 2025 19:17:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 19:17:48 GMT
WORKDIR /opt/drupal
# Thu, 13 Nov 2025 22:07:53 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 13 Nov 2025 22:07:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656e7846c7f44be5e3b20020683ff090edb2eb912594bbc202519629107b2cf`  
		Last Modified: Tue, 04 Nov 2025 02:18:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b9ffc03561872af5426b43902b2fa8677357153c8026953c971daa576c870`  
		Last Modified: Tue, 04 Nov 2025 02:18:50 GMT  
		Size: 109.6 MB (109597848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf1f4cde3b0ec73324641d784753c77627b0db1a0e1c39f0478fd104a862fa`  
		Last Modified: Tue, 04 Nov 2025 02:18:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12c388008e9cc92053d381edb5b5c198b5e25df8543bbb843372a746f6b1bf`  
		Last Modified: Tue, 04 Nov 2025 03:04:52 GMT  
		Size: 13.8 MB (13799724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb83b258194d65f6411e481969d68ccb3255de83ccace29505cdcc6c9ff58b6`  
		Last Modified: Tue, 04 Nov 2025 03:04:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26ed855a2fd05714a76dcd88c2fbaa1810942625c428e0e207ee8d1a90738c`  
		Last Modified: Tue, 04 Nov 2025 08:16:42 GMT  
		Size: 14.2 MB (14205902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c770ba072f478d5b38e9d0e9758856c196e4171f63e6e4ee3f31d14d8cc7bac`  
		Last Modified: Tue, 04 Nov 2025 04:00:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121abbf8afcbdec6a71782f4dfa1ea6b91de3be7469b62b2d0d1ca197d3ef`  
		Last Modified: Tue, 04 Nov 2025 04:00:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e6b03653c4e8ca46372cd8bb054dfda2a34cc0419f6c00041a9766056203c`  
		Last Modified: Tue, 04 Nov 2025 04:00:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175b83927e69307d5a394ac08bf52d721d20539de81903ae622492649323e40d`  
		Last Modified: Tue, 04 Nov 2025 04:00:33 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c9ed0b2adfa2f7b587df8199163b4da5588630415aeb824f65860eb30ccf4e`  
		Last Modified: Thu, 13 Nov 2025 19:18:59 GMT  
		Size: 1.8 MB (1821838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2f3118a10d28c51f0fe140ef8f6218951efa895ca42bedecdca9d402224187`  
		Last Modified: Thu, 13 Nov 2025 19:18:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fd868b88482afd6b09438819d96800c9fddeda1c8437c357a8549c4f507e9`  
		Last Modified: Thu, 13 Nov 2025 19:18:57 GMT  
		Size: 772.1 KB (772144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7c0fd2e075fbd62f540278c85ae08b082c99d169b8086d51b44e7610b74858`  
		Last Modified: Thu, 13 Nov 2025 19:18:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73776de2248fdd29dbedb270487fbb5178f29ad079dfdcf630264117e430a0b`  
		Last Modified: Thu, 13 Nov 2025 22:08:37 GMT  
		Size: 20.7 MB (20653106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:cd8becc52c0adbaf9689d6573107b8c2b484d80cdd3c1c1be4b1cbfa7c49a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6851149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b7761020b080faed8d8ec15fed5c9fc059c707452ab6a0dc3d15413ad74e16`

```dockerfile
```

-	Layers:
	-	`sha256:5bdbc2203f161c035e1fc6129e4418c7b04c803af9094ad44a3efddc93e1aafd`  
		Last Modified: Fri, 14 Nov 2025 00:13:53 GMT  
		Size: 6.8 MB (6812708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e0078d6a7aa528cedc11246a1dae66aed24e69e42d172126939c9eb40f81e7`  
		Last Modified: Fri, 14 Nov 2025 00:13:54 GMT  
		Size: 38.4 KB (38441 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:ba41d13d10209b9d8bd276038b6f10c487f0a8cdc23518261862bd422611ac46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224773226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7922ea09b36ed1e8b61216fbc613d1809fef09c78ddb4c0bfb2f8b55a746730e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 05:51:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 05:53:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 05:53:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 05:53:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 05:53:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 05:53:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 05:53:42 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 09:41:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 09:41:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 12:31:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 12:31:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 12:31:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 12:31:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 12:31:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 12:31:41 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 12:31:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 12:31:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 12:31:42 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 12:31:42 GMT
CMD ["php-fpm"]
# Thu, 06 Nov 2025 08:07:41 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Nov 2025 08:07:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 13 Nov 2025 20:18:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 20:18:09 GMT
ENV DRUPAL_VERSION=11.2.8
# Thu, 13 Nov 2025 20:18:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 13 Nov 2025 20:18:09 GMT
WORKDIR /opt/drupal
# Fri, 14 Nov 2025 18:32:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 14 Nov 2025 18:32:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b60b8763b9288d96a2c0a03f91b6bbda8b8e90cabe195aac6ab08bb9b7c3be`  
		Last Modified: Tue, 04 Nov 2025 06:58:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023ab2470133012ddd1028070c153f252fcdd37f14c86fe8f1b3bb6c5c16701c`  
		Last Modified: Tue, 04 Nov 2025 12:32:14 GMT  
		Size: 146.6 MB (146578993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9382a8b397fe6627424fd03c69c0c2a758bc0e6965d1d6005ac796e8fda70e`  
		Last Modified: Tue, 04 Nov 2025 06:58:50 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f17361ee032cd66332d69b356101753fa641c0b2c743fa397abc56629f02e9`  
		Last Modified: Tue, 04 Nov 2025 10:38:55 GMT  
		Size: 13.8 MB (13799575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ddc026a571f42a77d8e0bfcb9b4bc04a0aa8899be19c6268950bb80187ee52`  
		Last Modified: Tue, 04 Nov 2025 10:38:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6c0b892cf252817096e4c2b21d3a1aa37b659cb5c1f962f21b5b83c2298d4e`  
		Last Modified: Tue, 04 Nov 2025 12:34:50 GMT  
		Size: 13.1 MB (13131594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27134edd8ce3c1babb30e7f9aa42f9199be4d3851e1a3e62980fb9b0d518ce1a`  
		Last Modified: Tue, 04 Nov 2025 12:34:48 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8de49296df32d3399124292b87c0dd38694bd961e946014cd3646f363472709`  
		Last Modified: Tue, 04 Nov 2025 12:34:49 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874cc1f1dd8de312e692989ca54736aeb96f15d66548491c20312b1c1d0d956`  
		Last Modified: Tue, 04 Nov 2025 12:34:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd25430915e44f56f0912a3ae5b02a878bb4ff088975c07cb34ab2ff7095ff9`  
		Last Modified: Tue, 04 Nov 2025 12:34:50 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad42cfe8a2886a72d0a045cdb6cdb5de547750da1babf01e11d5afa5f30ebe`  
		Last Modified: Thu, 06 Nov 2025 08:13:04 GMT  
		Size: 1.5 MB (1548533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baebf8a0939fad7f13254892bb179c694aa543ed7a7c2ece0a1ecc8dfca8b24`  
		Last Modified: Thu, 06 Nov 2025 08:13:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145ba0a3db8a840fd033cb854c4a8a76b3ec8d1821c98f60e8c601ee6b4e292`  
		Last Modified: Thu, 13 Nov 2025 20:23:49 GMT  
		Size: 772.1 KB (772146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b20882a36a1de2dd8d28db3c3192d2d9a29df3a962c1bc4faf807bb3fb252a0`  
		Last Modified: Thu, 13 Nov 2025 20:23:49 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4ea42386ba046641fac5cfc4dcd88504080a971e75e6c6fccffaab64cfc8a7`  
		Last Modified: Fri, 14 Nov 2025 18:36:58 GMT  
		Size: 20.7 MB (20653040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:3d7118349c8e3efd0cd879983bdfeebb86630c06c1c43a8a92f4d1ec60d03925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6923209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618d710491a7c176d6c7a1d89cf30bb0d531530d473d13be971fe409577ff8d8`

```dockerfile
```

-	Layers:
	-	`sha256:a21dc55d100b07f9388abf38f7e5e7c484b0214bebeaca53e23ab429297a8405`  
		Last Modified: Fri, 14 Nov 2025 20:58:57 GMT  
		Size: 6.9 MB (6884769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3512fec1c7f4477e17d7143e904ed27b6ef8b69c042c2c95519a2136844a7eb3`  
		Last Modified: Fri, 14 Nov 2025 20:58:57 GMT  
		Size: 38.4 KB (38440 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:812255a6dfde9e8fe90164ee9bb268b08f0a6bedef04fb507d9ab9ea98a713f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172738986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddc35d8b8f81ffa8784bc363aab3069f5f244e59c6f2500a38e7885d65997bd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:23:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:23:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:23:15 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_VERSION=8.4.14
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 18 Nov 2025 02:23:15 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 18 Nov 2025 02:40:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:40:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:43:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:43:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:43:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:43:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:43:32 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:43:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 18 Nov 2025 02:43:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Nov 2025 02:43:32 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 18 Nov 2025 02:43:32 GMT
CMD ["php-fpm"]
# Tue, 18 Nov 2025 05:58:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:58:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Nov 2025 05:58:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:58:28 GMT
ENV DRUPAL_VERSION=11.2.8
# Tue, 18 Nov 2025 05:58:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 18 Nov 2025 05:58:28 GMT
WORKDIR /opt/drupal
# Tue, 18 Nov 2025 06:02:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 18 Nov 2025 06:02:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6112e3b80a3e216627481de123e8987e8cbfea908febedcef4d94eed43b14cf4`  
		Last Modified: Tue, 18 Nov 2025 02:26:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1cb9329bce7ae43bba9aade993af0716833c7ec3d06730bc0608966c31f5fe`  
		Last Modified: Tue, 18 Nov 2025 02:26:45 GMT  
		Size: 92.6 MB (92564354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc3e0671c639ec518dccc66d47a93c2878c73e2a26fb691b9604b4a7f6acf75`  
		Last Modified: Tue, 18 Nov 2025 02:26:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac38f4f86881882fd11f2bbee5b60d62a9695d85aa40fc15ff52ab60eb282e`  
		Last Modified: Tue, 18 Nov 2025 02:43:56 GMT  
		Size: 13.8 MB (13790209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dd9dcdf6ee5759ed497535c2fc8425c19d7a46bec9bf5fea223f411d9a744e`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee30960862e4c7f18656a3ed42e981ec23e2dd33fad13a549e7e21817a12f7d`  
		Last Modified: Tue, 18 Nov 2025 02:43:54 GMT  
		Size: 13.5 MB (13458606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdc92ec277d996082be86ee7616e0339ff7a3d395e3a89e87d9c99dde9a357b`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc17e811fac2aa081dce751b0d0bb31eec8bbc14eb4abde6965dfe35d713b2b`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4692b04cfd5343a7fbb4c2c08b295be2544629024fefdd2bdd3f48958b79f8c`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd341d193e78806161f22d02b2de702259cc3087c8528077c3e5067a6c8d52d8`  
		Last Modified: Tue, 18 Nov 2025 02:43:53 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22411ef83cc38a0c5f023dae30aec346fc4b658f5020e1492cbe923f353c34a1`  
		Last Modified: Tue, 18 Nov 2025 05:59:26 GMT  
		Size: 1.7 MB (1651585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c7cea3064f5c9ad4d5f371e96d59c371a065c90bac8aee4584e45506a5778a`  
		Last Modified: Tue, 18 Nov 2025 05:59:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4812a8fb8332f2467049195fb27176de36c2ac9f703a9dc8ee7ed594d66ee492`  
		Last Modified: Tue, 18 Nov 2025 05:59:26 GMT  
		Size: 772.1 KB (772147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0bd6ad7d290cf63e0597dc8893801093c8eb7a7d4a9650bb1e992a3d7ed60d`  
		Last Modified: Tue, 18 Nov 2025 05:59:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1a982545938308b8ad1933e7120e025ee0ee04d57cbc67f07d5263d42f046a`  
		Last Modified: Tue, 18 Nov 2025 06:03:17 GMT  
		Size: 20.7 MB (20654167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:18df645b1d2c18ef97c1cc7781c4632f4ac31bafbdefcf3866f05feedb7b2099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fe314a1baf8abcf337024b0836fa96821479f7d51a861715d802bfcf1832fa`

```dockerfile
```

-	Layers:
	-	`sha256:7c530fb6e222c37569f985799adef7cec3db561b1017666f75d6c5965a8983bf`  
		Last Modified: Tue, 18 Nov 2025 09:08:52 GMT  
		Size: 6.6 MB (6630219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8ec9bf78999a8d4af784aa647cb4ad42d5e13b7cccc7f0d35f4c37dbd108e8`  
		Last Modified: Tue, 18 Nov 2025 09:08:53 GMT  
		Size: 38.3 KB (38303 bytes)  
		MIME: application/vnd.in-toto+json
