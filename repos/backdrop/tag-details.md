<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.29`](#backdrop129)
-	[`backdrop:1.29-apache`](#backdrop129-apache)
-	[`backdrop:1.29-fpm`](#backdrop129-fpm)
-	[`backdrop:1.29.1`](#backdrop1291)
-	[`backdrop:1.29.1-apache`](#backdrop1291-apache)
-	[`backdrop:1.29.1-fpm`](#backdrop1291-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:65b5649c4ee394f121c7c5e0b15000ee34325ae73742778ac66e571c3e86b4aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b003e7677af4024c0fbcda84d8d3468636fa3ea7a6bca30e21736972066f685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183656791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a4db2b6dac4980f87ecaa43a3e8e3f2261d69afeac1b191cda7b2213b424b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eef2a5dc1b65f7c6c1d52bc33548c51ee34d74d7977c2cf79eab50fd8e47e7c`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 12.0 MB (12045040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969b38e145fa3c5e6eedc74525f1fc87a11a71371d0468f94183fa2d4a81ca8`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549affc734ea0c201087ba0b480b836b4b13245bfc9a1ecc9d5bd9b23be8c874`  
		Last Modified: Wed, 25 Dec 2024 00:38:34 GMT  
		Size: 11.2 MB (11157613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f694155e8bbb56ba3a9bc887400639c9e32b7c7a6df4d028562f9325f7cab`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa796aa5b34ed7565fe846b39b5a89626061244a73e95329edea98ea93c3825`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b475d415794f60fdf9b34581e3e7051ff4c67bc0d16bbdd32b27e64f1a959b`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed877f7b2e77705fec0a1ac55216df654eae2a35fc1a491bddbf67354e0021`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e694b1c845e150c50d2100bef6cef5b4b081dad8b811c5d654d21031708b45c1`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 5.5 MB (5526340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff138a25e5c5b847589ed1e2924839db5bb8082778fb44cbd26b1d34ee172807`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3118ed6eef12e645866fe3abc49825b641203bf9c9eb9cdd3fb8d7bf9c88fa`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:734976c4ab72936702df0a36911ebcabb0816804e1ae1e7e2b7e9f17b2a2854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda19a9ded352c2f86922d0e9e88a204ceb468b5ce5483db22e8036a2a7143da`

```dockerfile
```

-	Layers:
	-	`sha256:480b17067542ed61f8d3c50a12c5d11aa7731634f1efda148e4377f4f34be2dc`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 7.0 MB (6968735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbb377a9ab5d90f4dc835e7a4fa61b8f9eea190c99e1d46258f0cd893dd7a5e`  
		Last Modified: Wed, 25 Dec 2024 08:09:50 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:65b5649c4ee394f121c7c5e0b15000ee34325ae73742778ac66e571c3e86b4aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b003e7677af4024c0fbcda84d8d3468636fa3ea7a6bca30e21736972066f685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183656791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a4db2b6dac4980f87ecaa43a3e8e3f2261d69afeac1b191cda7b2213b424b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eef2a5dc1b65f7c6c1d52bc33548c51ee34d74d7977c2cf79eab50fd8e47e7c`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 12.0 MB (12045040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969b38e145fa3c5e6eedc74525f1fc87a11a71371d0468f94183fa2d4a81ca8`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549affc734ea0c201087ba0b480b836b4b13245bfc9a1ecc9d5bd9b23be8c874`  
		Last Modified: Wed, 25 Dec 2024 00:38:34 GMT  
		Size: 11.2 MB (11157613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f694155e8bbb56ba3a9bc887400639c9e32b7c7a6df4d028562f9325f7cab`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa796aa5b34ed7565fe846b39b5a89626061244a73e95329edea98ea93c3825`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b475d415794f60fdf9b34581e3e7051ff4c67bc0d16bbdd32b27e64f1a959b`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed877f7b2e77705fec0a1ac55216df654eae2a35fc1a491bddbf67354e0021`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e694b1c845e150c50d2100bef6cef5b4b081dad8b811c5d654d21031708b45c1`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 5.5 MB (5526340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff138a25e5c5b847589ed1e2924839db5bb8082778fb44cbd26b1d34ee172807`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3118ed6eef12e645866fe3abc49825b641203bf9c9eb9cdd3fb8d7bf9c88fa`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:734976c4ab72936702df0a36911ebcabb0816804e1ae1e7e2b7e9f17b2a2854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda19a9ded352c2f86922d0e9e88a204ceb468b5ce5483db22e8036a2a7143da`

```dockerfile
```

-	Layers:
	-	`sha256:480b17067542ed61f8d3c50a12c5d11aa7731634f1efda148e4377f4f34be2dc`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 7.0 MB (6968735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbb377a9ab5d90f4dc835e7a4fa61b8f9eea190c99e1d46258f0cd893dd7a5e`  
		Last Modified: Wed, 25 Dec 2024 08:09:50 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:639d6242e9f5a0076fa4e9f63ee9d44c3fa3a36e9392d0c6fd67712c21879573
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:4ce338bb1450acc6becdde36c67333e6280877d9d13edd79fa52a1d3eed29ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188353897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0611eed914d02bdf13e31d75676db805316571d643e9f68add5286c4088d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa37e3d8d9dcd6652d9cfd093b3facbefb8d2afa95e4bbda6eef2d87418a7f`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803a18903b97b0fb167b6eaa28c2d0b4358f4af1aabb5aef4396d405bf00047`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 104.2 MB (104150634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a6188a92ffa96d9eabbb7e7400ada69c0639362bfc9edf71f574bf5861bff7`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a8edea7242cc170995ed60f1c008487fec0c7cf7360cca6c85359bac07d3a`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 12.6 MB (12634164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcd1b4fbab1974d1b94965cd7219e2e4ee5fe189a1b75407b804619b3592f99`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72131e6f22a2ea7ce1ba1bb295248168d2b9884cf7d230b4b89fc2482363f767`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 27.8 MB (27824660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e766504f27d3db1dd34280ddcbf990ac28efc311bacd9de08f70b0132c6a5bb3`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da02540269ec11780285b616e26ba332d5b9f40a9d06c2d2843c45dad8e9d2`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5dd1ad3cce0d4e65a5297dce3006592ea56ed41413c80ce5410c260ad6b1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faad1d3c8355712d9f34e3b2ce980e10a5153cdf206aef76436ff82081f46bf`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 5.6 MB (5587661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66402df32985bd1de3199dda2bd56494b83a7828c025d9f5aee68a138bce2976`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 9.9 MB (9911386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683e9e86f1db5e68d632557d7e3dd7283a6cba2973beeeb35466859f4cafe71`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:30736a3da3f8d79441f95fff1b678eb3764457fcb5e95eb50c284f4b12441ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c30c70b3819d322b1bc6fe4673bfd2a2dc4cb5ed52c1e449c87aac65f0173a5`

```dockerfile
```

-	Layers:
	-	`sha256:c7961a4f11ea2dda1476ef8af0b7a1660a643bc082682a54e9b93cde54e7cdfe`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 6.4 MB (6429770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655a177be6b5b818c61b17981d87b418299815db84b24202f166841ca67116f0`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:67caca0374960d2843c3e5d431fdeabbb0c0377e80b13dd07f701781536c95d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179648488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0236e603909870e91420c785b8c86b8664a7d9c8f788e0799d91796d7e09ebff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ddf54116a48086ac347acbc8cda41c60bf1047d4855e10736738d43190aa9f`  
		Last Modified: Wed, 25 Dec 2024 00:34:31 GMT  
		Size: 12.0 MB (12026443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf71636a2f00adbd95976a6331c62bbca8f9de224699aa66ef1d3ea209e6e4`  
		Last Modified: Wed, 25 Dec 2024 00:34:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4391c8e54be1601e72f28b7809fe0ad0045e5fcf3896dd40049624839a76d6`  
		Last Modified: Wed, 25 Dec 2024 00:42:23 GMT  
		Size: 27.3 MB (27278762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860da53d1b8319cfe047c744038092722ccbce4acd39842f29091fc4daf7681`  
		Last Modified: Wed, 25 Dec 2024 00:42:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abf51b8b870f39bbae4db83a61d349272ebc437916a8a6a28f7f91149c0982d`  
		Last Modified: Wed, 25 Dec 2024 00:42:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a96243ed3cfc5796ed4e6464f235196608ea49db0013c22d69c09f965ff5a8`  
		Last Modified: Wed, 25 Dec 2024 00:42:22 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742cbe9d9784250c7f6ddfca7048b4eb3ddded504fbb13cd771eb575071892d`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 5.5 MB (5529627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118622c90eb72e00381d4b00c0d9553c14f7d6ae8118d220d85d3556e83e7081`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ec892150962167dba7d71d543f958a0bf40701a5ae58db1652d755762e0d24`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:4035652de5d2e9ad3339914bec259adca56a215957fd49576057243e60ca56d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9587f3b4bc6bbf09fba2c8e9a8830c69c06492d1ee01b017ba01f7a064d31fd4`

```dockerfile
```

-	Layers:
	-	`sha256:fb6c252dbe4ea833252dda54fc2112612673c417b50fcdf43a2d74689f991020`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 6.5 MB (6458186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fe47c998d7cda12ac60ab77a48c08ac91810247c1243eca5942377359731f6`  
		Last Modified: Wed, 25 Dec 2024 08:11:10 GMT  
		Size: 21.7 KB (21683 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.29`

```console
$ docker pull backdrop@sha256:bc411546d7ac695c60731fa8b23aee49d1be07bc1c3bbd8f8b46f50dd7b4915b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `backdrop:1.29` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.29` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.29-apache`

```console
$ docker pull backdrop@sha256:bc411546d7ac695c60731fa8b23aee49d1be07bc1c3bbd8f8b46f50dd7b4915b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `backdrop:1.29-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.29-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.29-fpm`

```console
$ docker pull backdrop@sha256:df7dadcdf7fd745e1ef59f5b4be5725259d6fecd7081b68b527bb4d552c48591
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `backdrop:1.29-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:4ce338bb1450acc6becdde36c67333e6280877d9d13edd79fa52a1d3eed29ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188353897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0611eed914d02bdf13e31d75676db805316571d643e9f68add5286c4088d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa37e3d8d9dcd6652d9cfd093b3facbefb8d2afa95e4bbda6eef2d87418a7f`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803a18903b97b0fb167b6eaa28c2d0b4358f4af1aabb5aef4396d405bf00047`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 104.2 MB (104150634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a6188a92ffa96d9eabbb7e7400ada69c0639362bfc9edf71f574bf5861bff7`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a8edea7242cc170995ed60f1c008487fec0c7cf7360cca6c85359bac07d3a`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 12.6 MB (12634164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcd1b4fbab1974d1b94965cd7219e2e4ee5fe189a1b75407b804619b3592f99`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72131e6f22a2ea7ce1ba1bb295248168d2b9884cf7d230b4b89fc2482363f767`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 27.8 MB (27824660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e766504f27d3db1dd34280ddcbf990ac28efc311bacd9de08f70b0132c6a5bb3`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da02540269ec11780285b616e26ba332d5b9f40a9d06c2d2843c45dad8e9d2`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5dd1ad3cce0d4e65a5297dce3006592ea56ed41413c80ce5410c260ad6b1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faad1d3c8355712d9f34e3b2ce980e10a5153cdf206aef76436ff82081f46bf`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 5.6 MB (5587661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66402df32985bd1de3199dda2bd56494b83a7828c025d9f5aee68a138bce2976`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 9.9 MB (9911386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683e9e86f1db5e68d632557d7e3dd7283a6cba2973beeeb35466859f4cafe71`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.29-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:30736a3da3f8d79441f95fff1b678eb3764457fcb5e95eb50c284f4b12441ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c30c70b3819d322b1bc6fe4673bfd2a2dc4cb5ed52c1e449c87aac65f0173a5`

```dockerfile
```

-	Layers:
	-	`sha256:c7961a4f11ea2dda1476ef8af0b7a1660a643bc082682a54e9b93cde54e7cdfe`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 6.4 MB (6429770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655a177be6b5b818c61b17981d87b418299815db84b24202f166841ca67116f0`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.29.1`

```console
$ docker pull backdrop@sha256:bc411546d7ac695c60731fa8b23aee49d1be07bc1c3bbd8f8b46f50dd7b4915b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `backdrop:1.29.1` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.29.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.29.1-apache`

```console
$ docker pull backdrop@sha256:bc411546d7ac695c60731fa8b23aee49d1be07bc1c3bbd8f8b46f50dd7b4915b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `backdrop:1.29.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.29.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.29.1-fpm`

```console
$ docker pull backdrop@sha256:df7dadcdf7fd745e1ef59f5b4be5725259d6fecd7081b68b527bb4d552c48591
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `backdrop:1.29.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:4ce338bb1450acc6becdde36c67333e6280877d9d13edd79fa52a1d3eed29ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188353897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0611eed914d02bdf13e31d75676db805316571d643e9f68add5286c4088d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa37e3d8d9dcd6652d9cfd093b3facbefb8d2afa95e4bbda6eef2d87418a7f`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803a18903b97b0fb167b6eaa28c2d0b4358f4af1aabb5aef4396d405bf00047`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 104.2 MB (104150634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a6188a92ffa96d9eabbb7e7400ada69c0639362bfc9edf71f574bf5861bff7`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a8edea7242cc170995ed60f1c008487fec0c7cf7360cca6c85359bac07d3a`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 12.6 MB (12634164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcd1b4fbab1974d1b94965cd7219e2e4ee5fe189a1b75407b804619b3592f99`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72131e6f22a2ea7ce1ba1bb295248168d2b9884cf7d230b4b89fc2482363f767`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 27.8 MB (27824660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e766504f27d3db1dd34280ddcbf990ac28efc311bacd9de08f70b0132c6a5bb3`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da02540269ec11780285b616e26ba332d5b9f40a9d06c2d2843c45dad8e9d2`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5dd1ad3cce0d4e65a5297dce3006592ea56ed41413c80ce5410c260ad6b1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faad1d3c8355712d9f34e3b2ce980e10a5153cdf206aef76436ff82081f46bf`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 5.6 MB (5587661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66402df32985bd1de3199dda2bd56494b83a7828c025d9f5aee68a138bce2976`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 9.9 MB (9911386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683e9e86f1db5e68d632557d7e3dd7283a6cba2973beeeb35466859f4cafe71`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.29.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:30736a3da3f8d79441f95fff1b678eb3764457fcb5e95eb50c284f4b12441ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c30c70b3819d322b1bc6fe4673bfd2a2dc4cb5ed52c1e449c87aac65f0173a5`

```dockerfile
```

-	Layers:
	-	`sha256:c7961a4f11ea2dda1476ef8af0b7a1660a643bc082682a54e9b93cde54e7cdfe`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 6.4 MB (6429770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655a177be6b5b818c61b17981d87b418299815db84b24202f166841ca67116f0`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:65b5649c4ee394f121c7c5e0b15000ee34325ae73742778ac66e571c3e86b4aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b003e7677af4024c0fbcda84d8d3468636fa3ea7a6bca30e21736972066f685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183656791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a4db2b6dac4980f87ecaa43a3e8e3f2261d69afeac1b191cda7b2213b424b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eef2a5dc1b65f7c6c1d52bc33548c51ee34d74d7977c2cf79eab50fd8e47e7c`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 12.0 MB (12045040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969b38e145fa3c5e6eedc74525f1fc87a11a71371d0468f94183fa2d4a81ca8`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549affc734ea0c201087ba0b480b836b4b13245bfc9a1ecc9d5bd9b23be8c874`  
		Last Modified: Wed, 25 Dec 2024 00:38:34 GMT  
		Size: 11.2 MB (11157613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f694155e8bbb56ba3a9bc887400639c9e32b7c7a6df4d028562f9325f7cab`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa796aa5b34ed7565fe846b39b5a89626061244a73e95329edea98ea93c3825`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b475d415794f60fdf9b34581e3e7051ff4c67bc0d16bbdd32b27e64f1a959b`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed877f7b2e77705fec0a1ac55216df654eae2a35fc1a491bddbf67354e0021`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e694b1c845e150c50d2100bef6cef5b4b081dad8b811c5d654d21031708b45c1`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 5.5 MB (5526340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff138a25e5c5b847589ed1e2924839db5bb8082778fb44cbd26b1d34ee172807`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3118ed6eef12e645866fe3abc49825b641203bf9c9eb9cdd3fb8d7bf9c88fa`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:734976c4ab72936702df0a36911ebcabb0816804e1ae1e7e2b7e9f17b2a2854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda19a9ded352c2f86922d0e9e88a204ceb468b5ce5483db22e8036a2a7143da`

```dockerfile
```

-	Layers:
	-	`sha256:480b17067542ed61f8d3c50a12c5d11aa7731634f1efda148e4377f4f34be2dc`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 7.0 MB (6968735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbb377a9ab5d90f4dc835e7a4fa61b8f9eea190c99e1d46258f0cd893dd7a5e`  
		Last Modified: Wed, 25 Dec 2024 08:09:50 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:639d6242e9f5a0076fa4e9f63ee9d44c3fa3a36e9392d0c6fd67712c21879573
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:4ce338bb1450acc6becdde36c67333e6280877d9d13edd79fa52a1d3eed29ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188353897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0611eed914d02bdf13e31d75676db805316571d643e9f68add5286c4088d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["php-fpm"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aa37e3d8d9dcd6652d9cfd093b3facbefb8d2afa95e4bbda6eef2d87418a7f`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803a18903b97b0fb167b6eaa28c2d0b4358f4af1aabb5aef4396d405bf00047`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 104.2 MB (104150634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a6188a92ffa96d9eabbb7e7400ada69c0639362bfc9edf71f574bf5861bff7`  
		Last Modified: Tue, 24 Dec 2024 22:25:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a8edea7242cc170995ed60f1c008487fec0c7cf7360cca6c85359bac07d3a`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 12.6 MB (12634164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcd1b4fbab1974d1b94965cd7219e2e4ee5fe189a1b75407b804619b3592f99`  
		Last Modified: Tue, 24 Dec 2024 22:25:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72131e6f22a2ea7ce1ba1bb295248168d2b9884cf7d230b4b89fc2482363f767`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 27.8 MB (27824660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e766504f27d3db1dd34280ddcbf990ac28efc311bacd9de08f70b0132c6a5bb3`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da02540269ec11780285b616e26ba332d5b9f40a9d06c2d2843c45dad8e9d2`  
		Last Modified: Tue, 24 Dec 2024 22:25:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5dd1ad3cce0d4e65a5297dce3006592ea56ed41413c80ce5410c260ad6b1a6`  
		Last Modified: Tue, 24 Dec 2024 22:25:20 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faad1d3c8355712d9f34e3b2ce980e10a5153cdf206aef76436ff82081f46bf`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 5.6 MB (5587661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66402df32985bd1de3199dda2bd56494b83a7828c025d9f5aee68a138bce2976`  
		Last Modified: Wed, 08 Jan 2025 23:32:44 GMT  
		Size: 9.9 MB (9911386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683e9e86f1db5e68d632557d7e3dd7283a6cba2973beeeb35466859f4cafe71`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:30736a3da3f8d79441f95fff1b678eb3764457fcb5e95eb50c284f4b12441ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c30c70b3819d322b1bc6fe4673bfd2a2dc4cb5ed52c1e449c87aac65f0173a5`

```dockerfile
```

-	Layers:
	-	`sha256:c7961a4f11ea2dda1476ef8af0b7a1660a643bc082682a54e9b93cde54e7cdfe`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 6.4 MB (6429770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655a177be6b5b818c61b17981d87b418299815db84b24202f166841ca67116f0`  
		Last Modified: Wed, 08 Jan 2025 23:32:43 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:67caca0374960d2843c3e5d431fdeabbb0c0377e80b13dd07f701781536c95d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179648488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0236e603909870e91420c785b8c86b8664a7d9c8f788e0799d91796d7e09ebff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ddf54116a48086ac347acbc8cda41c60bf1047d4855e10736738d43190aa9f`  
		Last Modified: Wed, 25 Dec 2024 00:34:31 GMT  
		Size: 12.0 MB (12026443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf71636a2f00adbd95976a6331c62bbca8f9de224699aa66ef1d3ea209e6e4`  
		Last Modified: Wed, 25 Dec 2024 00:34:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4391c8e54be1601e72f28b7809fe0ad0045e5fcf3896dd40049624839a76d6`  
		Last Modified: Wed, 25 Dec 2024 00:42:23 GMT  
		Size: 27.3 MB (27278762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860da53d1b8319cfe047c744038092722ccbce4acd39842f29091fc4daf7681`  
		Last Modified: Wed, 25 Dec 2024 00:42:22 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abf51b8b870f39bbae4db83a61d349272ebc437916a8a6a28f7f91149c0982d`  
		Last Modified: Wed, 25 Dec 2024 00:42:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a96243ed3cfc5796ed4e6464f235196608ea49db0013c22d69c09f965ff5a8`  
		Last Modified: Wed, 25 Dec 2024 00:42:22 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742cbe9d9784250c7f6ddfca7048b4eb3ddded504fbb13cd771eb575071892d`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 5.5 MB (5529627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118622c90eb72e00381d4b00c0d9553c14f7d6ae8118d220d85d3556e83e7081`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ec892150962167dba7d71d543f958a0bf40701a5ae58db1652d755762e0d24`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:4035652de5d2e9ad3339914bec259adca56a215957fd49576057243e60ca56d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9587f3b4bc6bbf09fba2c8e9a8830c69c06492d1ee01b017ba01f7a064d31fd4`

```dockerfile
```

-	Layers:
	-	`sha256:fb6c252dbe4ea833252dda54fc2112612673c417b50fcdf43a2d74689f991020`  
		Last Modified: Wed, 25 Dec 2024 08:11:11 GMT  
		Size: 6.5 MB (6458186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fe47c998d7cda12ac60ab77a48c08ac91810247c1243eca5942377359731f6`  
		Last Modified: Wed, 25 Dec 2024 08:11:10 GMT  
		Size: 21.7 KB (21683 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:65b5649c4ee394f121c7c5e0b15000ee34325ae73742778ac66e571c3e86b4aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:e8db6ac16d4a36612469698d3d468a49b40bcdba2b6ac7d485b6e02ed89de1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192309965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdcfeef6013971a13ba084332a27b970e93d2e715fd716b8dd9843e22f7c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Thu, 02 Jan 2025 20:55:20 GMT
RUN a2enmod rewrite # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
WORKDIR /var/www/html
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_VERSION=1.29.2
# Thu, 02 Jan 2025 20:55:20 GMT
ENV BACKDROP_MD5=dcb27feb72d78f1f14120d4c9a6bc70b
# Thu, 02 Jan 2025 20:55:20 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 02 Jan 2025 20:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Jan 2025 20:55:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4aa5c3d57f9c53708bec8c65315261e2ac1996c279afaaffa03703b402c5040`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d5f1913860021d9e4939fe6fe06ac748d38ce0ce9cd1cdb4f6f6c1d9b59cf`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 104.2 MB (104150917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d722d2711757ac01b6f4dd63f6dc13e451ee64cae1f048b7a935623bd8d6bfd`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607318548f8d527fe222622ae223167f4e2dfaf76ded3d2a261292523c77395`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 20.1 MB (20123806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6301dd3d2a055241777a76b7892c83f51fa77a1e8890428ece5095f0ab5c3a5`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56df30ff8b4aa571144d39bb1ec300c57a4be6e462b0453245430ac142d16a0`  
		Last Modified: Tue, 24 Dec 2024 22:24:43 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db430a74a92f936310388f978af7f942c66f00c52c09376e530c1e8875b37bc0`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 12.7 MB (12653097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8874a713cbf5a147e74fcb290dae2568726df04e4be334ff48edf36508a913`  
		Last Modified: Tue, 24 Dec 2024 22:24:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8c4c440f2ff157c32993704921d4ed3271f0e1232fc945123569db85a5f6b`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 11.7 MB (11652374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb26e53fd3639e545bc99ecc0227f1a3e336a4fbb0101013796e28547346ab`  
		Last Modified: Tue, 24 Dec 2024 22:24:45 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391f7a6f4105dfe5ffb72540cfb4cabb850af1a9186c878f798d0e1b38a7ea0`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e72d70e49bb823550c0b313e0f93e7da711c51faadf8765fe671b52cf19f22f`  
		Last Modified: Tue, 24 Dec 2024 22:24:46 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de41ebb3c28bbcd67009cb473b90e80209f1cf3c295ac07c7c8b6c0f5d8295`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2282cb7ad81b0e6609a07826198c5e59e1c6ce8033bcde7e8c133c3161d8d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 5.6 MB (5580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6747cbdd92af9522a5ba0d60132530558890115a7df0faa5564d29eb5be4d8`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 9.9 MB (9911381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8522ad2c3fbbea6a0a67465ea38c35910d6d9c4a493df92dded558bd22e2a9`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:17b60c3d6e4b6b8f8a5c291cd01789c72f75df13510fbd7e92f804a2ec58897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2819a78649a3f3616891611c23e2fa60241add4ac8479b4d3f661dd98f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:383e66b7e4cf18ab43a41ae6eac95605cc04095aaff35494fac9331a41b7d303`  
		Last Modified: Wed, 08 Jan 2025 23:32:24 GMT  
		Size: 6.9 MB (6940255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56e83b6386639db67b7824641918210fd780fcd0b7c6cfcbc0a40edb2e22468`  
		Last Modified: Wed, 08 Jan 2025 23:32:23 GMT  
		Size: 29.7 KB (29683 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b003e7677af4024c0fbcda84d8d3468636fa3ea7a6bca30e21736972066f685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183656791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a4db2b6dac4980f87ecaa43a3e8e3f2261d69afeac1b191cda7b2213b424b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eef2a5dc1b65f7c6c1d52bc33548c51ee34d74d7977c2cf79eab50fd8e47e7c`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 12.0 MB (12045040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969b38e145fa3c5e6eedc74525f1fc87a11a71371d0468f94183fa2d4a81ca8`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549affc734ea0c201087ba0b480b836b4b13245bfc9a1ecc9d5bd9b23be8c874`  
		Last Modified: Wed, 25 Dec 2024 00:38:34 GMT  
		Size: 11.2 MB (11157613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166f694155e8bbb56ba3a9bc887400639c9e32b7c7a6df4d028562f9325f7cab`  
		Last Modified: Wed, 25 Dec 2024 00:38:32 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa796aa5b34ed7565fe846b39b5a89626061244a73e95329edea98ea93c3825`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b475d415794f60fdf9b34581e3e7051ff4c67bc0d16bbdd32b27e64f1a959b`  
		Last Modified: Wed, 25 Dec 2024 00:38:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed877f7b2e77705fec0a1ac55216df654eae2a35fc1a491bddbf67354e0021`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e694b1c845e150c50d2100bef6cef5b4b081dad8b811c5d654d21031708b45c1`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 5.5 MB (5526340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff138a25e5c5b847589ed1e2924839db5bb8082778fb44cbd26b1d34ee172807`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3118ed6eef12e645866fe3abc49825b641203bf9c9eb9cdd3fb8d7bf9c88fa`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:734976c4ab72936702df0a36911ebcabb0816804e1ae1e7e2b7e9f17b2a2854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6998558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda19a9ded352c2f86922d0e9e88a204ceb468b5ce5483db22e8036a2a7143da`

```dockerfile
```

-	Layers:
	-	`sha256:480b17067542ed61f8d3c50a12c5d11aa7731634f1efda148e4377f4f34be2dc`  
		Last Modified: Wed, 25 Dec 2024 08:09:51 GMT  
		Size: 7.0 MB (6968735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbb377a9ab5d90f4dc835e7a4fa61b8f9eea190c99e1d46258f0cd893dd7a5e`  
		Last Modified: Wed, 25 Dec 2024 08:09:50 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json
