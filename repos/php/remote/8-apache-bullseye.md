## `php:8-apache-bullseye`

```console
$ docker pull php@sha256:53be01265d81e89f4af4fe29416f4dd803dc0eb56bdf103cc2971d48e08cdf4e
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

### `php:8-apache-bullseye` - linux; amd64

```console
$ docker pull php@sha256:f7c0f7faba0d11210923eb8452f97ebd545fee5256186de41bc35fe75a2d0698
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166714000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc0646259a7ff238257b8ac64312fab71cd32d192aae06857b41006be200349`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 10:10:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 10:10:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 10:11:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 10:11:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 10:11:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 10:14:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 10:14:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 10:14:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 10:14:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 10:14:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 10:14:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 10:14:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 10:14:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 10:14:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Apr 2024 18:10:41 GMT
ENV PHP_VERSION=8.3.6
# Thu, 11 Apr 2024 18:10:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Thu, 11 Apr 2024 18:10:41 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Thu, 11 Apr 2024 18:10:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Apr 2024 18:10:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 18:14:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 18:14:07 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Apr 2024 18:14:08 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 18:14:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 18:14:08 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Apr 2024 18:14:08 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Apr 2024 18:14:09 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 18:14:09 GMT
EXPOSE 80
# Thu, 11 Apr 2024 18:14:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a09bf591af6aa18ca1e47bf7fb6d5b8a94b361f49d572e22973eaffb9c61d3`  
		Last Modified: Wed, 10 Apr 2024 12:26:56 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a63fe8cf3a3ac18fbbeb84a6bcfd82dca8f26e775dd8ff9b1042dbcccfb04f0`  
		Last Modified: Wed, 10 Apr 2024 12:27:09 GMT  
		Size: 91.6 MB (91640010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b92c4ecc2a1a38639ae53e2931c4b637365db397a7bb7bea09e097637979c69`  
		Last Modified: Wed, 10 Apr 2024 12:26:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c90252fcc0571c2b6e50c7fcbe629517ba0cf269a2c92b2171853719ad5026`  
		Last Modified: Wed, 10 Apr 2024 12:27:26 GMT  
		Size: 19.3 MB (19258377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32183726aaa5f55cd2ca3e3382900f1e3bc14c941ad90f91c7842283af025440`  
		Last Modified: Wed, 10 Apr 2024 12:27:23 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5347604417b38d526466b64f3e983028e59b63c1168a31f0e095afbd62b333`  
		Last Modified: Wed, 10 Apr 2024 12:27:23 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58aeee410248da0551fafd7b7c33d324e99df37144cfd53e5de3e03df1dc585`  
		Last Modified: Thu, 11 Apr 2024 19:42:45 GMT  
		Size: 12.8 MB (12808695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ec1324c0009cde03fd8b2575dee6352d003ab3cb65e66530ffe3c7ac3c3dd5`  
		Last Modified: Thu, 11 Apr 2024 19:42:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a08263592e9ed27f0007c5fa7564d1ec2d6bcf35c68ee52c8a30b04e52aa4c`  
		Last Modified: Thu, 11 Apr 2024 19:42:44 GMT  
		Size: 11.6 MB (11573598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaee8939b2752ca2bb944cfcfbc16bbe75dfc1a0094ffbee8b3cfb8bcd46691`  
		Last Modified: Thu, 11 Apr 2024 19:42:42 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3c5384923bd990af12fb29d057b74385c2cde6aab3699fb86115ff60bd7b1e`  
		Last Modified: Thu, 11 Apr 2024 19:42:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00294aba7ed6b11e76e8769fe8c71b8aecf4e9ee0fe768e4c13e79d20584edeb`  
		Last Modified: Thu, 11 Apr 2024 19:42:43 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm variant v5

```console
$ docker pull php@sha256:75cdb39e9ae02e143b60b6fc3a1b256f5bd66585fffa1790ace7847d95de0965
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144597551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746d9b7d7f9b20e8ffb81a935de9823a23b6426159ac263145aac6be9ae6a5aa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:28 GMT
ADD file:4ccbd1f9bcc76d259ba2b235681f1b749e86690e8805ee49f9fb44abc9ff5dc2 in / 
# Wed, 24 Apr 2024 03:53:29 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:43:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:43:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:43:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:43:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:47:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:47:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:47:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:47:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:47:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:47:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:47:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:47:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:47:34 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:47:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:47:34 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:47:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:47:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:51:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:51:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:51:19 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:51:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:51:19 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:51:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:51:19 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:51:19 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:51:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2438f3883cb848a901cb08a6c99ec3ef261d41ca6f0d5321f274d995c58fa24e`  
		Last Modified: Wed, 24 Apr 2024 03:57:14 GMT  
		Size: 28.9 MB (28936577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b1fed60046b77429b931fc66a6be64acf0e11d22e0e4ef1fb91f8113bad54a`  
		Last Modified: Wed, 24 Apr 2024 06:56:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0032ba84da49373d681245f99fafd9eb63d45ef8f7f8be28080203acf81b8186`  
		Last Modified: Wed, 24 Apr 2024 06:56:48 GMT  
		Size: 73.7 MB (73695287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3b70edc4571e55cbe7405b2f200edb12f330b4ecc5e7692edf57f06af483fc`  
		Last Modified: Wed, 24 Apr 2024 06:56:33 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613e7c369d5b7eb1840e9cbf8c8cc494935e555eecde2cccc9acb6fd05d20cb`  
		Last Modified: Wed, 24 Apr 2024 06:57:14 GMT  
		Size: 18.6 MB (18580992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20832c0ebb8ee6dbcff8485fb9e836fdf70f149de4a1370e37152fad746c90`  
		Last Modified: Wed, 24 Apr 2024 06:57:11 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103e229d25c9123586473d7f5f200727183ede82c07b5055c251f8e815a31ead`  
		Last Modified: Wed, 24 Apr 2024 06:57:11 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24c9df24cb51969e1d6a4d3f0fb51e51c5b281beeec30f7bead7676e622959c`  
		Last Modified: Wed, 24 Apr 2024 06:57:12 GMT  
		Size: 12.8 MB (12807849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837b9491dd695d0ca30bbf7ef9bbf24b4cfefcbd1408c61109c13be4aa18389e`  
		Last Modified: Wed, 24 Apr 2024 06:57:09 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476b26055729c1c1a67ae2c3ac4db2646f7c9920d532a70f81932c76a917afb`  
		Last Modified: Wed, 24 Apr 2024 06:57:11 GMT  
		Size: 10.6 MB (10571267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57958e43f29fe73de9815dde163fc260970fbc23ed42f51355e8e396bba5cd1c`  
		Last Modified: Wed, 24 Apr 2024 06:57:09 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da026780cb825c81dde78b2a2e09fa5347598f843e8159293ba195b2e64e8a6e`  
		Last Modified: Wed, 24 Apr 2024 06:57:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb90b5ccd7105f586aba1b60a94d0c3f4921e7a2a9f13f8450d7f044e27f569f`  
		Last Modified: Wed, 24 Apr 2024 06:57:09 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:855f0ab66238e3de0c747ddff98604bcc18d9c7b02e5cb87449dd124c317301c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136749746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4289d414b678699f04392e93fcf61cd07e3dfa289ff05627091c1d9599ff8ae7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:46 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Wed, 10 Apr 2024 00:58:46 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:09:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 12:09:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 12:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:10:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 12:10:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 12:17:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 12:17:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 12:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 12:17:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 12:17:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 12:17:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 12:17:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 12:17:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 12:17:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Apr 2024 20:06:06 GMT
ENV PHP_VERSION=8.3.6
# Thu, 11 Apr 2024 20:06:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Thu, 11 Apr 2024 20:06:06 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Thu, 11 Apr 2024 20:06:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Apr 2024 20:06:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:10:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 20:10:15 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:10:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 20:10:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 20:10:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Apr 2024 20:10:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:10:16 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 20:10:16 GMT
EXPOSE 80
# Thu, 11 Apr 2024 20:10:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0a36d9891eefe34cc386e8f6e07bb4a652abb6889dba10af0d41e5bad62ec9`  
		Last Modified: Wed, 10 Apr 2024 15:50:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11f4929d4ebe8a6444b4b3e2fecf310b784254e270c11226e566a981a274c59`  
		Last Modified: Wed, 10 Apr 2024 15:50:52 GMT  
		Size: 69.3 MB (69322863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df67edc88110a99e5baa75d813f45c5c4a65d0efa18a57773c1706349828a23f`  
		Last Modified: Wed, 10 Apr 2024 15:50:40 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9aeed1f01bb97573aa5b12b9cc36b65bcf60db555e6354e9ca32e196f8a970`  
		Last Modified: Wed, 10 Apr 2024 15:51:10 GMT  
		Size: 18.0 MB (18017614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d8b4e70f4b084437e788317a9cc992325122e8ea9722e63daad3ada7491c64`  
		Last Modified: Wed, 10 Apr 2024 15:51:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f7828acb96a4ac10db29925d8b4231aa21778d3b51367dc9c29d343a81cbdf`  
		Last Modified: Wed, 10 Apr 2024 15:51:07 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf3e278459bdf17bfdae75f852b27a157a614275dd0b250b4b610d679062dee`  
		Last Modified: Thu, 11 Apr 2024 21:36:04 GMT  
		Size: 12.8 MB (12807320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aa9580335ebe254674677898e3eb95520f64ae61a0198c2d9a3af63925d976`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17f49d2f73e5d299d8e13c60772d055b3b8afb81e8357326153052db79344b0`  
		Last Modified: Thu, 11 Apr 2024 21:36:01 GMT  
		Size: 10.0 MB (10007892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1f59ff050a7076f52cf6b33d300ae1105e3b7e21877fdf8b472d120fc67d7a`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52e53886dd7aae3aeffed3ba4f2cf8f4df6baaf6860a94a0e31bd3e750aef94`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde7581e764772c557edf9b6a4c29ed33719b2ff167999390f0fdb2822762b50`  
		Last Modified: Thu, 11 Apr 2024 21:35:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:300ad0f854a490b7b9e318aed237da0c4d4239db2c2116483c28cb0452f031ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160671408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88a616d4f396fbf49d3b1574fcad18ea6483f053d15cbe48713989ccd7a6285`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:25:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:25:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:26:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:26:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:29:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:29:36 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:29:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:29:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:29:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:29:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:29:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:29:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:29:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:29:44 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:29:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:29:44 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:29:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:33:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:33:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:33:02 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:33:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:33:02 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:33:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:33:02 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:33:03 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:33:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f8a83e467d1485a6f79dfbadc2936594c6385b2750c6ae5479724b16e6d53`  
		Last Modified: Wed, 24 Apr 2024 06:37:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45672ff77f6a7e8b9efd3215ce9def00822c7cfe5ee191bb16298b457f12bb4e`  
		Last Modified: Wed, 24 Apr 2024 06:37:42 GMT  
		Size: 86.9 MB (86936919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12cec5cb77950690d947e911ae799bfc107c91bc30b6fbd7d11337e715227ef`  
		Last Modified: Wed, 24 Apr 2024 06:37:33 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a204f2e3d7bcc3f8fcc146c19d239915045721f9315fe043dd7d96e9c994810d`  
		Last Modified: Wed, 24 Apr 2024 06:38:06 GMT  
		Size: 19.2 MB (19192631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47759b7f9a960673936521363abf0dfaf88627473f4c3ccdb029fc2f785f23ee`  
		Last Modified: Wed, 24 Apr 2024 06:38:04 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9260d5ca164af958add740defd29d3fd13b9662ec67749e963e3134e89927f`  
		Last Modified: Wed, 24 Apr 2024 06:38:04 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50582c0620e8c40090b5659e62913499cd7510246664267f9d79b34af3c2ee22`  
		Last Modified: Wed, 24 Apr 2024 06:38:05 GMT  
		Size: 12.8 MB (12808670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce244eb31a3ec0f6e611a2059304582a6b2ad1846b904f4bc59d4d1827b0b77`  
		Last Modified: Wed, 24 Apr 2024 06:38:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56acd16254d9905b5b79c1d9964aff0e115b8efd24c486cc067ecc27b4f4fac8`  
		Last Modified: Wed, 24 Apr 2024 06:38:04 GMT  
		Size: 11.6 MB (11640277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f55c2a4a7b295d02debd42b058a7c67ad931c5f243af6dbb5192a959ed3dd81`  
		Last Modified: Wed, 24 Apr 2024 06:38:02 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f854823289e200d2c9b90fd25f055481b5d301f364f13f874ea5636a882f8309`  
		Last Modified: Wed, 24 Apr 2024 06:38:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda92689548185515d0881b33fa5ca2ab4cdb61b139206eb4cb9c3833d43a2a6`  
		Last Modified: Wed, 24 Apr 2024 06:38:02 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; 386

```console
$ docker pull php@sha256:867111f8542360846f6ccd79cbdaf5a98ede3ac9740a79d7b69ad32f14ee0344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169482542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0873472b29bcd23ee890ccf02fb1566e578159f4bb51d13c488b2823f8d28f1e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:34 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
# Wed, 10 Apr 2024 00:57:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:13:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 12:13:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 12:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:13:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 12:13:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 12:19:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 12:19:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 12:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 12:19:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 12:19:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 12:19:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 12:19:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 12:19:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 12:19:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Apr 2024 18:12:35 GMT
ENV PHP_VERSION=8.3.6
# Thu, 11 Apr 2024 18:12:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Thu, 11 Apr 2024 18:12:35 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Thu, 11 Apr 2024 18:12:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Apr 2024 18:12:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 18:18:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 18:18:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Apr 2024 18:18:19 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 18:18:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 18:18:19 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Apr 2024 18:18:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Apr 2024 18:18:19 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 18:18:19 GMT
EXPOSE 80
# Thu, 11 Apr 2024 18:18:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ed3dadf1c21feb2ff16df18b571ba54145f46f3b6040b0ac6a1aad1b96653`  
		Last Modified: Wed, 10 Apr 2024 16:02:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b436e2a26ab5647f311e180cf02589b2fe37976e32a161d54e0967c7cb70fca`  
		Last Modified: Wed, 10 Apr 2024 16:03:01 GMT  
		Size: 92.7 MB (92721468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079ee4d362949c5e7064e0dbfa8f04547e6aeb38cad32fecb6e2ae7ea7d75b70`  
		Last Modified: Wed, 10 Apr 2024 16:02:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e607cd004a82750f89d56d2efd473e4d30ded01833c0837c4c5612ff65d6598`  
		Last Modified: Wed, 10 Apr 2024 16:03:22 GMT  
		Size: 19.7 MB (19744236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189268e404872539b171f731b51d20f97896419264c7e256bec2ae65bcdaba23`  
		Last Modified: Wed, 10 Apr 2024 16:03:18 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec06a311c51dd4465e0e5b1f570b727f7cc52396a5f33fa8f75cdbcdccd71549`  
		Last Modified: Wed, 10 Apr 2024 16:03:18 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db9d60acf9c8c586296a9b6a327b6b03eba403d7b393c1a18c6389835ae2685`  
		Last Modified: Thu, 11 Apr 2024 20:49:07 GMT  
		Size: 12.8 MB (12807971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5954b97e32dc23b7816837f62e20a690b4257d6495d9eac9440f317508ad44f`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901f86177ab7b6bcd05e7def86d83fc12c289fbb415817b070b5b60f5db301d9`  
		Last Modified: Thu, 11 Apr 2024 20:49:08 GMT  
		Size: 11.8 MB (11789874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499470d7d2367ed3124a9a38267dc32038ab2abd0840d8b8537113d71d0a2758`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410d06a6fd1754e06d4a00ed8eb1e2d00b2d662bdecb6e001d717535978a3067`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bbbe4b31faf3540338f2775c22dce3664d16538324b9e20cb03b367e1e2bc5`  
		Last Modified: Thu, 11 Apr 2024 20:49:04 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; mips64le

```console
$ docker pull php@sha256:d1493193b83901b649d9cee69f496fdf1c13cabb05d8198beffb08432218d8f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143906078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fefc489e31c1ed8f5f5e01a1b368745d7f56cf3199a4b47d099c5aebac9e65`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:11:25 GMT
ADD file:5a3b2305df619d313e2592819c382781fd774d11c3f687bc9ca004eba259694b in / 
# Wed, 10 Apr 2024 01:11:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:32:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 05:32:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 05:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:33:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 05:34:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 05:48:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 05:49:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 05:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 05:50:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 05:50:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 05:50:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 05:50:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 05:50:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 05:50:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Apr 2024 20:13:26 GMT
ENV PHP_VERSION=8.3.6
# Thu, 11 Apr 2024 20:13:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Thu, 11 Apr 2024 20:13:33 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Thu, 11 Apr 2024 20:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Apr 2024 20:14:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:28:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 20:28:48 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:28:55 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 20:28:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 20:29:02 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Apr 2024 20:29:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:29:09 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 20:29:13 GMT
EXPOSE 80
# Thu, 11 Apr 2024 20:29:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:94315f37c06e4616cd911d9cfbe5597a620ca0249447454791c232fa7b1e2724`  
		Last Modified: Wed, 10 Apr 2024 01:23:22 GMT  
		Size: 29.6 MB (29645932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b582dc17ffdcd58471330a4b121a8986eb897b80bf8dcaba419ff937afbeef5`  
		Last Modified: Wed, 10 Apr 2024 14:46:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143cf3cf325cbea060c6c1856c747936bb89af5c4b0fca3a7c6bbc25a1ef1380`  
		Last Modified: Wed, 10 Apr 2024 14:47:22 GMT  
		Size: 72.0 MB (72019713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3a5e41e2a68cf8860612e0eb9b7e48d1304dc2925f9e09d30ebf9bef52a446`  
		Last Modified: Wed, 10 Apr 2024 14:46:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4999c52cabdea1d196485f240a613efa75915b78917d632daf582f7fe88477c7`  
		Last Modified: Wed, 10 Apr 2024 14:47:52 GMT  
		Size: 19.0 MB (18955362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bc9bd35a75970cd79abfc329ba1de09f89294533cdd56650e0d26cd13f6514`  
		Last Modified: Wed, 10 Apr 2024 14:47:40 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5aa99fd9623dcfcd5eda928df621be8d2021630f9cfc038243c3a01b3b122`  
		Last Modified: Wed, 10 Apr 2024 14:47:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c34471933392d3a91f4f2a318e57461d7291310b225d2e5840fd249b2fed05a`  
		Last Modified: Thu, 11 Apr 2024 23:06:51 GMT  
		Size: 12.6 MB (12591988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b99ec93e10a4111834b2271a3e7fc89fbfe6762e5812d426a8619ada4809e2`  
		Last Modified: Thu, 11 Apr 2024 23:06:45 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5ff61d63aab22129a5374f3f652ed3354a501882dacd88d7ec3efc5b31ca8f`  
		Last Modified: Thu, 11 Apr 2024 23:06:54 GMT  
		Size: 10.7 MB (10687601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3104239edb9f9d90c0f9130a79d7f8417c78684e4ead71a931523e6786bae99`  
		Last Modified: Thu, 11 Apr 2024 23:06:45 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634efa582cd246d06dddeb37a08f6184d2f39e6c0e19449a795e11af24724253`  
		Last Modified: Thu, 11 Apr 2024 23:06:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab21a0d90882f826bad447a8e01535d54a6056fa5ac1b648c5333cd37f9f6cd`  
		Last Modified: Thu, 11 Apr 2024 23:06:45 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; ppc64le

```console
$ docker pull php@sha256:4952c0b2e302acc41190add11551ba75046dd13ed181d6b7e19bd516af666182
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167258036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de577fd594c31ff835257ea79c1d08b507d887dc5184112a67a44e143396db5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:04:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 10 Apr 2024 09:04:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 10 Apr 2024 09:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:05:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Apr 2024 09:05:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 10 Apr 2024 09:09:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 10 Apr 2024 09:09:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 10 Apr 2024 09:10:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 10 Apr 2024 09:10:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 10 Apr 2024 09:10:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 10 Apr 2024 09:10:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 09:10:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Apr 2024 09:10:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Apr 2024 09:10:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Apr 2024 17:53:16 GMT
ENV PHP_VERSION=8.3.6
# Thu, 11 Apr 2024 17:53:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Thu, 11 Apr 2024 17:53:16 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Thu, 11 Apr 2024 17:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Apr 2024 17:53:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 17:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 17:56:36 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Apr 2024 17:56:37 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 17:56:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 17:56:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Apr 2024 17:56:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Apr 2024 17:56:38 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 17:56:38 GMT
EXPOSE 80
# Thu, 11 Apr 2024 17:56:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d55142cd3123552c44a0e1701f8cd168bc522175bc75c850189de125d70fb`  
		Last Modified: Wed, 10 Apr 2024 11:51:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddbd240e160e1289c6d6b5e93d65b6e60feada9d89fc02edf160b1a799b861b`  
		Last Modified: Wed, 10 Apr 2024 11:51:58 GMT  
		Size: 86.7 MB (86651989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debc3c4f90d609bdab9cc23403c78861d833f4e099e49befddd660674bf5e49e`  
		Last Modified: Wed, 10 Apr 2024 11:51:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5b71e65c481447d08e87f77fbc81c15db0c24b77f03f27574cd7e850fd8a4`  
		Last Modified: Wed, 10 Apr 2024 11:52:19 GMT  
		Size: 20.5 MB (20473729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b313fb545912f5c440f81255801d291fc171b5d3fe66904af0badd13fdc3ce2b`  
		Last Modified: Wed, 10 Apr 2024 11:52:15 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d937caa7e434a76e8f5fc981bd308ce8b77f0c79791dd00ffe2171f530dbb3`  
		Last Modified: Wed, 10 Apr 2024 11:52:14 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477d9edd66b84988cf31d8aa13cc67d7cfc25b2cb4abb22e8cc70efbf5c7cd2c`  
		Last Modified: Thu, 11 Apr 2024 19:09:10 GMT  
		Size: 12.8 MB (12808612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2f82b8a8df7050ff173cf6a9141eb1c8c7988d003a7729147bae13417a0cc`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b161e3c72cbbe18e2b642cf8404926dd62a88ed739a0d8b0ef1fbf799854871`  
		Last Modified: Thu, 11 Apr 2024 19:09:10 GMT  
		Size: 12.0 MB (12014027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106c30e7916d20d3f9a24038746e10af94024e9d24fa4b90e749696e723eb2e`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf7b1b74ed6eed444581197113856846dcea63460661604d6bdf2766d0cb22`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f82b01e3fd0c8720826073b556518520eeb23041437471513a771631e88dbe`  
		Last Modified: Thu, 11 Apr 2024 19:09:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; s390x

```console
$ docker pull php@sha256:4d822c5189141d9099ffeee2df963b465f44f3df26e143492916ca82ee445894
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143891422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9eb3bd3ef47fc7c0543266ac28d245b48b95d02272496fd822a8ac415514766`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:49:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:49:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:49:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:49:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:52:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:52:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:52:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:52:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:52:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:52:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:52:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:52:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:52:34 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:52:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:52:34 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:52:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:52:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:55:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:55:42 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:55:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:55:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:55:43 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:55:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:55:43 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:55:43 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:55:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e355f57694d592fc3cffa2329210804918508167439b2e60cfb03f673ff0078e`  
		Last Modified: Wed, 24 Apr 2024 06:54:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab701f81a0748f304c306192740a8cbcadb7c90fcd55a404ae9dca453a166dbb`  
		Last Modified: Wed, 24 Apr 2024 06:55:04 GMT  
		Size: 71.6 MB (71640691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae179fb2b6f7d70273108318730114a33d82bdc2b97e6c0ef408105c03d3ee3`  
		Last Modified: Wed, 24 Apr 2024 06:54:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3333e3f24fee960b489613c0446b748aa2a51fcf65a26dbef77db9a5e471c03`  
		Last Modified: Wed, 24 Apr 2024 06:55:22 GMT  
		Size: 19.1 MB (19097782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b6742c6a31d25c4a2d913a80a4bff49f03c738b9172960fec34e034f82015f`  
		Last Modified: Wed, 24 Apr 2024 06:55:19 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619275d3d7bd42fb139302932d59a35d303bc15970be9b624974b3511abe568c`  
		Last Modified: Wed, 24 Apr 2024 06:55:19 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d7f1cb63093fe34cf530138d6cbab2b258ecc5b9d9fb2bde30a49e96991c05`  
		Last Modified: Wed, 24 Apr 2024 06:55:20 GMT  
		Size: 12.8 MB (12808381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092f89d1561ca3780f64d17f1771ab475906b37d3a067da6ec2d81eb87c3c7e`  
		Last Modified: Wed, 24 Apr 2024 06:55:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9b0603790d16414de35f3fb4dbee64909e41681c7468b057ac40f1305e4acc`  
		Last Modified: Wed, 24 Apr 2024 06:55:21 GMT  
		Size: 10.7 MB (10665062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749642bb7e90655d7c2861b959e1340e83f947630235634d31f0a01a2b1bf9e1`  
		Last Modified: Wed, 24 Apr 2024 06:55:18 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba162cf94436c85f431bd45daf577859aa595e5a11d58904b6aea9b478a89b3`  
		Last Modified: Wed, 24 Apr 2024 06:55:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9985e22df001e22e201378b6defbff9291ef263196e80804836ab7b05a596f1`  
		Last Modified: Wed, 24 Apr 2024 06:55:18 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
