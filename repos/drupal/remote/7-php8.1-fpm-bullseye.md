## `drupal:7-php8.1-fpm-bullseye`

```console
$ docker pull drupal@sha256:ce3fa4ff2c8dbdb807239eddf547a8d751145226cf050502eaec9bd6fee9f66f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-php8.1-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:ecdc0d23718680a8abd6601a65a5a248616ee385ab24c83e8714e908f03b4646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166894692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e57cb15cfd2f108458b64325b63a532252c13d1ed8f7f471fbd5f1495612e07`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:2e65db977be37b862c7548e5420c5b3d40eec6f6e63f00a61b3d0e5182c786cd`  
		Last Modified: Tue, 13 Feb 2024 07:45:16 GMT  
		Size: 12.2 MB (12233984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efdb5e2df228747231f35162dd4053f3f48fce1cbcb89ad4a239b4ddbc7a565`  
		Last Modified: Tue, 13 Feb 2024 07:45:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0aae843e6dc6899db2a9b4ab05e911ee469400e02646a43e1804df121acb5f`  
		Last Modified: Tue, 13 Feb 2024 07:45:47 GMT  
		Size: 26.3 MB (26268070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfad1974da33a0b33b6be7a11d342928cfeb5d72b8c68203fda6a971d09342f`  
		Last Modified: Tue, 13 Feb 2024 07:45:44 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766edf9d0f0dd9ef4a2c5c3b409f22020f87ad6577a1ce691aab2c9a8aa52ad3`  
		Last Modified: Tue, 13 Feb 2024 07:45:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be367d4c4f67327e551e3f0abe6e371da1a37cfbb3d8a3436feac17e48e3174`  
		Last Modified: Tue, 13 Feb 2024 07:45:44 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9573e63b8388e89ab4c1a13eb4f9a5e63299d8256ff3a51dab5abce2a25608be`  
		Last Modified: Tue, 13 Feb 2024 08:57:47 GMT  
		Size: 1.9 MB (1898428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99920dc03722ce1ce514b09771da05db6aa15f422cc535ebf7d529048599cf`  
		Last Modified: Tue, 13 Feb 2024 08:57:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60916c2f653cc6e06073760b0f36e7cf4af9eb7eeeca59b3846e19ecb64d59cc`  
		Last Modified: Tue, 13 Feb 2024 08:57:48 GMT  
		Size: 3.4 MB (3418879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ade6310cd975323e18a0c5b02877fddf3d3ad7b9eea27a5b275a6dad28a5b097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5572305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6005fa9f30b4b37aa0159e93691d556baddae73ab2d06380efb9e75a15c1973`

```dockerfile
```

