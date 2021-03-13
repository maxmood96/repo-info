## `drupal:php8.0-apache-buster`

```console
$ docker pull drupal@sha256:b453e4e1ad4bf56d9ea4b35ee13475f24536390827dc49165bea6c57607fc981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `drupal:php8.0-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:3ef9d02b161c1ed38dd176312b87c60b3f34e8652f5c8309dec7548aeeb1633a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169473049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7cb65e0d9018f75df637120b6ea2892ae0a06f1285c3bc9315fac9d14d6073`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Sat, 06 Mar 2021 02:50:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 06 Mar 2021 02:50:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 06 Mar 2021 02:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 02:50:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 02:50:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 02:57:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 06 Mar 2021 02:57:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 06 Mar 2021 02:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 06 Mar 2021 02:58:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 06 Mar 2021 02:58:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 06 Mar 2021 02:58:16 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 06 Mar 2021 02:58:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 06 Mar 2021 02:58:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:58:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 02:58:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 02:58:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 06 Mar 2021 02:58:17 GMT
ENV PHP_VERSION=8.0.3
# Sat, 06 Mar 2021 02:58:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Sat, 06 Mar 2021 02:58:18 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Sat, 06 Mar 2021 02:58:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Mar 2021 02:58:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:05:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 03:05:48 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:05:50 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 03:05:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 03:05:51 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Mar 2021 03:05:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Mar 2021 03:05:52 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 03:05:52 GMT
EXPOSE 80
# Sat, 06 Mar 2021 03:05:52 GMT
CMD ["apache2-foreground"]
# Sat, 06 Mar 2021 06:52:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 06:52:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 06 Mar 2021 06:52:10 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Sat, 06 Mar 2021 06:52:10 GMT
ENV DRUPAL_VERSION=9.1.5
# Sat, 06 Mar 2021 06:52:10 GMT
WORKDIR /opt/drupal
# Sat, 06 Mar 2021 06:52:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 06 Mar 2021 06:52:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366d949cba16786c30c237edb76226ef76182ec80058f16895e01dc870ed72c2`  
		Last Modified: Sat, 06 Mar 2021 06:28:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c65628244f3d877562fcb1173ba0019e5dea30511511921370d39c81a4dd6e3`  
		Last Modified: Sat, 06 Mar 2021 06:28:32 GMT  
		Size: 76.7 MB (76678551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a8e4ec25c68866792a4ec85f038f3ae6d63b74f50bc8b39a467f3f03cecec5`  
		Last Modified: Sat, 06 Mar 2021 06:28:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3512b0c25baf785483e3c0af9e8e28530a5e47ebab453de50114af59124fe9cb`  
		Last Modified: Sat, 06 Mar 2021 06:29:29 GMT  
		Size: 18.7 MB (18679214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a983b5b9a384652c9ced64645b382d8d7ba94c2a6e7b18f32aa9ac3b376cd22e`  
		Last Modified: Sat, 06 Mar 2021 06:29:26 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0def93a72fb48f46099acca52e6f3cf929ac58cf7ec3a5c68133a583bf68707e`  
		Last Modified: Sat, 06 Mar 2021 06:29:26 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8bec9fa3831078f1c74e1676804e8cde7193efaec13cb407d68280c8d18852`  
		Last Modified: Sat, 06 Mar 2021 06:29:27 GMT  
		Size: 11.1 MB (11093902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80713ac3f2c7bce439ff4a1cb297ff69b1d847258b3c5a6486ea0b334fbff8a5`  
		Last Modified: Sat, 06 Mar 2021 06:29:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549982e9dd23524b2196a3d50b37fe0a8a1ddd08949f97a01b62d4503dac2a44`  
		Last Modified: Sat, 06 Mar 2021 06:29:27 GMT  
		Size: 14.5 MB (14481038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d487548f700a0ec9cfa2d6cf1797a7626aad95fcb0c41de8137c706c0b3e3c1`  
		Last Modified: Sat, 06 Mar 2021 06:29:24 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1dd2a59f0ab5af41099a8dc816fb347067adfef3447271c70fa2c67606c892`  
		Last Modified: Sat, 06 Mar 2021 06:29:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92ec02c18973683fe1784734e724cd5c40348ab77ae004bd81bf81a90192d1e`  
		Last Modified: Sat, 06 Mar 2021 06:29:24 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a880c8e72363e5f58af173333658b52c87d9657bfac13b15ec25beeb5283ef5b`  
		Last Modified: Sat, 06 Mar 2021 07:06:38 GMT  
		Size: 2.1 MB (2052952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0baa978da6ac76558d52e8e13f00ee3bd9190f12de7e37047533a29ba41f0`  
		Last Modified: Sat, 06 Mar 2021 07:06:38 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ffc6b3e10193636ed8d2dcbcd84cd1401b3e349ed0e3a9d5eeec0a49a5c22`  
		Last Modified: Sat, 06 Mar 2021 07:06:38 GMT  
		Size: 551.8 KB (551816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7317421d31febc94d8dee5bda238e6916bed361811da536d82f31ce35433c279`  
		Last Modified: Sat, 06 Mar 2021 07:06:38 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f350043ad2091e225d420eaad3108cbd6a0baf73443ce39fa97e610f10ffde`  
		Last Modified: Sat, 06 Mar 2021 07:06:43 GMT  
		Size: 18.8 MB (18834556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.0-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:7e40283909964af580a2150d29e406a993be97256a46025808f1eec260385c19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144172582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fda57e6b9d27d47adb446ad49021f0a0d62e5b256462f14b4cf6202235c9ed7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Mar 2021 02:00:12 GMT
ADD file:123da9848f87c8ed4c5122a104b8650564c09767725916f822def7b645a019f1 in / 
# Fri, 12 Mar 2021 02:00:14 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 08:58:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Mar 2021 08:58:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Mar 2021 08:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 08:59:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Mar 2021 08:59:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Mar 2021 09:03:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Mar 2021 09:03:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Mar 2021 09:03:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Mar 2021 09:03:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Mar 2021 09:03:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Mar 2021 09:03:39 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 12 Mar 2021 09:03:43 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 12 Mar 2021 09:03:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 09:03:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 09:03:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Mar 2021 09:03:49 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 12 Mar 2021 09:03:50 GMT
ENV PHP_VERSION=8.0.3
# Fri, 12 Mar 2021 09:03:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 12 Mar 2021 09:03:52 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 12 Mar 2021 09:04:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Mar 2021 09:04:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Mar 2021 09:07:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Mar 2021 09:07:04 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 12 Mar 2021 09:07:06 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Mar 2021 09:07:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Mar 2021 09:07:07 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Mar 2021 09:07:08 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Mar 2021 09:07:09 GMT
WORKDIR /var/www/html
# Fri, 12 Mar 2021 09:07:09 GMT
EXPOSE 80
# Fri, 12 Mar 2021 09:07:10 GMT
CMD ["apache2-foreground"]
# Sat, 13 Mar 2021 00:36:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 00:36:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 13 Mar 2021 00:36:30 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Sat, 13 Mar 2021 00:36:32 GMT
ENV DRUPAL_VERSION=9.1.5
# Sat, 13 Mar 2021 00:36:33 GMT
WORKDIR /opt/drupal
# Sat, 13 Mar 2021 00:37:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 13 Mar 2021 00:37:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e12d26f75fe8b7fd14712965ff5178762227d07d2151bb35fa21105ddfc4a14a`  
		Last Modified: Fri, 12 Mar 2021 02:10:28 GMT  
		Size: 22.7 MB (22709467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97de6173b7f7c8cb90cb7c3294b87fc1eee1e42223b91620341128b5119594a`  
		Last Modified: Fri, 12 Mar 2021 10:02:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2b82824d7becee8957d19b795e585f7a5154d758780f636358ad5dfc638124`  
		Last Modified: Fri, 12 Mar 2021 10:02:40 GMT  
		Size: 59.5 MB (59513006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732ffe8153f5415ad0deaf603c13ca07696188324be500902aa2d60abf5f657b`  
		Last Modified: Fri, 12 Mar 2021 10:02:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38df2bb5f9338849fe8cd651740bfa74e601be8674ef98a4530a9fdca80ff99d`  
		Last Modified: Fri, 12 Mar 2021 10:03:17 GMT  
		Size: 17.5 MB (17481742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1f17d694ace61a63fe6312fe0956b53a64c151195691b78350348e92c21934`  
		Last Modified: Fri, 12 Mar 2021 10:03:11 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a401a55da75d47e7bff923d871beeddb5f4f58693069e516712ff17d6c6326`  
		Last Modified: Fri, 12 Mar 2021 10:03:15 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ee21e4ff166c21d3ea02cfa1f4d2e2ecf4f54126a15ea130d4cd40d2a6414d`  
		Last Modified: Fri, 12 Mar 2021 10:03:13 GMT  
		Size: 11.1 MB (11092051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6580f45e3fb5a7efd17cc2e91cd8e051f07e9d6c864776f13662c2b82dfe6d27`  
		Last Modified: Fri, 12 Mar 2021 10:03:10 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e413599c2f3a4f4efee14313abb46bb7008e52ffa654f3b2fddcbeaaa23e808`  
		Last Modified: Fri, 12 Mar 2021 10:03:14 GMT  
		Size: 12.5 MB (12495440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6551080d01ab93b7954059d167381b5db8c9cf7126c0f8cb6e7e49a1ae605d94`  
		Last Modified: Fri, 12 Mar 2021 10:03:10 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93742a769d075b2b8bb080b493e8714a50977a01036333f24064f8266736d58f`  
		Last Modified: Fri, 12 Mar 2021 10:03:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15327cd65c63630f1ee18fc2523f2ddf5fffd08d28242fe6d9a09ac44f550cfc`  
		Last Modified: Fri, 12 Mar 2021 10:03:10 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aca80c8fcf710cb90e0498644ad07543fb49be65b81d817c627c8b22248da9`  
		Last Modified: Sat, 13 Mar 2021 00:51:42 GMT  
		Size: 1.5 MB (1488468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47034ffc87118525571213e3af20279f7de9b1f24c0c3ddb81a669908a567b6`  
		Last Modified: Sat, 13 Mar 2021 00:51:41 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9766bcfd0a575f0d3b0186cf200b3ee92c2e757d24d3a15ebdd12e87fe5f7704`  
		Last Modified: Sat, 13 Mar 2021 00:51:42 GMT  
		Size: 551.8 KB (551813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c11ed76d4c10fe916980944f4f4fd68c8e081079ff9a17280456f4db091078`  
		Last Modified: Sat, 13 Mar 2021 00:51:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cea8f7eed0183a310f79526ddf932fc4bd723b18036dd6b94a0da1a8711af35`  
		Last Modified: Sat, 13 Mar 2021 00:51:58 GMT  
		Size: 18.8 MB (18834725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.0-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:2c2a8859ff1de150c15dd4ca3f801e5c5d2bf6b17357ab6b466a7fabedba2222
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162638666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f842820baa0e5e75e869707b1282819f40318a38fcc54bc83ed21aa8bca81317`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 13:24:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Feb 2021 13:24:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Feb 2021 13:24:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 13:24:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Feb 2021 13:24:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Feb 2021 13:29:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Feb 2021 13:29:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Feb 2021 13:29:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Feb 2021 13:29:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Feb 2021 13:29:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Feb 2021 13:29:52 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Feb 2021 13:29:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Feb 2021 13:29:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Feb 2021 13:29:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Feb 2021 13:29:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Feb 2021 13:29:55 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 04 Mar 2021 23:45:41 GMT
ENV PHP_VERSION=8.0.3
# Thu, 04 Mar 2021 23:45:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Thu, 04 Mar 2021 23:45:42 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Thu, 04 Mar 2021 23:46:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 23:46:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Mar 2021 23:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Mar 2021 23:49:23 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 04 Mar 2021 23:49:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Mar 2021 23:49:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Mar 2021 23:49:27 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Mar 2021 23:49:28 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Mar 2021 23:49:29 GMT
WORKDIR /var/www/html
# Thu, 04 Mar 2021 23:49:30 GMT
EXPOSE 80
# Thu, 04 Mar 2021 23:49:31 GMT
CMD ["apache2-foreground"]
# Fri, 05 Mar 2021 01:33:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Mar 2021 01:33:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 05 Mar 2021 01:33:17 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 05 Mar 2021 01:33:18 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 05 Mar 2021 01:33:19 GMT
WORKDIR /opt/drupal
# Fri, 05 Mar 2021 01:33:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 05 Mar 2021 01:33:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7445693bd43e8246a8c166233392b33143f7f5e396c480f74538e5738fb6bd6e`  
		Last Modified: Tue, 09 Feb 2021 14:35:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb0363d084b9a838de3a1ef92a69c34131d0be020cc0474098ea80a07e16b6d`  
		Last Modified: Tue, 09 Feb 2021 14:35:38 GMT  
		Size: 70.4 MB (70355003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c2495950546c2e82fc496d7c39837a517f3f3095fb87598d1731d0529f907`  
		Last Modified: Tue, 09 Feb 2021 14:35:20 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1c5d697df1ad5b06b1191622869ff679a88a60b478a1d7f2dc94b38c249efa`  
		Last Modified: Tue, 09 Feb 2021 14:36:30 GMT  
		Size: 18.6 MB (18579948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361e2a373dc16cf325162b9be8d28ae695eaddb93f477dbad81713d17c4eb823`  
		Last Modified: Tue, 09 Feb 2021 14:36:15 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df605982341375d14e7a1c2767d248fe8e85a467ac502562d36f73b352f654e9`  
		Last Modified: Tue, 09 Feb 2021 14:36:15 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d552e3415429f46fca8f6c47bc051fcad06b63f47c65b6a34f8aa8c89fa7601a`  
		Last Modified: Fri, 05 Mar 2021 01:09:34 GMT  
		Size: 11.1 MB (11092820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d653ac472a8ef667f3e3a717a29dc1d2a0c6be8eb8ae441f94283c59e02a49c1`  
		Last Modified: Fri, 05 Mar 2021 01:09:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c555788ca8b2d2bfc126f1e4a42d4b3773b0e0584aafd5b65f1f2096d6df86`  
		Last Modified: Fri, 05 Mar 2021 01:09:36 GMT  
		Size: 15.7 MB (15657999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bfcc92fa2643820c4f8b2c82b7caa8516fa86edb820c393b855a0edc56eca1`  
		Last Modified: Fri, 05 Mar 2021 01:09:33 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f9b720a21ed1dca97d120d3d03d259e742a9f50e01073182c925081dead9a`  
		Last Modified: Fri, 05 Mar 2021 01:09:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f94dba88521a36d1ac954e24258b21d9e1d2a9f99652fa500e80b70a7e20e24`  
		Last Modified: Fri, 05 Mar 2021 01:09:31 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1550b7a8e5ca9452d62c0ee9cb3998c058cd19b6abb52613341064ce57a02a6`  
		Last Modified: Fri, 05 Mar 2021 01:52:57 GMT  
		Size: 1.7 MB (1709142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6460edea5a86297cf98fe43794d7f9ccf93f90af72d240768e3e4019afd44bbb`  
		Last Modified: Fri, 05 Mar 2021 01:52:57 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29db7ec92efcbdec5816a332979ee2e448f9c822b7e9ab0db873df65e519955`  
		Last Modified: Fri, 05 Mar 2021 01:52:57 GMT  
		Size: 551.8 KB (551816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75751858955c5c4fb07cf6724175386981661e6076c6c9e305d104f2c978f336`  
		Last Modified: Fri, 05 Mar 2021 01:52:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc8603e1452679bcfd0bf500e8ddf6a89ede8e26091801b4f2a090fc5fdc27e`  
		Last Modified: Fri, 05 Mar 2021 01:53:05 GMT  
		Size: 18.8 MB (18834618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.0-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:7c56906d1c6df31436cab859a412a26283d9645d0162b670be5132e9183e0291
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174869547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fd9180e9a7379ef0231e4768ad47298d0947486176c9c10050b02ac8e60ea8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Sat, 06 Mar 2021 01:48:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 06 Mar 2021 01:48:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 06 Mar 2021 01:48:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 01:48:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 06 Mar 2021 01:48:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 06 Mar 2021 01:55:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 06 Mar 2021 01:55:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 06 Mar 2021 01:55:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 06 Mar 2021 01:55:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 06 Mar 2021 01:55:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 06 Mar 2021 01:55:31 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 06 Mar 2021 01:55:31 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 06 Mar 2021 01:55:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 01:55:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 06 Mar 2021 01:55:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 06 Mar 2021 01:55:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Sat, 06 Mar 2021 01:55:32 GMT
ENV PHP_VERSION=8.0.3
# Sat, 06 Mar 2021 01:55:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Sat, 06 Mar 2021 01:55:33 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Sat, 06 Mar 2021 01:55:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Mar 2021 01:55:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Mar 2021 02:02:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Mar 2021 02:02:46 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Sat, 06 Mar 2021 02:02:47 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Mar 2021 02:02:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Mar 2021 02:02:48 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Mar 2021 02:02:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Mar 2021 02:02:48 GMT
WORKDIR /var/www/html
# Sat, 06 Mar 2021 02:02:49 GMT
EXPOSE 80
# Sat, 06 Mar 2021 02:02:49 GMT
CMD ["apache2-foreground"]
# Sat, 06 Mar 2021 06:07:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Mar 2021 06:07:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 06 Mar 2021 06:07:36 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Sat, 06 Mar 2021 06:07:36 GMT
ENV DRUPAL_VERSION=9.1.5
# Sat, 06 Mar 2021 06:07:36 GMT
WORKDIR /opt/drupal
# Sat, 06 Mar 2021 06:07:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Sat, 06 Mar 2021 06:07:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26795dcaf2a2cebe689b80436002037b25e5ac2fe52595e26ee579a0bd0957e8`  
		Last Modified: Sat, 06 Mar 2021 05:43:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afad6b533f62ba01351a6cf77b7963d6e9fee93f514ca97ec763f391d81ec8b`  
		Last Modified: Sat, 06 Mar 2021 05:43:41 GMT  
		Size: 81.2 MB (81229560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e837aeda74528e364ebf49b2bc84ce0ec794bdce3fbde67ac29305f73a311ce4`  
		Last Modified: Sat, 06 Mar 2021 05:43:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29c03b2034b28c836917ede97ee8072f34dff5ec45b5ca553fe1285b35d3003`  
		Last Modified: Sat, 06 Mar 2021 05:44:53 GMT  
		Size: 19.1 MB (19114936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce209370920bf5b832d7b2540366a4697057fcfa6606e0fd3d06e1593c6aea1a`  
		Last Modified: Sat, 06 Mar 2021 05:44:48 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02622cdcda51d64725df021d34381bb4a2644b780a1ba5202d7c042c5f0bd69`  
		Last Modified: Sat, 06 Mar 2021 05:44:48 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdd974c5e2272e2aeeb7ab02f63301751a1a199f8a706d83472203dc7ba110e`  
		Last Modified: Sat, 06 Mar 2021 05:44:50 GMT  
		Size: 11.1 MB (11093272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c187810d1f8bea1313730d7286e1f11dc85a87547d51d554830d34c587739e`  
		Last Modified: Sat, 06 Mar 2021 05:44:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dddd8489d33b2efd94132aad21d5665cd41bbc13e634a69e03f610470a52dda1`  
		Last Modified: Sat, 06 Mar 2021 05:44:51 GMT  
		Size: 14.5 MB (14476243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee3498c9c1ce1258ea5794923bbb2067fa121a3e3cb35ba6d35d02193af83bb`  
		Last Modified: Sat, 06 Mar 2021 05:44:45 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b9ffc699b56e5bed4c5bd653573cc42825d7e0c6806d0e80ed0508c26532a7`  
		Last Modified: Sat, 06 Mar 2021 05:44:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42553463c106e9f3c6cd82b2a610ecc5376bd93e04e756d1f1db0599f529ebd1`  
		Last Modified: Sat, 06 Mar 2021 05:44:45 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d15ee02a327412f247746553857b7b84019d559437f01f8904e1adcc05d09b7`  
		Last Modified: Sat, 06 Mar 2021 06:30:44 GMT  
		Size: 1.8 MB (1810047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84f0a58d069e2a97216871f84a8eeb903455c443c5904c370bfb0bf445aded1`  
		Last Modified: Sat, 06 Mar 2021 06:30:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118736e9fc3c48600e009ad40cd0fd9c9700d85fac7c0669a5650d4a4ab1ff8e`  
		Last Modified: Sat, 06 Mar 2021 06:30:44 GMT  
		Size: 551.8 KB (551803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc5525778c1072885929ed46df1bd57be8092accb0bcbb10bc95b7b7ad8dad7`  
		Last Modified: Sat, 06 Mar 2021 06:30:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4878069d10578c497afb874eb8af5890e26bf8ed62e4efd3da0f1bea589ad770`  
		Last Modified: Sat, 06 Mar 2021 06:30:51 GMT  
		Size: 18.8 MB (18835094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.0-apache-buster` - linux; ppc64le

```console
$ docker pull drupal@sha256:8f94bdc0d270ebc9fc2ce82a347fa32dc64d029ee15e8557e7879ec1a049d174
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182271629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172efb422433189891fab67ba55f648103207c71a3384deda160b9a27a1e26d1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 15:49:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 09 Feb 2021 15:49:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Feb 2021 15:54:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 15:54:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Feb 2021 15:54:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 09 Feb 2021 16:05:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Feb 2021 16:05:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Feb 2021 16:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 09 Feb 2021 16:07:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 09 Feb 2021 16:07:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 09 Feb 2021 16:08:02 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 09 Feb 2021 16:08:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 09 Feb 2021 16:08:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Feb 2021 16:08:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Feb 2021 16:08:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Feb 2021 16:08:29 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 04 Mar 2021 23:30:05 GMT
ENV PHP_VERSION=8.0.3
# Thu, 04 Mar 2021 23:30:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Thu, 04 Mar 2021 23:30:17 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Thu, 04 Mar 2021 23:32:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 23:32:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Mar 2021 23:41:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Mar 2021 23:41:36 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 04 Mar 2021 23:41:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Mar 2021 23:42:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Mar 2021 23:42:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Mar 2021 23:42:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Mar 2021 23:42:34 GMT
WORKDIR /var/www/html
# Thu, 04 Mar 2021 23:42:46 GMT
EXPOSE 80
# Thu, 04 Mar 2021 23:42:56 GMT
CMD ["apache2-foreground"]
# Fri, 05 Mar 2021 02:19:53 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Mar 2021 02:20:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 05 Mar 2021 02:20:32 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 05 Mar 2021 02:20:42 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 05 Mar 2021 02:21:03 GMT
WORKDIR /opt/drupal
# Fri, 05 Mar 2021 02:21:36 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 05 Mar 2021 02:21:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08ed6cfbd4e7b8f4f2d892c01b1976ced072938787d146fc0a55690e9883a74`  
		Last Modified: Tue, 09 Feb 2021 17:52:52 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cc4083d6613c902035d3b0dd1bb317f5bb699313bcd6e687ec17347192cdaa`  
		Last Modified: Tue, 09 Feb 2021 17:53:19 GMT  
		Size: 82.3 MB (82290490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d61a25f1b4f9da6f8c429b980f08dd7c19f7c6353704da136afc7e59343620`  
		Last Modified: Tue, 09 Feb 2021 17:52:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b1f6476e9275a2b18cd7fd1272d6dda57c23b2553c61e8498701ec7e37a54d`  
		Last Modified: Tue, 09 Feb 2021 17:54:20 GMT  
		Size: 19.8 MB (19818441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b84cb0491f75c5f31ddeb649efdc5c1b5105987ed26041d96b7415b17384dd`  
		Last Modified: Tue, 09 Feb 2021 17:54:15 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139cd3ca812b53dbae139a43e087189c11bfcbb27f2dba64e6defc1d5dd151ee`  
		Last Modified: Tue, 09 Feb 2021 17:54:15 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4bc4244ddf8471f6731cc506c9347ea5230f0c1229c0a15422a08a9ef913bf`  
		Last Modified: Fri, 05 Mar 2021 01:44:03 GMT  
		Size: 11.1 MB (11094190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f096286ce91f0859b1f8da911723174605610e203188ac8fb0d0056d16e925a6`  
		Last Modified: Fri, 05 Mar 2021 01:43:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862319b793930f0557eea26cdc9746e34606f7e38efa70db6352a492de6ea840`  
		Last Modified: Fri, 05 Mar 2021 01:44:03 GMT  
		Size: 17.2 MB (17195926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b3f3ac1a7085b15946596b53b19afa5a49e0c5f74cafb2af2d21afd7ce951c`  
		Last Modified: Fri, 05 Mar 2021 01:43:59 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2457c67a6ec35198b25f61cdeba9733d50ca5187d4e3d1bb26ffb5079713e4`  
		Last Modified: Fri, 05 Mar 2021 01:43:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17b18b91f40adaa4a6de356e0c14cc3c8389a4f80325bf0d404a687f6afab31`  
		Last Modified: Fri, 05 Mar 2021 01:43:59 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4700845653a17127293b3108293cf6291d0794d5442e745f8962d487c0accf`  
		Last Modified: Fri, 05 Mar 2021 02:54:49 GMT  
		Size: 2.0 MB (1960725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a14395adf26bfbc7ce6c7906ef65d07d0f4c46505c538a9adf6af2926a19ccc`  
		Last Modified: Fri, 05 Mar 2021 02:54:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aae83d985d75d7ec06f4ca5d2fe8f9ab1530cf0b1239f405075ee3b0470c6fe`  
		Last Modified: Fri, 05 Mar 2021 02:54:45 GMT  
		Size: 551.8 KB (551811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dd72b5b06b33d6f26983eeb657f1e54486d6c7eb5410637e588a695f0e6bc1`  
		Last Modified: Fri, 05 Mar 2021 02:54:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1193fb6237784c6706624ca1da9f4f22fa19c11d391a58347198da76ea7e214f`  
		Last Modified: Fri, 05 Mar 2021 02:56:16 GMT  
		Size: 18.8 MB (18834648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:php8.0-apache-buster` - linux; s390x

```console
$ docker pull drupal@sha256:c82178833c03ee9d2af6fabbf9708b6a3fb7af523e8ac1499bef6eacbc6e8102
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154486209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef82456fd4840f54a51a55a2e94a04d7ca823b65db94df7e07e447fd3622c9e2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 12 Mar 2021 01:46:04 GMT
ADD file:afec039adf230a9186a38b57eed85262696f8d178ac649a445657066f16fe806 in / 
# Fri, 12 Mar 2021 01:46:07 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 06:25:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Mar 2021 06:25:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Mar 2021 06:25:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 06:26:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Mar 2021 06:26:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Mar 2021 06:29:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Mar 2021 06:29:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Mar 2021 06:29:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 12 Mar 2021 06:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 12 Mar 2021 06:29:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 12 Mar 2021 06:29:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 12 Mar 2021 06:29:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 12 Mar 2021 06:29:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 06:29:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 06:29:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Mar 2021 06:29:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 12 Mar 2021 06:29:28 GMT
ENV PHP_VERSION=8.0.3
# Fri, 12 Mar 2021 06:29:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.3.tar.xz.asc
# Fri, 12 Mar 2021 06:29:29 GMT
ENV PHP_SHA256=c9816aa9745a9695672951eaff3a35ca5eddcb9cacf87a4f04b9fb1169010251
# Fri, 12 Mar 2021 06:29:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Mar 2021 06:29:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Mar 2021 06:32:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Mar 2021 06:32:27 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 12 Mar 2021 06:32:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Mar 2021 06:32:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Mar 2021 06:32:29 GMT
STOPSIGNAL SIGWINCH
# Fri, 12 Mar 2021 06:32:29 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 12 Mar 2021 06:32:29 GMT
WORKDIR /var/www/html
# Fri, 12 Mar 2021 06:32:29 GMT
EXPOSE 80
# Fri, 12 Mar 2021 06:32:30 GMT
CMD ["apache2-foreground"]
# Fri, 12 Mar 2021 13:17:37 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 13:17:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 12 Mar 2021 13:17:38 GMT
COPY file:deb590b59fc201c558f5c400490c99455a4f02093f44f8b429b21b024fa29bb3 in /usr/local/bin/ 
# Fri, 12 Mar 2021 13:17:38 GMT
ENV DRUPAL_VERSION=9.1.5
# Fri, 12 Mar 2021 13:17:39 GMT
WORKDIR /opt/drupal
# Fri, 12 Mar 2021 13:18:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 12 Mar 2021 13:18:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d41215965c091534e809ab2e8f4a2c1cebee3de536c2c74a7bc8302bbc8af7e1`  
		Last Modified: Fri, 12 Mar 2021 01:50:30 GMT  
		Size: 25.7 MB (25716294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9dd141052a65d998740b690bf23f87e66d5b424444a5ff93d6c48111ae249e`  
		Last Modified: Fri, 12 Mar 2021 07:08:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3bab8af34a0dbb027eb2a45b656ff1fac103644336c21897261781a5e1af4d`  
		Last Modified: Fri, 12 Mar 2021 07:09:09 GMT  
		Size: 64.7 MB (64709520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6048fd685ab61503dafb7e0f87745aad2b5333c1619b088ae5494895426349a`  
		Last Modified: Fri, 12 Mar 2021 07:08:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271f221477d4822a9d925f001d26c13fb7998b92db69d831b54ca5b4bd1e24a4`  
		Last Modified: Fri, 12 Mar 2021 07:09:40 GMT  
		Size: 18.5 MB (18524956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ff7e38c41f365dd65becc9c8e1340709af4368653258b91a64e2da62ba0699`  
		Last Modified: Fri, 12 Mar 2021 07:09:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59060dc72885f5f6a59b6badfe231da87b05039b0bc5993b5234b3e99b779136`  
		Last Modified: Fri, 12 Mar 2021 07:09:38 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530ede18afa8cb4893e2fed9fa766c0e08965033f31a60fa79172ac9561ebc1`  
		Last Modified: Fri, 12 Mar 2021 07:09:38 GMT  
		Size: 11.1 MB (11092369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b70451244b8697182a0023ce4b1655f17ae2440e52de25fa04250dcc421bcc`  
		Last Modified: Fri, 12 Mar 2021 07:09:36 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b564822b07225cc692a0c243ed6855c0a57fb52f0ebe2fa112605bdf4f8fe1e`  
		Last Modified: Fri, 12 Mar 2021 07:09:38 GMT  
		Size: 13.3 MB (13349966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393086872c8b08e3b515688e3b51c6e6c8198874704a88115fd35956592f10be`  
		Last Modified: Fri, 12 Mar 2021 07:09:36 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c7c8f25923e393b233cf934335f8b9fbdb0f3a535b48b4d51f7a70e42fa4de`  
		Last Modified: Fri, 12 Mar 2021 07:09:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1241335641e5aa039b741b679caa8569e9ccddb66f883c9fb0234a9a8b45d041`  
		Last Modified: Fri, 12 Mar 2021 07:09:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afce0f1247f959f73a30bfc96df25027def4781015c2cdc9854d5025de0dedb`  
		Last Modified: Fri, 12 Mar 2021 13:28:42 GMT  
		Size: 1.7 MB (1700833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7839a9a1a7d04b9863f58c6f3445383b6d52ad6c862e918b373f194c4b7dc5d`  
		Last Modified: Fri, 12 Mar 2021 13:28:42 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60f0d3bf7990f63e0b2083d3e544e8ec3e3198eaed8954659615357c8848a92`  
		Last Modified: Fri, 12 Mar 2021 13:28:42 GMT  
		Size: 551.8 KB (551806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f368b0d90bea3558a219b45b16676f88b17b172b493d7a537a775c12a58766`  
		Last Modified: Fri, 12 Mar 2021 13:28:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba40e990fa1834ee86ef5891018c89ea91d7b68c1daccbdd16060aee7ce35c82`  
		Last Modified: Fri, 12 Mar 2021 13:28:46 GMT  
		Size: 18.8 MB (18834612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
