## `drupal:rc-fpm`

```console
$ docker pull drupal@sha256:569b3b7dd13576beb8026dffa7f737f7a79a486d054789c75665daa539a3a92f
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

### `drupal:rc-fpm` - linux; amd64

```console
$ docker pull drupal@sha256:285b20822ca63df8922ecfc2923a52355cc26f9b7565d9235b0c5094ea6bd379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195373081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5888c55abe741cec95e8eb1f101bff839fe34f21b4b615ffc6dc85ce3e0b35c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e881592e808c901299c28181782f4352df25f3d05fb65aad76e6c9d10c6c27`  
		Last Modified: Wed, 29 May 2024 23:18:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a4c251f36c9a7cd5c6b279c62fe1009f9ae4960e681bef0697387ef94388df`  
		Last Modified: Wed, 29 May 2024 23:18:30 GMT  
		Size: 104.4 MB (104357409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433084d93d648338100d955c81e31a60256909b24864a2a676fc7578e2916400`  
		Last Modified: Wed, 29 May 2024 23:18:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172acf3375d101024d5f344058fa81777afcf5dd3b23a87250920bbba7e46844`  
		Last Modified: Thu, 06 Jun 2024 22:16:19 GMT  
		Size: 12.4 MB (12413790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d5f47e1e96fa95b5856b85fd0646bfe01471008ee253b2f22da9f34642c253`  
		Last Modified: Thu, 06 Jun 2024 22:16:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7607b8700eb78f241f73aeeb2349b92b482d7683bbb3dfef20ef68e80ae5fe9a`  
		Last Modified: Thu, 06 Jun 2024 22:17:04 GMT  
		Size: 27.8 MB (27778730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4ff67ef0952ba036a5ff9b6c11648aace229c8a16ec4893087c44668b5e3cb`  
		Last Modified: Thu, 06 Jun 2024 22:17:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f71b9514989b2ca80b51aa78d05d74534732d1b2d3a84a1cb597ecc5bcc612`  
		Last Modified: Thu, 06 Jun 2024 22:17:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4114dd03e7c590f61c32f198e68f4ac74b539abfab3f605288d77a1c595939`  
		Last Modified: Thu, 06 Jun 2024 22:17:00 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3804504287070a54e462e87c6460aea2ffe272b5611ba4bb3a40025410e0d797`  
		Last Modified: Fri, 07 Jun 2024 01:01:10 GMT  
		Size: 2.0 MB (1974574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f0f61f8df588780bc5b28679bf97aadd7f3af021c6a233504e5fb95c330646`  
		Last Modified: Fri, 07 Jun 2024 01:01:10 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b651d6f68ed813120bc5e39267c1c96f332b1d37a5f8659b17d6b00d0d7ed69`  
		Last Modified: Fri, 07 Jun 2024 01:01:10 GMT  
		Size: 724.7 KB (724737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5006082d07360f604463b2c07d23b924d92ad2fc615431e689e8b0cda2f7900`  
		Last Modified: Fri, 07 Jun 2024 01:01:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e34260b74e7315a5028149e78beca9bde996a18d0e671b4a01a78ec8067830f`  
		Last Modified: Fri, 07 Jun 2024 01:01:11 GMT  
		Size: 19.0 MB (18960130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:e8468161d8b78565722d333e9403d8dc9936681f3fe50930ec8122c974c1f604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6311633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2097ea84794e288acfe613fa22609a50ad6e377c5e738db99be35fedab11bff7`

```dockerfile
```

-	Layers:
	-	`sha256:4edc4d2b2272378825f9cae036832de963c850cd7ad1d85fcb2b014ab4f4d063`  
		Last Modified: Fri, 07 Jun 2024 01:01:09 GMT  
		Size: 6.3 MB (6276572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543abe9ccd73b7f5fd071916193ceca110dcaa866a4ff3f4edcd1c2c41f6ec80`  
		Last Modified: Fri, 07 Jun 2024 01:01:09 GMT  
		Size: 35.1 KB (35061 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:1b483ec4504f44392790b09f3731a3a69cfb58ee8b7c8a4478f0733084ef0d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159743164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9e9cde1b6c8f772c929cafce8f6150364c18326dcd24eb921a7af8ffd8aa0d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0669aad48e5535f7a37a1db4ef7adc3041b27d6401be481d96b2f1caec7135`  
		Last Modified: Wed, 29 May 2024 23:34:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1889970113df85d42205d7749e42d9479aafae8a28ee304a252b39596d9d15`  
		Last Modified: Wed, 29 May 2024 23:34:54 GMT  
		Size: 76.2 MB (76173127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ba193271322395ee1837a5096cc8266945252cf87c1611520b9a9d37d64eb`  
		Last Modified: Wed, 29 May 2024 23:34:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c3dcde11138e6345024776eff6a23d6cbf9140d5f3b7372417e16311b4c0b3`  
		Last Modified: Thu, 06 Jun 2024 21:42:44 GMT  
		Size: 12.4 MB (12411507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af7079485f95e498a835bcd2f603db17e02adf6e6b0a8357e9d7371f9c0ef24`  
		Last Modified: Thu, 06 Jun 2024 21:42:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d168681cd6296dabffaf481a4568050c834892d70ab33f3678fe2a8c3f018c`  
		Last Modified: Thu, 06 Jun 2024 21:43:31 GMT  
		Size: 25.4 MB (25389058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e05a2085f6a4726141f45fb1f451ad1718ae5bda8fd06530f0c200481789d`  
		Last Modified: Thu, 06 Jun 2024 21:43:26 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591f1ba579b3932d50261c42123d0b47d4113abba2357d502efccffbe0d9ebf6`  
		Last Modified: Thu, 06 Jun 2024 21:43:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b538cb799c7270769cb5bf5342712a929e9de376941faba441a47d011f02ae`  
		Last Modified: Thu, 06 Jun 2024 21:43:26 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdf48f3c0128eb358e3e9d4b032ac66374d809979ab5021c57288b0c6d46cd6`  
		Last Modified: Fri, 07 Jun 2024 02:45:10 GMT  
		Size: 1.3 MB (1331141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d66750f3359db936442d37f6391978d979256476e702fb8b7d115584ab7a9b`  
		Last Modified: Fri, 07 Jun 2024 02:45:09 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67bcf42d93e63a011d447207cf6323e29e074d2c31e74079ded8b79a360f21a`  
		Last Modified: Fri, 07 Jun 2024 02:45:10 GMT  
		Size: 724.7 KB (724737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bbd020204be5f517508ebc5b2c122d09135385e38c48cbc4b82d8181b39a9`  
		Last Modified: Fri, 07 Jun 2024 02:45:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb63adbf0f7ec267243d1b99721e39c6a5cb0b85d9f62d96d1f5b462ffd9b41`  
		Last Modified: Fri, 07 Jun 2024 02:45:12 GMT  
		Size: 19.0 MB (18960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:d1a36fb3e6825b60ce75300f274074536ba5e86c704a366ee2b800a33476acb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6127889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b303796620b5fda50d42fd3a4305eb9f251d41ac04456c880cd37e6950e19d11`

```dockerfile
```

-	Layers:
	-	`sha256:c8f3b89134e30998003f82f7f8e5899583ae8c9337bb82445a8ae6d663cf3814`  
		Last Modified: Fri, 07 Jun 2024 02:45:08 GMT  
		Size: 6.1 MB (6092659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1593003e4ecc6bee6d66aa245132543e0fe2f9ec16ebda29ad56692061b0152`  
		Last Modified: Fri, 07 Jun 2024 02:45:08 GMT  
		Size: 35.2 KB (35230 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:3a417f12f39a68c47d3be3f45b58bafb4de27c086e714f785610d88fe44e5ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189396439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8e1c82577fc8fb060569696eb2ddf01a88d24dd9a5c7dfc7005798f23dcb9f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08227a7cdd1d3214d11329cf01f5114df7343b00fb37373161db1e32fd1cb35`  
		Last Modified: Wed, 29 May 2024 22:53:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea103f4ff29331e870d8e27667d0726fc38087fb5545660758eaa86427458d8`  
		Last Modified: Wed, 29 May 2024 22:53:54 GMT  
		Size: 98.1 MB (98133034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f43600df16ccc688ffc47123b84c497ed1483c88ad36a6eb39e2fb5c11e055`  
		Last Modified: Wed, 29 May 2024 22:53:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be098b7a646f9dc60da3e16dd3821f867e615f8ed7f17039b8b596413e06314`  
		Last Modified: Thu, 06 Jun 2024 22:23:27 GMT  
		Size: 12.4 MB (12413600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279a6e018989b132a1b8c8a79b23bc26e0e8e19f27cd440ae0cb5af21c40f9b`  
		Last Modified: Thu, 06 Jun 2024 22:23:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3b592031b2e7bfc5647be95cf32ad2bcb5788692248ccd43d31bcd37cf43a6`  
		Last Modified: Thu, 06 Jun 2024 22:24:09 GMT  
		Size: 27.7 MB (27740289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371a987cf72a80ead405e2f50b19323730b2102e755a4b7ad6beebcba384a78a`  
		Last Modified: Thu, 06 Jun 2024 22:24:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318fe09998c7e6c47c20c82706b9b35c6b9643bbb8314e3996a1404aed79c30e`  
		Last Modified: Thu, 06 Jun 2024 22:24:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a8829a8ab9f4f71027577409c32d9d97c04102090c31bb2eb0c36fce492cd0`  
		Last Modified: Thu, 06 Jun 2024 22:24:06 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f86f6c2e0c0cddbea49fd289661f220edb78b09ce5d88a4e21a76d572b6149`  
		Last Modified: Fri, 07 Jun 2024 04:30:10 GMT  
		Size: 2.2 MB (2231867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5e8b87c6d18c1ed3c1d4f1960f8582293ce01f9414c90cebe7a84c78f32c1`  
		Last Modified: Fri, 07 Jun 2024 04:30:10 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46490e5d1213ec5594de6e7f0f015fbfd4c873f28c4d14809fdb308d11c931`  
		Last Modified: Fri, 07 Jun 2024 04:30:11 GMT  
		Size: 724.7 KB (724739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bb3e3952518f9ca0547ece7df6322e664ff7bb7aaaa9e1a8c9fbecbc7549b5`  
		Last Modified: Fri, 07 Jun 2024 04:30:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379633a12627eb0a8e2355f1176a71646286e0f2de0bd87f49c524423c49139f`  
		Last Modified: Fri, 07 Jun 2024 04:30:12 GMT  
		Size: 19.0 MB (18960103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:394ee99c6ca64850d2b916f6b9a65e5f25ab6321ac0ae2af75e74e8a5bcdf49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfedcf63f30468bc5694c12c829087ca38fa228f821f3fa36951bf4db11387e`

```dockerfile
```

-	Layers:
	-	`sha256:4bf991dfca64537de6083722ea69a406717d85354abbc093318dbe5acf1106b8`  
		Last Modified: Fri, 07 Jun 2024 04:30:09 GMT  
		Size: 6.3 MB (6305096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9651aa62c533afd1321f9aa71037f45786f50388edd2dfb4b09eeb5684da033a`  
		Last Modified: Fri, 07 Jun 2024 04:30:08 GMT  
		Size: 35.7 KB (35696 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm` - linux; 386

```console
$ docker pull drupal@sha256:39b6702c5d7a2ba3add45f7bbe0d33217734648063dc0dfc047ca2e6114a9034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194123577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2bfd318d15f211983dec2f30849bf761e8601fe84db715529cbbf01c4bfaa6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae88c065305a602f05cd639106fec77ad90518828f24868e72e94f2b868a91db`  
		Last Modified: Thu, 30 May 2024 00:11:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38dc35f57533fe117dfe52d1ac36d9db0f5f48559d72644ab74f02e59872070`  
		Last Modified: Thu, 30 May 2024 00:11:48 GMT  
		Size: 101.5 MB (101522125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182dff1affda7ce47a96f6302ef714a6841c43a7a7cf068f253b6d813864f135`  
		Last Modified: Thu, 30 May 2024 00:11:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed4f2ea8407f03723b0336acf8cdf66792fd7e171dc77d6ad1fd30ff1a73be`  
		Last Modified: Fri, 07 Jun 2024 00:11:46 GMT  
		Size: 12.4 MB (12412897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252af366b73d629afd078560d21beca5c9cb386b42038b44bfff7a799637c3cf`  
		Last Modified: Fri, 07 Jun 2024 00:11:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c023275ac2dfe8118a96da75042d511b2a6d643997020b427d8a664d73d8e12`  
		Last Modified: Fri, 07 Jun 2024 00:12:39 GMT  
		Size: 28.3 MB (28300235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea3581fff576378a68ad57f7378ac03eefd4214dacdf219d145494708ecf40c`  
		Last Modified: Fri, 07 Jun 2024 00:12:33 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ff80e060a9e0f12a2390183b5dda4fdee11fa2e05ac68c087eff512d7747bc`  
		Last Modified: Fri, 07 Jun 2024 00:12:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449a32b70178db817c7e2d9509f60bf60cd472f5d75d46015af6f5a584d3b29d`  
		Last Modified: Fri, 07 Jun 2024 00:12:34 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2f7ba3bffde8047b28562e306b699121f431ca8bd856474800291806dfb8f6`  
		Last Modified: Fri, 07 Jun 2024 01:56:55 GMT  
		Size: 2.0 MB (2027302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1adb43eef9087ea319b9e6a3b0c2f234261fad30fb1ac8fc7afe3bf18de7c0`  
		Last Modified: Fri, 07 Jun 2024 01:56:54 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67454d332e9d5d7431433725373b96709e89c5c7c662396a7f9975a23bd1f18`  
		Last Modified: Fri, 07 Jun 2024 01:56:54 GMT  
		Size: 724.7 KB (724735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a43cb93bd28b07f7bc1159dea94254a2436e0d85203dc9c9fd0d16a62c82495`  
		Last Modified: Fri, 07 Jun 2024 01:56:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf45f70022a69cbdfbd7bb31b906915cb288106fd6a12d01ca3acccf7df6a01f`  
		Last Modified: Fri, 07 Jun 2024 01:56:56 GMT  
		Size: 19.0 MB (18960392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:38097f1b98c854056f4e2df8137039a8f06cc7aa74825bd08d44150df7c74fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6292314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53df4958ea2b52d1d7fb35424c227a4922e39c5186bc9450b0a04427888314c3`

```dockerfile
```

-	Layers:
	-	`sha256:5cdfff471e68c875e7f6b381c5a60ed320ccba31f64fe4332b0d5164f2dd6c86`  
		Last Modified: Fri, 07 Jun 2024 01:56:55 GMT  
		Size: 6.3 MB (6257330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c1be13271e8499287baacac60a60faffc94401215c2b2270ca8a84c380e62a`  
		Last Modified: Fri, 07 Jun 2024 01:56:54 GMT  
		Size: 35.0 KB (34984 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm` - linux; ppc64le

```console
$ docker pull drupal@sha256:6abc7a409651c760e99794ee039538657da43b571c45bee0ef46ae8cf5c3bfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199238285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bd08c75817657951785fcd9bf28ce36a5948fa9a74956851702555a07f869b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da3e260369cebf4c4f8ff3a322a8189ac84c811c2f0730eaf0e889033b35193`  
		Last Modified: Wed, 29 May 2024 23:47:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0b39fd81bebe81729ed8bac9fef9066c71d11a146b0ad366372e4e50686280`  
		Last Modified: Wed, 29 May 2024 23:47:54 GMT  
		Size: 103.3 MB (103316970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49947ee01e2a48415fc10d7c62c69ef77995b6b859d8014feffcbcdb074b7ef4`  
		Last Modified: Wed, 29 May 2024 23:47:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734b7527e3c290c58ba3a2008ac4418ecc45291dfce08f80810bfb88006fd23`  
		Last Modified: Thu, 06 Jun 2024 21:31:59 GMT  
		Size: 12.4 MB (12413064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc930427daca6d18aeab054857020cc539f35ab4706ab564324b2f4872c270e9`  
		Last Modified: Thu, 06 Jun 2024 21:31:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3935be7077103fbd657aa5fd54f87f32df3c3208063f7a229593f0342130ef`  
		Last Modified: Thu, 06 Jun 2024 21:32:48 GMT  
		Size: 28.8 MB (28836142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f3bb19c9535348fdd20852b57d2c67dd63243cc95e89fa8f11bfed45e15738`  
		Last Modified: Thu, 06 Jun 2024 21:32:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264bcce15cfeb142a91ef8f067246ebd2e3cf16c5eca5530979a5335d1cf376c`  
		Last Modified: Thu, 06 Jun 2024 21:32:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b2ab75d946d3b7e95686557a96da1103874d8d8446b6145e459bcb6acecc6`  
		Last Modified: Thu, 06 Jun 2024 21:32:43 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf862389966cb02fed8a0ca0e176724f0edb4d0b9bfb617b9f8529976ac2cc46`  
		Last Modified: Fri, 07 Jun 2024 03:14:41 GMT  
		Size: 1.8 MB (1832690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba658056e596ca18ac5c5af8f4d6ff0f5583218383beffc4cf13fcedf7226d8`  
		Last Modified: Fri, 07 Jun 2024 03:14:41 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b8ea7d3970cf0c6992e54602ea8140216ea7cd6557b6a3ca88da928c91bda5`  
		Last Modified: Fri, 07 Jun 2024 03:14:42 GMT  
		Size: 724.7 KB (724738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4336804222174e973c8b1cd034ee8bb1af585afbe5b8c3ed550a66475f2889`  
		Last Modified: Fri, 07 Jun 2024 03:14:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089cb46e6c1a5b21b88c357c3608f16c7d91bc5ae35fe4b2d65a1cecfe417c96`  
		Last Modified: Fri, 07 Jun 2024 03:14:43 GMT  
		Size: 19.0 MB (18960210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:c65ea03bcd4f25561cdaa93173ee2568c702da4ddf39ebebca2d7c5a52ca13a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6288977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487736e8341105d4770bdb2e5b6147734c4c3a0b7160cfb13fd3d8040e1eb0b1`

```dockerfile
```

-	Layers:
	-	`sha256:ad6b71b0d1bdfbd6078a614adb62ec25e9404dda18069257cd976a30c1e2b5fc`  
		Last Modified: Fri, 07 Jun 2024 03:14:40 GMT  
		Size: 6.3 MB (6253823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c364254703115020496062c69a7f7260600f399d98979c0a14eba6e196cb79`  
		Last Modified: Fri, 07 Jun 2024 03:14:39 GMT  
		Size: 35.2 KB (35154 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-fpm` - linux; s390x

```console
$ docker pull drupal@sha256:6f06d5bb881714ce72a4d305c71296e54394029b0a325a3a84e711fe10061f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168863654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d05c1a11c3cf4992c30c43f9062a526150b809e214c6ab293d93ab2d94752f1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.2.20
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:55:49 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c7c5236d1c8356fc773b8cce2bf09dec8f54b44c3223f36d6d3e7bf823d87`  
		Last Modified: Wed, 29 May 2024 22:42:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b095dac692581d3ab7d8d35382ada1f35fc014fb3b708c2c5a0228b973e596`  
		Last Modified: Wed, 29 May 2024 22:42:34 GMT  
		Size: 80.8 MB (80814039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781911421736c891768da7f2a43ef63663f6978a1e21555583dd6d6a8d630912`  
		Last Modified: Wed, 29 May 2024 22:42:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507464ebc1485c95010b9aedd1a42201370256a83932245b230ec969cb95f98e`  
		Last Modified: Thu, 06 Jun 2024 22:03:24 GMT  
		Size: 12.4 MB (12412002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f308d2675e609682acbc295829804029c91fd63fe66b112abab2e59915fd9d3d`  
		Last Modified: Thu, 06 Jun 2024 22:03:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca7b9b6c57d93fd628a3cf0726c5930894eb949c4e7da0871b712af074ef46f`  
		Last Modified: Thu, 06 Jun 2024 22:03:58 GMT  
		Size: 26.9 MB (26895585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303de92eeef5b45a0e6823a627320861cbecac90d558981147eaa17f6a219b04`  
		Last Modified: Thu, 06 Jun 2024 22:03:55 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a04c8fa4b9f18880f52ea1cbcec92e2072af1deb452f2c42d4d7bbad39489b`  
		Last Modified: Thu, 06 Jun 2024 22:03:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592fd3c202a66d340c083c07bae16ac5f2bb887a24935040fd53dc6cc672e279`  
		Last Modified: Thu, 06 Jun 2024 22:03:55 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad4fa1110a478270d25d89fcedb09e6a3265a002de49deb11a981bbb72b2f`  
		Last Modified: Fri, 07 Jun 2024 02:35:33 GMT  
		Size: 1.5 MB (1531171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19ee3e3d7be33b886ac434ac7b2d9539c908738a9298648e046689c19b5a648`  
		Last Modified: Fri, 07 Jun 2024 02:35:34 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7dde6e1becefd529911733b4ab83680639d18176870bfb66207d0e8eb14c5a`  
		Last Modified: Fri, 07 Jun 2024 02:35:34 GMT  
		Size: 724.7 KB (724734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fb3cc55f1385473d1e8ab4927b83b6bc9189c04a1d550265315719a32e30c0`  
		Last Modified: Fri, 07 Jun 2024 02:35:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faed1e210619a9b2f2f517348dc3b34d703633908e479c578847bc562dc6e75`  
		Last Modified: Fri, 07 Jun 2024 02:35:35 GMT  
		Size: 19.0 MB (18960422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-fpm` - unknown; unknown

```console
$ docker pull drupal@sha256:a0aef7a36f352d994c2e1b47e66aa9482dcd70fef9d56d4b3927c679aaaca447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6154065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1004e38fa53dd9e092fc6440962bd61366045920e8c59f799877f550edb679`

```dockerfile
```

-	Layers:
	-	`sha256:00d31489f8c7cda7f1f336d5c20f036c1ec8a324ef0bf491297d557b805a077e`  
		Last Modified: Fri, 07 Jun 2024 02:35:32 GMT  
		Size: 6.1 MB (6119010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7242a1177e886373df726ea8977e5cb3ea4d8ab7aee9c9c9df703ccffd3e6922`  
		Last Modified: Fri, 07 Jun 2024 02:35:32 GMT  
		Size: 35.1 KB (35055 bytes)  
		MIME: application/vnd.in-toto+json