-	Layers:
	-	`sha256:4afd2fe674506a6af4fa4821955b6684cf6dd7274a4656ba9861db06c97dfcc1`  
		Last Modified: Tue, 13 Feb 2024 08:57:46 GMT  
		Size: 5.5 MB (5547529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a47b72a6075e7943bbc21127105afa59bf1e32936ea374c52323b4c618b5123`  
		Last Modified: Tue, 13 Feb 2024 08:57:45 GMT  
		Size: 24.8 KB (24776 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; arm variant v5

```console
$ docker pull drupal@sha256:1b26b08841507b5f6610277e879d5a0778811955ada5f27de919c15fc3264264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144511742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e834403166d44536efa1d489840563bc16f0dcaab47d6c08634b238df2cdbe`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:1b6dd4809e22729ef9f0432014187762756f1518e85ecf13db6c505bfff65308 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:dfbf1dc0873e0cde30013d8526571f69d5c53be2b8d637a6235c623cc1f66192`  
		Last Modified: Wed, 31 Jan 2024 22:48:48 GMT  
		Size: 28.9 MB (28921333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1009ba391822779e1f869312d30401b4f3f6f5233d630d7033c877e3f0d936ff`  
		Last Modified: Thu, 01 Feb 2024 05:38:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e2fc5e2ef8b2f663258a78c132279ed058104e095dcd1b489f1fb1326fc59f`  
		Last Modified: Thu, 01 Feb 2024 05:38:31 GMT  
		Size: 73.7 MB (73689824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bc8c6067613483aa73338f4e3ce525675c82f7be34141acefc5135db6d7baf`  
		Last Modified: Thu, 01 Feb 2024 05:38:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffc60d47b794aa6f1b60f54abfab47329041c4f9c7144e4bbce2c57926e9ff3`  
		Last Modified: Thu, 01 Feb 2024 05:43:40 GMT  
		Size: 12.2 MB (12233215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692fc087c799b7b7fa02c6f9e338c3d3ed88a72e6fcfb3dd0d6dd4280652575b`  
		Last Modified: Thu, 01 Feb 2024 05:43:40 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03004ec74734b69fc3ae65b6056a645e0247d38e383f5bfd1d258ebee5f44fc0`  
		Last Modified: Thu, 01 Feb 2024 05:44:14 GMT  
		Size: 24.9 MB (24850535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc7f3ef42b08bfd5f56f9381d8bb83fb0cf504e71d00f1e3e4420cbaa0099ef`  
		Last Modified: Thu, 01 Feb 2024 05:44:10 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c073a615bad1f3f7dfdc93727f6ca259afc79fc5344a6a47d1e421b9d5b536`  
		Last Modified: Thu, 01 Feb 2024 05:44:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4683e2f24211e172c43636be2f06ea64ddd87ddd0ed4cc4b11ce7e4ca71b9f`  
		Last Modified: Thu, 01 Feb 2024 05:44:10 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01744484952a298d5e59860fb890be96e7aeb203749f0ab7cb6b8a855e128ddb`  
		Last Modified: Thu, 01 Feb 2024 19:11:24 GMT  
		Size: 1.4 MB (1385068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657d911ce1936b99ea87985dd3169bc7db882804795f7c1d3fba9875abf16343`  
		Last Modified: Thu, 01 Feb 2024 19:11:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469e6dfe80e6c598156830510745a5a0be3e80b121657b36e1b72c1269223634`  
		Last Modified: Thu, 01 Feb 2024 19:11:24 GMT  
		Size: 3.4 MB (3418880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a438dabf2433e2b751802ced22ab761489ae9d39b9ea379d94ce0db33099a53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693f9e2c3903fef7dd27d68f9caa49940df339e507da16db524a77843c499a90`

```dockerfile
```

-	Layers:
	-	`sha256:40ff5a14d80fdc9785d7e0376be1f8a60f4346abd3257e4b649beea7caf1cfed`  
		Last Modified: Thu, 01 Feb 2024 19:11:22 GMT  
		Size: 5.3 MB (5286260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1618896fa5445efeaf793c6e9d2eac1ff0d249fb15a56b852acce29baa4496ed`  
		Last Modified: Thu, 01 Feb 2024 19:11:21 GMT  
		Size: 24.9 KB (24873 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6b9c3b6c177f7baeb94e67c6156b883bef5aad2b2512de1d921d5f3acb15ddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136852721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6340c840f8766910ca0d27a5607f779b36e5975541162052a805f758ebea905`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:372dfad3ad12f60e2d197dd53e3324b5d72bb8991b0ab0c858498b2ab53eedc2`  
		Last Modified: Thu, 01 Feb 2024 04:32:45 GMT  
		Size: 12.2 MB (12233222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae289880a71c22d7adccbe32fa92e0456f72fd378cda7d926c3f2a8621c3a1e`  
		Last Modified: Thu, 01 Feb 2024 04:32:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761de80031876775ab5607d489384754ff19be3515e41c67f28d1dbb5f58fb08`  
		Last Modified: Thu, 01 Feb 2024 04:33:20 GMT  
		Size: 24.0 MB (24011516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100cd6ac3ad361d075378dce131f9cc43d0db1cd7d861fcbe314fbad8c8812bb`  
		Last Modified: Thu, 01 Feb 2024 04:33:15 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98604d78f83ed7a47877edfd5c120cca78b5df057188dec9322893d1e3c14e6e`  
		Last Modified: Thu, 01 Feb 2024 04:33:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02080573e6cf5ee101b77faa99a40cfb929586f8d83c1d104460e82434fcb38`  
		Last Modified: Thu, 01 Feb 2024 04:33:15 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb17a7f2641a1df54523f13f2afd4b20b79581f8f8db87061a9a4ddf475dafd2`  
		Last Modified: Fri, 02 Feb 2024 16:37:14 GMT  
		Size: 1.3 MB (1272996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713818ba80f1d3f2828de636583674a5ab3a918bbf7b3ce2616168ea6412ac29`  
		Last Modified: Fri, 02 Feb 2024 16:37:14 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367bcb8cfc1f91da2c7818a9299a6bb7cee9a42d8b0c37e7ad7408067b8234f9`  
		Last Modified: Fri, 02 Feb 2024 16:48:30 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f35564a6d64904ddd06cdda3b6ed62e27a53599acf790b4f3fd3dff107edc517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b8a3a651642db953c36080547771be3fde7bfa8c9b16e58760883f6d6ca148`

```dockerfile
```

-	Layers:
	-	`sha256:57e64b7af86f2fedf8104eeb8b93a3eba4b11fbbe58e0dbd5a0c4e4e8e4c3f92`  
		Last Modified: Fri, 02 Feb 2024 16:48:30 GMT  
		Size: 5.3 MB (5290136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c5fa32ecbfb3f93e8c47b128b642e757209c58f9c3d2f27cf4953ea76bc6fed`  
		Last Modified: Fri, 02 Feb 2024 16:48:30 GMT  
		Size: 23.2 KB (23248 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d0649db11434b56074ab08fa0110b34e6d728ccd7eb5d9742d5efb5af6d4608c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161139305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf4a366403bf14b8915895f462380b549ca13fbcf3568e8e1deed21f659333d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:d6986db676f00f6dcc6d510942fcedc16e8654d33746f3a2d4133e71f08479b7`  
		Last Modified: Tue, 13 Feb 2024 07:12:12 GMT  
		Size: 12.2 MB (12233071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cbc5c7c9d3ca3382b197b5c82dfbd67922895e956b1d388e24ac3c2742cddf`  
		Last Modified: Tue, 13 Feb 2024 07:12:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7afb1fa216832eb2d43fe34188f67a3c8f7057c1911d7636654a49c22ff9dd`  
		Last Modified: Tue, 13 Feb 2024 07:12:45 GMT  
		Size: 26.3 MB (26309818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b1c9d120fb5705545ec9eba57e26dce0b30ac525b32a08d7676b31a1d545c7`  
		Last Modified: Tue, 13 Feb 2024 07:12:41 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a747f51432668f14d51adbca47072fe2e28f1acf711083a39bdcbcddb681538`  
		Last Modified: Tue, 13 Feb 2024 07:12:41 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082f769ebdce487ad9d56790cee0d85698d8a4a199b66c17b0a82c45ce44b354`  
		Last Modified: Tue, 13 Feb 2024 07:12:41 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70230ccd713da8193cefc940ad65f6d30189c8a3f52bf1e02af6bb2297f815ba`  
		Last Modified: Tue, 13 Feb 2024 16:39:11 GMT  
		Size: 2.2 MB (2159429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8226146cf86b0acceb976ed60dbaf0de454296c4e2b1bd470ea3f434af7f077`  
		Last Modified: Tue, 13 Feb 2024 16:39:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae472ea069ec8a4ade493ff9ae111b2fff889c16b37392dda361f499d6e1e55`  
		Last Modified: Tue, 13 Feb 2024 16:53:08 GMT  
		Size: 3.4 MB (3418880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:1376f77b74c4e8251c99489c88cdb5f69054b29d9772905961b221c56d5be903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5573359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3a26d522d9399103d507fe58cd67284bdedbc9924b699ba7885ce34fb84752`

```dockerfile
```

-	Layers:
	-	`sha256:b9855dff9cc4c7e3bafcb5cc6d55ebd99b31be91e88009492578bf8cc12afd31`  
		Last Modified: Tue, 13 Feb 2024 16:53:09 GMT  
		Size: 5.6 MB (5550196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f067e9b13f8704700fc5e4d1fb0c06464984c025580f0c6e96bf96239106b31c`  
		Last Modified: Tue, 13 Feb 2024 16:53:08 GMT  
		Size: 23.2 KB (23163 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:2411ba64b7e4ef4fe1b3e97717b51612744fb0b2c62301f28ff22f2ab4d9da20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169509024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb0076886a9337f215e893f609476428e60e2eab8d4b1aba074b2a355b28f7a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:80af693dc0393862251b6a97260e97280f94b6b4adac616597d45c6edcbb1288`  
		Last Modified: Tue, 13 Feb 2024 09:22:54 GMT  
		Size: 12.2 MB (12233007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f2d88e4592059f2d7b33265d6f9336ceecf516f782513d68a4d1f16e3b351`  
		Last Modified: Tue, 13 Feb 2024 09:22:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb7b32f081705db168c0f01db515ed1b8e5736e247e6c13709b5d83f30389b7`  
		Last Modified: Tue, 13 Feb 2024 09:23:34 GMT  
		Size: 26.8 MB (26750395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab68b85e1694ad314ab357d4d24b325b8f6a1717300b85fa77f5d6f759a9c414`  
		Last Modified: Tue, 13 Feb 2024 09:23:27 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048a03a2d167858a7045f680f0aae87efb7cdb3659925403aadd7baa7b64ff5b`  
		Last Modified: Tue, 13 Feb 2024 09:23:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55042a6f15fc9e2da73b45387ede4dee745418ae4002afc42690897d2fb839a1`  
		Last Modified: Tue, 13 Feb 2024 09:23:27 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86210ebded9bb42e0badefd26993469acbe4164839186b088f80e7dfd9f3612`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 2.0 MB (1964826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5ec4263c36665b83c59008f2194622671c61967b594bff742c74aabb437f30`  
		Last Modified: Tue, 13 Feb 2024 09:58:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834f2cbba7ed8b474c7296b3fc48a18cc6fa5e1a6ccdb60bba468e4fe25b9b88`  
		Last Modified: Tue, 13 Feb 2024 09:58:18 GMT  
		Size: 3.4 MB (3418881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:6510d6cb8b04c480e75b72fbaffc6ce08edf131b5343759c4360e8d24fa40a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5563429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ebfc24310f76194d58caa11a53951cd1ead1f03f85df0c019290391c474b5`

```dockerfile
```

-	Layers:
	-	`sha256:53e3089638e9b715af41d02542d7ff4be8765cd5ac716e4163b66abea053743c`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 5.5 MB (5538685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b6ffc1699a9b7446bbd8f67aae674629bd5f52cc7dd3b6b9920e3d3481e7e76`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 24.7 KB (24744 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; mips64le

```console
$ docker pull drupal@sha256:c6ffd82322da049c94b8bfa96b3a538045e6b836a43fc0e70f9cc5ab5e1a8a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143655809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7babaee66028cd2a8ed4134648cb9b353edbeb7603bec4a8c2ae72eb89ba540c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:c74d2ef293040606b9450e82efd37b5ef0dc7ba25160e7762da18e804abd6338 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:231db420c5b3972aa42bcdfd7a71d4d6d22f911ebd5b7ed62d957cef65d0dddf`  
		Last Modified: Wed, 31 Jan 2024 22:39:47 GMT  
		Size: 29.6 MB (29636258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f955f0ffc39b95dac62b4e7d2492d80a82e545345bc0b9dc464a02392ea50f`  
		Last Modified: Thu, 01 Feb 2024 05:36:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5204a203c0471080d92c43833fd8c10bca0a6b82f9272947816b77c9b8f80e5`  
		Last Modified: Thu, 01 Feb 2024 05:37:38 GMT  
		Size: 71.8 MB (71815129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a387836f539547b6af5fea1a6863ef3cec958bda21fb184bf084bcceb23e4615`  
		Last Modified: Thu, 01 Feb 2024 05:36:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917ee72167166af8621a1b34bb277d24c5d29db0ea3081479fc88feff1f58c90`  
		Last Modified: Thu, 01 Feb 2024 05:46:14 GMT  
		Size: 12.0 MB (12016942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2a8f6b71c931923eb2efef2616dd05153cd1b0018e6b720964c88a22a63b8`  
		Last Modified: Thu, 01 Feb 2024 05:46:11 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8141d0e841634dc42c0ca707559a652d315561584295e7408bdc47c82ce7`  
		Last Modified: Thu, 01 Feb 2024 05:47:19 GMT  
		Size: 25.3 MB (25270825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d26dd0462ed3696c46da9788953f0b84fae69af52442119c5ae7b25c8022f0f`  
		Last Modified: Thu, 01 Feb 2024 05:47:04 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5413b9676e592d9ba98777b167e5fe5b9a8442643b1a17020c9eda84a466fa2`  
		Last Modified: Thu, 01 Feb 2024 05:47:04 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268fbfdaa9293b63e793280b3053c13959cb68e52cdad53f619985878eee60c2`  
		Last Modified: Thu, 01 Feb 2024 05:47:04 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4040dc74c9d554b14d683d9f69f5d6a1f9598fe64958bc4498b6d3305abe27`  
		Last Modified: Thu, 01 Feb 2024 19:22:04 GMT  
		Size: 1.5 MB (1484924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f87ca6d0fe50a11c8479e0713c3c8c3b6385855f5edf541830a76835a1d75f`  
		Last Modified: Thu, 01 Feb 2024 19:22:03 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8b8ac9a94ac6a5b5a1c0c606c924f86603eaa19392f505ae160acf0065f9d2`  
		Last Modified: Thu, 01 Feb 2024 19:22:04 GMT  
		Size: 3.4 MB (3418876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:af7ca946c986a7efe801e961f24aa176ebf2dfa264b13fe9cc78331a3e5fb684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 KB (24624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f390205537b74c8b63dbe4598e3dd9f4ea7f99ee717ecff68cfe2a34e35ef`

```dockerfile
```

-	Layers:
	-	`sha256:d541226b9b597d04d1f72aacb2146654bb72ed3c3482090ab5c1d04f47649eed`  
		Last Modified: Thu, 01 Feb 2024 19:22:02 GMT  
		Size: 24.6 KB (24624 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:f336a922e2982f613badf4de10759facfa248e83c3ff100e6a796682442b6011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166677133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de54f54577c01dfefdeb0ca48339feb923da786776203a0eca13841bd4cce765`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:8635fe76193b6fb08a048c96cc72557f01bab82a709d23a439a569ba446ced7b`  
		Last Modified: Tue, 13 Feb 2024 06:57:51 GMT  
		Size: 12.2 MB (12233825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cc028ad1ff4e9827e4d873fc96ffbb9c00b648541d2b08dbcc1697ccb9d471`  
		Last Modified: Tue, 13 Feb 2024 06:57:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31968c22cb665c27140e759326b88f5c200762ce652fe4f0750e99e2c717980`  
		Last Modified: Tue, 13 Feb 2024 06:58:28 GMT  
		Size: 27.3 MB (27300563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01f1b64e3b9278fe6f89085c4127e7b40e5905f67d2bd0a4b1c5c298448e27a`  
		Last Modified: Tue, 13 Feb 2024 06:58:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879ee5ab5c2471af736464fd1b5e5155886a2a5c55ac0294f84ff28edc1bdfc`  
		Last Modified: Tue, 13 Feb 2024 06:58:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c9bafe6639b54c47fa3bdfac4008f459864b707c439adc37592e1c1253265d`  
		Last Modified: Tue, 13 Feb 2024 06:58:24 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7a95993bf77bbc35107393ea531a7a76a768b44f410735126dbf0726f90e43`  
		Last Modified: Tue, 13 Feb 2024 14:53:01 GMT  
		Size: 1.8 MB (1760657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b566704f479e0dbbf0c8d5f654543ae66031191054a09a811a5ebb731c16b22d`  
		Last Modified: Tue, 13 Feb 2024 14:53:01 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e649d2312e6476552f19bf4f8ea73a988fc1fe210c9324573b9ff68d8584c5bc`  
		Last Modified: Tue, 13 Feb 2024 15:13:18 GMT  
		Size: 3.4 MB (3418878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:36263ece19863ab1a5b32eedbda983c94b524237649a8bd6f1caba80fd932140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11cfbaa2daec114a7bc36e033246d7f2aef0a3e0da7c9f2a9f615c9b431d79c`

```dockerfile
```

-	Layers:
	-	`sha256:d3daaf76684f0bd82311c90db28d0142451634af8d6755755e9c990fd0332b82`  
		Last Modified: Tue, 13 Feb 2024 15:13:17 GMT  
		Size: 5.5 MB (5519281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd90387293694e5499e584f98dfc4c23f96b38e2d28188aea5252cc178468ca`  
		Last Modified: Tue, 13 Feb 2024 15:13:17 GMT  
		Size: 23.2 KB (23195 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:db27ae998c91c43afb158bf4fd7219af70f68ea6867cef1e815a1a9f1c8a26a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143767180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df427cff39e786ffac92bcae0c2c599e0f2ec7be5c3c01a9483d18dd0a0817af`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 03 Jan 2024 18:58:56 GMT
ADD file:9a48c9d7fde8a2820cff9dc06434dc4dca8967438fa75bb93e6646cb44682b18 in / 
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 03 Jan 2024 18:58:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_VERSION=8.1.27
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 03 Jan 2024 18:58:56 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Jan 2024 18:58:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 03 Jan 2024 18:58:56 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 03 Jan 2024 18:58:56 GMT
RUN docker-php-ext-enable sodium
# Wed, 03 Jan 2024 18:58:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 03 Jan 2024 18:58:56 GMT
WORKDIR /var/www/html
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 03 Jan 2024 18:58:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Jan 2024 18:58:56 GMT
EXPOSE 9000
# Wed, 03 Jan 2024 18:58:56 GMT
CMD ["php-fpm"]
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_VERSION=7.99
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.99.tar.gz
# Wed, 03 Jan 2024 18:58:56 GMT
ENV DRUPAL_MD5=0fbcb06e354309356e6b4e33d2cd242d
# Wed, 03 Jan 2024 18:58:56 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:01ee533c6a2b660595f8ea73d954d38c5cad2906475d90d7befa08fcfa590ab9`  
		Last Modified: Thu, 01 Feb 2024 03:23:54 GMT  
		Size: 12.2 MB (12233706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7793006c1cd05fb3cf39b8d5d3798f02eddaf89064aebee044bf060e69e704`  
		Last Modified: Thu, 01 Feb 2024 03:23:53 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16494afe5b7b10a3c63593924322b33e4d0ddfb5a7fe86bf733264b7a622d924`  
		Last Modified: Thu, 01 Feb 2024 03:24:14 GMT  
		Size: 25.3 MB (25321525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b0574296b65022d26279c82d78df8be2751357d93963e3bfe9ea665260b28`  
		Last Modified: Thu, 01 Feb 2024 03:24:11 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d685ee0edee7535bfd8bb25f39c10f72326179d70c6bc4def3ae2cffc8e9138`  
		Last Modified: Thu, 01 Feb 2024 03:24:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4187fbb5549fa4ae7a18da7554e4358075711347fd92efee72749519f258c00c`  
		Last Modified: Thu, 01 Feb 2024 03:24:11 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db35a44dc7dba48cb2678953ae0ebede52cd2f9c7f020887ec40eeabff74da`  
		Last Modified: Fri, 02 Feb 2024 03:02:14 GMT  
		Size: 1.5 MB (1487598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7c1e18ca17b688167b99140b0441a85535f086787bdb700d4457e6c696b9bb`  
		Last Modified: Fri, 02 Feb 2024 03:02:14 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7facba65377291a7ae2023a141a792834b4ded152b6949685baf4f6cd16ce71f`  
		Last Modified: Fri, 02 Feb 2024 15:21:06 GMT  
		Size: 3.4 MB (3418875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:c7c9c6cdf95be61d5557f2c7d3a4bf1d448d18b4ec409eeaa598552b683772b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5db81b43632001929af044a324e64f0a8139b69937f3c0513c3608e2b7b4842`

```dockerfile
```

-	Layers:
	-	`sha256:d0ac68bb3dea88d9d7c707dfcfca87cf1fbb8c121fa8593c3f714bb996497e50`  
		Last Modified: Fri, 02 Feb 2024 15:21:06 GMT  
		Size: 5.3 MB (5307875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27b497993b37935fabc1380f6535e68d0071357443607189ee1e2ff76aa04aa`  
		Last Modified: Fri, 02 Feb 2024 15:21:06 GMT  
		Size: 23.2 KB (23153 bytes)  
		MIME: application/vnd.in-toto+json
