## `php:8-apache-bullseye`

```console
$ docker pull php@sha256:11cc36183edb74840009f386fd2853f29f99a39d23b14bfae624a8af6f9c26d4
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
$ docker pull php@sha256:830e8a56b30e00f888d6b442e0b45bef5826439fef240d480715b235771f82eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166743080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6341e93e1251a2ab2c53f06212f9d3376cf913ab5b6f0f91d97b2ba6997cb36`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:56:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 08:56:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 08:56:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:56:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 08:56:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 09:00:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 09:00:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 09:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 09:00:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 09:00:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 09:00:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 09:00:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 09:00:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 09:00:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 09:00:22 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 09:00:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 09:00:22 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 09:00:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 09:00:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:03:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 09:03:47 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:03:48 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 09:03:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 09:03:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 09:03:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 09:03:48 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 09:03:48 GMT
EXPOSE 80
# Wed, 24 Apr 2024 09:03:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4ea0ade393727808307074edf43fec68bd16248ca5d5e87fa48ff5d8058275`  
		Last Modified: Wed, 24 Apr 2024 10:15:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064c8ff4a89f66e6c5ac6de1f850a3406c7a365642b6e83c7db667043190ec1a`  
		Last Modified: Wed, 24 Apr 2024 10:15:24 GMT  
		Size: 91.6 MB (91641337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835cacc3785c3ea1fb8c6f8f0794b4ac348818e0a1d2856a80a418ac875da118`  
		Last Modified: Wed, 24 Apr 2024 10:15:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34a344384e1f3cd886719c960202415ee96a5d76f19cbf9f6456645294f1a3e`  
		Last Modified: Wed, 24 Apr 2024 10:15:48 GMT  
		Size: 19.3 MB (19276848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9df37f9cbb9da9a2eebf5cae67cbc4f73f7c2b7723881200ed47fa85cd3d6b`  
		Last Modified: Wed, 24 Apr 2024 10:15:45 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a5847d4744b49b9f87aa21e6f395b337bf69bbac48a50ee3ca47ffcfdba2ce`  
		Last Modified: Wed, 24 Apr 2024 10:15:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60c0388eeb2d6dbeda5c58cd7ca81b0945250f2613f565cc8cc0882a99c2164`  
		Last Modified: Wed, 24 Apr 2024 10:15:46 GMT  
		Size: 12.8 MB (12809432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c72fbfe2e55fdbe364c7294ed1f39950dd6b8413c0d2deb228a2772d54d99a`  
		Last Modified: Wed, 24 Apr 2024 10:15:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671bb7cbb44678fe069782cbe241137ab6ecf607900dd55b49aeb5d7b16daa7b`  
		Last Modified: Wed, 24 Apr 2024 10:15:45 GMT  
		Size: 11.6 MB (11575623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a30a053cc63be0bff594b88b366f45bd8f81cae28748fe7614901798417547`  
		Last Modified: Wed, 24 Apr 2024 10:15:44 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f5530e4bb79f568a90b8e3c34c362b8f21f407b302014f7360c4e0b0a21844`  
		Last Modified: Wed, 24 Apr 2024 10:15:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b774ba9951f6fc997e6ae72ce9b7099099ff14a92062e52012323e76ab3682e`  
		Last Modified: Wed, 24 Apr 2024 10:15:43 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm variant v5

```console
$ docker pull php@sha256:ef5fd0a59957107b14677d3175005ee450f93eeb3e545bb5242f2ed61fc207d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144583656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f2faee03e2f398124993994ed0ba16ede5f5efe04c25a42ea4734fe4c5b9fa`
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
# Fri, 10 May 2024 21:06:19 GMT
ENV PHP_VERSION=8.3.7
# Fri, 10 May 2024 21:06:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Fri, 10 May 2024 21:06:20 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Fri, 10 May 2024 21:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 May 2024 21:06:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 May 2024 21:10:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 May 2024 21:10:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 May 2024 21:10:54 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 May 2024 21:10:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 May 2024 21:10:55 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 May 2024 21:10:55 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 May 2024 21:10:55 GMT
WORKDIR /var/www/html
# Fri, 10 May 2024 21:10:55 GMT
EXPOSE 80
# Fri, 10 May 2024 21:10:55 GMT
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
	-	`sha256:172441c3cde67ee96c82edf759d2cfe251eb59c83584d20805f5ea736d7e0503`  
		Last Modified: Fri, 10 May 2024 21:54:37 GMT  
		Size: 12.8 MB (12796397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6f9617b845e760c317ccb0aa0564fbce6ec0ee185f6cc8ec6eaf0cf788b5b3`  
		Last Modified: Fri, 10 May 2024 21:54:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e95c0e37519352aa6164cb07b03529b876135ee6a3b0b7e2372b7f90d75777`  
		Last Modified: Fri, 10 May 2024 21:54:37 GMT  
		Size: 10.6 MB (10568826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9b565a8d42ca1be583547b63816d571751746d9c9669819fd09561443192dd`  
		Last Modified: Fri, 10 May 2024 21:54:34 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e711b4463156de94117c990774ab69298568c9e164f97b3b2e05543ff4fb15`  
		Last Modified: Fri, 10 May 2024 21:54:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d508c94153ab2cfcad2b7bb701f0b7f2aec2e1ae64e3a6e12a6046755fec07ea`  
		Last Modified: Fri, 10 May 2024 21:54:34 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:eadafdc79f68f235f1a573d175af8a56ed6b0d51df03a60680fbfa43db4b4df2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136764566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6a4556fc389909e886284867312ee39475bafec71ec886eda65a55b611aee5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:22:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 07:22:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 07:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:22:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 07:22:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 07:25:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 07:25:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 07:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 07:25:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 07:25:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 07:25:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 07:25:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 07:25:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 07:25:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 07:25:35 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 07:25:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 07:25:35 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 07:25:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 07:25:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:28:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 07:28:15 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:28:15 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 07:28:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 07:28:15 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 07:28:15 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:28:16 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:28:16 GMT
EXPOSE 80
# Wed, 24 Apr 2024 07:28:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a02b21a01d99286f84611b539c3cddf4dc10654180b0e1fbffa9feff107855`  
		Last Modified: Wed, 24 Apr 2024 08:26:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022a648ba91c8af160252b2ef76d8b565dac9e34107afd1753c4b4fd4b355f4c`  
		Last Modified: Wed, 24 Apr 2024 08:26:25 GMT  
		Size: 69.3 MB (69324519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab5a8826829f2350bfc9212a316a3b8668bef6318a18aa2bb5a0f3b41a99838`  
		Last Modified: Wed, 24 Apr 2024 08:26:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268db77852f915df51b17d35cceb1c0d839d78f2e305efc16ee42e24d26f5392`  
		Last Modified: Wed, 24 Apr 2024 08:26:55 GMT  
		Size: 18.0 MB (18022670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967fde2337a018d581a1e375bf75945399da48666647d31bb5fd9e5520e86ad1`  
		Last Modified: Wed, 24 Apr 2024 08:26:52 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c6aa6a4c51bc25a70fd18c8c8a464bc77681e9f3f31d59d8a7d8fe7033a0e3`  
		Last Modified: Wed, 24 Apr 2024 08:26:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787cb150f393b32a7d2a0270589ccbfce6390e72b421d36396535d6a5300e678`  
		Last Modified: Wed, 24 Apr 2024 08:26:53 GMT  
		Size: 12.8 MB (12807841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86545ca11f4b9d2cd002ae22ad422119bfd9708016b1416872a128db7167f7d5`  
		Last Modified: Wed, 24 Apr 2024 08:26:50 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7c406c602c85797e216bcd353a7cb5cb9bd24898fc76acaee733b12dda93e1`  
		Last Modified: Wed, 24 Apr 2024 08:26:53 GMT  
		Size: 10.0 MB (10009215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1670dd0672695e116a555c7c99a66afd81b553e5afcd6a517f4152e12c912bd4`  
		Last Modified: Wed, 24 Apr 2024 08:26:50 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1764e09ca20767211af6b21f38c68c98e63769d1991c0b06ccb25e564e26c9`  
		Last Modified: Wed, 24 Apr 2024 08:26:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ebfa9bad5234898b40bafd3ec249f9ce90eff9509b6b6cb945e471daaea50a`  
		Last Modified: Wed, 24 Apr 2024 08:26:50 GMT  
		Size: 898.0 B  
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
$ docker pull php@sha256:bf2dd0ad5a42868357f9f3589f2230e5650d67d0e4a752385d70697dccede79e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169518335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3117cc6dab2ae835e3337318df27c7fb9478bfc6d4d795b43711d04047989914`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:31:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:31:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:32:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:32:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:32:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:38:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:38:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:38:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:38:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:38:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:38:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:38:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:38:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:38:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 05:38:23 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 05:38:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 05:38:23 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 05:38:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 05:38:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:44:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 05:44:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:44:02 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 05:44:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 05:44:03 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 05:44:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:44:03 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:44:03 GMT
EXPOSE 80
# Wed, 24 Apr 2024 05:44:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a339981da912097fb6e5c1be3d7c773255aef2f4f47c1800001ee3a6462a27`  
		Last Modified: Wed, 24 Apr 2024 07:38:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f3e9474f16fdc243437498d821b683276a638cfcc3825469b096e08efb084`  
		Last Modified: Wed, 24 Apr 2024 07:38:56 GMT  
		Size: 92.7 MB (92723657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187647c2c8de55510d4b4d17c7049fa3727ebe383acdbbd88926f9cc5d1786ed`  
		Last Modified: Wed, 24 Apr 2024 07:38:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce581db3380d2d3e1171383488abdee6426f7c3d3acfecaf92289123be65ec81`  
		Last Modified: Wed, 24 Apr 2024 07:39:25 GMT  
		Size: 19.8 MB (19764793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06cca77805517fd3f18bc1b051755421d786e9f724540b74ca3438bb30ae5b0`  
		Last Modified: Wed, 24 Apr 2024 07:39:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4d24829a69533cccbcb34d788ca4545377d485afa36b1f060556a8005004d6`  
		Last Modified: Wed, 24 Apr 2024 07:39:21 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b725e573cddbbf91777301a108e202b07b8ddb87daa014080b2353f440c74e81`  
		Last Modified: Wed, 24 Apr 2024 07:39:22 GMT  
		Size: 12.8 MB (12808728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532fe1c5d005964c7df0213f72a55a1e093da05d35f0c69e9160e6f95cd4ddca`  
		Last Modified: Wed, 24 Apr 2024 07:39:19 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdfd419db2983cae38b49d4f0bb92875ed549fd2528427c18f502014c71f6ff`  
		Last Modified: Wed, 24 Apr 2024 07:39:23 GMT  
		Size: 11.8 MB (11790800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91e1ceda560b496673f7ce01efeb9dfed202374027975c0f57b94ed268972e5`  
		Last Modified: Wed, 24 Apr 2024 07:39:19 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f416b4b51bf310570780a298a596d0f5965d4442cc49fcfb4a76f722733543`  
		Last Modified: Wed, 24 Apr 2024 07:39:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243ec0196b193f09724551191d67f9213525dc07c3b3cf042a906c19bc2f08f5`  
		Last Modified: Wed, 24 Apr 2024 07:39:19 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; mips64le

```console
$ docker pull php@sha256:a16b3b11a7b90ae7f5a6859518c2d3cd4f2c98a845ab780ed87cf9f02aeb578b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143714722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f008eeba059dd368bfcac7908de16782e0633402106d7554450f2009d382b8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:15:35 GMT
ADD file:87680940dfe26d5f4583964a639405d4e00c6a3f72863f7b7e18eca764a73c67 in / 
# Wed, 24 Apr 2024 03:15:40 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 11:59:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 11:59:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 12:00:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 12:00:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 12:00:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 12:16:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 12:16:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 12:17:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 12:17:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 12:17:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 12:17:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 12:17:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 12:17:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 12:17:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 12:17:32 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 12:17:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 12:17:39 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 12:18:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 12:18:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 12:32:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 12:32:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 12:32:55 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 12:32:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 12:33:02 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 12:33:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 12:33:09 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 12:33:12 GMT
EXPOSE 80
# Wed, 24 Apr 2024 12:33:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2d257022fa7c7f0c7879f59891b7e4277d67c9114b820f229207724d5e65d6cf`  
		Last Modified: Wed, 24 Apr 2024 03:26:43 GMT  
		Size: 29.7 MB (29652163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e383bb45e0b519637e2954bb77bf63d937602282bffdd77978394926b772925`  
		Last Modified: Wed, 24 Apr 2024 17:12:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580bfc8b9f5a4624e02e4fa194c9ddcce8c7f9dc64ed6cd608752befa8517947`  
		Last Modified: Wed, 24 Apr 2024 17:13:01 GMT  
		Size: 71.8 MB (71816485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39bbef3dfeef70606effe4642a4e53d7c504f268aab9fd0a5fcf8c231215fe9e`  
		Last Modified: Wed, 24 Apr 2024 17:12:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da86842a3c2438b976b7e7988155da4b4b93643290ece71f79a367cc3e96e376`  
		Last Modified: Wed, 24 Apr 2024 17:13:41 GMT  
		Size: 19.0 MB (18959598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5b7cf520ed1bab8f621b1cbac2630bfcf304a6570bb69e3dab7899bca679aa`  
		Last Modified: Wed, 24 Apr 2024 17:13:29 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4bf582273aea25dd4e546bba73ad272dd851094f5edab5cd7b8bc4b01ccc8f`  
		Last Modified: Wed, 24 Apr 2024 17:13:28 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0e09010b647c74de19b8663b5cbb6f94114f2bbf94d04ddb6a93c35357a0fe`  
		Last Modified: Wed, 24 Apr 2024 17:13:32 GMT  
		Size: 12.6 MB (12591937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dec07b7ee2d0cdf3a2addb3041511acb38328707e390a6afd686559b0366fa`  
		Last Modified: Wed, 24 Apr 2024 17:13:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dad6102df65d5c0cb8ae0039ca4a4e06ceafbd80ea3ae4dde93476642bd4826`  
		Last Modified: Wed, 24 Apr 2024 17:13:36 GMT  
		Size: 10.7 MB (10689057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718c5e09e386eda71de8e74153c6d3922b392e3423c6afa20679cd3fba51d1f3`  
		Last Modified: Wed, 24 Apr 2024 17:13:26 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4df907f14244ded1e6a4425f4c6130af72ae59b6169b655691f421b14d5a14c`  
		Last Modified: Wed, 24 Apr 2024 17:13:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1d9765901ddcaab15c720d8e6aee308feb5d6a6d1a695ceb30a87460a7942c`  
		Last Modified: Wed, 24 Apr 2024 17:13:26 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; ppc64le

```console
$ docker pull php@sha256:e5f256ebd43b3c94d34a988c81816e63286ff6cd172ec47827e7977e6664b78b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167290750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6901661ff5c1fccd6fd225427deeba024a1a735df7d9c9340641d268eebdc7cb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 06:42:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 06:42:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 06:44:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 06:44:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 06:44:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 06:49:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 06:49:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 06:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 06:50:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 06:50:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 06:50:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 06:50:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 06:50:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 06:50:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Apr 2024 06:50:13 GMT
ENV PHP_VERSION=8.3.6
# Wed, 24 Apr 2024 06:50:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.6.tar.xz.asc
# Wed, 24 Apr 2024 06:50:15 GMT
ENV PHP_SHA256=53c8386b2123af97626d3438b3e4058e0c5914cb74b048a6676c57ac647f5eae
# Wed, 24 Apr 2024 06:51:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 24 Apr 2024 06:51:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:55:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 24 Apr 2024 06:55:55 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:55:58 GMT
RUN docker-php-ext-enable sodium
# Wed, 24 Apr 2024 06:55:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Apr 2024 06:55:59 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Apr 2024 06:55:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:56:00 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 06:56:01 GMT
EXPOSE 80
# Wed, 24 Apr 2024 06:56:01 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c07873e02122455a726150081e702193012035c44534913ab79b703d0c12a7`  
		Last Modified: Wed, 24 Apr 2024 08:09:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98db9297b4624835eff345693a862eff06c9da6644cfea0f59b7e71a5606b7f8`  
		Last Modified: Wed, 24 Apr 2024 08:09:53 GMT  
		Size: 86.7 MB (86654620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b506f6d7850d45a64e029acdeedecbb2e8fef3c43349902a30dc949117baa32`  
		Last Modified: Wed, 24 Apr 2024 08:09:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a742cf62927e6e727595a6ee6062e02da776af8750d9b5005e3753854bf123`  
		Last Modified: Wed, 24 Apr 2024 08:10:24 GMT  
		Size: 20.5 MB (20492624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66370b3c14d511e4c95f0243f1dbc1a44083487847c57408cfe4dbeba25bc94`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364ae8f33b6d1598c52bc7520195d695e786d076eb70b7c4fdca6eb28048e246`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93170b8458731ded7eae85aa71d2ede8b9dce1a4a606bd610af2f00b3c0cc685`  
		Last Modified: Wed, 24 Apr 2024 08:10:20 GMT  
		Size: 12.8 MB (12809693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c043b2adbdb86068cd853c1561a5317ac8b4602644da12554b96977120cb07`  
		Last Modified: Wed, 24 Apr 2024 08:10:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699465019a5145572e9161580df216e5d9a659c6d986ef782f4fca7b02ae3215`  
		Last Modified: Wed, 24 Apr 2024 08:10:19 GMT  
		Size: 12.0 MB (12016507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31024d65154e48ed38278c04862e3f9c90d51f9baac996e337c09c3329d137de`  
		Last Modified: Wed, 24 Apr 2024 08:10:17 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d226e4200044849f23424a5b3e72ce5515e1e3db4b361020f58049596bd49728`  
		Last Modified: Wed, 24 Apr 2024 08:10:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d20e355ea7d78ba9dafc9180fe6b0c83ec293b4d8a19cd9c12159561349b750`  
		Last Modified: Wed, 24 Apr 2024 08:10:17 GMT  
		Size: 897.0 B  
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
