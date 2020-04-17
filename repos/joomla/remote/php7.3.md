## `joomla:php7.3`

```console
$ docker pull joomla@sha256:f7f7c3070b1b43388745d7c0429451970a1d4e86dcfe17b739585faaff4a297a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `joomla:php7.3` - linux; amd64

```console
$ docker pull joomla@sha256:cdd247beb3b8085857f6f82bfacee33d5aea18cf0dca1d4477b79cd407b1b150
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162057409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5cf905edf6d7f8e6f9dd0a8f89ad194159a417b3a15981d93bf3da1d02201a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 18:09:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 31 Mar 2020 18:09:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 31 Mar 2020 18:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:10:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 31 Mar 2020 18:10:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 31 Mar 2020 18:16:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 31 Mar 2020 18:16:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 31 Mar 2020 18:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 31 Mar 2020 18:17:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 31 Mar 2020 18:17:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 31 Mar 2020 18:17:09 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 31 Mar 2020 18:17:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 31 Mar 2020 18:17:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:17:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:17:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 31 Mar 2020 18:43:34 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 31 Mar 2020 18:43:34 GMT
ENV PHP_VERSION=7.3.16
# Tue, 31 Mar 2020 18:43:34 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.16.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.16.tar.xz.asc/from/this/mirror
# Tue, 31 Mar 2020 18:43:35 GMT
ENV PHP_SHA256=91aaee3dbdc71b69b4f3292f9d99211172a2fa926c3f3bbdb0e85dab03dd2bcb PHP_MD5=
# Tue, 31 Mar 2020 18:43:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 31 Mar 2020 18:43:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 31 Mar 2020 18:48:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 31 Mar 2020 18:48:34 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Tue, 31 Mar 2020 18:48:35 GMT
RUN docker-php-ext-enable sodium
# Tue, 31 Mar 2020 18:48:36 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 31 Mar 2020 18:48:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 31 Mar 2020 18:48:36 GMT
STOPSIGNAL SIGWINCH
# Tue, 31 Mar 2020 18:48:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 31 Mar 2020 18:48:37 GMT
WORKDIR /var/www/html
# Tue, 31 Mar 2020 18:48:37 GMT
EXPOSE 80
# Tue, 31 Mar 2020 18:48:37 GMT
CMD ["apache2-foreground"]
# Wed, 01 Apr 2020 05:38:51 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Wed, 01 Apr 2020 05:38:52 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 01 Apr 2020 05:38:52 GMT
RUN a2enmod rewrite
# Wed, 01 Apr 2020 05:40:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Apr 2020 05:40:18 GMT
VOLUME [/var/www/html]
# Wed, 01 Apr 2020 05:40:18 GMT
ENV JOOMLA_VERSION=3.9.16
# Wed, 01 Apr 2020 05:40:18 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Wed, 01 Apr 2020 05:40:22 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 01 Apr 2020 05:40:23 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Wed, 01 Apr 2020 05:40:23 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 01 Apr 2020 05:40:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 05:40:23 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a635b94b3b9b333c4d1cd96e98335cf3da4cb038b56cd018d94742ef70aa725`  
		Last Modified: Tue, 31 Mar 2020 20:16:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf28be682a33b9533ee39fe019dd86455927b1717cec97319ee97496a0b74521`  
		Last Modified: Tue, 31 Mar 2020 20:16:45 GMT  
		Size: 76.7 MB (76651640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7118ab6e5511a8508001b21372cd6b33c9f8a8ecc1dea2db7a7fd62585f9f5d`  
		Last Modified: Tue, 31 Mar 2020 20:16:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925f628a16b817c5336f10d4305fe9d19242fed429a9c98e4c08d78afa3601c3`  
		Last Modified: Tue, 31 Mar 2020 20:17:12 GMT  
		Size: 18.7 MB (18675935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77cff9973b5f4e12bc65f581fd3c2c81bcd6665f08f695cdb5701db0e62ab4a`  
		Last Modified: Tue, 31 Mar 2020 20:17:08 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4f44173a15a134b1c2a86d7a7243e4ddf44366444ee130e1a6d6cb29c5cbbf`  
		Last Modified: Tue, 31 Mar 2020 20:17:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bd6c436ae3d2b5cd0a6b23278dba181b4944d937577b5241064fb9f12cb543`  
		Last Modified: Tue, 31 Mar 2020 20:18:20 GMT  
		Size: 12.5 MB (12452107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399316af3112cfd4f57b56b0a7fbf3b49266a80d99e46ddeebeb4e5dce6f9089`  
		Last Modified: Tue, 31 Mar 2020 20:18:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cea11f54c613581880eb3e95dc5297b76709b5893d934789fa9b181d80df5b6`  
		Last Modified: Tue, 31 Mar 2020 20:18:21 GMT  
		Size: 14.1 MB (14081273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebb66998d8fd22c15a48e5b8509959210a9ec648b1bf4385f96c880b06311f3`  
		Last Modified: Tue, 31 Mar 2020 20:18:16 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac288a1a6e08bd1b3a1de209aab271d9a2263bb770a6dc056a0cbd07db239cf8`  
		Last Modified: Tue, 31 Mar 2020 20:18:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776d750cfd59ef65a94fd83d9d30f9527303e9a7a28fd66358f6a4967edcc89e`  
		Last Modified: Tue, 31 Mar 2020 20:18:17 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a997f5c2f033b0dca54a4afba885db22977c8f903ca0a7603927558001b1e92d`  
		Last Modified: Tue, 31 Mar 2020 20:18:16 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891f892f9dfe087c87c44446f5354097dbd5c9a7d3cbff56423fa3242822a08a`  
		Last Modified: Wed, 01 Apr 2020 05:46:31 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1863bfc93b80fa3b435e9e51e53115a744a79ff3470099e62f6b665d33b83150`  
		Last Modified: Wed, 01 Apr 2020 05:46:31 GMT  
		Size: 3.4 MB (3443557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e812ad7bc30c6776e69f1dbb8a1b59935f84678137eaf8c3624b9ed9fc2872`  
		Last Modified: Wed, 01 Apr 2020 05:46:33 GMT  
		Size: 9.7 MB (9653480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295e58c016ed692fb75c6d69a32a13a40464d5f63cb040155002546e299dc802`  
		Last Modified: Wed, 01 Apr 2020 05:46:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8537c0e24a4084fb5aa3635f7aa540c137420012221ec90f3ffb0b971a67c8f`  
		Last Modified: Wed, 01 Apr 2020 05:46:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.3` - linux; arm variant v5

```console
$ docker pull joomla@sha256:92e1f9c781ea6a2e2b7b6526ea9b0fa3fda085aaa58b7bb298a0d8a33c4427c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140144421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59248d77f05478ed1ef10f89b670e0d44ddb540057f8db244ffdf0c59dbc758f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 00:50:14 GMT
ADD file:761a556ec2a7d8c742c860e429c9b9ba3f7abfcd9383c6b3767499de6dcad4bc in / 
# Thu, 16 Apr 2020 00:50:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:40:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 01:40:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 01:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:41:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 01:41:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 01:45:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 16 Apr 2020 01:45:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 16 Apr 2020 01:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 16 Apr 2020 01:46:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 16 Apr 2020 01:46:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 16 Apr 2020 01:46:17 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 16 Apr 2020 01:46:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 16 Apr 2020 01:46:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 01:46:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 01:46:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 02:03:41 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 16 Apr 2020 21:14:13 GMT
ENV PHP_VERSION=7.3.17
# Thu, 16 Apr 2020 21:14:14 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 21:14:15 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 16 Apr 2020 21:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 21:14:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 21:18:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 21:18:30 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 16 Apr 2020 21:18:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 21:18:34 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 21:18:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 21:18:36 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Apr 2020 21:18:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 16 Apr 2020 21:18:38 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 21:18:40 GMT
EXPOSE 80
# Thu, 16 Apr 2020 21:18:41 GMT
CMD ["apache2-foreground"]
# Thu, 16 Apr 2020 22:12:04 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 16 Apr 2020 22:12:05 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 16 Apr 2020 22:12:08 GMT
RUN a2enmod rewrite
# Thu, 16 Apr 2020 22:15:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:15:02 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2020 22:15:03 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 16 Apr 2020 22:15:04 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 16 Apr 2020 22:15:18 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 16 Apr 2020 22:15:21 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 16 Apr 2020 22:15:21 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 16 Apr 2020 22:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:15:24 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:600369660a591bc9594fcf333a847fe997901785f7032d3ad2822b2812c13243`  
		Last Modified: Thu, 16 Apr 2020 00:58:26 GMT  
		Size: 24.8 MB (24836437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29865f2ca7e0e64c2dbc473422a7c9d444c1daad98f5ea1299ffdafdb253129`  
		Last Modified: Thu, 16 Apr 2020 03:14:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e0065c973f6fdd11e90263bb281211d3321ceeef62f847ea256bdd6e99157`  
		Last Modified: Thu, 16 Apr 2020 03:15:14 GMT  
		Size: 58.8 MB (58799657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9576faf9c360672436dad4e93a54af59e3ceb35034f5d18a0c1a6854c672b93`  
		Last Modified: Thu, 16 Apr 2020 03:14:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7f40d7496c4fd49fcdb6b51d1fcbaab39524b7e2fb957d9703be440ca6ee2a`  
		Last Modified: Thu, 16 Apr 2020 03:15:50 GMT  
		Size: 18.0 MB (18024790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e5d3dd43902f3226a547e7336cfb4ce17b95bc16579f01f3062dfa766fff3c`  
		Last Modified: Thu, 16 Apr 2020 03:15:44 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f4532356eaaf2a4c5b847f64b7be2027ebb63eabc73538a247a6d26138ad79`  
		Last Modified: Thu, 16 Apr 2020 03:15:43 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2ad8bf307e37957c606dda2f8e27228e070a427a15fcf0dc4e4d5996b477b6`  
		Last Modified: Thu, 16 Apr 2020 21:54:35 GMT  
		Size: 12.5 MB (12452831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8b1502250c1b96b083faf478beda85d6a77cffff7ceb457ef6015b4126a671`  
		Last Modified: Thu, 16 Apr 2020 21:54:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67332260924d4e96ddc684bf89033807042e08be2f732eef62fd1f8d4f8d1da9`  
		Last Modified: Thu, 16 Apr 2020 21:54:37 GMT  
		Size: 13.1 MB (13096986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03bb65e5bf3ff38c94b660db4c0003768794044b0ddd7de49b553fb7d587210`  
		Last Modified: Thu, 16 Apr 2020 21:54:30 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95005a0c244c203ddbb823e3fcbcffe12ae5314137df06ad5bf6e622907f2f15`  
		Last Modified: Thu, 16 Apr 2020 21:54:30 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19acb01138011d392b644d2ec306b6fa3ac2e758091a63468f6ad6d505c221fa`  
		Last Modified: Thu, 16 Apr 2020 21:54:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fba3899195ec14227acdf3495c84024c1b36c907fd72e50e1b7b2abcf1d6272`  
		Last Modified: Thu, 16 Apr 2020 21:54:31 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85626686c9205518ffccd83d9facdb0233cd553e110ea446966101864be3c3b9`  
		Last Modified: Thu, 16 Apr 2020 22:28:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976710ed654e67a3d7485f428d9587fefbbce6268eadd1ac892c27bbd6a31b33`  
		Last Modified: Thu, 16 Apr 2020 22:28:15 GMT  
		Size: 3.3 MB (3272367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c5e3a9055e8b530390b03e846f0e5eb4ef8019142165b8a5bc34ceb83127ba`  
		Last Modified: Thu, 16 Apr 2020 22:28:19 GMT  
		Size: 9.7 MB (9653672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca889af983b0ed25ecdcbd3c2c00eab42ec4e3f657aae99dab66bfceed9ac1`  
		Last Modified: Thu, 16 Apr 2020 22:28:13 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aa052496d372ca932b2a7a4bf90e6cc0fc5c2398f6cca58befa95645d6d8cd`  
		Last Modified: Thu, 16 Apr 2020 22:28:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.3` - linux; arm variant v7

```console
$ docker pull joomla@sha256:0208e77f72b74d8b8126e2c7eda267e5f6dfb950830e6182a925c6c038f105dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137361755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d8b469cf1106c3d5365d27be1478dace958eb5f000f1f5c20f9e91252be97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 31 Mar 2020 01:48:12 GMT
ADD file:8c3ed0df404a6bcaf7583e71796cb4c1f40e87288953a21d4ee5946079c3274f in / 
# Tue, 31 Mar 2020 01:48:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 17:53:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 31 Mar 2020 17:53:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 31 Mar 2020 17:54:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 17:54:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 31 Mar 2020 17:54:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 31 Mar 2020 17:58:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 31 Mar 2020 17:58:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 31 Mar 2020 17:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 31 Mar 2020 17:58:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 31 Mar 2020 17:58:37 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 31 Mar 2020 17:58:38 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 31 Mar 2020 17:58:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 31 Mar 2020 17:58:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 17:58:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 17:58:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 31 Mar 2020 18:15:37 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 31 Mar 2020 18:15:38 GMT
ENV PHP_VERSION=7.3.16
# Tue, 31 Mar 2020 18:15:39 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.16.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.16.tar.xz.asc/from/this/mirror
# Tue, 31 Mar 2020 18:15:40 GMT
ENV PHP_SHA256=91aaee3dbdc71b69b4f3292f9d99211172a2fa926c3f3bbdb0e85dab03dd2bcb PHP_MD5=
# Tue, 31 Mar 2020 18:15:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 31 Mar 2020 18:15:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 31 Mar 2020 18:18:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 31 Mar 2020 18:18:49 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Tue, 31 Mar 2020 18:18:51 GMT
RUN docker-php-ext-enable sodium
# Tue, 31 Mar 2020 18:18:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 31 Mar 2020 18:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 31 Mar 2020 18:18:56 GMT
STOPSIGNAL SIGWINCH
# Tue, 31 Mar 2020 18:18:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 31 Mar 2020 18:18:57 GMT
WORKDIR /var/www/html
# Tue, 31 Mar 2020 18:18:58 GMT
EXPOSE 80
# Tue, 31 Mar 2020 18:18:59 GMT
CMD ["apache2-foreground"]
# Wed, 01 Apr 2020 04:08:44 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Wed, 01 Apr 2020 04:08:44 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 01 Apr 2020 04:08:47 GMT
RUN a2enmod rewrite
# Wed, 01 Apr 2020 04:11:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Apr 2020 04:11:30 GMT
VOLUME [/var/www/html]
# Wed, 01 Apr 2020 04:11:31 GMT
ENV JOOMLA_VERSION=3.9.16
# Wed, 01 Apr 2020 04:11:32 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Wed, 01 Apr 2020 04:11:42 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 01 Apr 2020 04:11:44 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Wed, 01 Apr 2020 04:11:45 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 01 Apr 2020 04:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 04:11:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:98098fa10651fdba12c848231b7428536a120e17637f1f9e0d25c63880483fcc`  
		Last Modified: Tue, 31 Mar 2020 01:56:24 GMT  
		Size: 22.7 MB (22699731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3a4f77e788058d571960904abb2aaf539bcd4ee222e1ab1e5abaac4660fd1c`  
		Last Modified: Tue, 31 Mar 2020 19:19:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1be72eb733d9ee3464150940f8a22f392a6bb1304cea60acb55d9836f88a3`  
		Last Modified: Tue, 31 Mar 2020 19:19:25 GMT  
		Size: 59.5 MB (59501945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e98e55feaf1dde506a1a5a8c8c207bd74c5d181aef4b94d51dc0e5ce1d8448e`  
		Last Modified: Tue, 31 Mar 2020 19:19:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb25ac5f5e56642a6bb2058512a520a97cf3bb444f3cac017792962b8ff3d3c`  
		Last Modified: Tue, 31 Mar 2020 19:19:59 GMT  
		Size: 17.5 MB (17481880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9b15da8e93d7911e223531ddb8beb155982d37b948eb4dbe39802e6ee6886e`  
		Last Modified: Tue, 31 Mar 2020 19:19:53 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a6984c1378c8495949f28ff95610c188a725dd10117d39c42909b41baa9321`  
		Last Modified: Tue, 31 Mar 2020 19:19:53 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be0883542f5a2aaca7f6b8433a3391019797339008ae2848307c36ec1b058aa`  
		Last Modified: Tue, 31 Mar 2020 19:21:39 GMT  
		Size: 12.5 MB (12450146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf5a2b755d1d9b8c10f96a1a49771a67d606f0aad5f0a088cea28e9d14f7fbe`  
		Last Modified: Tue, 31 Mar 2020 19:21:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b992340978a48e13feeec8cd7bfd8f550e88c9f16d7b649f269791c863f3347`  
		Last Modified: Tue, 31 Mar 2020 19:21:39 GMT  
		Size: 12.4 MB (12389540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bb8f84a220e0455d0886ff8710036972a363cbae2651420c84c0714428c407`  
		Last Modified: Tue, 31 Mar 2020 19:21:35 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd481e9e9cc96984681e03dfe34ffb6cf7d163bf392648069ad382b48edaee6`  
		Last Modified: Tue, 31 Mar 2020 19:21:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228d40ddce7c07bb17008e2e9a4921fae2133e4761b283fa6bb7fbadafb05570`  
		Last Modified: Tue, 31 Mar 2020 19:21:35 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df1c014245cf3eb64c542262a6070fc40608d9768c249dfc00fd3048ab7081a`  
		Last Modified: Tue, 31 Mar 2020 19:21:35 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e0349c5361bf648c9d8417d80c872bfc936f6fed5897ee738948e20da045d7`  
		Last Modified: Wed, 01 Apr 2020 04:23:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e4c858a2cb8421581498113447eaa1957569e18bac059a0a858baa08124685`  
		Last Modified: Wed, 01 Apr 2020 04:23:21 GMT  
		Size: 3.2 MB (3177167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f6a203e4ba461173f9240a9cf38f4f21ba40d1d6f93485341460514c5f5ee9`  
		Last Modified: Wed, 01 Apr 2020 04:23:26 GMT  
		Size: 9.7 MB (9653676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199c171b7766ec2820e6ba0631227f1ad1a4e713e1493c45dafc408740aa3cdb`  
		Last Modified: Wed, 01 Apr 2020 04:23:20 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5c89396caba4b6e220f2a109fe507987b36d6182f107ae07869954f88e8c0`  
		Last Modified: Wed, 01 Apr 2020 04:23:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.3` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:4998db7bd3ee388b9f260afdc47fcd64ac50b648ea53b94c55917104fa18343a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154032026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31174e9cd4842e016e0bf09dd5ebadac0be3dc6b1ebecb8c7740a3b86e092550`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 13:31:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 13:31:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 13:32:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 13:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 13:32:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 13:36:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 16 Apr 2020 13:36:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 16 Apr 2020 13:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 16 Apr 2020 13:36:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 16 Apr 2020 13:36:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 16 Apr 2020 13:36:53 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 16 Apr 2020 13:36:54 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 16 Apr 2020 13:36:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 13:36:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 13:36:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 13:55:49 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 16 Apr 2020 13:55:50 GMT
ENV PHP_VERSION=7.3.16
# Thu, 16 Apr 2020 13:55:51 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.16.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.16.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 13:55:52 GMT
ENV PHP_SHA256=91aaee3dbdc71b69b4f3292f9d99211172a2fa926c3f3bbdb0e85dab03dd2bcb PHP_MD5=
# Thu, 16 Apr 2020 13:56:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 13:56:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 13:59:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 13:59:10 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 16 Apr 2020 13:59:12 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 13:59:14 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 13:59:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 13:59:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Apr 2020 13:59:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 16 Apr 2020 13:59:17 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 13:59:18 GMT
EXPOSE 80
# Thu, 16 Apr 2020 13:59:18 GMT
CMD ["apache2-foreground"]
# Fri, 17 Apr 2020 01:02:08 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 17 Apr 2020 01:02:08 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 17 Apr 2020 01:02:11 GMT
RUN a2enmod rewrite
# Fri, 17 Apr 2020 01:04:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 01:04:53 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2020 01:04:54 GMT
ENV JOOMLA_VERSION=3.9.16
# Fri, 17 Apr 2020 01:04:55 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Fri, 17 Apr 2020 01:05:05 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 17 Apr 2020 01:05:08 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 17 Apr 2020 01:05:09 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 17 Apr 2020 01:05:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2020 01:05:10 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fdd0b0f5914e23b97e6b4c85e72419571f773834e9c5d730f39161697995d`  
		Last Modified: Thu, 16 Apr 2020 15:02:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc35f6808c49c804fbb7d49d5dc0cfb27df6b557216ae986e2d002c542c78b`  
		Last Modified: Thu, 16 Apr 2020 15:02:46 GMT  
		Size: 70.3 MB (70334995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d50046d41b1b2f8266660f05392abbe78af7f9798529c7b42d0860191555ea`  
		Last Modified: Thu, 16 Apr 2020 15:02:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23de6fdfa90633474f20febad6133bad0c1bc54b43105ed202fa306cb5cdfc28`  
		Last Modified: Thu, 16 Apr 2020 15:03:17 GMT  
		Size: 18.6 MB (18579332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1378fe9a3357949505b13edf6a5dcea2f352618b16718f2e8131ba6d94860255`  
		Last Modified: Thu, 16 Apr 2020 15:03:12 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81270616b79c7f0407fadba4df6ef4c3ca58c1c0caacb960ca558ede42411157`  
		Last Modified: Thu, 16 Apr 2020 15:03:12 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e1f9ea75e63d371afe4b5b0084ac11464d88068a50f87d3f7354eef7f673cd`  
		Last Modified: Thu, 16 Apr 2020 15:04:48 GMT  
		Size: 12.5 MB (12450919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c1cadc0c3b3f75b130765e4af7ae7cddc32babedafe073a6823074e0eff65e`  
		Last Modified: Thu, 16 Apr 2020 15:04:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f20e4e0eae148e4acc736c26cfd932776f4f206436dd5ff64757039b32cf09`  
		Last Modified: Thu, 16 Apr 2020 15:04:49 GMT  
		Size: 13.8 MB (13765899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a92db8a2717e6ed01c3c4d38b75fcd7dbbe3d65c6efc11b19ed612bddfda4a`  
		Last Modified: Thu, 16 Apr 2020 15:04:45 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096409a2bd3a8e969d74b9560ad9449998eadc92e025a9986356b8b9bbef717a`  
		Last Modified: Thu, 16 Apr 2020 15:04:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44f76faae955ac338233a43a4e2e229d24590c87fe531e18dde200e6e0cb877`  
		Last Modified: Thu, 16 Apr 2020 15:04:45 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee2ba3698cf25eaba7e6ffb350d4eb2205afa48f3d9bf4c48fd776aaa20ac73`  
		Last Modified: Thu, 16 Apr 2020 15:04:44 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6f285f230045546f42d630a8172606ab5b4bcf4382567fb7e9d508091520f0`  
		Last Modified: Fri, 17 Apr 2020 01:16:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26aa78ae152da791da331c35dbc3c75c591b695621cf872f2a48992f55c93c3`  
		Last Modified: Fri, 17 Apr 2020 01:16:47 GMT  
		Size: 3.4 MB (3381828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584544e26cb90feb22a4edbe653e99ced4b69efc60a72683ad4bce93d23b4b1b`  
		Last Modified: Fri, 17 Apr 2020 01:16:51 GMT  
		Size: 9.7 MB (9653675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193fa03a08930abbe56cfd7b25d0256df7e1837525c5c1f0f33f44df490da592`  
		Last Modified: Fri, 17 Apr 2020 01:16:46 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c27f0b26e49170a3d5b91943be1344eba217b088c69be03c02370f79caa8fa`  
		Last Modified: Fri, 17 Apr 2020 01:16:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.3` - linux; 386

```console
$ docker pull joomla@sha256:c3c9e86c024e9704a21edaf44a47067b05b21a72c4cf627e7dbd544a68e2e9e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168035210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5fc0a3a5e2227cc1b27e4546119ac0433fc9562a18fab6e5c1ad3487237da4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 11:42:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 11:42:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 11:42:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 11:42:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 11:42:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 11:50:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 16 Apr 2020 11:50:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 16 Apr 2020 11:51:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 16 Apr 2020 11:51:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 16 Apr 2020 11:51:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 16 Apr 2020 11:51:08 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 16 Apr 2020 11:51:08 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 16 Apr 2020 11:51:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 11:51:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 11:51:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 12:23:43 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 16 Apr 2020 12:23:43 GMT
ENV PHP_VERSION=7.3.16
# Thu, 16 Apr 2020 12:23:43 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.16.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.16.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 12:23:43 GMT
ENV PHP_SHA256=91aaee3dbdc71b69b4f3292f9d99211172a2fa926c3f3bbdb0e85dab03dd2bcb PHP_MD5=
# Thu, 16 Apr 2020 12:23:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 12:23:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 12:29:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 12:29:23 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 16 Apr 2020 12:29:24 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 12:29:25 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 12:29:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 12:29:26 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Apr 2020 12:29:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 16 Apr 2020 12:29:27 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 12:29:27 GMT
EXPOSE 80
# Thu, 16 Apr 2020 12:29:27 GMT
CMD ["apache2-foreground"]
# Thu, 16 Apr 2020 20:42:17 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 16 Apr 2020 20:42:18 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 16 Apr 2020 20:42:18 GMT
RUN a2enmod rewrite
# Thu, 16 Apr 2020 20:43:58 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 20:43:58 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2020 20:43:58 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 16 Apr 2020 20:43:58 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 16 Apr 2020 20:44:04 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 16 Apr 2020 20:44:04 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 16 Apr 2020 20:44:05 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 16 Apr 2020 20:44:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 20:44:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580962e9450ca1b5ce83bb772724b2d0ccb693fcb5621a2a183d4c4b623bdd79`  
		Last Modified: Thu, 16 Apr 2020 14:27:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e05ab240d5a6be86c4185445fb618f19bc1ac549f84f9ac7e70049e8c8bd9b9`  
		Last Modified: Thu, 16 Apr 2020 14:27:53 GMT  
		Size: 81.2 MB (81198973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328115a893c2014f3e46294f0eb8907d40cd3ffd4b14b93a13046d46e12225fb`  
		Last Modified: Thu, 16 Apr 2020 14:27:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b372ccf1ce987aca608913169496741248e10c975ad0fe5e5027b9843b19b0`  
		Last Modified: Thu, 16 Apr 2020 14:28:22 GMT  
		Size: 19.1 MB (19112643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a0b2cd566927df88f664663ed6e414866b210a9875ba628efd69392e069374`  
		Last Modified: Thu, 16 Apr 2020 14:28:14 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6701f205fc001f4b424b149c5e9467bf8ca61305a1addc3394f63bde57f1574c`  
		Last Modified: Thu, 16 Apr 2020 14:28:14 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c51295217457ee472b2f70177ba6ff37eb9667618846f4524487d11c39d7a0`  
		Last Modified: Thu, 16 Apr 2020 14:29:36 GMT  
		Size: 12.5 MB (12451387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c9fd2943cc3f09f2542f446cc3e98e8e75ce48710f1b3578a401d572e2e12c`  
		Last Modified: Thu, 16 Apr 2020 14:29:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e31ede7cb9368a16ac329e742ecb00a4918b4a7395f1651764b7a2383b710`  
		Last Modified: Thu, 16 Apr 2020 14:29:38 GMT  
		Size: 14.4 MB (14405319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f40e8b7aa6bca2967107b64b524a31d86a5a99b5fcff9c06025b5b18fc6bc3`  
		Last Modified: Thu, 16 Apr 2020 14:29:34 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a55bb5c4e0e409ac3b53c8a90cb17560410faa84260b4f142ea0443415b3e9`  
		Last Modified: Thu, 16 Apr 2020 14:29:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c8e0f22153d174189b88ab8acc4ef0d3251cfaba9177151060957fd190ac60`  
		Last Modified: Thu, 16 Apr 2020 14:29:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97afa9056c76021b072b20a07f1fbab4428a6a172ba9a210c68ee176108ff54`  
		Last Modified: Thu, 16 Apr 2020 14:29:33 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8c52c546792238ee269567d275f01d1b2a99e2592ad9958b0dc2989c16b90d`  
		Last Modified: Thu, 16 Apr 2020 20:51:47 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f0c35e9d51c064fb20af1f52a1549996b7d6674a33ae7eeb87472854b31fe7`  
		Last Modified: Thu, 16 Apr 2020 20:51:48 GMT  
		Size: 3.5 MB (3451874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f01e13c0198611b8897af6a6ed87a10b77de6ffb5d7ebe16c8197573ae43be`  
		Last Modified: Thu, 16 Apr 2020 20:51:51 GMT  
		Size: 9.7 MB (9653493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b5d2c301c5af288a679b77a515aeda586365380cc40810bdd3e7f173ed708`  
		Last Modified: Thu, 16 Apr 2020 20:51:47 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f7bed9ae4a894d6aaed56979900428d239937ae1f867f11c1a8e42df7a7777`  
		Last Modified: Thu, 16 Apr 2020 20:51:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.3` - linux; ppc64le

```console
$ docker pull joomla@sha256:5289c7effe76c95d3e89f4fb1dc80721ad51488618abb3c982ed573f8512cc8f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173457410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14aebf7889e90c4bc1225efc83cb414540fc55c99cdfa163b8f041fd78bd2b71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:42 GMT
ADD file:36c02e92574faba45b64cfed78a0a0359d65ad175b17128bf554a2a5c0086ff5 in / 
# Tue, 31 Mar 2020 01:32:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 18:20:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 31 Mar 2020 18:20:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 31 Mar 2020 18:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:23:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 31 Mar 2020 18:23:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 31 Mar 2020 18:30:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 31 Mar 2020 18:30:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 31 Mar 2020 18:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 31 Mar 2020 18:31:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 31 Mar 2020 18:31:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 31 Mar 2020 18:31:44 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 31 Mar 2020 18:31:47 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 31 Mar 2020 18:31:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:31:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:31:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 31 Mar 2020 18:57:22 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 31 Mar 2020 18:57:25 GMT
ENV PHP_VERSION=7.3.16
# Tue, 31 Mar 2020 18:57:28 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.16.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.16.tar.xz.asc/from/this/mirror
# Tue, 31 Mar 2020 18:57:31 GMT
ENV PHP_SHA256=91aaee3dbdc71b69b4f3292f9d99211172a2fa926c3f3bbdb0e85dab03dd2bcb PHP_MD5=
# Tue, 31 Mar 2020 18:58:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 31 Mar 2020 18:58:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 31 Mar 2020 19:03:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 31 Mar 2020 19:03:56 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Tue, 31 Mar 2020 19:04:05 GMT
RUN docker-php-ext-enable sodium
# Tue, 31 Mar 2020 19:04:14 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 31 Mar 2020 19:04:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 31 Mar 2020 19:04:21 GMT
STOPSIGNAL SIGWINCH
# Tue, 31 Mar 2020 19:04:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 31 Mar 2020 19:04:27 GMT
WORKDIR /var/www/html
# Tue, 31 Mar 2020 19:04:31 GMT
EXPOSE 80
# Tue, 31 Mar 2020 19:04:34 GMT
CMD ["apache2-foreground"]
# Wed, 01 Apr 2020 06:11:07 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Wed, 01 Apr 2020 06:11:10 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 01 Apr 2020 06:11:16 GMT
RUN a2enmod rewrite
# Wed, 01 Apr 2020 06:13:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Apr 2020 06:13:45 GMT
VOLUME [/var/www/html]
# Wed, 01 Apr 2020 06:13:48 GMT
ENV JOOMLA_VERSION=3.9.16
# Wed, 01 Apr 2020 06:13:51 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Wed, 01 Apr 2020 06:14:03 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 01 Apr 2020 06:14:07 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Wed, 01 Apr 2020 06:14:08 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 01 Apr 2020 06:14:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2020 06:14:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9df6bbae5eeb29e9aac2f39cff517c694cce60f01ee477abcdedcd8e8c01c38f`  
		Last Modified: Tue, 31 Mar 2020 01:45:59 GMT  
		Size: 30.5 MB (30518493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5f2c37c0de46cda2befedd3876fc78801a15be2dce4b0116818a7aab35c04`  
		Last Modified: Tue, 31 Mar 2020 20:47:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e114e9ba1490fcf41258b1a701ea45b783428085bf612daa8bda0e94cf1504`  
		Last Modified: Tue, 31 Mar 2020 20:48:04 GMT  
		Size: 82.3 MB (82259910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ab407be0c6f406f88af833d569c84d8ec441c22d3a940bb0db5abd2d137bf`  
		Last Modified: Tue, 31 Mar 2020 20:47:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef62b8c23875df996ec568583435b349d42fc879b097a532f224186e0162e8`  
		Last Modified: Tue, 31 Mar 2020 20:49:05 GMT  
		Size: 19.8 MB (19812915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b549995527d9f02c9204fd560a9070a90770917f6bef449e1f1ded64972809e0`  
		Last Modified: Tue, 31 Mar 2020 20:48:55 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60860dcdbae0ac57fabbcc292f19ad63b7a0cd3812f799d67a34b7449f15c863`  
		Last Modified: Tue, 31 Mar 2020 20:48:54 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f40527e3cf85a4d9d6a53109d000f07dcb04c19d1f21015023d8a2c0e1a3201`  
		Last Modified: Tue, 31 Mar 2020 20:51:41 GMT  
		Size: 12.5 MB (12452221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b42e672a2238c6dd0fe153dd779fcf99f00e447d64d14e8fcc5a004ffaf7b`  
		Last Modified: Tue, 31 Mar 2020 20:51:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6e9345c4a88f8f35b286262a1b5afcdd69124d2e0a2b2732df8ede872c8184`  
		Last Modified: Tue, 31 Mar 2020 20:51:41 GMT  
		Size: 15.1 MB (15126182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad45f61d76d82a870625510416aa99794c75fb0848eacbb477ba6f063760d5cc`  
		Last Modified: Tue, 31 Mar 2020 20:51:36 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd9b59a7a500740d45bd9dae2dc1b9a4af819f3860a55e72f8f77c2707758f3`  
		Last Modified: Tue, 31 Mar 2020 20:51:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5b471cc2c461025e696bf111be12e2a70823a89c26cc6211fa13aff22afea4`  
		Last Modified: Tue, 31 Mar 2020 20:51:36 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7b0531a2d50ca58dd075190f770ddbf3671fd9a622ca08099316b06d25a654`  
		Last Modified: Tue, 31 Mar 2020 20:51:36 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48758425f319f0e0fe95f1812feacf2c588749799f6e0bdbe1f38093a8bb4cab`  
		Last Modified: Wed, 01 Apr 2020 06:28:31 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69da8f2279a9359c8c8ea76159632e569ec82d0b20cab0e9848e5d5f1fcaa561`  
		Last Modified: Wed, 01 Apr 2020 06:28:34 GMT  
		Size: 3.6 MB (3626329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a270af2772e0157afbdab5001270ed8e9fc3a3dcd24b017b2098675f6fc7f380`  
		Last Modified: Wed, 01 Apr 2020 06:28:34 GMT  
		Size: 9.7 MB (9653677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055da39e66f706371f2fb3f4294b70006bb821d7ef447c0e886693b27b05e477`  
		Last Modified: Wed, 01 Apr 2020 06:28:31 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b09daf9ad5b192c1489f494952040fa3d1600382381e7a45ae546ab2ad81a36`  
		Last Modified: Wed, 01 Apr 2020 06:28:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.3` - linux; s390x

```console
$ docker pull joomla@sha256:dcb9e9ffe0bc4f04d642e4b1ea75f50f1b200574360bbd410b161ffaa9974c4b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147772404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1452fc25776ef47b5aadb09dca11886f7772c023e5eb81d00038b2b969b4f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 00:42:19 GMT
ADD file:f328b5d6dce2eaf00360542c1e3280958b818268b9150b12ffd1fddf030daf2f in / 
# Thu, 16 Apr 2020 00:42:20 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 05:27:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 05:27:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 05:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 05:27:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 05:29:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 16 Apr 2020 05:29:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 16 Apr 2020 05:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 16 Apr 2020 05:29:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 16 Apr 2020 05:29:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 16 Apr 2020 05:29:52 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 16 Apr 2020 05:29:52 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 16 Apr 2020 05:29:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 05:29:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 05:29:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 05:39:22 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 16 Apr 2020 21:31:49 GMT
ENV PHP_VERSION=7.3.17
# Thu, 16 Apr 2020 21:31:50 GMT
ENV PHP_URL=https://www.php.net/get/php-7.3.17.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.3.17.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 21:31:50 GMT
ENV PHP_SHA256=6a30304c27f7e7a94538f5ffec599f600ee93aedbbecad8aa4f8bec539b10ad8 PHP_MD5=
# Thu, 16 Apr 2020 21:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 21:31:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 21:33:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 21:33:18 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 16 Apr 2020 21:33:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 21:33:19 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 21:33:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 21:33:19 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Apr 2020 21:33:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 16 Apr 2020 21:33:20 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 21:33:20 GMT
EXPOSE 80
# Thu, 16 Apr 2020 21:33:20 GMT
CMD ["apache2-foreground"]
# Thu, 16 Apr 2020 23:12:36 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 16 Apr 2020 23:12:36 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 16 Apr 2020 23:12:37 GMT
RUN a2enmod rewrite
# Thu, 16 Apr 2020 23:13:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 23:13:41 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2020 23:13:41 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 16 Apr 2020 23:13:41 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 16 Apr 2020 23:13:45 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 16 Apr 2020 23:13:46 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 16 Apr 2020 23:13:47 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 16 Apr 2020 23:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 23:13:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:043f95f5412a986fb082b0193860bb9c0388c2fbcb5e8bf5bcbbeefb0e45c9c5`  
		Last Modified: Thu, 16 Apr 2020 00:46:19 GMT  
		Size: 25.7 MB (25712234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ddfa1fc602c1136eb18c12346e7ff6ec839daed15acdbf1e27928616fb0563`  
		Last Modified: Thu, 16 Apr 2020 06:17:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5755aea4f019990a669880dd812da175f10c5be62eb667cd79cf541a7a6e4f94`  
		Last Modified: Thu, 16 Apr 2020 06:18:10 GMT  
		Size: 64.7 MB (64698840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a1adc7e800496f536e4039e6551bf877920e79c7f4ec02ce13156b4e3b7212`  
		Last Modified: Thu, 16 Apr 2020 06:17:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6f7d873bb87ca6d5af35da662e7353137b92a8b75928ab9ab39f3626d915db`  
		Last Modified: Thu, 16 Apr 2020 06:18:35 GMT  
		Size: 18.5 MB (18522527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cde5ec5687e94dc278aaf0154d60d85d9f7e23bb61bf94992643b9790831332`  
		Last Modified: Thu, 16 Apr 2020 06:18:31 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25615924fe0ac851b8ed9581a2bd2e0b5fe8ee1fb5f4b2541242f2fff827f59b`  
		Last Modified: Thu, 16 Apr 2020 06:18:30 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92816f74e97a81d4366fd0648dfedfb32437451ffd4a7f711fbde3c4c16fbd1e`  
		Last Modified: Thu, 16 Apr 2020 22:08:52 GMT  
		Size: 12.5 MB (12452999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9facc81c78a3d4d824b8297466505c6a05efa51f60c10b89988e15b673b06c34`  
		Last Modified: Thu, 16 Apr 2020 22:08:49 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e440608776d6ac7d2d4892d0758748cd8c5608a8c724111c9a47eebe5b353ca0`  
		Last Modified: Thu, 16 Apr 2020 22:08:49 GMT  
		Size: 13.3 MB (13319236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93cdbd2d19c69ea797917b7240743bb65da09af5241922181028be893bacd91`  
		Last Modified: Thu, 16 Apr 2020 22:08:47 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557b48ce48273958182bfc260c8aca58744543560f9c0a9fb09ce76ca0221340`  
		Last Modified: Thu, 16 Apr 2020 22:08:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c5701305923c5539489887e43c8fc2f4394721024718211b91d61a574ee523`  
		Last Modified: Thu, 16 Apr 2020 22:08:52 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecccc57765826b020270e77b172b46d6d6bd39237a2d36abefca32977e52cd8b`  
		Last Modified: Thu, 16 Apr 2020 22:08:53 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8ab704039c3c0de327ba6515ff5fce622a18d000a16908a63d2a24c0b240f9`  
		Last Modified: Thu, 16 Apr 2020 23:21:06 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e870d0f23f6322fcb27572a568a70a233a67a950a2cff7eda12d5d9cd2c110`  
		Last Modified: Thu, 16 Apr 2020 23:21:12 GMT  
		Size: 3.4 MB (3405255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3bb5480cce1278d351e3bf50c4e4cb46ae0b0854ee1afdc8cbe1c6c2ee3d5d`  
		Last Modified: Thu, 16 Apr 2020 23:21:13 GMT  
		Size: 9.7 MB (9653672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9cb6feeba34becb93bc3312a0dc46db0764de91a03338265669e95661b3785`  
		Last Modified: Thu, 16 Apr 2020 23:21:06 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5946e81ee8ea1c868954c0fe48457d4b06aaf92608e0bf0e6a0d07a1f808f91`  
		Last Modified: Thu, 16 Apr 2020 23:21:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
