## `joomla:3-php7.2-apache`

```console
$ docker pull joomla@sha256:47e5966c07a1f669a8d4303e83e2f1eb537fbb168e977801e3720ce3bd463a89
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

### `joomla:3-php7.2-apache` - linux; amd64

```console
$ docker pull joomla@sha256:fa485367ab1bbfe9c7b8f21b5c13e56956a9a072e25438a1dd9d50551b5c2c04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161998714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efb16850906617621fb0bed9fe70aa0da2c65e8c4a7a6c28dd2e755e616a00e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 07:15:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 11 Dec 2020 07:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 11 Dec 2020 07:16:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 07:16:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:16:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:25:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 11 Dec 2020 07:25:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 11 Dec 2020 07:25:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 11 Dec 2020 07:25:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 11 Dec 2020 07:25:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 11 Dec 2020 07:25:59 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 11 Dec 2020 07:25:59 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 11 Dec 2020 07:26:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:26:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:26:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 10:46:10 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 11 Dec 2020 10:46:10 GMT
ENV PHP_VERSION=7.2.34
# Fri, 11 Dec 2020 10:46:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.34.tar.xz.asc
# Fri, 11 Dec 2020 10:46:11 GMT
ENV PHP_SHA256=409e11bc6a2c18707dfc44bc61c820ddfd81e17481470f3405ee7822d8379903
# Fri, 11 Dec 2020 10:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 11 Dec 2020 10:46:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 10:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 10:51:54 GMT
COPY multi:dc714d093d9a94baf082b278964398d495faeef837d3357693090c43ebfb6fb4 in /usr/local/bin/ 
# Fri, 11 Dec 2020 10:51:55 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 10:51:56 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 11 Dec 2020 10:51:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 10:51:56 GMT
STOPSIGNAL SIGWINCH
# Fri, 11 Dec 2020 10:51:57 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 11 Dec 2020 10:51:57 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 10:51:57 GMT
EXPOSE 80
# Fri, 11 Dec 2020 10:51:57 GMT
CMD ["apache2-foreground"]
# Fri, 11 Dec 2020 22:56:36 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 11 Dec 2020 22:56:36 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 11 Dec 2020 22:56:38 GMT
RUN a2enmod rewrite
# Fri, 11 Dec 2020 22:59:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.19; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 22:59:11 GMT
VOLUME [/var/www/html]
# Fri, 11 Dec 2020 22:59:11 GMT
ENV JOOMLA_VERSION=3.9.22
# Fri, 11 Dec 2020 22:59:11 GMT
ENV JOOMLA_SHA512=826f01683bd3d86f45a0e59dd6265cccdbeea9709604d19091572f6c5e3f8cd91a645789f6b8e8040c641badf76381acc4719cb29754c5d2bb2d5b6f4d17a60d
# Fri, 11 Dec 2020 22:59:17 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 11 Dec 2020 22:59:17 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 11 Dec 2020 22:59:18 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 11 Dec 2020 22:59:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 22:59:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db606474d60ce31604505c7d6dad9a66cb42f3818fca738832db2f2091cf89c9`  
		Last Modified: Fri, 11 Dec 2020 12:04:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb30f0cd8e0ff78b5eecdc2d9365a50441ad83c5db5f1e87942d6426237fa56`  
		Last Modified: Fri, 11 Dec 2020 12:04:17 GMT  
		Size: 76.7 MB (76652169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb2e805159413e5278b859f7fbb86ddfc99e667cb705d5d5aec0a7c8ffcf1b5`  
		Last Modified: Fri, 11 Dec 2020 12:04:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c761b44e2ccbff3f10b254b21bb00a52dfd26919ad9e3f7efcd569196e6c26b`  
		Last Modified: Fri, 11 Dec 2020 12:04:46 GMT  
		Size: 18.7 MB (18678264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2199db96575122fd559c29b619a2773fe9069e0266312a6369ac95f4464b1dd`  
		Last Modified: Fri, 11 Dec 2020 12:04:42 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9a9381eea8f93068e8043f18ea59b709c07256e2f90962931a1433fbdf5e79`  
		Last Modified: Fri, 11 Dec 2020 12:04:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd07bbc59d347c16686f107676436a2281e4128033f105ca7a602aa195bcbe04`  
		Last Modified: Fri, 11 Dec 2020 12:12:30 GMT  
		Size: 12.6 MB (12647845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b73ab27698b55aa309173abd0cdd758291b9feaac31342c48ff12f3be14876`  
		Last Modified: Fri, 11 Dec 2020 12:12:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983308f4f0d6304dc6cecde8fd66ba5a94a08873a3b8205eb5ff1ea98b419dbc`  
		Last Modified: Fri, 11 Dec 2020 12:12:31 GMT  
		Size: 13.8 MB (13820560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c13f026e6da09e10ca2edb704b335a62bac29e549a2d0b35e535c9aa8dbeeba`  
		Last Modified: Fri, 11 Dec 2020 12:12:28 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e6cd16368920e691da5b8791184d7a8d579dd5cd5e8c533ad2bf0b82c2d0fc`  
		Last Modified: Fri, 11 Dec 2020 12:12:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5516e56582a30bd2e69c32d17a169ed7227900318e9d7b5949c8fb447308f5`  
		Last Modified: Fri, 11 Dec 2020 12:12:29 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154729f6ba8609ef7d5af1bfad81efe814cbbca18509834908735c9aced174d3`  
		Last Modified: Fri, 11 Dec 2020 12:12:28 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52dcc008cf735a40096effe359e75e4727f2dfd127256658f1113f0ef3c83ca`  
		Last Modified: Fri, 11 Dec 2020 23:22:00 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ccf7a328a6cd2d95120606a37c258f759b1443f796f81ec4607564a46f389a1`  
		Last Modified: Fri, 11 Dec 2020 23:22:02 GMT  
		Size: 3.4 MB (3402647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ccacadac70521c54f87f3cd1d0756cb891a1d8b853d523fdc33415621e2319`  
		Last Modified: Fri, 11 Dec 2020 23:22:05 GMT  
		Size: 9.7 MB (9690315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfadc6909db18e676bc86bf1c4fb49736d7d1df59997ad08f439837c698f108`  
		Last Modified: Fri, 11 Dec 2020 23:22:00 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906abdccc957523242c9c693a27a8c729fd755cd1f4cd23c92a36c318a7f5db3`  
		Last Modified: Fri, 11 Dec 2020 23:22:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:29420a84c87773de151d18df17701a291cb0215abf96ee9e7c01cd4b8e3940f7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140133863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501274a6b3441ce24e2777972ee19f912ac65cd0429098ec67b5933b73b74cf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 07:13:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 11 Dec 2020 07:13:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 11 Dec 2020 07:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 07:13:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 07:13:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 07:18:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 11 Dec 2020 07:18:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 11 Dec 2020 07:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 11 Dec 2020 07:18:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 11 Dec 2020 07:18:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 11 Dec 2020 07:18:48 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 11 Dec 2020 07:18:49 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 11 Dec 2020 07:18:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:18:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 07:18:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 08:35:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 11 Dec 2020 08:35:49 GMT
ENV PHP_VERSION=7.2.34
# Fri, 11 Dec 2020 08:35:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.34.tar.xz.asc
# Fri, 11 Dec 2020 08:35:51 GMT
ENV PHP_SHA256=409e11bc6a2c18707dfc44bc61c820ddfd81e17481470f3405ee7822d8379903
# Fri, 11 Dec 2020 08:36:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 11 Dec 2020 08:36:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 08:39:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 08:39:47 GMT
COPY multi:dc714d093d9a94baf082b278964398d495faeef837d3357693090c43ebfb6fb4 in /usr/local/bin/ 
# Fri, 11 Dec 2020 08:39:52 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 08:39:57 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 11 Dec 2020 08:40:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 08:40:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 11 Dec 2020 08:40:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 11 Dec 2020 08:40:06 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 08:40:09 GMT
EXPOSE 80
# Fri, 11 Dec 2020 08:40:10 GMT
CMD ["apache2-foreground"]
# Fri, 11 Dec 2020 17:29:10 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 11 Dec 2020 17:29:11 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 11 Dec 2020 17:29:13 GMT
RUN a2enmod rewrite
# Fri, 11 Dec 2020 17:32:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.19; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:32:04 GMT
VOLUME [/var/www/html]
# Fri, 11 Dec 2020 17:32:05 GMT
ENV JOOMLA_VERSION=3.9.22
# Fri, 11 Dec 2020 17:32:05 GMT
ENV JOOMLA_SHA512=826f01683bd3d86f45a0e59dd6265cccdbeea9709604d19091572f6c5e3f8cd91a645789f6b8e8040c641badf76381acc4719cb29754c5d2bb2d5b6f4d17a60d
# Fri, 11 Dec 2020 17:32:17 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 11 Dec 2020 17:32:19 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 11 Dec 2020 17:32:20 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 11 Dec 2020 17:32:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:32:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed9b2f20ffb0bcade877c21585737821b1abdd1b29ec2742ef3d8bc1a8a71b2`  
		Last Modified: Fri, 11 Dec 2020 09:10:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a086596dbe8ce93733486082312fbe0cffefc063795aa2ae18459ce018c64bd`  
		Last Modified: Fri, 11 Dec 2020 09:10:30 GMT  
		Size: 58.8 MB (58801419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5a47fff6f79bd0fed3070e2cbe30a88324dcd19c6597080333fabbf9adf49d`  
		Last Modified: Fri, 11 Dec 2020 09:10:09 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4517107dffe6fc5dcbf76387b03c5f0f2ced48e2b48178cd9b615f3a2b13bc8`  
		Last Modified: Fri, 11 Dec 2020 09:11:08 GMT  
		Size: 18.0 MB (18026228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d52419e1d1b4bfe2b0d4c2c5225b6fd7fe59bba8acb8b28c697658bfb7365c`  
		Last Modified: Fri, 11 Dec 2020 09:11:03 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca7d691aeaf537d2c7d897bb473aec13e1f708157f08c95460271ad428a1011`  
		Last Modified: Fri, 11 Dec 2020 09:11:03 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f348e7be2a4959db3f1b8228b1d49651228723b879a74b36ee9d98778cc088d7`  
		Last Modified: Fri, 11 Dec 2020 09:17:17 GMT  
		Size: 12.6 MB (12645777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24684b1c86cdf89591625161c2df028f698f6f9c0e74df5ade27f9d40af47a0`  
		Last Modified: Fri, 11 Dec 2020 09:17:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76d22b0ff10f768de2efef27e01ce79d73c921adaa6b13cfe2927817270631c`  
		Last Modified: Fri, 11 Dec 2020 09:17:17 GMT  
		Size: 12.9 MB (12893787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4355a90fb3cbdc0b14846b6d12c3a8628a4a7a90575315c272638660c63b5f23`  
		Last Modified: Fri, 11 Dec 2020 09:17:12 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4968d536ed7ff7e733dd3e40a56ffda053e912fcb9ceab286dbd29c9bf0edc`  
		Last Modified: Fri, 11 Dec 2020 09:17:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313dc9178399610a9543bcc5f3c69014336b94a3dcc2b5d0f24da526a9819ba1`  
		Last Modified: Fri, 11 Dec 2020 09:17:13 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c99c7c66ad5b754b9c8f47c6a7a723b3cf14a471d827c2d3ea5eeb2e399eac7`  
		Last Modified: Fri, 11 Dec 2020 09:17:13 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a7b6bf6964e08039135e90c9fe59a42e4de85c6ed510685994c39c5767d8b2`  
		Last Modified: Fri, 11 Dec 2020 17:50:00 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2adcd59bd872a7b0c226c8b107ec77cb3759c00b7001da4863ba62edbc5bd5c`  
		Last Modified: Fri, 11 Dec 2020 17:50:02 GMT  
		Size: 3.2 MB (3225183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492fd8c78ccd2b13b65aaa435f73a4520dc45a54ebc2c3c501cfef5ac470e000`  
		Last Modified: Fri, 11 Dec 2020 17:50:05 GMT  
		Size: 9.7 MB (9690274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc40c111236354a7b68b52091aa2eb707b47c76bd39a05745366d97f522c467`  
		Last Modified: Fri, 11 Dec 2020 17:49:59 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5443c22ae8acdd64bbeb4a411fe7638b2138a1444991d8f5b306f4ce97f5afb0`  
		Last Modified: Fri, 11 Dec 2020 17:49:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:0b6d6b65bde6775b243f03716efe2fe7c1653f0a9f085162f73390bfa5c78f7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137342709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da78f77b3b1d6ff0244ea916e062936e6db29efa0fc468070e7d094d5d3b30d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 11 Dec 2020 02:23:37 GMT
ADD file:75ca842ac2d6e9f6617bb3df280af1e4c9619c9805fd5e00c1c3d6b8b4e3d802 in / 
# Fri, 11 Dec 2020 02:23:39 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:45:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 11 Dec 2020 06:45:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 11 Dec 2020 06:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 06:47:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 06:47:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 06:50:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 11 Dec 2020 06:50:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 11 Dec 2020 06:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 11 Dec 2020 06:51:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 11 Dec 2020 06:51:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 11 Dec 2020 06:51:18 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 11 Dec 2020 06:51:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 11 Dec 2020 06:51:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 06:51:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 06:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 08:31:51 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 11 Dec 2020 08:31:52 GMT
ENV PHP_VERSION=7.2.34
# Fri, 11 Dec 2020 08:31:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.34.tar.xz.asc
# Fri, 11 Dec 2020 08:31:53 GMT
ENV PHP_SHA256=409e11bc6a2c18707dfc44bc61c820ddfd81e17481470f3405ee7822d8379903
# Fri, 11 Dec 2020 08:32:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 11 Dec 2020 08:32:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 08:35:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 08:35:03 GMT
COPY multi:dc714d093d9a94baf082b278964398d495faeef837d3357693090c43ebfb6fb4 in /usr/local/bin/ 
# Fri, 11 Dec 2020 08:35:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 08:35:07 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 11 Dec 2020 08:35:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 08:35:10 GMT
STOPSIGNAL SIGWINCH
# Fri, 11 Dec 2020 08:35:10 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 11 Dec 2020 08:35:11 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 08:35:12 GMT
EXPOSE 80
# Fri, 11 Dec 2020 08:35:13 GMT
CMD ["apache2-foreground"]
# Fri, 11 Dec 2020 23:40:17 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 11 Dec 2020 23:40:18 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 11 Dec 2020 23:40:20 GMT
RUN a2enmod rewrite
# Fri, 11 Dec 2020 23:43:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.19; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 23:43:10 GMT
VOLUME [/var/www/html]
# Fri, 11 Dec 2020 23:43:11 GMT
ENV JOOMLA_VERSION=3.9.22
# Fri, 11 Dec 2020 23:43:11 GMT
ENV JOOMLA_SHA512=826f01683bd3d86f45a0e59dd6265cccdbeea9709604d19091572f6c5e3f8cd91a645789f6b8e8040c641badf76381acc4719cb29754c5d2bb2d5b6f4d17a60d
# Fri, 11 Dec 2020 23:43:21 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 11 Dec 2020 23:43:23 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 11 Dec 2020 23:43:24 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 11 Dec 2020 23:43:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 23:43:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c06905228d4fc5a5c840a70e2e6ced56596a8bc73abc69e6a1867bbb6f7ae7e7`  
		Last Modified: Fri, 11 Dec 2020 02:33:07 GMT  
		Size: 22.7 MB (22707662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff29bbfe5a8a35c816e943e30889f192df4e12d1b4c03a36540c0e4d40bcf3e8`  
		Last Modified: Fri, 11 Dec 2020 09:16:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01e4ef0e8e22e1ca2287988849c31e36c883039c399efe7cc63b9bfe617dfa7`  
		Last Modified: Fri, 11 Dec 2020 09:16:35 GMT  
		Size: 59.5 MB (59508954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c032054d75502633be18567f6e069e007d492b2bcb340991656015ae61b9e28`  
		Last Modified: Fri, 11 Dec 2020 09:16:15 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd024b01ae978f65f5eca3f392865e98a1d1d7f75d63595bb70730417f7dd0ac`  
		Last Modified: Fri, 11 Dec 2020 09:17:13 GMT  
		Size: 17.5 MB (17481707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bb823d44c0ee717bb9f076d7046d1b990d85d3ce4c6a35e760fc4b75618228`  
		Last Modified: Fri, 11 Dec 2020 09:17:09 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96022462b744f8f7af417b0189d26064f72fb6c3f25565ccfb590e0c38af87e`  
		Last Modified: Fri, 11 Dec 2020 09:17:09 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3408949b7066968e2135bd550e7bbe319ff185a4a564a653ed3e00ea279da08`  
		Last Modified: Fri, 11 Dec 2020 09:26:36 GMT  
		Size: 12.6 MB (12645814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a982f0b9260b0533911a5451366f23d908c965c528fa9a2ba99ec1abfc47f0e`  
		Last Modified: Fri, 11 Dec 2020 09:26:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62031d3e1179e41dcdaf812954d306a66489c2f966118fd83cf8742a41a89d28`  
		Last Modified: Fri, 11 Dec 2020 09:26:36 GMT  
		Size: 12.2 MB (12163875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfad3d9bc16d29b976fa39fad50ae6084678d75cb3d4457ae0bfbbd059a0491`  
		Last Modified: Fri, 11 Dec 2020 09:26:32 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cec5ebac9cf3c0ce7a493a701264e756ab426279ba93fa580420242951043eb`  
		Last Modified: Fri, 11 Dec 2020 09:26:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714d21f9adf3c8a2dfa25eb59b7abb8bcf8738a92785ec0875695347cbf27ae`  
		Last Modified: Fri, 11 Dec 2020 09:26:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe6a7900ed20469e1720345473f56acbef5120ac6145ee833793b0e504c0090`  
		Last Modified: Fri, 11 Dec 2020 09:26:32 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ef03cc96758c49e723c25fcb577554d2a40370d170e07f2dddcdcd5c1faae8`  
		Last Modified: Sat, 12 Dec 2020 00:10:59 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ac1db9ab442efaf42a9afacdd7e43233ced4daa7c55c58a07a59dcc5cafeb7`  
		Last Modified: Sat, 12 Dec 2020 00:11:00 GMT  
		Size: 3.1 MB (3136682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3fde4e9c5bd4c973b4d5b7c20890460017c9437e1fd07c530561e3e01e0bac`  
		Last Modified: Sat, 12 Dec 2020 00:11:17 GMT  
		Size: 9.7 MB (9690290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c60aaa2ae33d661c9906e69d6eaef8152f27d9906b4a5d096000f0c2a9801e`  
		Last Modified: Sat, 12 Dec 2020 00:10:59 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97449b6670691e62d5d925eec29d69652e47588122032fe4ca99414785cd4a4`  
		Last Modified: Sat, 12 Dec 2020 00:10:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:e72fc3192efbbbbd29174c552e54826ec06eda994bd9479a3e6a584c255d46f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153997601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1500ea4fd7ae835ce735304278b17b7b66cf62d7719aa3ad2bc6a751aae437a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 09:33:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 11 Dec 2020 09:33:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 11 Dec 2020 09:33:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 09:33:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 09:33:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 09:37:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 11 Dec 2020 09:37:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 11 Dec 2020 09:38:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 11 Dec 2020 09:38:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 11 Dec 2020 09:38:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 11 Dec 2020 09:38:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 11 Dec 2020 09:38:23 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 11 Dec 2020 09:38:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 09:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 09:38:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 11:16:10 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 11 Dec 2020 11:16:11 GMT
ENV PHP_VERSION=7.2.34
# Fri, 11 Dec 2020 11:16:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.34.tar.xz.asc
# Fri, 11 Dec 2020 11:16:13 GMT
ENV PHP_SHA256=409e11bc6a2c18707dfc44bc61c820ddfd81e17481470f3405ee7822d8379903
# Fri, 11 Dec 2020 11:16:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 11 Dec 2020 11:16:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 11:19:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 11:19:32 GMT
COPY multi:dc714d093d9a94baf082b278964398d495faeef837d3357693090c43ebfb6fb4 in /usr/local/bin/ 
# Fri, 11 Dec 2020 11:19:34 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 11:19:37 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 11 Dec 2020 11:19:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 11:19:38 GMT
STOPSIGNAL SIGWINCH
# Fri, 11 Dec 2020 11:19:39 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 11 Dec 2020 11:19:40 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 11:19:40 GMT
EXPOSE 80
# Fri, 11 Dec 2020 11:19:41 GMT
CMD ["apache2-foreground"]
# Sat, 12 Dec 2020 01:22:43 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 12 Dec 2020 01:22:43 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 12 Dec 2020 01:22:46 GMT
RUN a2enmod rewrite
# Sat, 12 Dec 2020 01:25:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.19; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 01:25:27 GMT
VOLUME [/var/www/html]
# Sat, 12 Dec 2020 01:25:28 GMT
ENV JOOMLA_VERSION=3.9.22
# Sat, 12 Dec 2020 01:25:29 GMT
ENV JOOMLA_SHA512=826f01683bd3d86f45a0e59dd6265cccdbeea9709604d19091572f6c5e3f8cd91a645789f6b8e8040c641badf76381acc4719cb29754c5d2bb2d5b6f4d17a60d
# Sat, 12 Dec 2020 01:25:38 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 12 Dec 2020 01:25:41 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Sat, 12 Dec 2020 01:25:43 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Sat, 12 Dec 2020 01:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 01:25:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88cecc04e76783f0006b9fed72be749e834825383e941e16de2565a0e4a8cc3`  
		Last Modified: Fri, 11 Dec 2020 11:57:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30eb7a300f132babe7d5ed65f9e81a1fdd4542ecf70ac29a91bc290484dbc5e5`  
		Last Modified: Fri, 11 Dec 2020 11:58:04 GMT  
		Size: 70.3 MB (70338279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17a0a78e91d3ac0ec4a0c0566f57580154ead8d8967258efe94989d86cd05bd`  
		Last Modified: Fri, 11 Dec 2020 11:57:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d436d7bb0262f042a9554b5c54b25bc1d19cabbb9435747672c34d12f8dc1d0`  
		Last Modified: Fri, 11 Dec 2020 11:58:40 GMT  
		Size: 18.6 MB (18579888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5543a36f8eed548f436944bf39a2e918115fc9b30b54416c1081566f25716010`  
		Last Modified: Fri, 11 Dec 2020 11:58:35 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28135fd83ed1ac66e6f4288fabe4c84616cfe420e8e6808ba92d052771325ab4`  
		Last Modified: Fri, 11 Dec 2020 11:58:35 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485201b000c7ca5a73c2f9d047a204442ea5871a8a1405809d623884d83afc05`  
		Last Modified: Fri, 11 Dec 2020 12:07:53 GMT  
		Size: 12.6 MB (12646590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e92e56de9f5b0243dc28d80127f51f9f773d64ce4ae1ad58cfff06c2dcd4c29`  
		Last Modified: Fri, 11 Dec 2020 12:07:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709f68bc1d50527b9d9de50c516cb337468feb59c6135b414dda628d902a1bc8`  
		Last Modified: Fri, 11 Dec 2020 12:07:54 GMT  
		Size: 13.5 MB (13517508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff78edaefc7917757ec4e434738d5561d016bedd20ebdeeee362ec53c8d200`  
		Last Modified: Fri, 11 Dec 2020 12:07:49 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119f7607f913c50661a95311027b7b944c7bf2ee9e7af5361a14b72ce4d36b34`  
		Last Modified: Fri, 11 Dec 2020 12:07:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c04bb0b5fbe7c2927e6282625ccf4c5e0399e9da46f4a84bb8072dc98add6e5`  
		Last Modified: Fri, 11 Dec 2020 12:07:48 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9639d8c8cc76eb6501b4135a054c1a85bd7397db1010d043bcc03d32bf6d79b6`  
		Last Modified: Fri, 11 Dec 2020 12:07:49 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fa9252ee2f0ee580f80b286f01c0696447c22b27623e02f5dae66c3165e95`  
		Last Modified: Sat, 12 Dec 2020 01:52:47 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71841cf28d1e3c2150f0faec3216d2de3ffdb28b07fd6f06df2543d7479ba21`  
		Last Modified: Sat, 12 Dec 2020 01:52:48 GMT  
		Size: 3.4 MB (3361132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69b89e2e81028ee653dd163950ae2e082210330a24bcb0f9f6dfd9e8ffca715`  
		Last Modified: Sat, 12 Dec 2020 01:52:51 GMT  
		Size: 9.7 MB (9690268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560f9d3ba331818150f6442da4f55095a93853ede6be61cc768462ae989657d7`  
		Last Modified: Sat, 12 Dec 2020 01:52:47 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c517f6c6caf697643caa66dc962f58a79c33957f5561f76ae63857d7207985e5`  
		Last Modified: Sat, 12 Dec 2020 01:52:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-apache` - linux; 386

```console
$ docker pull joomla@sha256:87dda9ac99bd88244143ed687d06b20222250382f9b41691b95489f6d60d6f0a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167850482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239ddf2a59a5cf07582ba33a5c14b5fee9a602d42513b50d0b182ef64529adfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 12:50:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Aug 2020 12:50:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Aug 2020 12:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 12:50:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Aug 2020 12:50:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 04 Aug 2020 12:55:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Aug 2020 12:55:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Aug 2020 12:56:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 04 Aug 2020 12:56:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 04 Aug 2020 12:56:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 04 Aug 2020 12:56:10 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 04 Aug 2020 12:56:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 04 Aug 2020 12:56:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Aug 2020 12:56:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Aug 2020 12:56:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Aug 2020 14:21:14 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 06 Aug 2020 22:51:41 GMT
ENV PHP_VERSION=7.2.33
# Thu, 06 Aug 2020 22:51:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.33.tar.xz.asc
# Thu, 06 Aug 2020 22:51:42 GMT
ENV PHP_SHA256=0f160a3483ffce36be5962fab7bcf09d605ee66c5707df83e4195cb796bbb03a PHP_MD5=
# Thu, 06 Aug 2020 22:51:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Aug 2020 22:51:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Aug 2020 22:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 06 Aug 2020 22:56:41 GMT
COPY multi:af24b1d34daac0a277386947399eceaaf20d3065d4be5db00b1d6466cf006c49 in /usr/local/bin/ 
# Thu, 06 Aug 2020 22:56:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Aug 2020 22:56:42 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 06 Aug 2020 22:56:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Aug 2020 22:56:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Aug 2020 22:56:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Aug 2020 22:56:43 GMT
WORKDIR /var/www/html
# Thu, 06 Aug 2020 22:56:43 GMT
EXPOSE 80
# Thu, 06 Aug 2020 22:56:44 GMT
CMD ["apache2-foreground"]
# Fri, 07 Aug 2020 03:01:16 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 07 Aug 2020 03:01:16 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 07 Aug 2020 03:01:17 GMT
RUN a2enmod rewrite
# Fri, 07 Aug 2020 03:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Aug 2020 03:03:17 GMT
VOLUME [/var/www/html]
# Fri, 07 Aug 2020 03:03:17 GMT
ENV JOOMLA_VERSION=3.9.18
# Fri, 07 Aug 2020 03:03:18 GMT
ENV JOOMLA_SHA512=1bf4590a761cc24f59fc0d5b07ffbb8f9e50073b3536edc261b8785ff168aca2066d133a81c4ac33bcfe7b843559320ef4d1f97c5eb16096ca4b550a18b7f44d
# Fri, 07 Aug 2020 03:03:24 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 07 Aug 2020 03:03:25 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 07 Aug 2020 03:03:25 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 07 Aug 2020 03:03:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Aug 2020 03:03:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329242062d68d28d6b2a87364a30d8b71938ba033610ecfd79f13769a96294e2`  
		Last Modified: Tue, 04 Aug 2020 14:58:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8aaae05adb825dff3551448f99133aba9f351d7f26f8c75f6486b4b38bd51c`  
		Last Modified: Tue, 04 Aug 2020 14:59:19 GMT  
		Size: 81.2 MB (81196323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a65de971d0774dc002b56e15b037e7d4db04da66913020270e1285355323dbb`  
		Last Modified: Tue, 04 Aug 2020 14:58:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5237681b89148747d9421150d867c5cc8449bf341cbc8ad214f71d9b03794a23`  
		Last Modified: Tue, 04 Aug 2020 14:59:36 GMT  
		Size: 19.1 MB (19112679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7cf510e15402722d29174d2b186ac456076ed7d047fe794a07db362136ba17`  
		Last Modified: Tue, 04 Aug 2020 14:59:30 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be410499ff850773e8553b98b72aa2ee3faac6f4ae8040ea8f296bd35a419521`  
		Last Modified: Tue, 04 Aug 2020 14:59:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6efe484f493ef80a7f6495ca55c4b85207702542ff1ea572b7edcd7ee36addf`  
		Last Modified: Fri, 07 Aug 2020 00:52:53 GMT  
		Size: 12.6 MB (12648411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4120067059663d8f19afa8b36bdac8982a71aee3c5e728b57959ffbd38610e41`  
		Last Modified: Fri, 07 Aug 2020 00:52:51 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba0a69a392fae34aa0613740276d16c5e0f064963a7079cb5d3c73bba31c4df`  
		Last Modified: Fri, 07 Aug 2020 00:52:56 GMT  
		Size: 14.1 MB (14142794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e326359e832250a0912fee7884b8b1ee1bc099ec9c38399135a851c0f1b22ce`  
		Last Modified: Fri, 07 Aug 2020 00:52:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de584a5b52f9033142aa58582985da5c4f18ca1d424027c31a9341efee3b745`  
		Last Modified: Fri, 07 Aug 2020 00:52:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a4b69536ef132dd422665a950a111ea97759b62b1ab942ed406e65136922f5`  
		Last Modified: Fri, 07 Aug 2020 00:52:50 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6affb40d7c30ab19f271447b8614b2f5373839ad43e8c34d27017f96592036`  
		Last Modified: Fri, 07 Aug 2020 00:52:50 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475c32f46a39605c62e732178478135ea75e3d91a4a8b8183ad7adf4fd8ab322`  
		Last Modified: Fri, 07 Aug 2020 03:20:07 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270b32b40fba16f38cc884a9d94eb4b423394c129e9be8e5d1ed64ad57166dd5`  
		Last Modified: Fri, 07 Aug 2020 03:20:08 GMT  
		Size: 3.3 MB (3338952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d545ba78744720b9b01c15dbd0b6079d63272dcd3699be79fbe0ea7308c0654`  
		Last Modified: Fri, 07 Aug 2020 03:20:13 GMT  
		Size: 9.7 MB (9653286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe109a9198fd653738677f3b76c557776ac1bc4aaeb3b86225b0436167d93d82`  
		Last Modified: Fri, 07 Aug 2020 03:20:07 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9265cd5f26f6fc1d20bf55158245edbd05b856eac490d347083a7d01933cbe57`  
		Last Modified: Fri, 07 Aug 2020 03:20:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:a9ac55a03ba619597ca6a4761be7ff0e6ec0909f7ffb0d9c97dad832162270df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173401907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30327410ea95f64428eefc4da40489ba6e492959b886c4cead92e2c4442929`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:02 GMT
ADD file:eca1a7737bd5e84ff883c4c284c0cd22492145d9cd7ae3b8e7b490e3d8e5aefb in / 
# Fri, 11 Dec 2020 03:34:11 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 09:35:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 11 Dec 2020 09:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 11 Dec 2020 09:37:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 09:37:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 09:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 09:43:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 11 Dec 2020 09:43:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 11 Dec 2020 09:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 11 Dec 2020 09:44:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 11 Dec 2020 09:44:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 11 Dec 2020 09:45:00 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 11 Dec 2020 09:45:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 11 Dec 2020 09:45:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 09:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 09:45:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 11:51:03 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 11 Dec 2020 11:51:10 GMT
ENV PHP_VERSION=7.2.34
# Fri, 11 Dec 2020 11:51:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.34.tar.xz.asc
# Fri, 11 Dec 2020 11:51:20 GMT
ENV PHP_SHA256=409e11bc6a2c18707dfc44bc61c820ddfd81e17481470f3405ee7822d8379903
# Fri, 11 Dec 2020 11:52:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 11 Dec 2020 11:52:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 11:59:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 11:59:53 GMT
COPY multi:dc714d093d9a94baf082b278964398d495faeef837d3357693090c43ebfb6fb4 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:00:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 12:00:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 11 Dec 2020 12:00:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 12:00:48 GMT
STOPSIGNAL SIGWINCH
# Fri, 11 Dec 2020 12:00:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 11 Dec 2020 12:00:56 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 12:01:07 GMT
EXPOSE 80
# Fri, 11 Dec 2020 12:01:22 GMT
CMD ["apache2-foreground"]
# Sat, 12 Dec 2020 03:15:35 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 12 Dec 2020 03:15:39 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 12 Dec 2020 03:15:49 GMT
RUN a2enmod rewrite
# Sat, 12 Dec 2020 03:19:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.19; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sat, 12 Dec 2020 03:19:34 GMT
VOLUME [/var/www/html]
# Sat, 12 Dec 2020 03:19:37 GMT
ENV JOOMLA_VERSION=3.9.22
# Sat, 12 Dec 2020 03:19:44 GMT
ENV JOOMLA_SHA512=826f01683bd3d86f45a0e59dd6265cccdbeea9709604d19091572f6c5e3f8cd91a645789f6b8e8040c641badf76381acc4719cb29754c5d2bb2d5b6f4d17a60d
# Sat, 12 Dec 2020 03:20:09 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 12 Dec 2020 03:20:16 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Sat, 12 Dec 2020 03:20:17 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Sat, 12 Dec 2020 03:20:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 12 Dec 2020 03:20:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c0f0648876332890be87a9f32ec4ad2a939e805be3152ab991a923f7dec2b35d`  
		Last Modified: Fri, 11 Dec 2020 03:41:39 GMT  
		Size: 30.5 MB (30524717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5b99ad441d88921297aa0d8c7e2939c5e9612193590ff93145ebd13672ca87`  
		Last Modified: Fri, 11 Dec 2020 12:43:40 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a1c0581b0c2819f18cd9c840a6d32586aa9de3889e54251a3327b0b77c3cb5`  
		Last Modified: Fri, 11 Dec 2020 12:43:59 GMT  
		Size: 82.3 MB (82259915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5dbb5ac2103376300e56e95cc3ccd22e74917a509747b1dd2049869642692e`  
		Last Modified: Fri, 11 Dec 2020 12:43:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1cc816ea84b3a6ebd801a1e953d4afae51890cc4615b4689a104267b7d7de`  
		Last Modified: Fri, 11 Dec 2020 12:44:56 GMT  
		Size: 19.8 MB (19817738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492dff1cd8cb5ef532e553a18fbb10193b386b2a3fd13799a01c79bf8fecf327`  
		Last Modified: Fri, 11 Dec 2020 12:44:51 GMT  
		Size: 484.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659212e8c9d5e16eb1fdfeeb59b411bb6589a67dc62c2fb00f0d03a261fa3175`  
		Last Modified: Fri, 11 Dec 2020 12:44:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6fc5941393eeac9896abd604865378448723fe333ad896190d71a8d343a955`  
		Last Modified: Fri, 11 Dec 2020 12:56:05 GMT  
		Size: 12.6 MB (12647677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff2b1ab464268038bbcdcb4cae6f821556ea7e2cc72ff4efb80bab9f5be051f`  
		Last Modified: Fri, 11 Dec 2020 12:56:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c745d97a23db7f57b4cc8a39809232581019feb6edc11043d10883fd1a80e56`  
		Last Modified: Fri, 11 Dec 2020 12:56:04 GMT  
		Size: 14.9 MB (14858346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c1a1326fa7e92a03da3895952c78673c1d2b7a339d52404812f361de0841f6`  
		Last Modified: Fri, 11 Dec 2020 12:56:01 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44b6ff54cb2b66c7628cbc4527a31b80fb8b08b2705082f06eb5efef1a240c6`  
		Last Modified: Fri, 11 Dec 2020 12:56:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b26b209044dbce728cb5f482c10dab1014c3081cd0b3e34ba0e7708e835fac`  
		Last Modified: Fri, 11 Dec 2020 12:56:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec3018512bf9609b5fc61249e2ad4f02d98ab6340dfac7e6f769259c56e55ac`  
		Last Modified: Fri, 11 Dec 2020 12:56:00 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de148661959e609c57ab45e07cbead53668855a56cd56a81733e1a44c7a565c`  
		Last Modified: Sat, 12 Dec 2020 03:58:07 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e90a56a6657b795d6497d5ae8afa4ad60fef2ffe389d2d30e1c8fa740712d4`  
		Last Modified: Sat, 12 Dec 2020 03:58:09 GMT  
		Size: 3.6 MB (3595481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5fc415b6de08456dea93c41a47e5e791670c26dd1356303e97342becbfd164b`  
		Last Modified: Sat, 12 Dec 2020 03:58:13 GMT  
		Size: 9.7 MB (9690278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e7a74ce6aa5ea7a91926939123edaf0dd4b1ce447eb21cd0d3364af169fc4d`  
		Last Modified: Sat, 12 Dec 2020 03:58:07 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a368d87a817d2c9c3c34d584623f8ac4be4ac4ff810c33405659f85f77e630`  
		Last Modified: Sat, 12 Dec 2020 03:58:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-apache` - linux; s390x

```console
$ docker pull joomla@sha256:2d30c023436abec99fd3673b61766bfd2cc7da90f8552914c73cdde670c0d4dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147733405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9380f2ad47e360c556e7fedae1b66285d90b2a5850fa1e6e9b368b66356c6c06`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 11:11:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 11 Dec 2020 11:11:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 11 Dec 2020 11:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 11:12:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Dec 2020 11:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 11 Dec 2020 11:16:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 11 Dec 2020 11:16:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 11 Dec 2020 11:17:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 11 Dec 2020 11:17:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 11 Dec 2020 11:17:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 11 Dec 2020 11:17:05 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Fri, 11 Dec 2020 11:17:06 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Fri, 11 Dec 2020 11:17:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:17:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Dec 2020 11:17:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Dec 2020 13:07:59 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 11 Dec 2020 13:08:00 GMT
ENV PHP_VERSION=7.2.34
# Fri, 11 Dec 2020 13:08:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.34.tar.xz.asc
# Fri, 11 Dec 2020 13:08:01 GMT
ENV PHP_SHA256=409e11bc6a2c18707dfc44bc61c820ddfd81e17481470f3405ee7822d8379903
# Fri, 11 Dec 2020 13:08:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 11 Dec 2020 13:08:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Dec 2020 13:12:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Dec 2020 13:12:59 GMT
COPY multi:dc714d093d9a94baf082b278964398d495faeef837d3357693090c43ebfb6fb4 in /usr/local/bin/ 
# Fri, 11 Dec 2020 13:13:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Dec 2020 13:13:03 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 11 Dec 2020 13:13:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Dec 2020 13:13:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 11 Dec 2020 13:13:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 11 Dec 2020 13:13:05 GMT
WORKDIR /var/www/html
# Fri, 11 Dec 2020 13:13:06 GMT
EXPOSE 80
# Fri, 11 Dec 2020 13:13:06 GMT
CMD ["apache2-foreground"]
# Fri, 11 Dec 2020 17:44:11 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 11 Dec 2020 17:44:11 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 11 Dec 2020 17:44:13 GMT
RUN a2enmod rewrite
# Fri, 11 Dec 2020 17:47:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.19; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:47:38 GMT
VOLUME [/var/www/html]
# Fri, 11 Dec 2020 17:47:38 GMT
ENV JOOMLA_VERSION=3.9.22
# Fri, 11 Dec 2020 17:47:39 GMT
ENV JOOMLA_SHA512=826f01683bd3d86f45a0e59dd6265cccdbeea9709604d19091572f6c5e3f8cd91a645789f6b8e8040c641badf76381acc4719cb29754c5d2bb2d5b6f4d17a60d
# Fri, 11 Dec 2020 17:47:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 11 Dec 2020 17:47:56 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 11 Dec 2020 17:47:56 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 11 Dec 2020 17:47:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Dec 2020 17:47:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e848b987a55bcc9612a0ff983cfffc62ac173eb600e57e1f26d2f62d666fdf`  
		Last Modified: Fri, 11 Dec 2020 13:46:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeb6ec9142dee6d014f57c94fb0a215e2d28aa691b8568428e5e462d17ebd92`  
		Last Modified: Fri, 11 Dec 2020 13:46:19 GMT  
		Size: 64.7 MB (64707189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd418c632e5e527db12983ceffec6fb69c3ae70b420bb36ce3f0bc2f72b76bee`  
		Last Modified: Fri, 11 Dec 2020 13:46:08 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c27fa8d6c033bb6eb8edfe95328683591c0a4f6da22496bef5bcc6820050f55`  
		Last Modified: Fri, 11 Dec 2020 13:46:55 GMT  
		Size: 18.5 MB (18524998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2f7c3fe697fb3c5d37183a5ba4ec1ec85713bc8312d43e83ce67082f0bc04`  
		Last Modified: Fri, 11 Dec 2020 13:46:51 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c28aa1ab7bf0ca80b41f2d404a96e514e6595bd1646ac7104bd8aba3b3cccc`  
		Last Modified: Fri, 11 Dec 2020 13:46:52 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9853849dae73df7d177ef07c63b51102ff1471edac29d71f21c8e23b8f9041b0`  
		Last Modified: Fri, 11 Dec 2020 13:54:03 GMT  
		Size: 12.6 MB (12646123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb0f44557b16bbfd183258902d24d43a860933492540a194c57a28ed7befdc6`  
		Last Modified: Fri, 11 Dec 2020 13:54:01 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfaf3ded13dbee8075d5f92a659ea5a66b6f52afb4a1c78ed88ccd0d6319581`  
		Last Modified: Fri, 11 Dec 2020 13:54:01 GMT  
		Size: 13.1 MB (13090948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052f73a98a50822099222aed72d6a01a4a06901870c7dbc0092e2ae5c54763d3`  
		Last Modified: Fri, 11 Dec 2020 13:53:59 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e5ddfb7abedb181be074dff28849896251dd7489d696faf25f13821d679383`  
		Last Modified: Fri, 11 Dec 2020 13:54:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c2255dc2eddf26b832dce90b392fcb6f01e052805282be46ce7d9f626c4a9`  
		Last Modified: Fri, 11 Dec 2020 13:53:59 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850d75048b0f28121bd2db6bb2714270d2aafcd895951b155238ba3477936b9`  
		Last Modified: Fri, 11 Dec 2020 13:53:59 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6591e6b526c8a1114101743eeab5cd7d2f73641321b99995ded41997d36fc0`  
		Last Modified: Fri, 11 Dec 2020 18:21:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea41143e1f33f895b9dc42e3674322a6d69b664249e30122e8db2703fe7f374`  
		Last Modified: Fri, 11 Dec 2020 18:21:18 GMT  
		Size: 3.4 MB (3352181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2942914a2074422b46d06af9a1bfe2f2a08e7371dc745639058efb671bea695c`  
		Last Modified: Fri, 11 Dec 2020 18:21:20 GMT  
		Size: 9.7 MB (9690277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a20c2b74ae8c765b65abdd156d53f13fd79d3c2d8ec5c54c9c7bd4eba10edd8`  
		Last Modified: Fri, 11 Dec 2020 18:21:20 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce742746aaa85e88752773233cc9e8745ef6a93c36f16875cc42ac0361f07b77`  
		Last Modified: Fri, 11 Dec 2020 18:21:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
