## `php:8-apache`

```console
$ docker pull php@sha256:28a04938a75615cc467f3d399da7aff2f41cb00036729965213c18d095c6a263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `php:8-apache` - linux; amd64

```console
$ docker pull php@sha256:3dd4df7bdf81a042b2f93bf582c7a98f54fd14b7ab7976e3d6e7fef03af73a8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178285270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81fa90a219bb438902a17551a9792a89df865822cafb54ed4228c1c7791723a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:39:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 08:39:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 08:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:40:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 08:40:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 08:44:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 08:44:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 08:44:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 08:44:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 08:44:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 08:44:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 08:44:16 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 08:44:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 08:44:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 08:48:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 08:48:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 08:48:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 08:48:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 08:48:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 08:48:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 08:48:12 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 08:48:12 GMT
EXPOSE 80
# Wed, 24 Apr 2024 08:48:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93478d4793284c7a75389488e31ab45acb8ea56f8ba474bdb2359ecd2132177`  
		Last Modified: Wed, 24 Apr 2024 10:13:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74cc574d0d2183a964ea5880bba6308b7653c4cc7ff2010beb2c1b157168a3a`  
		Last Modified: Wed, 24 Apr 2024 10:13:18 GMT  
		Size: 104.4 MB (104357707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4782e138a9004836453694f515681a93d6635ab26f05b7f2dfea2baa4b761ad`  
		Last Modified: Wed, 24 Apr 2024 10:13:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeec87621aeb5b3bf8907398acc95a5e9b85a5f3faa6a68e0640e7d6653f850`  
		Last Modified: Wed, 24 Apr 2024 10:13:58 GMT  
		Size: 20.3 MB (20329716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1badcd002c0a773002eaf87724b5a303e17873ae752e7e69dfd6b22c05a7dea`  
		Last Modified: Wed, 24 Apr 2024 10:13:56 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d463a60cb62b1b64dd43c0defef018c6ab557e474c029d17824cc9d1b5d103`  
		Last Modified: Wed, 24 Apr 2024 10:13:55 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67111b81cd89e953ca7b5245bcb84dd84a2c95af821df4570f11fab5939944d`  
		Last Modified: Wed, 24 Apr 2024 10:13:57 GMT  
		Size: 12.8 MB (12802951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9417e7281935470b713cf578e094647d9f4659c83a06ee52fd631b13b6a6b3c`  
		Last Modified: Wed, 24 Apr 2024 10:13:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8774e168fe725ef99886559e9a6d4d4f1201e35f3aebcc84433420102e76e042`  
		Last Modified: Wed, 24 Apr 2024 10:13:56 GMT  
		Size: 11.6 MB (11638835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d72544eef596fc0092f7af9332838fe5a44fb40e3d5193fada9b890ef5ee892`  
		Last Modified: Wed, 24 Apr 2024 10:13:54 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a6ff90fc8497150b23cce092a0b945e9d7223275f3fc966eff0dca4f0522be`  
		Last Modified: Wed, 24 Apr 2024 10:13:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c1f8c453b586f24f90c4269520b81d40804dfaf0cbb7eeedd88b74fd92f00a`  
		Last Modified: Wed, 24 Apr 2024 10:13:54 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; arm variant v5

```console
$ docker pull php@sha256:29e41a9ff3430106f4cf5ea9a6c9562f9fa8e14cfd372e9d757a016bc9cd5b97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151937716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b6a4bb4e8dc355a0f7eec582235c7582934679031ed4f3f786b75e818659c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:28:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:28:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:28:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:28:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:28:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:32:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:32:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:33:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:33:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:33:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:33:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:33:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:33:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:33:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 10 May 2024 20:52:01 GMT
ENV PHP_VERSION=8.3.7
# Fri, 10 May 2024 20:52:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Fri, 10 May 2024 20:52:02 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Fri, 10 May 2024 20:52:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 May 2024 20:52:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 May 2024 20:55:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 May 2024 20:55:47 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 May 2024 20:55:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 May 2024 20:55:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 May 2024 20:55:48 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 May 2024 20:55:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 May 2024 20:55:48 GMT
WORKDIR /var/www/html
# Fri, 10 May 2024 20:55:48 GMT
EXPOSE 80
# Fri, 10 May 2024 20:55:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51615e4309fe3f4243f2ebef6416ed0e259fcf7a77c1f51cddf26fd9000fe2de`  
		Last Modified: Wed, 24 Apr 2024 06:54:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd9c023e8b6e6486532460ab3244084445f053e19ee8775bb4689b0143f0f00`  
		Last Modified: Wed, 24 Apr 2024 06:54:34 GMT  
		Size: 82.0 MB (82002419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685ffe3d3616a8f8c773f8043a67a418c185c5fdb6f4d767631349a391587a00`  
		Last Modified: Wed, 24 Apr 2024 06:54:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36427a405cf177054e947e9baeef56feb7b30b66554c246dcccef90034e5da1`  
		Last Modified: Wed, 24 Apr 2024 06:55:16 GMT  
		Size: 19.6 MB (19622260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db7c5fc4b717b1579e929d568bd1d9b410ef5222d871df15efa9f166014bb50`  
		Last Modified: Wed, 24 Apr 2024 06:55:13 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3465262ec0d939d77c76a7bd4c02dc1d98b254c2540b9ea1adbeb7f783d4079f`  
		Last Modified: Wed, 24 Apr 2024 06:55:13 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4065a97d6126783317f1903f120a96c1850be36917d50ded0fcf0376ad0799e1`  
		Last Modified: Fri, 10 May 2024 21:52:46 GMT  
		Size: 12.8 MB (12788603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3f44d9766f0b8e6e102fc1ce1d8dd487a9293b95de174db004c04b4157d73f`  
		Last Modified: Fri, 10 May 2024 21:52:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d728c58c4c590340711b78fb80d050a2a509fc2e079e2597de90391a5f7957`  
		Last Modified: Fri, 10 May 2024 21:52:46 GMT  
		Size: 10.6 MB (10608823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ba95b75f7e8c5e35ac7931d5c44d57e16ce0fb94916f6f0c753b256420373c`  
		Last Modified: Fri, 10 May 2024 21:52:43 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3ee45e1a962d7fe083c6a7f1096c57eac041b48f2535f0e5811756b4618562`  
		Last Modified: Fri, 10 May 2024 21:52:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bcf13af6ee5b76cd420be301017b2ebf904aa16a49f6a7aaf60e9b3af6dc88b`  
		Last Modified: Fri, 10 May 2024 21:52:43 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; arm variant v7

```console
$ docker pull php@sha256:99be375eb22a7f00fb234130eb940eeb9295a452e8508c3619ad93106eb2d7e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142811580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ff8b785d2f6fe8e672564ddcbf93503cd436e9bc412b0efb45421f21f3f7fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:09:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 07:09:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 07:09:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:09:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 07:09:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 07:12:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 07:12:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 07:12:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 07:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 07:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 07:12:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 07:12:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 07:12:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 07:12:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 07:12:46 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 07:12:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 07:12:46 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 07:12:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 07:12:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:15:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 07:15:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:15:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 07:15:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 07:15:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 07:15:52 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:15:52 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:15:52 GMT
EXPOSE 80
# Wed, 24 Apr 2024 07:15:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c91bdb9ec5d9afc1dbdc1c85af855e0b737ff91427b0514d37a85344a78a418`  
		Last Modified: Wed, 24 Apr 2024 08:24:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52001de386fe0b3894ce8d75ba5565b1243274c815093bec2a9dda136b5b6715`  
		Last Modified: Wed, 24 Apr 2024 08:24:12 GMT  
		Size: 76.2 MB (76172843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113642f4fdf30b4a570807775f684e30125c2e03565c8a73486d8562dc49e8c`  
		Last Modified: Wed, 24 Apr 2024 08:24:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0e892a65683abb56ae3c750f0cc4d6e9bd9a4e3f597041edffe56d8f7e9df7`  
		Last Modified: Wed, 24 Apr 2024 08:24:58 GMT  
		Size: 19.1 MB (19059142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f908c1d59ecca5b5dbdc422e2d1a2aaa4511430ac6cddb0bb15ad42960c8a4`  
		Last Modified: Wed, 24 Apr 2024 08:24:54 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50ac67d48d9bf873d068e3de7e967a93e4b35d3d8d91ccf92cb1211eed0aa28`  
		Last Modified: Wed, 24 Apr 2024 08:24:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb84810a2f9bd0f0bf77146ad89246078d238ea73673a52a8a7b2f115b696967`  
		Last Modified: Wed, 24 Apr 2024 08:24:55 GMT  
		Size: 12.8 MB (12800969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ef750cf184a60af5bb67f1752567c3aa7d219aea19c8b20466402fc31beaf3`  
		Last Modified: Wed, 24 Apr 2024 08:24:52 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab77051f56a48a2da4cfa557e048a47b33f528e23d97b8a5f1a21e29baa4cabf`  
		Last Modified: Wed, 24 Apr 2024 08:24:56 GMT  
		Size: 10.0 MB (10032613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5db84d58abd8896862302872f42fc371f31c5025c45c0ba716b8d223f672c4`  
		Last Modified: Wed, 24 Apr 2024 08:24:52 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3603c829dfa89ebb09eafed49361e2df7348ec02bd056fd2558b3d6fc6b95411`  
		Last Modified: Wed, 24 Apr 2024 08:24:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b163af328a733b31ce2d6aa8e53754e58bd610a4e89be982d195c0e826fea9`  
		Last Modified: Wed, 24 Apr 2024 08:24:52 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; arm64 variant v8

```console
$ docker pull php@sha256:c5ede94f255d4b535e58a8b6a407ceb883d600adb6eec24d4540780e9a99b212
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172077361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b394066923eb8592c03b67ca3f348e8f15b9bf735ee4633e0018b0455cdb5187`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:09:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:09:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:10:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:10:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:14:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:14:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:14:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:14:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:14:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:14:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:14:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:14:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:14:27 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:14:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:14:27 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:14:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:14:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:18:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:18:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:18:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:18:18 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:18:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:18:18 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:18:18 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:18:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246bb70e866bd7dd3dccad886145a828fb1a1323f17ef26ec181465dbcb0b28`  
		Last Modified: Wed, 24 Apr 2024 06:35:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d9cbc94d9e79c445b63152194f2f71247fc73f539ba2b78046fd04c59ff44b`  
		Last Modified: Wed, 24 Apr 2024 06:35:43 GMT  
		Size: 98.1 MB (98132015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f776f4854c09ee785a8e7e0b102fbcd2483de52db872f8a92ce21e43cac04`  
		Last Modified: Wed, 24 Apr 2024 06:35:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a0ec8ef6bc2cde02f58dc81eeee21fde397e0ad51d4ab138f21b67b77c89c4`  
		Last Modified: Wed, 24 Apr 2024 06:36:24 GMT  
		Size: 20.3 MB (20322298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d170b72693bbaede3e95c7b3f669df38b31b21d3d1a25458e4153823999ceb1`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dda424ab92b122f202ae6b960aa32dd30bc2da243480399c10b1bb870e3342`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070b0b6e5cf9cd3562966e931d2604c0ab983de08e4ec09b0cf54413284906c6`  
		Last Modified: Wed, 24 Apr 2024 06:36:22 GMT  
		Size: 12.8 MB (12802590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6c001e93c2a54dcc62b38f413dcd8d2c3f30c22ebca74d0cdf6a7cb60c35ae`  
		Last Modified: Wed, 24 Apr 2024 06:36:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fcf99c6536891a04beed878d58f153e613ae15f8caa0810a47fa928f3d83aa2`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 11.6 MB (11634947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4465266b4d51074c766e05c27d7d9a56479815032aad49e0fb2fc8fafba70e`  
		Last Modified: Wed, 24 Apr 2024 06:36:19 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f5df9d9476eda8735992b09b6872617130b37f3fb7d80737fed896d7eb5ae6`  
		Last Modified: Wed, 24 Apr 2024 06:36:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26537ce1999d1d2ecfa4afc78f00bda8f95b44485a9740c5f7eac7e5616e0d17`  
		Last Modified: Wed, 24 Apr 2024 06:36:19 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; 386

```console
$ docker pull php@sha256:6cf20b92d2bea838380f9bc87853fefac8cf4ba98b840ecff0e524e958edcda2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.2 MB (177201852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae8fb23f5509a0a439a86b0b6d6151846ae533c4f31ce0f4a3c21f4ec79e8d2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:02:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:02:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:03:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:03:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:10:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:10:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:10:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:10:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:10:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:10:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:10:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:10:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:10:48 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:10:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:10:48 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:11:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:11:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:17:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:17:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:17:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:17:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:17:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:17:45 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:17:45 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:17:45 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:17:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb1b3a226af34ddecc6d2893906c2c06039ad4a2e8de3b340d85dce69d80022`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492e3888464375d37ac47d192dc5edd8fa2a1146cc5b3542c21ca67bc5e080e6`  
		Last Modified: Wed, 24 Apr 2024 07:36:25 GMT  
		Size: 101.5 MB (101522095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a318120f6f010a0842e1a7d0c601c50a55f8f3822db28e6889a943b1e1c103`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa961eb09ca3c9b99fc06b865a7a6fd8608a50684db856f6da97733cecb9c0e`  
		Last Modified: Wed, 24 Apr 2024 07:37:11 GMT  
		Size: 20.8 MB (20844719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8105c623b5e86209dc2d11e7aff7ae42685ea6efbd232f64750a7d2d42e817`  
		Last Modified: Wed, 24 Apr 2024 07:37:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c7989bc9f4db0aeee6f780bdfd90643adebf6585c505c8ba1cb7fdee8b4b7b`  
		Last Modified: Wed, 24 Apr 2024 07:37:06 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db609e9387b856f720f10204ea406d533d853cf408ef100319449558e9560a0`  
		Last Modified: Wed, 24 Apr 2024 07:37:08 GMT  
		Size: 12.8 MB (12802097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3be6ac150a1b14d7a1f224d900a62c1e8f58e2da0803810e95ab3128bf90fb3`  
		Last Modified: Wed, 24 Apr 2024 07:37:04 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d54751e46eba8df8d867776ae7c5ab7fcaaccbab083c0b574e029b970b444aa`  
		Last Modified: Wed, 24 Apr 2024 07:37:08 GMT  
		Size: 11.9 MB (11864181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e09965fb5bf15f58ac2d00c24731cf65cd0f884d92db8172561aff0c66a6e6`  
		Last Modified: Wed, 24 Apr 2024 07:37:04 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fcb36355d6e78df874988cd561f7d776a059cb2775b237e443284ed52691f7`  
		Last Modified: Wed, 24 Apr 2024 07:37:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cece4d81624a7adfd9e99264057f00004c694d83cddd28d389b3b106f435f2b4`  
		Last Modified: Wed, 24 Apr 2024 07:37:04 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; mips64le

```console
$ docker pull php@sha256:f51ec9ac6c97a25affb3d2e57b0c989e7f2b7005c19aadb826e3728457a7cc68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152993049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b923bf3314f195129c6c39559aaf54a2102bff740ba08239a6653256623de97`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:50:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 10:50:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 10:52:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:52:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 10:52:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 11:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 11:09:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 11:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 11:10:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 11:10:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 11:10:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 11:10:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 11:10:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 11:10:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 11:10:56 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 11:10:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 11:11:03 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 11:11:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 11:11:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 11:27:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 11:27:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 11:27:37 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 11:27:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 11:27:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 11:27:47 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 11:27:51 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 11:27:54 GMT
EXPOSE 80
# Wed, 24 Apr 2024 11:27:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2dfa3d36c21ae20eadd92525e61517d0277ef14398994b215d50f524e69655`  
		Last Modified: Wed, 24 Apr 2024 17:08:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a61fb25c010a33f1a3c4b6a08fb02be6a6c0b5d22d9b3ce52a1dd1c356a0024`  
		Last Modified: Wed, 24 Apr 2024 17:09:13 GMT  
		Size: 80.5 MB (80474735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239652ab0a80c5dad89154985f8ceec71b76e056f18e7dcb6ffaea27e8984b59`  
		Last Modified: Wed, 24 Apr 2024 17:08:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796fa395fb05e5a39254d0d9582b02b4121109eda21399913880a92cf308465f`  
		Last Modified: Wed, 24 Apr 2024 17:10:14 GMT  
		Size: 20.1 MB (20064275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a013e8397474ca02386b15a3f4275dd3bafea255c7d4a0473efdade3a7a35305`  
		Last Modified: Wed, 24 Apr 2024 17:10:01 GMT  
		Size: 440.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13a0066263138d3939a9dbee014c328c5cff619f5a5e211581815e00aac8ae`  
		Last Modified: Wed, 24 Apr 2024 17:10:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffc8a2a69fc5c014074d7942be5e3c990709602043699c2c4dd70d4478259b2`  
		Last Modified: Wed, 24 Apr 2024 17:10:04 GMT  
		Size: 12.6 MB (12595077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae130155b09558c33896d49ca3b2cafdafe473543aa6e700b9dcae09f941837`  
		Last Modified: Wed, 24 Apr 2024 17:09:58 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd72f2bbaceb14337ed47d57d44c9e71f8416f4a68159dfcdf255bed983ba92d`  
		Last Modified: Wed, 24 Apr 2024 17:10:07 GMT  
		Size: 10.7 MB (10709309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae1433451245f5d2d2c23b8f06580f34fb3aa57f4a55d4222bcde4d58746c4a`  
		Last Modified: Wed, 24 Apr 2024 17:09:58 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d51e1cd51792f5557e6d50f753f0856112653caa1d459f9f2d59f1cacc5bde`  
		Last Modified: Wed, 24 Apr 2024 17:09:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c621b69707483a89d16b52c21eda9c0bf627c7c5cfde433cc79930f93484d3c4`  
		Last Modified: Wed, 24 Apr 2024 17:09:58 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; ppc64le

```console
$ docker pull php@sha256:896e4b8e75a485489dfb25fdd502a29762e394f4517b0f178e95c2fde0f10b1c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182834295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd86879dab1f2defef1441c15a22840156f0188eeba0ab112b14ad3943d46fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 06:21:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 06:21:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 06:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 06:22:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 06:23:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 06:27:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 06:27:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 06:28:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 06:28:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 06:28:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 06:28:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 06:28:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 06:28:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 06:28:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 06:28:12 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 06:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 06:28:13 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 06:28:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 06:28:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:33:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 06:33:58 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:34:00 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 06:34:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 06:34:04 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 06:34:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:34:07 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 06:34:11 GMT
EXPOSE 80
# Wed, 24 Apr 2024 06:34:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0691face80da0cd3cc797ec4a2ebc8b8db4a2220cd3512317f2a7482987d6c`  
		Last Modified: Wed, 24 Apr 2024 08:07:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b402bfece7b36278991277cb8b969b21bc0826c9f39c9a280b58069053d3cec`  
		Last Modified: Wed, 24 Apr 2024 08:07:24 GMT  
		Size: 103.3 MB (103317105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c476f59d918d2f80058be2efb33e35fd07d1eb9041c856545feea018b2dd7f`  
		Last Modified: Wed, 24 Apr 2024 08:07:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803028d2487c30e28b2758457f5e9a3a47ac99023399a4633ee3f3ac7a5c4f20`  
		Last Modified: Wed, 24 Apr 2024 08:08:13 GMT  
		Size: 21.5 MB (21512987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5acf4731e76e597efa1ab916917c0e56f03dedadd6732441a8d2d7dc4902a8`  
		Last Modified: Wed, 24 Apr 2024 08:08:09 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ef4f8146013e8c50b7057af1996d1297cd096d1cfe4231dc778e85e371bae8`  
		Last Modified: Wed, 24 Apr 2024 08:08:09 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26450a292c7fc55ca73c499ab15849970eefe99dc56042b2e185e76df3a99c5d`  
		Last Modified: Wed, 24 Apr 2024 08:08:10 GMT  
		Size: 12.8 MB (12802600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bd43076d5e4c183d59b1e886a57fa9bec0a49101ea9d2fc7ae42563abdf720`  
		Last Modified: Wed, 24 Apr 2024 08:08:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf5f5533819a7cf40573509ad520020df9efe7e339fa455b4a9fe4d48ab9f64`  
		Last Modified: Wed, 24 Apr 2024 08:08:10 GMT  
		Size: 12.1 MB (12054806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3607bf4ac4d127f19b4e04ae79fb543d32d7ef5c4d4cd92651eed7184e73d3b0`  
		Last Modified: Wed, 24 Apr 2024 08:08:07 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b14866cc613fd16d77bd718d9096738b813ad824ec72e83b5d641e01cb1948a`  
		Last Modified: Wed, 24 Apr 2024 08:08:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a071967375de76c47411623ea17d406c814de807aed4f7be5b667a2609727772`  
		Last Modified: Wed, 24 Apr 2024 08:08:07 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache` - linux; s390x

```console
$ docker pull php@sha256:a1aeed1b89db075abe4bce9b83e27efe939633a4ba17330fdf3bbb14a14b7101
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151907412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cea6644b34242e6e5e841154a34b46d76f1ec76fdce4d8baab6d7520acc5034`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:36:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:36:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:36:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:36:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:36:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:40:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:40:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:40:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:40:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:40:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:40:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:40:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:40:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:40:12 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:40:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:40:12 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:40:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:40:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:43:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:43:01 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:43:01 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:43:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:43:02 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:43:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:43:02 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:43:02 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:43:02 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8edc12e84d8fff112a0cc3d177d3fbe96c3567532a93e6384157c2eca202975`  
		Last Modified: Wed, 24 Apr 2024 06:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f846cc9ad0f18ccaaa8385881df6be477a6820ff7756d3e4df0aba7fa367e0e`  
		Last Modified: Wed, 24 Apr 2024 06:53:24 GMT  
		Size: 80.8 MB (80813871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4c9301a2fdb185845ccb97a1038e220c172bf60a536388eeb18182a3a295a0`  
		Last Modified: Wed, 24 Apr 2024 06:53:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f65d9c7a3c7fbabbee65db4bc3f6b89c6e4658ebd4c4f4bc8d22072c120e8b2`  
		Last Modified: Wed, 24 Apr 2024 06:53:56 GMT  
		Size: 20.1 MB (20103206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09fa0ce42167bd609392aa4caec40de5fb1ac54bae4ddd67c1b30f41a457a9b`  
		Last Modified: Wed, 24 Apr 2024 06:53:54 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f36c8a20b0c6f1b50c385757e29f5d1653bb89fac62ab9c56f01d8799873f23`  
		Last Modified: Wed, 24 Apr 2024 06:53:54 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58fa609a8e4ed683a12fb709cd7b0b85dfe441d472a62afbb726fdc9ea8a4e3`  
		Last Modified: Wed, 24 Apr 2024 06:53:54 GMT  
		Size: 12.8 MB (12801509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f51801367efa9103f912b64d493e5b872bb02eec3a68aa6c0fbc1adfae84f51`  
		Last Modified: Wed, 24 Apr 2024 06:53:52 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eedb502ea42cd79220c1ee6ae10c1f25e4b0233073380a66eee6a952006d9e`  
		Last Modified: Wed, 24 Apr 2024 06:53:55 GMT  
		Size: 10.7 MB (10670901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a658ddf21982d738285f057ea8d0a365cc0b6ccb46aa1aff9f46e450d29c2ae6`  
		Last Modified: Wed, 24 Apr 2024 06:53:52 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9df34c6b280fd83e4f05bf8c2496ed92bd30554e7bc5960c92885a07f1463cd`  
		Last Modified: Wed, 24 Apr 2024 06:53:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a49863ea62b7c869eee49e507af2b1d8fe80d83344d8264048bcec13b9ee60`  
		Last Modified: Wed, 24 Apr 2024 06:53:52 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
