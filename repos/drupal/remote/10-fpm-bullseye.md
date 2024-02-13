## `drupal:10-fpm-bullseye`

```console
$ docker pull drupal@sha256:59dabd202f9fc349def830b0393a6ccb05f986c7b56c80a969978ff37fbd8107
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
$ docker pull drupal@sha256:c29e838703d8bf5bdfc46f7685d7a8b9534a8a3d1e83f2c7ec8a1578368dfc44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183852356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b19abab8b589e6db0b4c197cc0263415e947f8d7a112efc08ba8a0eeacdfce4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 9000
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee69c64d732ecebe5d2919ba64b1f81070d6294ecdea3f26212804996138cc2`  
		Last Modified: Tue, 13 Feb 2024 07:34:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f340802765d00d2774c8c4f6d1676c95e56149c32b2141e667ae5732cdee5559`  
		Last Modified: Tue, 13 Feb 2024 07:34:40 GMT  
		Size: 91.6 MB (91640032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c633b2e11f96bfde31d21c104f45ec3f3c3e59713bbeac1719df7774fb9bc`  
		Last Modified: Tue, 13 Feb 2024 07:34:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077e0b6e18d82d1944aa0e0e059fb45266db8156f9943d88e76ff7a75bef7ed2`  
		Last Modified: Tue, 13 Feb 2024 07:42:54 GMT  
		Size: 12.4 MB (12394249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c6e168e426ce642d6e29137aca445a7562a0a5df084242873f3d6456c69e4c`  
		Last Modified: Tue, 13 Feb 2024 07:42:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee00b18d2d52b6780bcee6b2b974f8ac1fb30fcc96c332662a07f89608a34aa9`  
		Last Modified: Tue, 13 Feb 2024 07:43:25 GMT  
		Size: 26.5 MB (26511289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bb8436fa9cce2f17593edb45eaf6ff9a2515af1107fdcd5987b3f2e09efb36`  
		Last Modified: Tue, 13 Feb 2024 07:43:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb0fe747eac177d5db26f58ef412d18fb9f3507c7f6661341fe226b9735f99`  
		Last Modified: Tue, 13 Feb 2024 07:43:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa60542a8b2056942a33fec497b2ff17b4a488df2501307488289a1c02d560`  
		Last Modified: Tue, 13 Feb 2024 07:43:22 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2efac8d8040b02e951a2b0c75162cf785129f86e48923761156bae00c217ec2`  
		Last Modified: Tue, 13 Feb 2024 08:57:43 GMT  
		Size: 1.9 MB (1902033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431b4483350b10fd6da4a40190302435ff76c72cb8c3ac70001d86821ed66c3`  
		Last Modified: Tue, 13 Feb 2024 08:57:43 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba07ceac8a1d9ca2cc359ec34ce3b31370a2860c45f410fe2e224e914ff24d`  
		Last Modified: Tue, 13 Feb 2024 08:57:43 GMT  
		Size: 721.6 KB (721579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecfab3139fc41832753ae335994df11961085d727c0636a3094616991186671`  
		Last Modified: Tue, 13 Feb 2024 08:57:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4353a8c137b6ff5d86f392db16cdbcee9d41c9e06a5c4a43e12225334dfcc550`  
		Last Modified: Tue, 13 Feb 2024 08:57:44 GMT  
		Size: 19.2 MB (19247463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:3c1b2362b10874d480ce56376153e5c77dcc5ac7ad7e5ca5afdf0e7a39222218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6159313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f0623d1653ce76f66ff460dab1e5a3edfe174a3502b58f57c59558420cb55e`

```dockerfile
```

