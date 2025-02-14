## `matomo:5-apache`

```console
$ docker pull matomo@sha256:e1653d9b3784e622c340e70713f7a279e392efc1ffb6f7d7e6d71f66296af9cf
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

### `matomo:5-apache` - linux; amd64

```console
$ docker pull matomo@sha256:6b113d546c33ab5b0e84f3110821d759633677e6d0dfa4580e83807699fda4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202198508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956fb9437472795417b592b9607f0478aa684a15ea2661e77b835095debd7017`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a75c3e6a3090db961f187e726d4f8d9470d109873ea82676d20418337fa99`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fb56484a65ab530ed3a13c37c0d4490e5b20d60544117d1355bc924ca741f0`  
		Last Modified: Fri, 14 Feb 2025 05:08:29 GMT  
		Size: 104.3 MB (104345484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a8c28e2a6462b881346f671a6a138b8939b522b6a59f1df9dc3b47a373d513`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4b52ba138f07eb5a43b4e999ad5d9732f80424c1146edfe4506f9d400dc234`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2801a0b661a741cda5801c08a9760b5e2b6b8ff90aeea85213a9aa76beb55f7`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abaaa7aab0e297aa578b9ffc188ad34b99d5f908a418db4a09c0fcaab0e102f`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624140c5bee349372ea34fcb86cab39f68ec4c3c923bc58c70374b7ef5dc9b8`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 12.7 MB (12669743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5250a5fbf9003989ed0004e7b3806c9c589b17fb8b9ff5272292e0eea114218d`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0765d0c88fa1531a15a2fe8c98660619acdc1d236f7c94ceeeb2c25c31ab5d1`  
		Last Modified: Fri, 14 Feb 2025 05:08:25 GMT  
		Size: 11.7 MB (11653066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872b33dacafd826ad0d6eb2e2b26976f2bdb354884cdaa6c2e93a7371101c67`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bca8216293d7220363a34e35012c4b87555e8f4fed4d41ca0399c210db629`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54cdbe7b63b97c4f159133a93e51d5eb96a937eef274224cf47f3ab474c4590`  
		Last Modified: Fri, 14 Feb 2025 05:08:24 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af55c362c3d608f2f3612e7fd95bc2e8097920be6ce3b7ce790c2ddc1114ba20`  
		Last Modified: Fri, 14 Feb 2025 07:11:55 GMT  
		Size: 3.3 MB (3280238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4028b9d8518b47f7a88885006d45fece3c63314bf618a9359a7a117fee1dffca`  
		Last Modified: Fri, 14 Feb 2025 07:11:55 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2860bfa00f45e6f7cd112aada96a00e85e44a5cc76d1513eb8dc2cea830598fb`  
		Last Modified: Fri, 14 Feb 2025 07:11:57 GMT  
		Size: 21.9 MB (21906956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a62efab858d4a5500ee2e04f58d96c26f19dbe466b6e706f2bba1e1ae0cfdf0`  
		Last Modified: Fri, 14 Feb 2025 06:11:56 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536203337102b6afcc60568475eb12afea17382ec482489c6a0b5fc4e6c26ad6`  
		Last Modified: Fri, 14 Feb 2025 06:11:59 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:977fc4eea1d920d3f81e893a0f6bfbe14ec28d6792e733b513157b5a88f2b5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49530f548884169f227ba8bc6da6683a223854121468e0bc4e62e829dddeba11`

```dockerfile
```

-	Layers:
	-	`sha256:e68d24f57d66c19388a2c1859475827cb87195ba73059458e8c190920605bf69`  
		Last Modified: Fri, 14 Feb 2025 07:11:33 GMT  
		Size: 36.4 KB (36373 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm variant v5

```console
$ docker pull matomo@sha256:09fe02383489da1e66e2b822845a725351997ac4bb49fca4fbeb1cf5fb17b14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175100797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab95dcb23134f90c00407cf0b4400c9a9ea3c3d891c68cad31b9d1b2ed6dea1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972786f04f039fb3a4d1b82c728a7c7ea9ffc0e85efd517dc45b571b1f62752d`  
		Last Modified: Tue, 04 Feb 2025 09:33:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e43da89859192986d7ea9c98d997ffc5a0763c751bc8a114b8ac40e7013eb3`  
		Last Modified: Tue, 04 Feb 2025 09:33:31 GMT  
		Size: 82.0 MB (81993010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d164497324e1f248e21428931b6af1422a36e02ee93ec9321130fe7aef51ee`  
		Last Modified: Tue, 04 Feb 2025 09:03:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257cd43f7d4316ca1918591e64f7902f4d9229571ee075507c13db3784dc6ab8`  
		Last Modified: Tue, 04 Feb 2025 09:33:28 GMT  
		Size: 19.4 MB (19418914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c1e816e9bcdb84e76e57033177a7423be099d5d2c40dbc6cbec675fe88b9a3`  
		Last Modified: Tue, 04 Feb 2025 09:33:27 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f10c342a754c0ad57e72a24702b3dd7bca22d09f36e99ed67b18cef29826ed`  
		Last Modified: Tue, 04 Feb 2025 09:33:27 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332757d4175f7bcaf5bb2469db1d735d62e4b3328e6a7fd63514052aca12d509`  
		Last Modified: Fri, 14 Feb 2025 05:13:58 GMT  
		Size: 12.7 MB (12667999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4269d3697efd5ee5f39b4e6f22aeeb53182c72e7aafbacb8a0ddb4c9f8b23af0`  
		Last Modified: Fri, 14 Feb 2025 04:11:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf5b6168b56ad8fdbc9e416038b944fd4944df34d45269f40d6e88fea955719`  
		Last Modified: Fri, 14 Feb 2025 05:13:58 GMT  
		Size: 10.6 MB (10625223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704e8842a004dfa605739341c6e94722c575536ab2fd377c7138c0c03b8aa644`  
		Last Modified: Fri, 14 Feb 2025 04:11:40 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f043b63b64d00b800a1b974dccfdc0416ab66c11b12fc8e18dad173911d5f289`  
		Last Modified: Fri, 14 Feb 2025 05:13:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f532b7eb89883df0c59a7ceaa130e8df02bb1ad8530d4e629e4cee7fe4919fdb`  
		Last Modified: Fri, 14 Feb 2025 04:11:43 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f1317e7c03ab77cd1cb11bce875b55ebedd5196ef9a729ba4290a7ed709d57`  
		Last Modified: Fri, 14 Feb 2025 07:11:55 GMT  
		Size: 2.7 MB (2746902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b884a72a3b3e86ec1a7eac737a03a4e1af035503683bafd832ada83345b25181`  
		Last Modified: Fri, 14 Feb 2025 07:11:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c1d80110c74f6f06eb8e97ebc18f46842ae8e1f0d283b82f299c919c90ea5`  
		Last Modified: Fri, 14 Feb 2025 07:11:56 GMT  
		Size: 21.9 MB (21905237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0b2a702e7a9e94634590e0f404679832e60305ace1f2116d0e6a8574f08f2c`  
		Last Modified: Fri, 14 Feb 2025 05:08:44 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5615b0859456930c853ce7cf88a93adab2339c31df735e7393afe975de841615`  
		Last Modified: Wed, 05 Feb 2025 12:45:38 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:ad9fb4c589ea2e44a3c733b021a8ce6e28ae38afd0713ac761a8b30758e44468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab333f9fdae0e84f308780feefd990db717fe90356a2957b70b15b42a266c89`

```dockerfile
```

-	Layers:
	-	`sha256:ebdc26b8c19d1ff40fd368ff5680321f43dc8a2683f05c4efd4aa9703b656d0b`  
		Last Modified: Fri, 14 Feb 2025 07:11:34 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm variant v7

```console
$ docker pull matomo@sha256:88d311b1306b47c9ad6ed04b0e5a75e50832afd9b9fbff282876321b55c73d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166183970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a64e1d75cf70d3bb325f24dd5f54b097a3ab7bf4181dd81f5a25573d8d269c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf3121bf0a9ad47be9cd9230d76c59964a3c5c2ad428f1f2d5e0ea10c439534`  
		Last Modified: Tue, 04 Feb 2025 16:46:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4e514983dd1fb84c6ee305b52a5a3c4aa50f60f471002066ed6c1fc22642b`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 76.2 MB (76162605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2400437b25b5d1b02d62a06166a2fb642e727da4868737aedeb7e86797c34448`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db855c0ccbd5449d40ab70032bf7b56fb3cfea2bade47fc7c1bda6c7772901`  
		Last Modified: Tue, 04 Feb 2025 09:33:29 GMT  
		Size: 18.9 MB (18857283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe7af15f7e5d8a84ddc0ee0c05a5748052ebb16cdf52e6db919f2bc9e48d4d0`  
		Last Modified: Tue, 04 Feb 2025 09:17:04 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb55ddf2b979059029229318166cb34829e074c9b4af0504b65ac6066e9e0fc`  
		Last Modified: Tue, 04 Feb 2025 09:33:28 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0061a65af18d1f444ddce2a9c5adcda383e392b43f907d4f1cfccbdd86eb7b`  
		Last Modified: Fri, 14 Feb 2025 08:30:10 GMT  
		Size: 12.7 MB (12667938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2ddeea63a4ce930814517c148050885a1dcc675b49b9a0cb215c1a5071d783`  
		Last Modified: Fri, 14 Feb 2025 08:30:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cf17c9822fbc25061c1bedf52d2fe828e813acc20b155300c96059e2c8cdcb`  
		Last Modified: Fri, 14 Feb 2025 08:30:09 GMT  
		Size: 10.0 MB (10044324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103242c028fb3f94e70f6aad3a8acb02c3609e9f161c59a0d3fac14a123b22`  
		Last Modified: Fri, 14 Feb 2025 08:30:09 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d287db14ec7ae0af84306be48a164ec40227a26eb34dc1c91b7bb34998758007`  
		Last Modified: Fri, 14 Feb 2025 08:30:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a2185f46b047a9c314d2de357f5c8fc7686a6e3f1debb4f977571569477d91`  
		Last Modified: Fri, 14 Feb 2025 08:30:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdab8c94b0b58184caf35768333a62b1bfc5d6acda78f537f5649636028be3b`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 2.6 MB (2625130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948267fd8305da7c7c8d5b3238c836e6b06fd9b98e922e54b505985dd2f37a33`  
		Last Modified: Fri, 14 Feb 2025 10:11:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f440e4f1131f6bb2226f439099c91c67d629f82e7e141a003b33c92118e2fa4`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 21.9 MB (21905194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db8d339dfc76321eebd4c97d4e18bcebdc53d5af79468c4de071d499d0b46c5`  
		Last Modified: Fri, 14 Feb 2025 10:11:56 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297df1aba83ed69204ffa156cda8987ec10fb100ef32da65d1fa3b1af067f7d`  
		Last Modified: Fri, 14 Feb 2025 10:11:56 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:de566b8e4b7c827890dd887e3f0b20ad18b43ebd2b9fec24fe2e14eb29fa0406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791878932e53394ef36b15f0c3d7b8288545d55ce2fcac12ecc83b76899622a1`

```dockerfile
```

-	Layers:
	-	`sha256:aead8259b6e97dc9a426e1ac74f21b157191b423d4fab5759e4ebc866a1d9683`  
		Last Modified: Fri, 14 Feb 2025 10:11:38 GMT  
		Size: 36.5 KB (36501 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:d910230b9f0379dfa21700e0a3e7e7dc0f0a0356a2aab0c3e25922a5ea6973ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196055872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3b0db05f15d00fc90acc9cb9d5621788aacf8347c467d057f2fb7be3165695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16d737fb0a30c662d9b2adf51f2dff7d89c28971aed9f2463503588644f91d`  
		Last Modified: Tue, 04 Feb 2025 09:01:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8571b79e8caaac6ec73bed43c061c8744cd39e18a67d9cd17dd79b0d6ea2e1`  
		Last Modified: Tue, 04 Feb 2025 08:59:42 GMT  
		Size: 98.1 MB (98130343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f74dc117b0b71ab00cf12fe8d534cbeab80ebf367380080264b1ddede90d92`  
		Last Modified: Tue, 04 Feb 2025 08:49:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349801e0b439bb7399adf1a3bad741322f9e25c3d7095d77525bb3d33598bde0`  
		Last Modified: Tue, 04 Feb 2025 09:11:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfb56ebf305e8086f08b1a2decda71f875642031182c450dfa65bc15d26a02e`  
		Last Modified: Tue, 04 Feb 2025 09:19:04 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6d105874122db2dfaacc1f9637c71272786724301db52dff0c0738d2155a94`  
		Last Modified: Tue, 04 Feb 2025 09:09:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21196ec8e1c1dfd80024f57b05b04a0eaf34e114f8127bd370edc9a9aa9dd22b`  
		Last Modified: Fri, 14 Feb 2025 05:13:56 GMT  
		Size: 12.7 MB (12669564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1bcbcbb81b84139eeae4d92fd2035ea91bbb53ae2efe44ff97031cfb95d5db`  
		Last Modified: Fri, 14 Feb 2025 05:13:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a63caf847a0fabb747e47c1443cba52008580717256dbf524c7ffa4a55806`  
		Last Modified: Fri, 14 Feb 2025 05:13:56 GMT  
		Size: 11.6 MB (11649823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038e8a356a7a2cea4755c5b51fa8347428771002844d198bfdbee26c69bb645f`  
		Last Modified: Fri, 14 Feb 2025 05:13:07 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26402d45dda19b9f8fd7e95944a4978aaa74d560a4427455777573caf52c6979`  
		Last Modified: Fri, 14 Feb 2025 05:13:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca75595b7a8267cee7228887aafbe6541d7d12a2ba80e86936f3d58baa134c`  
		Last Modified: Fri, 14 Feb 2025 05:13:14 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b066faf1f468ad243181865a069fe807814760d1a2c727d11bb10154cce103`  
		Last Modified: Fri, 14 Feb 2025 07:11:55 GMT  
		Size: 3.5 MB (3530453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618da4431d9d25e594b603a2273acf065b081c6634e1558f3fde31dde3c5ae4b`  
		Last Modified: Fri, 14 Feb 2025 07:11:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c630360a63d2c118376d0dc28f8780002162bd0c61a3d20accba91e372c7609d`  
		Last Modified: Fri, 14 Feb 2025 07:11:56 GMT  
		Size: 21.9 MB (21906917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d123ec407d87c5eb454130eabf35e3ec65e31e4f238f448586b85622a459fc00`  
		Last Modified: Fri, 14 Feb 2025 05:13:28 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd037fdf9d5302ef292b7748acfddceb6aae59781c1f3890e574ba0394c024`  
		Last Modified: Fri, 14 Feb 2025 05:13:30 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:b703df1e07a32b6e0b50b5d137067c49adb19b135aebee349a102cb29844dcac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2945f8c5cfc9e2628a78b3948429f867b2060c2e0c29c1f7a7e329ad3474ae`

```dockerfile
```

-	Layers:
	-	`sha256:1037d84450966e65368781690322e3cfedd06d490b893e396f584803c087dc93`  
		Last Modified: Fri, 14 Feb 2025 07:11:37 GMT  
		Size: 36.5 KB (36549 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; 386

```console
$ docker pull matomo@sha256:900f17b7dd3dfe1ce83e3ad08e610ed7412f310694ed7b2d382e256121b33281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201029678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ec4a28ede59cbb540128811352d7e20c60fd0c7b9674897a381b965f08f622`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b613625d23792fb714ed0ea23144c0605d29b6fed360bb76e054fde26d8c3866`  
		Last Modified: Fri, 14 Feb 2025 05:08:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35610fb0fd5a6dcd1f7abbd6b925a39db37b185b165d2056a200f62c9d1d04`  
		Last Modified: Fri, 14 Feb 2025 05:08:42 GMT  
		Size: 101.5 MB (101513729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc9694c3bcfa66783af0c675abac303483f3e7ec83ee53e26f67929675bbcc`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f370c1b3f7740375abdfeea774005f34789be5d0e9a375b1518bfd8afbbdc990`  
		Last Modified: Fri, 14 Feb 2025 05:08:36 GMT  
		Size: 20.6 MB (20638450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd4d0c6093b741980cfa89de6ed93898cf1a6303df104fcde6a387c0bc8c3d6`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be28fade995e8ec99823d90011a18c578f524f1027dcd5c73c855d449928c15`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506ecd4a857258c7c70be8d97489c05eef37a09f6a3b4d0803a419d83f1993ee`  
		Last Modified: Fri, 14 Feb 2025 05:08:35 GMT  
		Size: 12.7 MB (12668927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf4c835ba433a1d172b9ba07f43f966f0eb05ee10284f09cfd882368bd2c8ca`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d185d7363802500e0336fe058a83b8c6a8c64c0334680507fc5fdfca9d140a74`  
		Last Modified: Fri, 14 Feb 2025 05:08:35 GMT  
		Size: 11.9 MB (11875658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68ed86d82217e240f5f70b173ae60912abaadd9bac6084fde125962c4b19781`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a33b761c64605c9d26198d448ac81df7b83abc67800d7fd4b8e6f259548f4e`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170694b4d37420e4e388ce3b55e04465a055748c58ae0a4730a838a63f435a5f`  
		Last Modified: Fri, 14 Feb 2025 05:08:34 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ccfc5a8ac83059da432a5b73dea4b9f047467c67bbabfe2b8133d7a04898b2`  
		Last Modified: Fri, 14 Feb 2025 10:11:55 GMT  
		Size: 3.2 MB (3232490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e398f3a45e4b3d9853173e693c0e9eb4297b014feaf6b05c816d5fcbb0788ac0`  
		Last Modified: Fri, 14 Feb 2025 10:11:55 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce2e3f1938b0c524a005258e6ff94018155f2e885c3b8fbed3d35b37e1b11`  
		Last Modified: Fri, 14 Feb 2025 10:12:12 GMT  
		Size: 21.9 MB (21906002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09859d89419f5f89685cf302caf13ab46a46ba7e57a337fcc4d28b92ccb6652b`  
		Last Modified: Fri, 14 Feb 2025 08:23:37 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3561933e9b7812a5cc16129816d9839fa05ecff9f8101a02908fac6fea66119`  
		Last Modified: Fri, 14 Feb 2025 08:23:39 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:3e57127ecfdb4822ee43822bd2394965fbbc262354cb2cccd3f097cc3abb41f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 KB (36316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4786a785319c694fd5e0a0c04cefd1f4e229c056dc227c8cc8402548079ab34f`

```dockerfile
```

-	Layers:
	-	`sha256:8d6e1706dc1f8b8e433375c15e3936f6c1a1c14b5677fecf8523a665218a0d75`  
		Last Modified: Fri, 14 Feb 2025 10:11:40 GMT  
		Size: 36.3 KB (36316 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; mips64le

```console
$ docker pull matomo@sha256:70e36ce7c9102ca123eb2b9c44a77960283fa705f89532ee92e6a4057b59faec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177380245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf8428bc4b17e6b2d0c7da6561ad9c914d255f0ec096c371a9dac3b8b32d2fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d943b67c93634afa3f4f4b4aa79cd45b624e4044db2d2aacb4f3924c131b94`  
		Last Modified: Tue, 04 Feb 2025 13:54:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56cad68a9722aed1b3c8b4084c18b366b958254fc3e910b0ed406bed05712c5`  
		Last Modified: Tue, 04 Feb 2025 12:11:30 GMT  
		Size: 80.7 MB (80668958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b77cb490565570ef702dfd920d31b7ad1786c141054119dec7b27a69d8cc18c`  
		Last Modified: Tue, 04 Feb 2025 13:54:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84413b34c68fe3b282fbae3ebd4f342aa18ab46de0ff4c3995d32d03c57291b2`  
		Last Modified: Tue, 04 Feb 2025 16:46:55 GMT  
		Size: 20.1 MB (20069138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb821b25bb0ef132901400586297224999cce50382f6a082c8f1f3a38b1a46`  
		Last Modified: Tue, 04 Feb 2025 16:01:13 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ac42e4ec5813093cea6442ac9aa2c8879e8039cde264330a3d5b4d6aed29b`  
		Last Modified: Wed, 05 Feb 2025 01:02:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6b3dc28a2ff1bbb2d54a004139ad4c1b856e95edc93c94b43cf8346640e2e`  
		Last Modified: Fri, 14 Feb 2025 08:13:44 GMT  
		Size: 12.7 MB (12667626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd17be52a3d54204d58cc568e1c3db3e1fd4824da6d7735c3557a7c31ccdfe6`  
		Last Modified: Fri, 14 Feb 2025 08:13:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0422aeb8a346c7eb02d565de3f8e155992d5cab70192703d079e855c706dfa58`  
		Last Modified: Fri, 14 Feb 2025 08:13:44 GMT  
		Size: 10.7 MB (10723093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8944e5fc176afc1acbe58a82f697e89c129438de6e0d98bdc929eac6a0b918b8`  
		Last Modified: Fri, 14 Feb 2025 08:13:44 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377ea43334854f1a5a63dcc5f47c6094fcd631e7e382b3499fa74613800e85e0`  
		Last Modified: Fri, 14 Feb 2025 08:13:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38127f2f3b53b483c07c5b381e9e9c9979ad0dfc7c0138e8308de09eb424779c`  
		Last Modified: Fri, 14 Feb 2025 08:13:44 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60bf93707d6e30749bd9b9902ddfa773b80db8d5530596ec8f399b02918c17c`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 2.9 MB (2852858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3059f80ec00281ca9dcb4796d855a3b3ca3bfb4b8ccc4d3efeb9f1446be04c`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e9d6039f589124c6663c754748fe456ab1805a8eeb639f1522ee2f9be3ec39`  
		Last Modified: Fri, 14 Feb 2025 10:11:59 GMT  
		Size: 21.9 MB (21905000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4bcb702ccf60a2f54a0a14241184e6879c89b49248de8f0ccb1d7d598fc1d3`  
		Last Modified: Fri, 14 Feb 2025 09:27:08 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d60b890c3ec9cc10c0f3ec7717155329fbc5f6b7606025683be62a5905af94`  
		Last Modified: Fri, 14 Feb 2025 09:27:11 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:c5ec66794d160affbcc1ab0a385b7a62e63f8c5a365549d771f90d49ed4c198a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977036a93eeb234a5c30c5c08f4d5b06ce00d5940dcf262542e755fc189cb177`

```dockerfile
```

-	Layers:
	-	`sha256:5739c2e4d7480d715d2d6c5653dac888a60a2a2e7eff7f3faebadd819b482911`  
		Last Modified: Fri, 14 Feb 2025 10:11:42 GMT  
		Size: 36.5 KB (36473 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; ppc64le

```console
$ docker pull matomo@sha256:96f8a870cfdd9207bff022a6bf774fc25087c3c05140497a4242a0e39d9115e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206518608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c3b5d08600d6687d1fc6a036af3d441f638f967f3a6f6590d0f524409f9c1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa84e2e7c890e21e6e4725b61a89702b8e63762c9a3ff81b49aa9d99b48ac4b`  
		Last Modified: Tue, 04 Feb 2025 09:33:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcd99fcd86991b417fb95ad64060b06785ff7f6352ce24df8d275dbdd6a315`  
		Last Modified: Tue, 04 Feb 2025 09:24:12 GMT  
		Size: 103.3 MB (103324008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ca1e7b60d264395b41c4a4787105a41c87e2bd5e9d67895db262fad4873dd`  
		Last Modified: Tue, 04 Feb 2025 23:02:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5218c0aca3f23dfaf27a513c2d06daa612d2386294a53d81f7ddbaba9d45ee`  
		Last Modified: Tue, 04 Feb 2025 09:33:32 GMT  
		Size: 21.3 MB (21308399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e7b8f37e12d934578444c6271234e36e9309afc271390ee87415e245ca5b87`  
		Last Modified: Tue, 04 Feb 2025 09:33:30 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca689848e7e5a26455cede87aec423ec507686f316f5ae1d8789563c816b887a`  
		Last Modified: Tue, 04 Feb 2025 23:02:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5d967f821ca1fb79746ae807f48942031ff2d439b9b9f9df26ed06c154b2f0`  
		Last Modified: Fri, 14 Feb 2025 05:44:43 GMT  
		Size: 12.7 MB (12669396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49214599fe5e44263b4f29eec79a048aec632a3a0c9ec9306cef90705e2c318e`  
		Last Modified: Fri, 14 Feb 2025 04:35:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70af670052714511036edba6a195ad4ac53e19472f619cf8af458c6a6055154e`  
		Last Modified: Fri, 14 Feb 2025 05:44:44 GMT  
		Size: 12.1 MB (12069363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcd0d7e9b95be4af021d09c6b8fe1941e9a9343a7257ecc5c313f88e67cacde`  
		Last Modified: Fri, 14 Feb 2025 04:35:38 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b08c890f85c486e806f894555738bb2681c8b2e582158fa9b947ff69ef6baeb`  
		Last Modified: Fri, 14 Feb 2025 05:44:44 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85e02e440d877c5e9601bfa96781c8574bff6ee1c23a7cbd6e4f18005b6768`  
		Last Modified: Fri, 14 Feb 2025 04:35:43 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf04d0571a98f276c1a546fee4a3ea12887621caaf886db57c2dae49ccdebec8`  
		Last Modified: Fri, 14 Feb 2025 07:11:52 GMT  
		Size: 3.2 MB (3188837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7dff8463f87b08778e59c59e22359ce4187530f8f6ea5b22a0da5da1d48597`  
		Last Modified: Fri, 14 Feb 2025 07:11:52 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f689197fc899898f3d80b39d3a79672a9c57056457b5adecc0ab82c1199771`  
		Last Modified: Fri, 14 Feb 2025 07:11:53 GMT  
		Size: 21.9 MB (21906856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79df02da7b93311294fd7a6e799032b81d71c62b2405b6db8bcb5d45914ad462`  
		Last Modified: Fri, 14 Feb 2025 05:10:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e24bbd12d67dc6265e646b88fc91cfcccaf43628259a611a5e1122b099f3df2`  
		Last Modified: Fri, 14 Feb 2025 05:10:10 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:8652a48865e5181fe855932b7b3db5ebe98bbbbfdd2249365503616ee9c31046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dda8a9e868ea32a0393cf91dd53a1300c597388d8105be795cf1874b64ec319`

```dockerfile
```

-	Layers:
	-	`sha256:abb8b34f6d6109e3dfb51240031da79575a37e0bc255feada3af7ff676e238c5`  
		Last Modified: Fri, 14 Feb 2025 07:11:40 GMT  
		Size: 36.4 KB (36445 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; s390x

```console
$ docker pull matomo@sha256:94f56fe863d310ef691c9a7ceb3c06939fced3b969c949579004f47aecf54639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175851119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b583d296f6613f6bfcc050a70e58a769609a0260435e9ccf451530b9a969d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 24 Jan 2025 15:44:16 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 24 Jan 2025 15:44:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Jan 2025 15:44:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_VERSION=8.3.17
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2025 15:44:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2025 15:44:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2025 15:44:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2025 15:44:16 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.24; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
ENV MATOMO_VERSION=5.2.2
# Fri, 24 Jan 2025 15:44:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 24 Jan 2025 15:44:16 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2025 15:44:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2025 15:44:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 12:11:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 09:33:36 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 16:01:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8253988c6a24fa76feaf6e34729bf23e9a788e7438b3da6a7db669f072c5ab9e`  
		Last Modified: Tue, 04 Feb 2025 11:21:40 GMT  
		Size: 19.9 MB (19895180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82684711048482eb8cc4b2f6548b4d6e7ece37d508c1ea3a12ab8f229f29fda`  
		Last Modified: Wed, 05 Feb 2025 00:01:56 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5cab685c9f3203c43aafec691ac532f2bd71706ad37119783a03535a44ba2a`  
		Last Modified: Tue, 04 Feb 2025 23:09:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f122e6df6f4a530391eafe96fd22f7a827680552569d20e74ceb44bb2feaaaf`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 12.7 MB (12668348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd33a4b2e38cc678b5373957e39c88c2ba6c28a5708a0b6e3ecd411f4cda46f`  
		Last Modified: Fri, 14 Feb 2025 09:10:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955870271e205902dd486313c7108103c880114c5080faba66a02d18c6c05fb6`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 10.9 MB (10874900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228daba1b2e4e648f074319bfe954f10e9e4ed702532264242c0265083326238`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450024d85b97e8263ff6f299351829d0b323d899830479d49ccd9e4038ec8888`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802c5dddb1c07139cf78fb9933e64dd90748f2c3e7c3e8071d393dc1136eb025`  
		Last Modified: Fri, 14 Feb 2025 09:10:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0bbc68a7153f37bf5951a669326ca06d9517bad432fb8e0cee8094f9c2852d`  
		Last Modified: Fri, 14 Feb 2025 10:11:58 GMT  
		Size: 2.8 MB (2824116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027d943a1d38fac326b228488b6356ee3af79cd7901c66266216a8c312eddc17`  
		Last Modified: Fri, 14 Feb 2025 10:11:57 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a0e739156171bb5c610b1946fed34990920a5d002e47c769ff129fd47f9e65`  
		Last Modified: Fri, 14 Feb 2025 10:11:59 GMT  
		Size: 21.9 MB (21905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7f0fbd7af4d97513aa9d9047a4b41821dd6d948b5a7a56c1dc3d501aa8e83`  
		Last Modified: Fri, 14 Feb 2025 10:06:55 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa3c81e5278643800c0e3dafdf8fafa649647bd14c009752f0d4e8b1970aaf7`  
		Last Modified: Fri, 14 Feb 2025 10:06:58 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:38b17012bb40393666540e714d9a868a1fca81c2b84a5a0356ed43dbce43e4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270092375db32b9a18ab6d7c504d280424f5f8771545ecb2c5e03271856f8566`

```dockerfile
```

-	Layers:
	-	`sha256:6c64248bd435bcdf874dde413f7149679b966240bc5dd1fca0f1ac0377ed5f39`  
		Last Modified: Fri, 14 Feb 2025 10:11:44 GMT  
		Size: 36.4 KB (36367 bytes)  
		MIME: application/vnd.in-toto+json
