## `joomla:3-php7.2`

```console
$ docker pull joomla@sha256:73fee33862903e1e7190a1fcc5f01e43788b271a0ef545fe7ff5b9f757544088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `joomla:3-php7.2` - linux; amd64

```console
$ docker pull joomla@sha256:f562dc05c6e21ff5acd3cad9af616af77bb24a899d82b48b3e73a056b0d756d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161939870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd28ac9bb44bfabad2b5dd4fba4f31921e7018863d5da6d06cb8d8e7c79d95d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:54 GMT
ADD file:ba0c39345ccc4a882289d473ae8a67087056aa4475a26f3492fff75933d707de in / 
# Sat, 01 Feb 2020 17:20:54 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 19:26:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 01 Feb 2020 19:26:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2020 19:26:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 19:26:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2020 19:26:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 01 Feb 2020 19:34:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 01 Feb 2020 19:34:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 01 Feb 2020 19:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 01 Feb 2020 19:34:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 01 Feb 2020 19:34:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 01 Feb 2020 19:34:53 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 01 Feb 2020 19:34:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 01 Feb 2020 19:34:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 19:34:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 19:34:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 01 Feb 2020 21:03:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Sat, 01 Feb 2020 21:03:28 GMT
ENV PHP_VERSION=7.2.27
# Sat, 01 Feb 2020 21:03:28 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Sat, 01 Feb 2020 21:03:28 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Sat, 01 Feb 2020 21:03:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 01 Feb 2020 21:03:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:07:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sat, 01 Feb 2020 21:07:21 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:07:22 GMT
RUN docker-php-ext-enable sodium
# Sat, 01 Feb 2020 21:07:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sat, 01 Feb 2020 21:07:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2020 21:07:24 GMT
STOPSIGNAL SIGWINCH
# Sat, 01 Feb 2020 21:07:24 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:07:25 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2020 21:07:25 GMT
EXPOSE 80
# Sat, 01 Feb 2020 21:07:25 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 11:34:26 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Sun, 02 Feb 2020 11:34:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sun, 02 Feb 2020 11:34:28 GMT
RUN a2enmod rewrite
# Sun, 02 Feb 2020 11:36:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:36:12 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 11:36:12 GMT
ENV JOOMLA_VERSION=3.9.15
# Sun, 02 Feb 2020 11:36:12 GMT
ENV JOOMLA_SHA512=d68e32de6cfe9af92ff7f7991c9253a4487832e55e32e6f74f2b4d592a4777f3b4d8bd74dcd0b10d4262c5e39bdad1e9f7698dedb2ef2989dbc06aa7ab2f6c69
# Sun, 02 Feb 2020 11:36:17 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sun, 02 Feb 2020 11:36:17 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Sun, 02 Feb 2020 11:36:18 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Sun, 02 Feb 2020 11:36:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:36:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bc51dd8edc1b1132bb97827ed6bd16aac332b03fb03d4c02d2088067a5fbb499`  
		Last Modified: Sat, 01 Feb 2020 17:26:19 GMT  
		Size: 27.1 MB (27092260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3224e2c3a8935eadbb2b4ae8f162c5cdda9e4b5693f763d7c7fa1c4e0288374`  
		Last Modified: Sat, 01 Feb 2020 21:46:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7a066df88f078e73668ecda25e6f74ddb03c4b542565e0e8cb675fa4e25631`  
		Last Modified: Sat, 01 Feb 2020 21:47:06 GMT  
		Size: 76.7 MB (76652069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdf741d72a992e97109c02ec1f5f583127a47b1c4c054a351b96a5f259ca1ab`  
		Last Modified: Sat, 01 Feb 2020 21:46:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e612a5f04cbe3614379626ba28df5b5f7d30197db4affd84a1ae5aa873dd55`  
		Last Modified: Sat, 01 Feb 2020 21:47:25 GMT  
		Size: 18.7 MB (18675672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c026d8d0e8cbd007fbd6dde82fc9f613be9d1c064cacfee7079ba94645d74a49`  
		Last Modified: Sat, 01 Feb 2020 21:47:20 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94096c4941cb0fa6688fa291cf9dac6db7a2ae33010ceaaa723da0a26222122`  
		Last Modified: Sat, 01 Feb 2020 21:47:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9653ad58aebaf0f70958d3954cc7309f02075cc4b4ac6a924a6bfa688680b3`  
		Last Modified: Sat, 01 Feb 2020 21:50:49 GMT  
		Size: 12.6 MB (12645342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d97d51f6437220577d6e230158a1aba71795cd7cfe3dfee79b04f7ff3c2e853`  
		Last Modified: Sat, 01 Feb 2020 21:50:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad873fa227d739e3324908ab4ef17f1670635fef88cca790e84829b0d0e0055`  
		Last Modified: Sat, 01 Feb 2020 21:50:50 GMT  
		Size: 13.8 MB (13841469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933056a49e3bf50622ff26798039cddfe83e147f70dce037927cef0fe1ec9a8f`  
		Last Modified: Sat, 01 Feb 2020 21:50:46 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948195254531606300e2aa91accbe2696cd9ebb32eb87c0b5001b46df9bf4006`  
		Last Modified: Sat, 01 Feb 2020 21:50:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ab11975556b42ebc4be64d27ad1982d52a147835bfd0e3dfee47ce64eb615f`  
		Last Modified: Sat, 01 Feb 2020 21:50:47 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acb7af78b5333032a5afc779e4c32cbc372dbdb7e56bd74ac68cae8783f6e9b`  
		Last Modified: Sat, 01 Feb 2020 21:50:46 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f74263f252d513fcf84288e97e24a013f08d8968ce83f55043ea89bcb5931e3`  
		Last Modified: Sun, 02 Feb 2020 11:47:20 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa126295c379cf17b42849bc27155c6cff32ee9e00025a2f4d13f5fc02b644e`  
		Last Modified: Sun, 02 Feb 2020 11:47:21 GMT  
		Size: 3.4 MB (3373537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa1c27d8ee8d435824c49954ab077d2b1d13e7be37aa2abcee501476e670503`  
		Last Modified: Sun, 02 Feb 2020 11:47:25 GMT  
		Size: 9.7 MB (9651970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1248f111df5790f2541ae671a84dc94ee72187139d5992146a1db746e7b024cc`  
		Last Modified: Sun, 02 Feb 2020 11:47:20 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f9ab406c2c0ad41599de4c09861a031e12d3f8b874ccceb023d25124d7db6a`  
		Last Modified: Sun, 02 Feb 2020 11:47:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2` - linux; arm variant v5

```console
$ docker pull joomla@sha256:ffe31d0eb634953a42d3840a029db1b3076c95165fce3cc77e98b87973ffc23b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140075014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a7a7ad15847e400000a3365b6275ef7328ea9e421a8f8faf6c7fea81260b6e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:35 GMT
ADD file:0d515bfdb830d6d8bec1544b49cc51e696411abf2a1afbc856f406ceb5a82a6c in / 
# Sat, 01 Feb 2020 16:50:36 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 20:53:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 01 Feb 2020 20:53:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 01 Feb 2020 20:54:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 20:54:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 01 Feb 2020 20:54:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 01 Feb 2020 20:58:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 01 Feb 2020 20:58:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 01 Feb 2020 20:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 01 Feb 2020 20:58:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 01 Feb 2020 20:59:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 01 Feb 2020 20:59:02 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 01 Feb 2020 20:59:03 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 01 Feb 2020 20:59:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 20:59:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 01 Feb 2020 20:59:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 01 Feb 2020 21:51:49 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 20 Feb 2020 22:55:19 GMT
ENV PHP_VERSION=7.2.28
# Thu, 20 Feb 2020 22:55:20 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.28.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.28.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 22:55:21 GMT
ENV PHP_SHA256=afe1863301da572dee2e0bad8014813bcced162f980ddc8ec8e41fd72263eb2d PHP_MD5=
# Thu, 20 Feb 2020 22:55:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Feb 2020 22:55:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 22:59:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:59:29 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 22:59:32 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 20 Feb 2020 22:59:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 22:59:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Feb 2020 22:59:35 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:59:35 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 22:59:36 GMT
EXPOSE 80
# Thu, 20 Feb 2020 22:59:37 GMT
CMD ["apache2-foreground"]
# Fri, 21 Feb 2020 02:52:50 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 21 Feb 2020 02:52:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 21 Feb 2020 02:52:53 GMT
RUN a2enmod rewrite
# Fri, 21 Feb 2020 02:56:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 02:56:06 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 02:56:07 GMT
ENV JOOMLA_VERSION=3.9.15
# Fri, 21 Feb 2020 02:56:08 GMT
ENV JOOMLA_SHA512=d68e32de6cfe9af92ff7f7991c9253a4487832e55e32e6f74f2b4d592a4777f3b4d8bd74dcd0b10d4262c5e39bdad1e9f7698dedb2ef2989dbc06aa7ab2f6c69
# Fri, 21 Feb 2020 02:56:19 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 21 Feb 2020 02:56:22 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 21 Feb 2020 02:56:26 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 21 Feb 2020 02:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Feb 2020 02:56:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1a225882fe3b547848dd2414c8996683ea413873930a1f3a7dcb241e14fe3e85`  
		Last Modified: Sat, 01 Feb 2020 16:57:06 GMT  
		Size: 24.8 MB (24829678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c45ccccae36b11824d60e44524af7b6fa50071e3d611d84cb304dd77defab8`  
		Last Modified: Sat, 01 Feb 2020 22:23:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bb0996b6fdaded26517b7c76776a1a9c8884099f10dedce0542539497f118b`  
		Last Modified: Sat, 01 Feb 2020 22:23:37 GMT  
		Size: 58.8 MB (58799601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd04cf71e89913a06b80581e3e995075f83ad72367a777cf4c4eab806021fe5`  
		Last Modified: Sat, 01 Feb 2020 22:23:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131ace4e4c27b550d591879f80b8d52452f9fb96584693afcdd334cd25b25daf`  
		Last Modified: Sat, 01 Feb 2020 22:24:11 GMT  
		Size: 18.0 MB (18024313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130915aaebc420917f4f14f8952cd199a41fac46229026cb258b43fa35ea551e`  
		Last Modified: Sat, 01 Feb 2020 22:24:05 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483a3e1d1b8476aefea9a00f5659a69afd0524cd25d601bfd6a360d517e07288`  
		Last Modified: Sat, 01 Feb 2020 22:24:05 GMT  
		Size: 518.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6870d15f4436edea4966cab46408f84da08174eb85521634ab8486bbef4ed7f7`  
		Last Modified: Thu, 20 Feb 2020 23:37:16 GMT  
		Size: 12.6 MB (12648485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1828a3d8dd7400274aed0b158c570b4fd9b81e6bd36ea1882e5edce64c680201`  
		Last Modified: Thu, 20 Feb 2020 23:37:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86162dd6fe125d4d6b41730be67abffe9a0d5f7813b24ca7873f85a2eba45320`  
		Last Modified: Thu, 20 Feb 2020 23:37:17 GMT  
		Size: 12.9 MB (12920411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a52c49bb2e645091cb4c5d412f30ca2a6fc2005702633aeda4b3d6847a0deb`  
		Last Modified: Thu, 20 Feb 2020 23:37:12 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd67246be5ea9d9045209203790beaa13bcfdb28c59fb32c42e0be08a767c70`  
		Last Modified: Thu, 20 Feb 2020 23:37:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3409fe05f6e53982a3c4fa7948f6d95f7914a53cefb06e2df832601545733f4`  
		Last Modified: Thu, 20 Feb 2020 23:37:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b092117a535331880a6acf12f6df8b8d5f6d5bdde549ca33a2afdc16925450`  
		Last Modified: Thu, 20 Feb 2020 23:37:12 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c93d9f2ec7fc62ea679f00af964b5c9c3865ee53af854763f518ff679f0b2f`  
		Last Modified: Fri, 21 Feb 2020 03:15:11 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b0102215d98e86436602982998170dd9b27fd301b82dff63def734dc9ea7ab`  
		Last Modified: Fri, 21 Feb 2020 03:15:11 GMT  
		Size: 3.2 MB (3192897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438fac52b19f5645becaf2be5e34fae80849a550f30694c2fc298c9072b55a00`  
		Last Modified: Fri, 21 Feb 2020 03:15:16 GMT  
		Size: 9.7 MB (9651956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736ae2b349ad184d117cd7d1139293b5765993f88e162aa84557404c2b0fc371`  
		Last Modified: Fri, 21 Feb 2020 03:15:11 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da228127b45d1a1f4b6ddfd5dac7b8bae8c4a06ecfadfbdd4f8b4cb7cb897fe`  
		Last Modified: Fri, 21 Feb 2020 03:15:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2` - linux; arm variant v7

```console
$ docker pull joomla@sha256:a8a2dcb7b47daa65dcc5da9575e0e02990fb23483104ace026e6c6ce596375ad
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137288887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4be8d184b5174964935aa4639435142f22c2ed410ba0b4ad79b8af7152259ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:28 GMT
ADD file:8658fd39d2726b84ace6e940a73e3f5fdf03b339f01e8cca3166e44abe3f9ac3 in / 
# Sat, 01 Feb 2020 17:00:29 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:58:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 00:58:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 00:59:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:59:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 00:59:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 01:03:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 01:03:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 01:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 01:04:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 01:04:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 01:04:08 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 01:04:08 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 01:04:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 01:04:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 01:04:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 01:55:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 20 Feb 2020 22:26:18 GMT
ENV PHP_VERSION=7.2.28
# Thu, 20 Feb 2020 22:26:20 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.28.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.28.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 22:26:21 GMT
ENV PHP_SHA256=afe1863301da572dee2e0bad8014813bcced162f980ddc8ec8e41fd72263eb2d PHP_MD5=
# Thu, 20 Feb 2020 22:26:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Feb 2020 22:26:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:31:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 22:31:31 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:31:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 22:31:40 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 20 Feb 2020 22:31:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 22:31:42 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Feb 2020 22:31:42 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 20 Feb 2020 22:31:43 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 22:31:44 GMT
EXPOSE 80
# Thu, 20 Feb 2020 22:31:45 GMT
CMD ["apache2-foreground"]
# Fri, 21 Feb 2020 02:49:03 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 21 Feb 2020 02:49:04 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 21 Feb 2020 02:49:08 GMT
RUN a2enmod rewrite
# Fri, 21 Feb 2020 02:51:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 02:51:53 GMT
VOLUME [/var/www/html]
# Fri, 21 Feb 2020 02:51:54 GMT
ENV JOOMLA_VERSION=3.9.15
# Fri, 21 Feb 2020 02:51:54 GMT
ENV JOOMLA_SHA512=d68e32de6cfe9af92ff7f7991c9253a4487832e55e32e6f74f2b4d592a4777f3b4d8bd74dcd0b10d4262c5e39bdad1e9f7698dedb2ef2989dbc06aa7ab2f6c69
# Fri, 21 Feb 2020 02:52:05 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 21 Feb 2020 02:52:07 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 21 Feb 2020 02:52:08 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 21 Feb 2020 02:52:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Feb 2020 02:52:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0c7074b2d47c15922db5c0eda14250224eb72756c800081d2b0627ffb369568d`  
		Last Modified: Sat, 01 Feb 2020 17:07:47 GMT  
		Size: 22.7 MB (22699138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37cb050f89036596ba7c3e4ddbe118156973fe8b59516e353a42ac97a3f6ba5`  
		Last Modified: Sun, 02 Feb 2020 02:28:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd60b6434b4a4eac9a8103900797e1a4260baf12d401a112911179fe3c37e00`  
		Last Modified: Sun, 02 Feb 2020 02:29:01 GMT  
		Size: 59.5 MB (59500876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a07b40ddbc553f32319192f74a79015c5c90e56e523b22f6ad70245aa8411ff`  
		Last Modified: Sun, 02 Feb 2020 02:28:40 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b0f70f7cf72677481f1f7b0fcbaf58293fb971ab9d483d4eb1f654c2e4bbe5`  
		Last Modified: Sun, 02 Feb 2020 02:29:36 GMT  
		Size: 17.5 MB (17482350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1a9f3fbad3f634b9d669e64e1181b798ecde659503ba74d4ed52a3e6119c93`  
		Last Modified: Sun, 02 Feb 2020 02:29:30 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb834b6f2aeffb397f544f2401041d4bbedfea605f899fd9f1df6cc3c305922e`  
		Last Modified: Sun, 02 Feb 2020 02:29:30 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a5915411c12c04009425a736c51bbe9c07108a73be6e42ef3fc0726c079b87`  
		Last Modified: Thu, 20 Feb 2020 23:32:27 GMT  
		Size: 12.6 MB (12648514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace59f146d14ef8c1fa565632efbf3454238ee0caf80b7e43ba040da39baf71d`  
		Last Modified: Thu, 20 Feb 2020 23:32:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19a1c6772a8d1fb88d8933296cbb0dc3747ee61629ce879f1f8903494a65502`  
		Last Modified: Thu, 20 Feb 2020 23:32:28 GMT  
		Size: 12.2 MB (12187887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e046cfd844d72e4fd9f92d94889c5ddbbd5fd36f112d8fd7eb7346e08f34098f`  
		Last Modified: Thu, 20 Feb 2020 23:32:24 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9792b4cc3e4df862268424109e38029af16794b955a04f614c80566b230b7a8c`  
		Last Modified: Thu, 20 Feb 2020 23:32:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29221dd5b7146fbad4c60801a5ebab19b0a8b5909d183dbef15ba81fa634b597`  
		Last Modified: Thu, 20 Feb 2020 23:32:23 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617829d90447b0cb87d3abb55205caf7a48064663b75ad8659566f64cd14e9ee`  
		Last Modified: Thu, 20 Feb 2020 23:32:24 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883bdf3e14d96435f377064f979719f02f274537937bf625b911e24b33874b25`  
		Last Modified: Fri, 21 Feb 2020 03:18:18 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e401bc03903a5cae67a958912e663daa4334570941a646f641f1a0cc5e7d48a`  
		Last Modified: Fri, 21 Feb 2020 03:18:17 GMT  
		Size: 3.1 MB (3110484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08738d005348f8cfa8402117673e74641d47af7176fed30bb138cb2baea31e7`  
		Last Modified: Fri, 21 Feb 2020 03:18:20 GMT  
		Size: 9.7 MB (9651963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e953ad1872a779663e913969860f3407fe088081e6c290765cfdfd9ff77c0a`  
		Last Modified: Fri, 21 Feb 2020 03:18:18 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aa8b63e5cf2210f7ef19b932de2958a408675eb480832a8b1df40d582fce90`  
		Last Modified: Fri, 21 Feb 2020 03:18:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:fee619d16b903a4c450f7634f7655942bf4fa54b8de29257c235e91d1d8eb18c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153923178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3537c37b5d26e64f52eb222bceb3642376e3b2297588a37c376ccb9d70f313`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:11 GMT
ADD file:cd38c10a494a1bdab0bab5baef1886651931e96b6db2d34ff4415660a299470f in / 
# Sat, 01 Feb 2020 16:41:12 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 08:04:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 08:04:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 08:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 08:05:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 08:05:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 08:09:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 08:09:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 08:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 08:10:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 08:10:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 08:10:08 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 08:10:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 08:10:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 08:10:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 08:10:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 09:02:58 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Sun, 02 Feb 2020 09:02:59 GMT
ENV PHP_VERSION=7.2.27
# Sun, 02 Feb 2020 09:03:00 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 09:03:02 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Sun, 02 Feb 2020 09:03:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 09:03:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 09:06:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 09:06:26 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 09:06:28 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 09:06:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sun, 02 Feb 2020 09:06:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 09:06:31 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 09:06:32 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 09:06:32 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 09:06:33 GMT
EXPOSE 80
# Sun, 02 Feb 2020 09:06:34 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 17:48:54 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Sun, 02 Feb 2020 17:48:54 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sun, 02 Feb 2020 17:48:57 GMT
RUN a2enmod rewrite
# Sun, 02 Feb 2020 17:51:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 17:51:42 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 17:51:43 GMT
ENV JOOMLA_VERSION=3.9.15
# Sun, 02 Feb 2020 17:51:43 GMT
ENV JOOMLA_SHA512=d68e32de6cfe9af92ff7f7991c9253a4487832e55e32e6f74f2b4d592a4777f3b4d8bd74dcd0b10d4262c5e39bdad1e9f7698dedb2ef2989dbc06aa7ab2f6c69
# Sun, 02 Feb 2020 17:51:50 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sun, 02 Feb 2020 17:51:53 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Sun, 02 Feb 2020 17:51:53 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Sun, 02 Feb 2020 17:51:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 17:51:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f7ca645dfd2fe61e7661b7f3b3951c589ccbff71aa054611475de455650bd8a8`  
		Last Modified: Sat, 01 Feb 2020 16:46:28 GMT  
		Size: 25.9 MB (25850659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ef482177c11080f835ff485ad054b5897ed5bc3778a7a2ebe68b655a930e06`  
		Last Modified: Sun, 02 Feb 2020 09:33:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff48b131cc3e3c219ce42e8dd4b8f558c3f2b70b6b5a533ec8ec378a8244a5df`  
		Last Modified: Sun, 02 Feb 2020 09:34:15 GMT  
		Size: 70.3 MB (70334393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38b85eef9c7a9d92bcece36db91d11c75af83cbce73aef5e34bf5c9d3bfddc0`  
		Last Modified: Sun, 02 Feb 2020 09:33:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3602ff96d387498c1caace636b507e47e9cac004a2477d89cab6cd6b957e79a`  
		Last Modified: Sun, 02 Feb 2020 09:34:47 GMT  
		Size: 18.6 MB (18577742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7bfeab785c7cebf1091684ec52fcbec4e0c5970b2496a53b01b50e6dc73bd9`  
		Last Modified: Sun, 02 Feb 2020 09:34:41 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d442e9c16a14167f5bf10c5764fa4338a59e568630f46c87a9a6f9d7658eba6`  
		Last Modified: Sun, 02 Feb 2020 09:34:41 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5fc3bbe21e178aa9a2e7f3204f161ac81a3087be20dceebd2587b9e3a2c36f`  
		Last Modified: Sun, 02 Feb 2020 09:38:46 GMT  
		Size: 12.6 MB (12643872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd73368ce3c76b226f29054536850d7c1697f12ba645349ead9eb485ca04f22`  
		Last Modified: Sun, 02 Feb 2020 09:38:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5edbdbe0a2411b26525849790ab1630d1ccf89b4843395905be9ab7d43e02b6`  
		Last Modified: Sun, 02 Feb 2020 09:38:47 GMT  
		Size: 13.5 MB (13536535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754d523cd4f76db673a73c1ec3fe2083563accfb0411db55fd39b5e40fc7ba2c`  
		Last Modified: Sun, 02 Feb 2020 09:38:42 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b54ba501012005a1f9b3f571265426477c9dccc7acbbd67c372d33b5b97ae16`  
		Last Modified: Sun, 02 Feb 2020 09:38:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4583eaec9561c2bef75efd333eb08e8a7b5275180632dcf1e976f7afed6416ca`  
		Last Modified: Sun, 02 Feb 2020 09:38:42 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249a0e2da932dc94aec09d768c1b3bcd65a43e97f792edd2ed8a4ec2c6642008`  
		Last Modified: Sun, 02 Feb 2020 09:38:42 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892872a756621d31ccd4bef985f207a8e5502a7fc1c5def8719909cccb50d927`  
		Last Modified: Sun, 02 Feb 2020 18:10:06 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647188ad0bc45d36c110a780c89de333e25d4f508d11d9ca168590fa66d2b4f4`  
		Last Modified: Sun, 02 Feb 2020 18:10:07 GMT  
		Size: 3.3 MB (3320363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedfc627ede41b3191a54a2d41eb3dba258df63ec8f9bd5e1174c6befd9caf52`  
		Last Modified: Sun, 02 Feb 2020 18:10:19 GMT  
		Size: 9.7 MB (9651950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3822dd2fd15b96da1976c74a66011d5fa7cb526df0a6868e798d2c52e05b9dc`  
		Last Modified: Sun, 02 Feb 2020 18:10:07 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5fe605027300d1e22bbf2919fa35bb266930ed3f747b42ccbd78f3f484d7f7`  
		Last Modified: Sun, 02 Feb 2020 18:10:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2` - linux; 386

```console
$ docker pull joomla@sha256:886d623f7e28854a0b4556aaa97d4718c2aa7c771212d00c23e14f4b485847ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167875327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b910d5eb7ff263d2cff648ae223f878d3917bda38157ec9086f9d0b4cf4c33bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:35 GMT
ADD file:be03c936f8d9737b4167f6563785971b009f05e4e508eb8249b365a9fae7b0e8 in / 
# Sat, 01 Feb 2020 16:39:35 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 01:33:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 01:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 01:33:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 01:33:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 01:42:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 01:42:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 01:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 01:43:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 01:43:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 01:43:06 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 01:43:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 01:43:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 01:43:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 01:43:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 03:21:37 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Sun, 02 Feb 2020 03:21:37 GMT
ENV PHP_VERSION=7.2.27
# Sun, 02 Feb 2020 03:21:38 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 03:21:38 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Sun, 02 Feb 2020 03:21:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 03:21:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 03:27:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 03:27:31 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 03:27:32 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 03:27:33 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sun, 02 Feb 2020 03:27:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 03:27:34 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 03:27:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 03:27:35 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 03:27:35 GMT
EXPOSE 80
# Sun, 02 Feb 2020 03:27:35 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 11:38:11 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Sun, 02 Feb 2020 11:38:11 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sun, 02 Feb 2020 11:38:12 GMT
RUN a2enmod rewrite
# Sun, 02 Feb 2020 11:40:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 11:40:08 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 11:40:08 GMT
ENV JOOMLA_VERSION=3.9.15
# Sun, 02 Feb 2020 11:40:08 GMT
ENV JOOMLA_SHA512=d68e32de6cfe9af92ff7f7991c9253a4487832e55e32e6f74f2b4d592a4777f3b4d8bd74dcd0b10d4262c5e39bdad1e9f7698dedb2ef2989dbc06aa7ab2f6c69
# Sun, 02 Feb 2020 11:40:14 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sun, 02 Feb 2020 11:40:15 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Sun, 02 Feb 2020 11:40:15 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Sun, 02 Feb 2020 11:40:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 11:40:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:57b164929d223abf41064de94f9f53ca37ec9f09843646c80344ff10c302051a`  
		Last Modified: Sat, 01 Feb 2020 16:44:32 GMT  
		Size: 27.7 MB (27747052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0193cddf0dacef353a98632490e6784d5095e706edcb983fcee6ec51374d4e`  
		Last Modified: Sun, 02 Feb 2020 04:18:24 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f1ce80033990dddefaab407e414c32c56e517edc78604a6fc39c2acd3b7b59`  
		Last Modified: Sun, 02 Feb 2020 04:18:52 GMT  
		Size: 81.2 MB (81198555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d6c8fa8b704d1717c63218688cdf03db3ffac7714f4e5590adf18ff5b6b039`  
		Last Modified: Sun, 02 Feb 2020 04:18:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86555f8f8ffe08a5b4304594f807875257c11ccb02334be1a0126b995d338f61`  
		Last Modified: Sun, 02 Feb 2020 04:19:34 GMT  
		Size: 19.1 MB (19112025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac21c4a945c9b54742a3c69931be823addbabeb952325ab73ff1e3e7748e1f42`  
		Last Modified: Sun, 02 Feb 2020 04:19:24 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe6e52821e5c8c2efcdbae0ab4fcc9d202dd46b27ad0b6e6fbf7e231d2179b9`  
		Last Modified: Sun, 02 Feb 2020 04:19:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610938e9bf69bbdc27f4503c37f1edf5ed4b6efc0d5c043057830891e12cb71c`  
		Last Modified: Sun, 02 Feb 2020 04:23:37 GMT  
		Size: 12.6 MB (12644521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57af7d43a515ee94393ca1b067feea6b38edbd87c59e90c533c8749ecbdf8320`  
		Last Modified: Sun, 02 Feb 2020 04:23:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4f3497c0cf54b218915ff0c6c5395a40e83c1528a1c7bb94f03ec999589ae`  
		Last Modified: Sun, 02 Feb 2020 04:23:42 GMT  
		Size: 14.2 MB (14169219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368dbd2c126851ba3e840b0cafa35f8dba49184a8ea7235a87a921b3fc769b9a`  
		Last Modified: Sun, 02 Feb 2020 04:23:33 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2781c3fb5b986f505ef86a6f4b825bc0bce23e2a6c6235ec8f289024c9d24231`  
		Last Modified: Sun, 02 Feb 2020 04:23:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b68b75135d4d81b3bf0308c48acf339ed4390185a59530f2f3dc822bc6b7ca`  
		Last Modified: Sun, 02 Feb 2020 04:23:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96d4c87ac1599fc38407f0bbe8d63e520a72ef04f55e5c8da9667dbf096cd9`  
		Last Modified: Sun, 02 Feb 2020 04:23:33 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd835a2fc13904e9df2f338ca24a12f63a9886bd48c35604738769cc877ef1e4`  
		Last Modified: Sun, 02 Feb 2020 11:51:30 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9048e92e9bd4070d0fc56e92a40cdd6650a2e8f00b64fb884f38bd25f950718`  
		Last Modified: Sun, 02 Feb 2020 11:51:32 GMT  
		Size: 3.3 MB (3344435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21536e278ec7fb5e7d7b63175776a54438df3847d019d4b76c7c770acb5d7704`  
		Last Modified: Sun, 02 Feb 2020 11:51:38 GMT  
		Size: 9.7 MB (9651967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0977d9da5b839c7040aaaba1ddcad61616ae0e72d19f8b8e9ec379f381eca38f`  
		Last Modified: Sun, 02 Feb 2020 11:51:30 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc127f05424dac6dcf985c86394e42c6bb2e676840df6ce0bcbde80ae1c247fb`  
		Last Modified: Sun, 02 Feb 2020 11:51:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2` - linux; ppc64le

```console
$ docker pull joomla@sha256:425e2ba8e767e3ed4f5bb391ccbd2e5ed94f236819e03addc5318307a350f0f7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173318326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8521d6e04101c0c72f09d6f7d70907191e435f3df1dec10d1f453c8a5b45e7f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 01 Feb 2020 17:18:04 GMT
ADD file:aadd94011800934ec665edb193029ab2be0aeb668c566ba4bc52bd678e71a735 in / 
# Sat, 01 Feb 2020 17:18:06 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 08:56:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 02 Feb 2020 08:56:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 02 Feb 2020 08:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 08:58:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 02 Feb 2020 08:58:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 02 Feb 2020 09:04:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sun, 02 Feb 2020 09:04:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sun, 02 Feb 2020 09:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sun, 02 Feb 2020 09:05:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sun, 02 Feb 2020 09:05:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sun, 02 Feb 2020 09:05:21 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sun, 02 Feb 2020 09:05:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sun, 02 Feb 2020 09:05:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 09:05:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 02 Feb 2020 09:05:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sun, 02 Feb 2020 10:22:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Sun, 02 Feb 2020 10:22:40 GMT
ENV PHP_VERSION=7.2.27
# Sun, 02 Feb 2020 10:22:42 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 10:22:43 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Sun, 02 Feb 2020 10:23:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 10:23:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 10:27:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 10:27:10 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 10:27:15 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 10:27:19 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sun, 02 Feb 2020 10:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 10:27:24 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 10:27:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 10:27:27 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 10:27:28 GMT
EXPOSE 80
# Sun, 02 Feb 2020 10:27:31 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 19:11:29 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Sun, 02 Feb 2020 19:11:31 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sun, 02 Feb 2020 19:11:38 GMT
RUN a2enmod rewrite
# Sun, 02 Feb 2020 19:14:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 19:14:26 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 19:14:30 GMT
ENV JOOMLA_VERSION=3.9.15
# Sun, 02 Feb 2020 19:14:31 GMT
ENV JOOMLA_SHA512=d68e32de6cfe9af92ff7f7991c9253a4487832e55e32e6f74f2b4d592a4777f3b4d8bd74dcd0b10d4262c5e39bdad1e9f7698dedb2ef2989dbc06aa7ab2f6c69
# Sun, 02 Feb 2020 19:14:43 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sun, 02 Feb 2020 19:14:46 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Sun, 02 Feb 2020 19:14:47 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Sun, 02 Feb 2020 19:14:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 19:14:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:16a7e1c5b23ec3cf93421f5f868c1cf2cda468cfebb1b2bc62f4d533d99d256b`  
		Last Modified: Sat, 01 Feb 2020 17:26:05 GMT  
		Size: 30.5 MB (30517693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5966ccdc0aecd2b2408b79193c2e5da4621b70dd05cb33f690a6085cbd68d828`  
		Last Modified: Sun, 02 Feb 2020 11:04:14 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80918ab44a55db4cf3524614dbdcea0931538e382d9c436c05ef5c2052a79993`  
		Last Modified: Sun, 02 Feb 2020 11:05:22 GMT  
		Size: 82.3 MB (82259405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2941531c52c5a3060bb214f05618924812516ae9a5686b18eb72ecfb2d072f1`  
		Last Modified: Sun, 02 Feb 2020 11:04:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3183f8fb1b098ac03c98e8a9e66548260e871ba18dd3b0f12d9f59f37eb0a74`  
		Last Modified: Sun, 02 Feb 2020 11:06:52 GMT  
		Size: 19.8 MB (19811323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d85b6bf562499902acd42f85c0e8fe9bd2cc1975c855d1d51d3dd5d978ae55`  
		Last Modified: Sun, 02 Feb 2020 11:06:11 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c62e2308d0f70f478bac2fb5c6d6a3f0aa1483b7f68caa56e7036f75cd844e`  
		Last Modified: Sun, 02 Feb 2020 11:06:11 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4732c6c3bc58af2163895216532a4ea6e578d06e77be17571b4d5e65f1e407de`  
		Last Modified: Sun, 02 Feb 2020 11:13:44 GMT  
		Size: 12.6 MB (12644920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13f0f73d6e1ea3227dc0b344e7b367f762c7e3c3e1442cf31e71db46edd247`  
		Last Modified: Sun, 02 Feb 2020 11:13:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cfc92040e15198a9db2ea5be99b71590fc80bd43b56306aac37338922968b2`  
		Last Modified: Sun, 02 Feb 2020 11:13:37 GMT  
		Size: 14.9 MB (14882675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834b77fcc89887efb8a4ade702630addf7698ee8c5e8781a333d4cd15bfb64b`  
		Last Modified: Sun, 02 Feb 2020 11:13:32 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6cc15ee7dd46352653842ee7df577a1236f51d1aaaed5f93e9501980971e7d`  
		Last Modified: Sun, 02 Feb 2020 11:13:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508c24fd9e371905146d24914fb3cf422b05af5fab174fdef530aba3f3ffde1`  
		Last Modified: Sun, 02 Feb 2020 11:13:32 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733306fe2bacc9fdfbac93d18241d5567033f103304a9b7672634acde3da49dc`  
		Last Modified: Sun, 02 Feb 2020 11:13:32 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa00617bb56be1f2cf10df1d036f65b0bf0dfe7e93bc812565487d617d3c866a`  
		Last Modified: Sun, 02 Feb 2020 19:32:13 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ff2c8f7c8fb1700b07b728dccc59a7a02db27c11350b66e851ca5eac771c7a`  
		Last Modified: Sun, 02 Feb 2020 19:32:16 GMT  
		Size: 3.5 MB (3542669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac21c93bdb756a25ffa7a73804df5e02ba00f431c0e293f6706ab9a956c0f951`  
		Last Modified: Sun, 02 Feb 2020 19:32:17 GMT  
		Size: 9.7 MB (9651962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fac0d0de2da0edc9ad4b61be8dc4950cbbab6e993f0b25ff03708b5acda51b`  
		Last Modified: Sun, 02 Feb 2020 19:32:13 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fb1c467bfafc0cf0519ef43b6caee06edb9e97a7c2d33cf7fc20001ba18de9`  
		Last Modified: Sun, 02 Feb 2020 19:32:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