-	Layers:
	-	`sha256:11c8917e44c0f43077ebc361b10c6e707fc18fa17c815d8db4ced432f232a16e`  
		Last Modified: Tue, 13 Feb 2024 08:57:43 GMT  
		Size: 6.1 MB (6122273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1016df25e8ca5b8dba6825a1c12d332e7b162c708416e2d3beed13ae51198644`  
		Last Modified: Tue, 13 Feb 2024 08:57:42 GMT  
		Size: 37.0 KB (37040 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:c018d88084dace8249a43d0cadc84109ddff798359b742ac4071b89e92d82cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153801814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8568646344148aed551f5313a321ce7a4e1014b751d1fbe7bf8590f108332b9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:20:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 03:20:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 03:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:20:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 03:20:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 03:20:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 03:20:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 03:20:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 03:45:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Feb 2024 03:45:49 GMT
ENV PHP_VERSION=8.2.15
# Thu, 01 Feb 2024 03:45:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 01 Feb 2024 03:45:50 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 01 Feb 2024 03:46:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 03:46:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:55:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 03:55:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:55:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 03:55:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 03:55:33 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 03:55:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Feb 2024 03:55:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Feb 2024 03:55:34 GMT
EXPOSE 9000
# Thu, 01 Feb 2024 03:55:34 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5252a47b45edd6cea077483e42a2eaed2dd0d962da76878e4f08ee0f178b8`  
		Last Modified: Thu, 01 Feb 2024 04:27:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffeddc903db1a88b20dd08efe0235a835518390e0ea4f194e044848d1f9f72`  
		Last Modified: Thu, 01 Feb 2024 04:27:26 GMT  
		Size: 69.3 MB (69324006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6770e3000dbf2bfacda02d788f35c49745c4d61edfd5508ec224469de7832857`  
		Last Modified: Thu, 01 Feb 2024 04:27:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4fb557124c78a7c377ddea3f2b3355626e6e8507b71b647432ce08a4c4eefe`  
		Last Modified: Thu, 01 Feb 2024 04:30:23 GMT  
		Size: 12.4 MB (12393542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a6f9bf52dfcd07974835a0d8819c0ce6282772b34c828a2165eb412574e1b`  
		Last Modified: Thu, 01 Feb 2024 04:30:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b930dba04c0e3c5031143a494620fd7353c086213c1e209eb04ce7a889bf6527`  
		Last Modified: Thu, 01 Feb 2024 04:30:56 GMT  
		Size: 24.2 MB (24240110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6794d1a2da1a09d393f37461b6e30365c2d1ec14fe2822d5d947262ec7a601`  
		Last Modified: Thu, 01 Feb 2024 04:30:52 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83acf4e146a7df5ab86ae13a46607aae4283276555cdb1cac0d5a33531111f51`  
		Last Modified: Thu, 01 Feb 2024 04:30:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e9db15e8a071ee33788216f5b11dd25e962d7d8ee8009bb45526bf31ccc3e8`  
		Last Modified: Thu, 01 Feb 2024 04:30:52 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a73c33c350479eed869dc8f22861b6378aae6b8bfc1ac964fc38cd3eeec25`  
		Last Modified: Fri, 02 Feb 2024 15:41:59 GMT  
		Size: 1.3 MB (1282673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ed1dd69e526cbb5b354c0dfa3109ca4fb7782d7adf33115543e2256b369655`  
		Last Modified: Fri, 02 Feb 2024 15:41:59 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56feaca2207aaa79265bad2e8689f442a1d3bc12197d20412783e8a765ff54f1`  
		Last Modified: Mon, 12 Feb 2024 22:21:33 GMT  
		Size: 721.6 KB (721587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18bf0b7bc5e3d88eeb96da70f83190e8c41f5b865007ff6dd926a3686a670a8`  
		Last Modified: Mon, 12 Feb 2024 22:21:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c722ee3c43443cade3bc00da5e200918f32eacd5bf32a7b7ec96101f772d9fd`  
		Last Modified: Mon, 12 Feb 2024 22:21:34 GMT  
		Size: 19.2 MB (19247379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:218898cf90d22d7419fa5102c6a995a09cd79ff4297b0476661236c312cfe09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d2a90c865727364bbc3c99126d54a82723f5f6ace62e6e08fb0fb625ad7d89`

```dockerfile
```

-	Layers:
	-	`sha256:b3485b45fb90e7e04ec68d3b0e0620928bd7e2639d74068b4ecc458a2a8b0ca3`  
		Last Modified: Mon, 12 Feb 2024 22:21:33 GMT  
		Size: 5.9 MB (5864912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a368b5fd140a70ea8e4ae9ff12ab26dd8f6a709c02d63a1ad9782d3a0f4c09`  
		Last Modified: Mon, 12 Feb 2024 22:21:33 GMT  
		Size: 33.3 KB (33286 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ef1348e9f68a454225a775d35ebc35abc0df2acfa3b92ec32c43605133e82ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178123776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab63fe74b622fb3e2e87b1452f60ced3240c72a14a480cef62fbd7fef0f25f2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 9000
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e6761f5309e7053d74e42ca6e73ff3d4654fcb94eafe53927cd9f968ded5d9`  
		Last Modified: Tue, 13 Feb 2024 07:01:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d087a9a699e52864665689cf4ab9b86b9acb06b2c89742057e48e0f4dc6000e`  
		Last Modified: Tue, 13 Feb 2024 07:01:57 GMT  
		Size: 86.9 MB (86934155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868526445d4e7ba5e3298454a4c65450b2a0f6a038cbee0c148f97ebfe8d4e3d`  
		Last Modified: Tue, 13 Feb 2024 07:01:47 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a81874610b573ca354f450c634172bba8bbef8b3c114247f24eaf6f61b13de7`  
		Last Modified: Tue, 13 Feb 2024 07:09:49 GMT  
		Size: 12.4 MB (12393598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768df7be2a70f455dc8ffde42732d53fe4fac98eb35b05f28a4f3a41767cef9`  
		Last Modified: Tue, 13 Feb 2024 07:09:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1883a91ed65076dd03290f3827818d5eb6b9e443ee5901e9de7e0fe3948ec8de`  
		Last Modified: Tue, 13 Feb 2024 07:10:22 GMT  
		Size: 26.6 MB (26574688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495129725cad0d2fb750c4f9f21967e6fd476d4c959e39854f9ae927e2ea5b57`  
		Last Modified: Tue, 13 Feb 2024 07:10:19 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aaf945474c1b8e9d573a61630658bbee6d422f09f95dece21d47bd36d463aa`  
		Last Modified: Tue, 13 Feb 2024 07:10:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddabdd240700919f8c9acfe26026599477ab0cd8c23a1966837b358fd4a0ef6`  
		Last Modified: Tue, 13 Feb 2024 07:10:19 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30502ca5351fe37b86ab4bb1da659baedc97b71db3d4cac2adf402ff4df58184`  
		Last Modified: Tue, 13 Feb 2024 16:29:01 GMT  
		Size: 2.2 MB (2167923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ea0f2d409d79b4f2954150a7dadc1025a7e61d287e3fecbcd51dec92ac9f5`  
		Last Modified: Tue, 13 Feb 2024 16:29:01 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a74bb8f039b8abbee57e2cea7e5ad0efa44e58ce1d2cfa98a5c9dd36da10b98`  
		Last Modified: Tue, 13 Feb 2024 16:29:02 GMT  
		Size: 721.6 KB (721582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec60e9c1799d4a36d094c9f823510cc249f7efc6b7bdadec25e834a7892ef88`  
		Last Modified: Tue, 13 Feb 2024 16:29:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e4741f12c908e8cd55364fb365f970f0e89e296fe867f6f5eb720f767acc1`  
		Last Modified: Tue, 13 Feb 2024 16:29:03 GMT  
		Size: 19.2 MB (19247460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:cf465b6b5c110c02a1b76c1e4be35e44edf324056ca9ac13cd6b06ab75660d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6159732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a27b68fdd8798b4fe5e24b2a6da5a9311cdb731c69c07ac22732a9c16ca2b4`

```dockerfile
```

-	Layers:
	-	`sha256:64016e0c19667832db4d47cfca6b35a0b18f39371c3d8a6885d88c5014e1b4ce`  
		Last Modified: Tue, 13 Feb 2024 16:28:59 GMT  
		Size: 6.1 MB (6124948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c5064c54c97be44c360f6edc93405b8260a8b95c89027251cf0af54f1bd71c9`  
		Last Modified: Tue, 13 Feb 2024 16:28:59 GMT  
		Size: 34.8 KB (34784 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:a32247ea4af0ef5c23a61e7a6e999d2289ef236cb59276a1d59c18198815f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186483100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1fcb9071138a817fb9c073beaabe3a57307d6266c5613bf205b6f13e1ff075`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 9000
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3089d788bef97302cbe520a086c8524ac2b4a692e40f7cd0e8a04eb4959459`  
		Last Modified: Tue, 13 Feb 2024 09:10:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbadaec58231cef49a6417f637ed3cc03c2e621ec0f98a9fdfc281d910f1741`  
		Last Modified: Tue, 13 Feb 2024 09:11:05 GMT  
		Size: 92.7 MB (92721599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f163a869e94f27c47a66c7b521e98be6d6be0ae174d7a2e4f2f64b0e3e4437f`  
		Last Modified: Tue, 13 Feb 2024 09:10:45 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10d34f2155e65d9df040c6282249e80a680bab3235eb9c9541bb6b13d599515`  
		Last Modified: Tue, 13 Feb 2024 09:20:15 GMT  
		Size: 12.4 MB (12393504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96088b652ef54b0771a2bf71a3d9544918d62bb08c184dfe691b399b674bda00`  
		Last Modified: Tue, 13 Feb 2024 09:20:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de95974b9b3d604c1a3ef70a837c156e5f011acb9e78bda636e2709857fc2631`  
		Last Modified: Tue, 13 Feb 2024 09:20:52 GMT  
		Size: 27.0 MB (27008557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ac628d913304197cd163a5cca3591b2b5a7e6ed17b6e81b3de4537294bdec0`  
		Last Modified: Tue, 13 Feb 2024 09:20:47 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec397619b53a0a9fa92effa80fd9861fe965125ad8a9914da12fc197e594f953`  
		Last Modified: Tue, 13 Feb 2024 09:20:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936be7ec5c7976a9f3a7504ccf62f29b8557de36a29526058bf77faeae527b77`  
		Last Modified: Tue, 13 Feb 2024 09:20:47 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a238f194ebe2ae7fe780a659b99e1cf7d0ceae0b2591cc6c44140b4db222d44`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 2.0 MB (1969629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcadca492493510b29aa59515937c4324c75efc42320acce43e746f7301da013`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9221d565c614449eafa72a2e09b9fb7e0b7ba219b7a04d2d280cafaccb1a38c`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 721.6 KB (721581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b50227a9a7aa8a92e4266595e2a15038259130dd09e961380f2c435b82345e`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff37fcae77c76af95f296b2ed66751f0cf5f916de411a9e20adf8eed6f1995`  
		Last Modified: Tue, 13 Feb 2024 09:58:10 GMT  
		Size: 19.2 MB (19247495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:4a86c9b0b84f8946a15560f315729b2b8a894560d8d5dae51a240c7f53fbae48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6150392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8474dc72f8edc32582d898c18e38dae353c2007b1e694b6def952efb0ba03b6f`

```dockerfile
```

-	Layers:
	-	`sha256:ecf2be624ce22ed833715d8c6faaf1543fb2dfb25bb79e82b9e3c7d18ef0644b`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 6.1 MB (6113409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0258ddde7193c61312446a3ad813511368552aada829ef1884f19e31ac78f2`  
		Last Modified: Tue, 13 Feb 2024 09:58:09 GMT  
		Size: 37.0 KB (36983 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:c8bc63b92ad038dee189785592a4250260345ca60e45453f7ba6b8425ddac851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183702742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dadc7658c427cc1631fdc9920e0dfc2056538507cce22c981c4fff62f6559f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 9000
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60a2e07f944badb5933cd05a85dffeb9381d92a5d4aa9ec6c8734107ed8d100`  
		Last Modified: Tue, 13 Feb 2024 06:45:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e8a4ec517f6c888244a9425d7fffe86960f5f7b9d094d7a27ad6bf7cd71a3e`  
		Last Modified: Tue, 13 Feb 2024 06:45:41 GMT  
		Size: 86.7 MB (86652532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4206748c9c84f95b69bb7c840742125b8415508600486e0ff2cec15cd13ffd91`  
		Last Modified: Tue, 13 Feb 2024 06:45:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafc9a57fc93e2a66a3cdaaa795f050a1629ed5051535b2f7b82c23a9ec8a5e3`  
		Last Modified: Tue, 13 Feb 2024 06:55:11 GMT  
		Size: 12.4 MB (12394221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270814a9f46e35001ab00c466cec1797ee2b6a635690bfabbc4dd4b27ed50ebb`  
		Last Modified: Tue, 13 Feb 2024 06:55:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83f9307ff0e771a42bf064046839f02d9d1f2f0aeee4f2d11dc4a8c6b262876`  
		Last Modified: Tue, 13 Feb 2024 06:55:48 GMT  
		Size: 27.6 MB (27607132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8f0cb756af96dbcf97f135e9b6c5e66a842609c60096e19d29d5e678ceba3`  
		Last Modified: Tue, 13 Feb 2024 06:55:43 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff927ae8f06fa79e8dccb147f04ab1b7b322b8df3660bcf1b336c327cfac983d`  
		Last Modified: Tue, 13 Feb 2024 06:55:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4904916258ba93005eff9fc8d6e43f25c135189356f8bc3ee3d57a12f703179`  
		Last Modified: Tue, 13 Feb 2024 06:55:43 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b26d06940143394e3071a0c3f3b8c5a7245b055a5467d4186e0cc8ee40edf78`  
		Last Modified: Tue, 13 Feb 2024 14:41:46 GMT  
		Size: 1.8 MB (1768696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa237bcbce76368bac0eb182f50e46a00a2fe315f2dd9e4483d31b2d3d93c26`  
		Last Modified: Tue, 13 Feb 2024 14:41:46 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c62ec8223f8c13acb46d6c82073af8f7d0e23310d7e1b4aa94e3fb8002f4ef4`  
		Last Modified: Tue, 13 Feb 2024 14:41:46 GMT  
		Size: 721.6 KB (721581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9360306a988491a354078a73be2db5b6a8de09cd94bb2009f193e168423b0228`  
		Last Modified: Tue, 13 Feb 2024 14:41:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234321080c1715449885da610277ae22e3d0e349a734a2f9c02fa4361c7bd3e`  
		Last Modified: Tue, 13 Feb 2024 14:41:48 GMT  
		Size: 19.2 MB (19247494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:6f1043265a77c9076ccdb67781a8f62de9e1a5eba2ebcd269ea4553c656aab39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6128886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820200fdf7d90cadda60de1a0170b711e5f589f25fcc2a060b990607af5bc2e`

```dockerfile
```

-	Layers:
	-	`sha256:0889d1c73c46d2387d14494bc7c31e1f87a3b7d272811b70ea59ec100f9fca9e`  
		Last Modified: Tue, 13 Feb 2024 14:41:45 GMT  
		Size: 6.1 MB (6094049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a26fd7384583795e5ec1debf346f6bb33a0218e705168ed2448dcdb550e3259`  
		Last Modified: Tue, 13 Feb 2024 14:41:44 GMT  
		Size: 34.8 KB (34837 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:59dce7f93d1f5c6fea1a1540354cb135cacacf0f09f11d0fb784ad7dd718e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160725013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a429ecf2c10897e9301767f0c684bd687e1f8bb9e8a3af6f686f4d3bf6b4d2dc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 31 Jan 2024 23:02:52 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 31 Jan 2024 23:02:55 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:35:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 01:35:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 01:36:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:36:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 01:36:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 01:36:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:36:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:36:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 02:16:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Feb 2024 02:16:24 GMT
ENV PHP_VERSION=8.2.15
# Thu, 01 Feb 2024 02:16:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 01 Feb 2024 02:16:24 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 01 Feb 2024 02:16:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 02:16:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:25:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 02:25:42 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:25:43 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 02:25:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 02:25:43 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 02:25:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Feb 2024 02:25:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Feb 2024 02:25:44 GMT
EXPOSE 9000
# Thu, 01 Feb 2024 02:25:44 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b97bcdc3dc03347191b2f148550b53e7ce76a72235d37dc7001b942384b221`  
		Last Modified: Thu, 01 Feb 2024 03:19:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1f72c1803ab9a6c0542c03e8fabed985787369cf715831e9538f5e2d97cdd6`  
		Last Modified: Thu, 01 Feb 2024 03:20:07 GMT  
		Size: 71.6 MB (71635450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0226493a3fefc8dddf4a852e076cc2dfd6981203493af7f6cdf8dd95f111468e`  
		Last Modified: Thu, 01 Feb 2024 03:19:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4663a56cbdfd28d2bcf139b4eca91260db531c7505dc8d0d3d713aa823ef4a0f`  
		Last Modified: Thu, 01 Feb 2024 03:22:14 GMT  
		Size: 12.4 MB (12393987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f67fc73b1167f845029504ed5ec9742ef09c2d6f96b2ad64fa3e8005480f7f6`  
		Last Modified: Thu, 01 Feb 2024 03:22:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a559886d46c7700516f6232da2bcb4de52ad50c544ed3cd5bb6c73d8c33d3e`  
		Last Modified: Thu, 01 Feb 2024 03:22:37 GMT  
		Size: 25.6 MB (25560185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72ba073e48e07ef92fc2e18e308239a1b930c0b48a49d41136835dca149c922`  
		Last Modified: Thu, 01 Feb 2024 03:22:33 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783fb9f60fc2b65539edd66c014c86ed383bae63156be5da74c51824e8ed4af5`  
		Last Modified: Thu, 01 Feb 2024 03:22:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc62c660947a68ac297cf519aeb29d62aaa3cb96ccd8fb40110cd7315239242`  
		Last Modified: Thu, 01 Feb 2024 03:22:33 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e1f293bde9ed0270a96f893ebbc215a58b2922f3e85faefbfd7d3616914ead`  
		Last Modified: Mon, 12 Feb 2024 23:28:24 GMT  
		Size: 1.5 MB (1496031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa1e4c9ccb7dfd22b69f21d5f8e74cb63ea64159b6080cf993f4412f971e066`  
		Last Modified: Mon, 12 Feb 2024 23:28:24 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fc8ba67bd2d4f701999f95b4e8154e02ed0d09af834c03c4a20adb774313ad`  
		Last Modified: Mon, 12 Feb 2024 23:28:24 GMT  
		Size: 721.6 KB (721585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a489f5e9ceea0ab9d5170e77e7e4fed9cb5600d20769ba9e9630352731f30896`  
		Last Modified: Mon, 12 Feb 2024 23:28:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96057f09e252235bc843d551821822aa58654e78fec73159b880660d91c2df`  
		Last Modified: Mon, 12 Feb 2024 23:28:25 GMT  
		Size: 19.2 MB (19247338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ae9703cc8c3258fc56ad9eab556a209ba51fe29c7f7ae572f72ab0d46c0e54ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5917386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31e5b1b87f3e87138254d87c6daa0a952e15c061c50072a7458c8cd17485564`

```dockerfile
```

-	Layers:
	-	`sha256:d0cc5d33b8cefae3b881a9d8b733c26a12a4012af18fa66b4d520269b5e392fe`  
		Last Modified: Mon, 12 Feb 2024 23:28:23 GMT  
		Size: 5.9 MB (5882619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:298df956859dd28345395cf0025f13296530e948d903b6c999f52a80fccce895`  
		Last Modified: Mon, 12 Feb 2024 23:28:23 GMT  
		Size: 34.8 KB (34767 bytes)  
		MIME: application/vnd.in-toto+json
