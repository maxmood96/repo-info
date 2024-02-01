## `php:8-apache-bullseye`

```console
$ docker pull php@sha256:761c314c4a8055e7e2306a030d8ab00a943e2e46b3d2660d17fc8ac0d0a5fcdb
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
$ docker pull php@sha256:47ad0a883c25764ba538acc390e9617591a040c6de78149c6357a2e97f745893
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166667506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe5dbba8b67f803ce0323a7aaa2d7ee797ef5c8c1063e5e9eb840611f078260`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:09:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 02:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 02:09:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:09:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 02:09:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 02:13:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 02:13:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 02:13:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 02:13:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 02:13:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 02:13:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 02:13:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 02:13:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 02:13:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 02:13:26 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 02:13:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 02:13:27 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 02:13:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 02:13:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:16:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 02:16:46 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:16:46 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 02:16:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 02:16:46 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 02:16:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:16:47 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 02:16:47 GMT
EXPOSE 80
# Thu, 01 Feb 2024 02:16:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93af539c68f3289aca734c98cf6b3df63a68ef0fc67b710eca86e1335a777f3`  
		Last Modified: Thu, 01 Feb 2024 03:25:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6ca42c11e115e149faeeb3ea813cf3779b60a672c2927ce583f80fcfd866c`  
		Last Modified: Thu, 01 Feb 2024 03:26:04 GMT  
		Size: 91.6 MB (91636039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b490c454cd56fef110c8c0740ac9aea955736b87e65e6b7810e19ba6ce8056ee`  
		Last Modified: Thu, 01 Feb 2024 03:25:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93dea3841037fb7be77e49b7f614de12af951ce2ff3eb0a22af639aae4fe0e0`  
		Last Modified: Thu, 01 Feb 2024 03:26:30 GMT  
		Size: 19.3 MB (19259315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9eb303f7af8281a5f42fba6a5330898559d7fa4e99810272dce2ab4ef84f32`  
		Last Modified: Thu, 01 Feb 2024 03:26:28 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d224706905809e593a081037ab367410249bab6561d272dd1e01c4454f2575`  
		Last Modified: Thu, 01 Feb 2024 03:26:28 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c3631dccd094bf2ab932ced1333a2e0d8ce4071314e3e676854328072a73fe`  
		Last Modified: Thu, 01 Feb 2024 03:26:29 GMT  
		Size: 12.8 MB (12782386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679694036853ab2a37d4a0d401a243e1994a772712a767f2b58693982c80944b`  
		Last Modified: Thu, 01 Feb 2024 03:26:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ccf583e6d5ed1cc7923b3ccef0145109eaa8fce007c275b2ed25e228d4cc87`  
		Last Modified: Thu, 01 Feb 2024 03:26:28 GMT  
		Size: 11.6 MB (11566358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd6003c0adb04b2feb4b3e22273c7f872f8c65392bc6989b1e67f8cba104bd6`  
		Last Modified: Thu, 01 Feb 2024 03:26:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d161236ea418bcf38462611e9f7c4d684744769f3132e1e759816b2f0a57524`  
		Last Modified: Thu, 01 Feb 2024 03:26:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029de5c902760ee884ed5fa91ec1866aa7dcd5ce9c7761367eab4d1cb404909c`  
		Last Modified: Thu, 01 Feb 2024 03:26:26 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm variant v5

```console
$ docker pull php@sha256:ea8814039721c8b8484deb9b0318e547ae68828791f4cba9635415cddf3c93d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144525571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6ebd6c1be8191b3140c02c629a28f9ef189de72cd557195abd23495648f056`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:40 GMT
ADD file:1b6dd4809e22729ef9f0432014187762756f1518e85ecf13db6c505bfff65308 in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 04:31:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 04:31:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 04:31:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 04:31:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 04:31:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 04:34:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 04:34:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 04:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 04:34:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 04:34:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 04:34:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 04:34:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 04:34:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 04:34:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 04:34:46 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 04:34:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 04:34:46 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 04:35:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 04:35:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 04:37:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 04:37:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 04:37:26 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 04:37:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 04:37:27 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 04:37:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 04:37:27 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 04:37:27 GMT
EXPOSE 80
# Thu, 01 Feb 2024 04:37:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dfbf1dc0873e0cde30013d8526571f69d5c53be2b8d637a6235c623cc1f66192`  
		Last Modified: Wed, 31 Jan 2024 22:48:48 GMT  
		Size: 28.9 MB (28921333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1009ba391822779e1f869312d30401b4f3f6f5233d630d7033c877e3f0d936ff`  
		Last Modified: Thu, 01 Feb 2024 05:38:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e2fc5e2ef8b2f663258a78c132279ed058104e095dcd1b489f1fb1326fc59f`  
		Last Modified: Thu, 01 Feb 2024 05:38:31 GMT  
		Size: 73.7 MB (73689824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc8c6067613483aa73338f4e3ce525675c82f7be34141acefc5135db6d7baf`  
		Last Modified: Thu, 01 Feb 2024 05:38:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3951ffa6a1215230ebffe288756d67b0b2ab0cac19941110614d93d07e8925`  
		Last Modified: Thu, 01 Feb 2024 05:38:58 GMT  
		Size: 18.6 MB (18558786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919feac47e884cd0f313fba65e448e645e75cde9ca1a57ca456ba05eb03f9e1f`  
		Last Modified: Thu, 01 Feb 2024 05:38:55 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc8d565b7eb7128e7d84c4b211a7d688db867debed40ac5b714fe877fdd15b9`  
		Last Modified: Thu, 01 Feb 2024 05:38:55 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca469b4a749f126c91e131f1be16dfb78a17367c831392f5eaecd7fe166b1d55`  
		Last Modified: Thu, 01 Feb 2024 05:38:56 GMT  
		Size: 12.8 MB (12780785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c11014d0dd87e8ab6e622bba99f6b52f2f3f44d0e3e12c9e0fa7f102f8ad5b`  
		Last Modified: Thu, 01 Feb 2024 05:38:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354af550035a3f45423885e6b44fecd1043ba4645aaacc32470ef49f545e226`  
		Last Modified: Thu, 01 Feb 2024 05:38:56 GMT  
		Size: 10.6 MB (10569271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6500bafb39b3c72eb43bbca484445c5e793eb3df6bf58bdb6734c5879a54dd77`  
		Last Modified: Thu, 01 Feb 2024 05:38:53 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcf495ecc674f6d422b8bdbd2fc44f1849cd8e50bda9732b48b89ddd4f003fd`  
		Last Modified: Thu, 01 Feb 2024 05:38:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee101276682f8faab06514953042f36403d24d1b95671c6de88e908a26a521a2`  
		Last Modified: Thu, 01 Feb 2024 05:38:53 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:2b871da843d8bdad11596a3e2cf39093a4b58f10ba4028558baf3719f82a1473
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136713523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc6525d0a7b0221a84c4044816bc59dac9e9462789e742587b9d4c8c437d5c1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

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
# Thu, 01 Feb 2024 03:23:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 03:23:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 03:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 03:23:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 03:23:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 03:23:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 03:23:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 03:23:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 03:23:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 03:23:42 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 03:23:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 03:23:42 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 03:23:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 03:23:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:26:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 03:26:57 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:26:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 03:26:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 03:26:58 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 03:26:58 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:26:58 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 03:26:58 GMT
EXPOSE 80
# Thu, 01 Feb 2024 03:26:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb5252a47b45edd6cea077483e42a2eaed2dd0d962da76878e4f08ee0f178b8`  
		Last Modified: Thu, 01 Feb 2024 04:27:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ffeddc903db1a88b20dd08efe0235a835518390e0ea4f194e044848d1f9f72`  
		Last Modified: Thu, 01 Feb 2024 04:27:26 GMT  
		Size: 69.3 MB (69324006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6770e3000dbf2bfacda02d788f35c49745c4d61edfd5508ec224469de7832857`  
		Last Modified: Thu, 01 Feb 2024 04:27:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60d4a203414cbe1c9d41720f9aa407a03a4c2326a15f0bd7958aff95e259262`  
		Last Modified: Thu, 01 Feb 2024 04:27:54 GMT  
		Size: 18.0 MB (18017895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37814eca41a3674ddef53bd363740bfde2371b484c9c03e98eddc06711248c93`  
		Last Modified: Thu, 01 Feb 2024 04:27:51 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf43381fb9a4ed1fc224e4b4de5b62d0d8daf374964512201b4e8aa430a4684`  
		Last Modified: Thu, 01 Feb 2024 04:27:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc4ac980e631d3b8e18e904780c1b19c062cfda8f7a5bb973754a73e0b21db6`  
		Last Modified: Thu, 01 Feb 2024 04:27:51 GMT  
		Size: 12.8 MB (12780754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0d30fd963a8938fe0b4128a18f609c5cb35dda4cb1792013dcb7bd752c1ecb`  
		Last Modified: Thu, 01 Feb 2024 04:27:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e485ee696daf40ef12b92ce5ce1cb3db30d9fa87b7536430cfa4fb3ced17b1`  
		Last Modified: Thu, 01 Feb 2024 04:27:51 GMT  
		Size: 10.0 MB (10006082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31e19eadaa0779ece6c5f837d28dc81dc67d8d1299c83ab7dfa15a49146cd01`  
		Last Modified: Thu, 01 Feb 2024 04:27:48 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24a35ef0c5e1d66f4e9bdf6962a6a051313eb94302acc2b5b0306c73d5b37b3`  
		Last Modified: Thu, 01 Feb 2024 04:27:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b29cb49ccad27bc7fe6583e0eee877c784cb5db1ca2e4b1f8a14984615c1d3c`  
		Last Modified: Thu, 01 Feb 2024 04:27:49 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:a3e43011073c05e0ccccf4c496fd008bfedf29ef60b2f4f53b5dbb6417f043e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160602066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099ccbb610056b381295baf87a16f512b6366b3bbaa0fbbf0abadc4649ef8398`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:48:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 01:48:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 01:48:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:48:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 01:48:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 01:52:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 01:52:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 01:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 01:52:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 01:52:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 01:52:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:52:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:52:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 01:52:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 01:52:25 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 01:52:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 01:52:25 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 01:52:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 01:52:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 01:55:50 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:55:50 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 01:55:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 01:55:50 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 01:55:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:55:50 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 01:55:51 GMT
EXPOSE 80
# Thu, 01 Feb 2024 01:55:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0095e84c689069912e39e21cbc8e79d2c1bff8a09bcb34d118ae85228c9d40`  
		Last Modified: Thu, 01 Feb 2024 03:01:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6986ebd90295f3b6731e740dcbb82f20aad68502bf93d4c683bbc5728870aa6a`  
		Last Modified: Thu, 01 Feb 2024 03:01:56 GMT  
		Size: 86.9 MB (86934871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af71ccbb52bffbdd1509bfe4c824c6ae8ed2bc864e487aabb7aa4ebc183a0d8`  
		Last Modified: Thu, 01 Feb 2024 03:01:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6757d426215a84aa6104723778037e9c964bd13caa06be0e1221cd9189787b8`  
		Last Modified: Thu, 01 Feb 2024 03:02:23 GMT  
		Size: 19.2 MB (19177661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d51ccc86bdbb69fb78528fd0f650d52dc7e61893179c525b3ffc09a617d1d8`  
		Last Modified: Thu, 01 Feb 2024 03:02:20 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137e11d4ede4a2fb580b0a551ea2d09671470fd198f3f3ce8167ee7cfa90317f`  
		Last Modified: Thu, 01 Feb 2024 03:02:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf99c5322a91c48cef859f753f25222f0534e66bd9eb491e54ee6eb02bf7383`  
		Last Modified: Thu, 01 Feb 2024 03:02:21 GMT  
		Size: 12.8 MB (12781645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10379ca18f6e016cbd43da8b520d450c43c05539e3cef9785aed84007adf5c85`  
		Last Modified: Thu, 01 Feb 2024 03:02:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f8baa63b296d1069186cff2d77066767a4578b346c01ba8162041a8dfdc19`  
		Last Modified: Thu, 01 Feb 2024 03:02:20 GMT  
		Size: 11.6 MB (11637981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab54fcdbbe8ef87ae1cdb2e1fc6e2fb652148eb64db46ab13642c6f9e7d73a21`  
		Last Modified: Thu, 01 Feb 2024 03:02:18 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293fc63edf00d8cd16a39f7ca030753c26c5c990a53d24b7db883eb44259ac25`  
		Last Modified: Thu, 01 Feb 2024 03:02:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7dd6a937ccd33e1899dfe6cd592bc89f4c32bf066f1b07c871498dacb344fc2`  
		Last Modified: Thu, 01 Feb 2024 03:02:18 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; 386

```console
$ docker pull php@sha256:c82d536c0c8f8c4df42852a91fd69375b72e2c0f21b177665601ace14f44785e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169450898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3b27b7ce7fa3c35f90c313746676f74c5f2a6caf90854a0dfb04c9cfd78ec0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:23 GMT
ADD file:0e0961062de8ea0706118b883ee7638aae4465761dec06896f1bd28b9fb4b516 in / 
# Wed, 31 Jan 2024 22:39:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 08:56:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 08:56:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 08:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 08:56:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 08:56:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 09:02:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 09:02:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 09:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 09:02:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 09:02:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 09:02:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 09:02:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 09:02:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 09:02:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 09:02:40 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 09:02:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 09:02:40 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 09:02:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 09:02:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 09:08:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 09:08:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 09:08:26 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 09:08:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 09:08:27 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 09:08:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 09:08:27 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 09:08:27 GMT
EXPOSE 80
# Thu, 01 Feb 2024 09:08:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:854acbf4b2df9e625a11c0e67025dce58b41d948bb7e5d4d5e708e25489f6e8f`  
		Last Modified: Wed, 31 Jan 2024 22:44:37 GMT  
		Size: 32.4 MB (32402507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed64bc5ddce33e4406d9bb826cb4ab438fc22768e1a3e45d7bb45b84194e849`  
		Last Modified: Thu, 01 Feb 2024 11:02:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b6977c751ef8fff383fefa2b351db168a2f2c3633f7ebbd1cad7952b67a200`  
		Last Modified: Thu, 01 Feb 2024 11:02:45 GMT  
		Size: 92.7 MB (92726633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ef7c38a3381053790edc36f6505376417ce43de87e2013bb30cdc099f0021d`  
		Last Modified: Thu, 01 Feb 2024 11:02:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648dfcca603c5f93dc593bd9bd21260ebe4f1a711e470ec51fb49060e7507810`  
		Last Modified: Thu, 01 Feb 2024 11:03:15 GMT  
		Size: 19.7 MB (19745403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6611a7471604d2aaae58e1b1d994cad970884ae04da9b4c0b1c089baa311f4ef`  
		Last Modified: Thu, 01 Feb 2024 11:03:10 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37edd7bacd364e1d8c63381c12e7fcc89c605ee09d5bd87d4c2cb6e5ddcd6b8d`  
		Last Modified: Thu, 01 Feb 2024 11:03:10 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20bc4232a506d14feddcea01efd70b7abe41470e6f87ffc7525f62e85349872`  
		Last Modified: Thu, 01 Feb 2024 11:03:12 GMT  
		Size: 12.8 MB (12781656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3662a14762893445429f2b12658a30e15fd69b21158c45c70cb390f07a990a96`  
		Last Modified: Thu, 01 Feb 2024 11:03:08 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d725e9fa394b923bf90a40b8d68ed3b469b4ae98bcc6cb141e94666fa10f704`  
		Last Modified: Thu, 01 Feb 2024 11:03:12 GMT  
		Size: 11.8 MB (11789124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0391f875c4f2058050debf40dd109d66725e1e47f1763befd499746add293463`  
		Last Modified: Thu, 01 Feb 2024 11:03:08 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c91d944ab7d946c1c4ce5df402e0a83e639d7dceade83dc58b4d8c879105218`  
		Last Modified: Thu, 01 Feb 2024 11:03:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f26063e503c99282bc79d83a51802540d321b4a0e4870b203e4f0aec266ee4c`  
		Last Modified: Thu, 01 Feb 2024 11:03:08 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; mips64le

```console
$ docker pull php@sha256:4ca97a29c8e1d1f3e3dc92c7d52c5d84b808eee14a3c0114dbbf4f9af03f06e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143658702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943f88316d5c445a22d42b064e4e11a86553f1a87ccb779e55c71edd503100c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:28:28 GMT
ADD file:c74d2ef293040606b9450e82efd37b5ef0dc7ba25160e7762da18e804abd6338 in / 
# Wed, 31 Jan 2024 22:28:33 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:26:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 00:26:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 00:28:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:28:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 00:28:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 00:43:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 00:43:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 00:44:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 00:44:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 00:44:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 00:44:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 00:44:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 00:44:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 00:44:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 00:45:02 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 00:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 00:45:09 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 00:45:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 00:45:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 01:00:14 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:00:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 01:00:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 01:00:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 01:00:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:00:35 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 01:00:39 GMT
EXPOSE 80
# Thu, 01 Feb 2024 01:00:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:231db420c5b3972aa42bcdfd7a71d4d6d22f911ebd5b7ed62d957cef65d0dddf`  
		Last Modified: Wed, 31 Jan 2024 22:39:47 GMT  
		Size: 29.6 MB (29636258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f955f0ffc39b95dac62b4e7d2492d80a82e545345bc0b9dc464a02392ea50f`  
		Last Modified: Thu, 01 Feb 2024 05:36:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5204a203c0471080d92c43833fd8c10bca0a6b82f9272947816b77c9b8f80e5`  
		Last Modified: Thu, 01 Feb 2024 05:37:38 GMT  
		Size: 71.8 MB (71815129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a387836f539547b6af5fea1a6863ef3cec958bda21fb184bf084bcceb23e4615`  
		Last Modified: Thu, 01 Feb 2024 05:36:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08fe981349239bf9f5c54063e1620cb1e0d8ace4626a566c8f9a3b1c7787dc7`  
		Last Modified: Thu, 01 Feb 2024 05:38:18 GMT  
		Size: 19.0 MB (18955444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f724ac56a4003e47abde846296092d9cbc375e1c5d6fa584166ae2a7b549c`  
		Last Modified: Thu, 01 Feb 2024 05:38:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb40655ca2a553d3cb6b5c8a05295eadb12027c68ce5da064bab3148c957693`  
		Last Modified: Thu, 01 Feb 2024 05:38:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809af4a44eaae1b7b29d04bbaccc170941a07add2f56b3b4f1e9e6b40ef42f97`  
		Last Modified: Thu, 01 Feb 2024 05:38:09 GMT  
		Size: 12.6 MB (12563673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ed095f1002bfc263f378034a9a524c5b2e5fb6d1f1806982ae683a4806889d`  
		Last Modified: Thu, 01 Feb 2024 05:38:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f4d6da2e912c5af21d18976df6e4f95e24c274d3974a56e407ebe9a28066bf`  
		Last Modified: Thu, 01 Feb 2024 05:38:13 GMT  
		Size: 10.7 MB (10682720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d997d1436679c892391cb88b2839aedb346b104c2ab500ba6fe7ed514fbc483c`  
		Last Modified: Thu, 01 Feb 2024 05:38:03 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f798048af7353593cdf2e8f57a13de41db0fe1827ea43db5428e9145d8d74f`  
		Last Modified: Thu, 01 Feb 2024 05:38:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c9eb4a2b485605b7fb6e08f30ea6ce78dfe82c504cacfb179217b8bc8fcbe3`  
		Last Modified: Thu, 01 Feb 2024 05:38:03 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; ppc64le

```console
$ docker pull php@sha256:a59b16aff8802ac0af31c200120cbc60e1ce8994c4f39426a88f4bd5761628ab
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167212129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ff7bcaf4f28f8b1dba808564dce6a792b8dbbfeded1d27d91ab64e23e187d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:11 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 31 Jan 2024 22:30:14 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:32:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 01:32:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 01:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:33:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 01:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 01:37:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 01:37:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 01:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 01:38:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 01:38:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 01:38:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:38:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:38:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 01:38:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 01:38:09 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 01:38:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 01:38:10 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 01:38:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 01:38:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:42:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 01:43:00 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:43:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 01:43:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 01:43:03 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 01:43:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:43:04 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 01:43:05 GMT
EXPOSE 80
# Thu, 01 Feb 2024 01:43:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8bc6e59d55fc787f96bd3b10786ec8dca5276fff391e368e70b15e21b5f765`  
		Last Modified: Thu, 01 Feb 2024 02:52:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ef8b25843b3d0d4ab364efb516594e28ce1fd99eafceff7d344553b4b17ee9`  
		Last Modified: Thu, 01 Feb 2024 02:53:01 GMT  
		Size: 86.6 MB (86643839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058b6c2377df2b7efd955cef8971b6de1d8de7a13cb66c4219867e959adbcc74`  
		Last Modified: Thu, 01 Feb 2024 02:52:45 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452826efa9cb6de712449b90e425454e46235b83f8846fc714fc1805b5cd5257`  
		Last Modified: Thu, 01 Feb 2024 02:53:32 GMT  
		Size: 20.5 MB (20474992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fc5574efa5a8e62394bfd47ac769a290feeff7835497f359e483e9aab44e1d`  
		Last Modified: Thu, 01 Feb 2024 02:53:29 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fa49325f634c7278fb729abcf19ba5876f2a435dbbf4854996545baf145540`  
		Last Modified: Thu, 01 Feb 2024 02:53:29 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c13a26f12d6e99b3ff72b3b2c6531cda23756a5c3225933e81a0a74e0e8860`  
		Last Modified: Thu, 01 Feb 2024 02:53:30 GMT  
		Size: 12.8 MB (12782325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff4f0267db86e638d3cc94d8d171a47095466f3522f0c6736cf77a8192cadbb`  
		Last Modified: Thu, 01 Feb 2024 02:53:27 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030a5b63f9a01b7213bb21f73684f6b2626f21849701418e34dc3a62d0223e6b`  
		Last Modified: Thu, 01 Feb 2024 02:53:29 GMT  
		Size: 12.0 MB (12011737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb500ca1340db9018fdae53dbf87d2750ab028fa7e56049f7316ee7b9785911`  
		Last Modified: Thu, 01 Feb 2024 02:53:27 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a78d7247e4609acfebe49ace675b4f59f135a6f7e99f349a59da69e74b268c6`  
		Last Modified: Thu, 01 Feb 2024 02:53:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4b254c1f3c591db4d2dc59b209a9e20cc6f7d1642fd27e8c592ab974ccd4a8`  
		Last Modified: Thu, 01 Feb 2024 02:53:27 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:8-apache-bullseye` - linux; s390x

```console
$ docker pull php@sha256:519ebcdd370203ea0a5f805f608ac91db664bde52e660815b44d09816e1e8d83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143821852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed783115994d0b5acfedc6c29245375e01dd11c8d4ea986c84f123d17a34fb1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

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
# Thu, 01 Feb 2024 01:39:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 01:39:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 01:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 01:40:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 01:40:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 01:40:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:40:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:40:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 01:40:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Feb 2024 01:40:08 GMT
ENV PHP_VERSION=8.3.2
# Thu, 01 Feb 2024 01:40:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Thu, 01 Feb 2024 01:40:08 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Thu, 01 Feb 2024 01:40:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 01:40:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:42:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 01:42:34 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:42:34 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 01:42:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 01:42:35 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 01:42:35 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:42:35 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 01:42:35 GMT
EXPOSE 80
# Thu, 01 Feb 2024 01:42:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:16651f5430ff52661c6729a9dc23c80d76205b6bd77d7730f38e39aca6731613`  
		Last Modified: Wed, 31 Jan 2024 23:29:40 GMT  
		Size: 29.7 MB (29657133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b97bcdc3dc03347191b2f148550b53e7ce76a72235d37dc7001b942384b221`  
		Last Modified: Thu, 01 Feb 2024 03:19:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1f72c1803ab9a6c0542c03e8fabed985787369cf715831e9538f5e2d97cdd6`  
		Last Modified: Thu, 01 Feb 2024 03:20:07 GMT  
		Size: 71.6 MB (71635450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226493a3fefc8dddf4a852e076cc2dfd6981203493af7f6cdf8dd95f111468e`  
		Last Modified: Thu, 01 Feb 2024 03:19:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78290616c4fed9bf617b5b980c012b25819e3f28a8cc0d1394f22706bf691d7f`  
		Last Modified: Thu, 01 Feb 2024 03:20:29 GMT  
		Size: 19.1 MB (19080565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7071dc8a1fa4a43730782bfde86fca511f5ab630af3d1d51d5cef61cfdee6a83`  
		Last Modified: Thu, 01 Feb 2024 03:20:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419336e10a15f63e206ca9e925037a7459d467b8bb55a1ea31550c754527430a`  
		Last Modified: Thu, 01 Feb 2024 03:20:25 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c4ad85472ae50a89c1526e87fc5fae90f44de96fa7eb7a3fdba0ca3011581`  
		Last Modified: Thu, 01 Feb 2024 03:20:26 GMT  
		Size: 12.8 MB (12781218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8f598b73ff9fb49464b6316bd70c67d011e08eb50b3c9db37c55ae1b841b29`  
		Last Modified: Thu, 01 Feb 2024 03:20:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eed10414f41fdfc63c76d363185d27b1adba13287dbcd0f85552ad7352f349`  
		Last Modified: Thu, 01 Feb 2024 03:20:26 GMT  
		Size: 10.7 MB (10661912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff7f67cc98aec37b08bdf4d282c0dfe533257ad1a8703542c7e4a75fc11508d`  
		Last Modified: Thu, 01 Feb 2024 03:20:24 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6375f3d2fa796f9933db7fa96daf33846719700fe079dad4f5227ba84e31e9`  
		Last Modified: Thu, 01 Feb 2024 03:20:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe43c5394f4fe7c40bfe1a92a2834ce5d37f9394c87c70f2b91804332120f2a`  
		Last Modified: Thu, 01 Feb 2024 03:20:24 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
