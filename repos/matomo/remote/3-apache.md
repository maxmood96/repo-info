## `matomo:3-apache`

```console
$ docker pull matomo@sha256:6cf45c3239079c2df63a9dd2a1b894b90dd8da7fc1442689525626ef59ba137a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `matomo:3-apache` - linux; amd64

```console
$ docker pull matomo@sha256:681359bdc0e586446f616b52685f22dda8dcd57524dfc7d5c69f5c0e1cf014da
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165666801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6caad7c05b1ca38983015c261c423722a54641456ce21fe54520565bc1b9128`
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
# Sat, 01 Feb 2020 19:34:53 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 20 Feb 2020 21:25:07 GMT
ENV PHP_VERSION=7.4.3
# Thu, 20 Feb 2020 21:25:07 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Thu, 20 Feb 2020 21:25:07 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Thu, 20 Feb 2020 21:25:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Feb 2020 21:25:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 20 Feb 2020 21:28:13 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:28:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Feb 2020 21:28:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Feb 2020 21:28:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Feb 2020 21:28:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 20 Feb 2020 21:28:14 GMT
WORKDIR /var/www/html
# Thu, 20 Feb 2020 21:28:14 GMT
EXPOSE 80
# Thu, 20 Feb 2020 21:28:15 GMT
CMD ["apache2-foreground"]
# Fri, 21 Feb 2020 04:38:16 GMT
LABEL maintainer=pierre@piwik.org
# Fri, 21 Feb 2020 04:40:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 04:40:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 25 Feb 2020 01:25:38 GMT
ENV MATOMO_VERSION=3.13.3
# Tue, 25 Feb 2020 01:27:48 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 814E346FA01A20DBB04B6807B5DBD5925590A237; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Feb 2020 01:27:48 GMT
COPY file:5a36d7fba12e383595e7235267e54c5714dbf865acd4c4596c92ac0f17d139b3 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Tue, 25 Feb 2020 01:27:48 GMT
COPY file:5a7e05d095f2d5d960fd43fac9e7317ffe1cd3fb9251933251a337b583272d45 in /entrypoint.sh 
# Tue, 25 Feb 2020 01:27:49 GMT
VOLUME [/var/www/html]
# Tue, 25 Feb 2020 01:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 25 Feb 2020 01:27:49 GMT
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
	-	`sha256:bcd58f07153bff23fc6abb2998faec828aaf895c5a35db60e259b3511402a8b0`  
		Last Modified: Fri, 21 Feb 2020 02:27:03 GMT  
		Size: 10.6 MB (10598839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c63de37dd423c2d4b56504898b271e32ebaf254ac91753bb091d428438b083`  
		Last Modified: Fri, 21 Feb 2020 02:27:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09759644ef6aecd308e01045ca20931df3ae5c4dac7f9961c370b3856463d418`  
		Last Modified: Fri, 21 Feb 2020 02:27:07 GMT  
		Size: 13.8 MB (13802434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fa00a2e45bae0ec7abccd3a672af91510cbb122bfbb5e234729e73a15bd6c2`  
		Last Modified: Fri, 21 Feb 2020 02:27:00 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9483a8f9b3b63bc5500fb5914071673530f811bae1a6113500770f8853e28e`  
		Last Modified: Fri, 21 Feb 2020 02:27:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8e8708ca3f2f95472c57b15744ce8fc512cad146f709fb66be3135fe9b028a`  
		Last Modified: Fri, 21 Feb 2020 02:27:00 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be5096280c36126664d320271b0811ff5bb37b28d735f666f0e48bbc2e4122b`  
		Last Modified: Fri, 21 Feb 2020 04:44:07 GMT  
		Size: 3.4 MB (3387763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a952d9299d247ec05eaa3eb3e758410d137afca26611b8c9c741f8d1b0642d26`  
		Last Modified: Fri, 21 Feb 2020 04:44:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7be4a73713983b368525aca7746e40619d64bb62e8d4f061f649312ae241b5c`  
		Last Modified: Tue, 25 Feb 2020 01:33:22 GMT  
		Size: 15.5 MB (15451681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb89e8e3a92e44abd95469378d94b3179af5a911f0491d9229e3d83583b7f8a`  
		Last Modified: Tue, 25 Feb 2020 01:33:19 GMT  
		Size: 303.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7149e962bf121ae7cc46c68230869763b43f9dd03b637c0a5f6dc961d2e99419`  
		Last Modified: Tue, 25 Feb 2020 01:33:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:3-apache` - linux; arm variant v5

```console
$ docker pull matomo@sha256:3c5a4ca533fd5006cfe9be64964b71cbbb39f28885aaf76912626d951ab1b0aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143803300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d37fd6fd5ffbe35e93c0d729254d6158a778f49e04a33d33aadb0cced7c682d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:47:49 GMT
ADD file:745d3236976c8213b805ca6d14f150561816cd2eeec5aa7e1aaea44d9d5675e9 in / 
# Wed, 26 Feb 2020 00:47:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:32:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 26 Feb 2020 04:32:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 26 Feb 2020 04:33:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:33:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Feb 2020 04:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Feb 2020 04:38:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 26 Feb 2020 04:38:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 26 Feb 2020 04:38:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 26 Feb 2020 04:38:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 26 Feb 2020 04:38:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 26 Feb 2020 04:38:39 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 26 Feb 2020 04:38:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 26 Feb 2020 04:38:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 04:38:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 04:38:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 26 Feb 2020 04:38:42 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 26 Feb 2020 04:38:43 GMT
ENV PHP_VERSION=7.4.3
# Wed, 26 Feb 2020 04:38:44 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Wed, 26 Feb 2020 04:38:45 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Wed, 26 Feb 2020 04:39:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Feb 2020 04:39:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Feb 2020 04:42:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 26 Feb 2020 04:42:14 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Wed, 26 Feb 2020 04:42:16 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Feb 2020 04:42:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Feb 2020 04:42:18 GMT
STOPSIGNAL SIGWINCH
# Wed, 26 Feb 2020 04:42:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 26 Feb 2020 04:42:19 GMT
WORKDIR /var/www/html
# Wed, 26 Feb 2020 04:42:20 GMT
EXPOSE 80
# Wed, 26 Feb 2020 04:42:21 GMT
CMD ["apache2-foreground"]
# Wed, 26 Feb 2020 15:39:07 GMT
LABEL maintainer=pierre@piwik.org
# Wed, 26 Feb 2020 15:41:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 15:41:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Feb 2020 15:41:40 GMT
ENV MATOMO_VERSION=3.13.3
# Wed, 26 Feb 2020 15:42:14 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 814E346FA01A20DBB04B6807B5DBD5925590A237; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 15:42:16 GMT
COPY file:5a36d7fba12e383595e7235267e54c5714dbf865acd4c4596c92ac0f17d139b3 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Wed, 26 Feb 2020 15:42:17 GMT
COPY file:5a7e05d095f2d5d960fd43fac9e7317ffe1cd3fb9251933251a337b583272d45 in /entrypoint.sh 
# Wed, 26 Feb 2020 15:42:18 GMT
VOLUME [/var/www/html]
# Wed, 26 Feb 2020 15:42:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 15:42:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d9f9009f908455fa93c5b3e0d3230df44ea75299b2de375ab35b74193f679076`  
		Last Modified: Wed, 26 Feb 2020 00:59:18 GMT  
		Size: 24.8 MB (24830277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d924f652197b083a9a110930b7548ba9fe1fcc87e963cd10516dd54b172a9804`  
		Last Modified: Wed, 26 Feb 2020 06:04:05 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd86ee1863629868607b0a8c088897c302f5f1e23d0bd51a610f0d5aae26bdcf`  
		Last Modified: Wed, 26 Feb 2020 06:04:26 GMT  
		Size: 58.8 MB (58799831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e751ab6d9f11edd9376e6fa63465ad0c6a006fc52c130bdf4f5b8ff05ffe936`  
		Last Modified: Wed, 26 Feb 2020 06:04:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29c6f074c8b56a4ced1fc26a03ebbaf23a55333eafec2cc5bfe35d18b28d508`  
		Last Modified: Wed, 26 Feb 2020 06:04:59 GMT  
		Size: 18.0 MB (18024359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c312669fae45780587f8489022310772f13d0279f13e1e169b91bac753d015`  
		Last Modified: Wed, 26 Feb 2020 06:04:53 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349ecc709c43cc8747f1d8ad4b055f5bece773687c9ec100f662d8e872681ff4`  
		Last Modified: Wed, 26 Feb 2020 06:04:53 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d2f9c7b0f1380ca961b022e085a3872bc2f2d7990ad1eb809c44457a4f9af6`  
		Last Modified: Wed, 26 Feb 2020 06:04:54 GMT  
		Size: 10.6 MB (10596749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea418f7c591b1020dcd4aabea2a668a0fba5e75a7b78e2290440afd6ed234960`  
		Last Modified: Wed, 26 Feb 2020 06:04:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7ba2b85df6b5dbfbdbba473fb0870475cb18502df98febfb109efa5fad2083`  
		Last Modified: Wed, 26 Feb 2020 06:04:57 GMT  
		Size: 12.9 MB (12889679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db3ab5f5e9022c3bd30fffb2072c92ea8a86ce8813a822e7f842d93946544fc`  
		Last Modified: Wed, 26 Feb 2020 06:04:52 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841ea883aaf717a45a88caa72e76ea8e81ad83f6f3cefd6cc173a6bf49fd6f94`  
		Last Modified: Wed, 26 Feb 2020 06:04:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f579ba3fbc9e64d18a45fc14f8f6cfbe71180370db5a3f0d4c6cf645f4c711`  
		Last Modified: Wed, 26 Feb 2020 06:04:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f009830a82117c60728a0c242c7727c577f5c5f48343fbf57281fc55458e59c`  
		Last Modified: Wed, 26 Feb 2020 15:46:05 GMT  
		Size: 3.2 MB (3206382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47252b4b31cf27d8e976053f631e1978d473759d554cb10951bee31eee9272dc`  
		Last Modified: Wed, 26 Feb 2020 15:46:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434c69d2916dc9080be772534c3fba19533320308ab5a0ccadbce76ac652dcdd`  
		Last Modified: Wed, 26 Feb 2020 15:46:11 GMT  
		Size: 15.4 MB (15449826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2454e188e4d5c48325df2feb66bbec227a5f4177e81d6076767c1d9046be20a0`  
		Last Modified: Wed, 26 Feb 2020 15:46:04 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753e1718f175bf8d5fbbc02a4ef43686c88c3e0f82747cba2d3ebe54511b17ca`  
		Last Modified: Wed, 26 Feb 2020 15:46:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:3-apache` - linux; arm variant v7

```console
$ docker pull matomo@sha256:12e9a599f32e1f31a6023cf233b2f8d9feec3d76937824823b998a27beced93c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141005906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74580f3f771304728972189a9fafac6824c9b2325559f64fab632fdd7043bafe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:52:11 GMT
ADD file:2488038744e2e15217e67dd7f4bec5dcc7e9abe8a1010fe720a5ba7cbe7ab0eb in / 
# Wed, 26 Feb 2020 00:52:13 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:27:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 26 Feb 2020 14:27:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 26 Feb 2020 14:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:27:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Feb 2020 14:28:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Feb 2020 14:31:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 26 Feb 2020 14:31:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 26 Feb 2020 14:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 26 Feb 2020 14:32:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 26 Feb 2020 14:32:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 26 Feb 2020 14:32:15 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 26 Feb 2020 14:32:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 26 Feb 2020 14:32:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 14:32:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 14:32:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 26 Feb 2020 14:32:22 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 26 Feb 2020 14:32:23 GMT
ENV PHP_VERSION=7.4.3
# Wed, 26 Feb 2020 14:32:24 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Wed, 26 Feb 2020 14:32:26 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Wed, 26 Feb 2020 14:32:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Feb 2020 14:32:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:35:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 26 Feb 2020 14:35:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:35:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Feb 2020 14:35:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Feb 2020 14:35:45 GMT
STOPSIGNAL SIGWINCH
# Wed, 26 Feb 2020 14:35:46 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 26 Feb 2020 14:35:47 GMT
WORKDIR /var/www/html
# Wed, 26 Feb 2020 14:35:48 GMT
EXPOSE 80
# Wed, 26 Feb 2020 14:35:49 GMT
CMD ["apache2-foreground"]
# Thu, 27 Feb 2020 01:26:17 GMT
LABEL maintainer=pierre@piwik.org
# Thu, 27 Feb 2020 01:28:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 01:28:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 27 Feb 2020 01:28:59 GMT
ENV MATOMO_VERSION=3.13.3
# Thu, 27 Feb 2020 01:29:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 814E346FA01A20DBB04B6807B5DBD5925590A237; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 01:29:32 GMT
COPY file:5a36d7fba12e383595e7235267e54c5714dbf865acd4c4596c92ac0f17d139b3 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Thu, 27 Feb 2020 01:29:33 GMT
COPY file:5a7e05d095f2d5d960fd43fac9e7317ffe1cd3fb9251933251a337b583272d45 in /entrypoint.sh 
# Thu, 27 Feb 2020 01:29:34 GMT
VOLUME [/var/www/html]
# Thu, 27 Feb 2020 01:29:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 01:29:36 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fff3167bf8c79dc08baf67eb607823aadcbee2033f9620cc502e2c49423f605b`  
		Last Modified: Wed, 26 Feb 2020 01:07:32 GMT  
		Size: 22.7 MB (22699783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cd5cd61b6f8de3cb9b8eaf9920ee92db196f4c73365a731f08c51fdec97be4`  
		Last Modified: Wed, 26 Feb 2020 15:55:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b7e5098979c0c6921b0ba0a8f1e1625ffe7a6f8b565feae67a7a293e74e9db`  
		Last Modified: Wed, 26 Feb 2020 15:55:46 GMT  
		Size: 59.5 MB (59501205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2e6e500bc14a91c0e209ad61d4cab4947d2f99c2be6908475b8c3d61189f25`  
		Last Modified: Wed, 26 Feb 2020 15:55:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96129b300ee13117f2e91bbbeb1b1c0f050ff559195f3868d9dea095e9cc0040`  
		Last Modified: Wed, 26 Feb 2020 15:56:21 GMT  
		Size: 17.5 MB (17482498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9609adc074bde9ab5e5e3e4ad529f15389d8713a0e08d313f25bb5b6728d477e`  
		Last Modified: Wed, 26 Feb 2020 15:56:16 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c123cbb02068e03e45997be8582ae08b24d8ff8ec2716c611db76465f9c1d46`  
		Last Modified: Wed, 26 Feb 2020 15:56:16 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961c523b5cfeb0158cf38961b791f4180043536c4359554830165eab12ee2f4b`  
		Last Modified: Wed, 26 Feb 2020 15:56:17 GMT  
		Size: 10.6 MB (10596754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f7cf85a06e8f9f94a6527bef1492d48dd54e36e2a10ede46ecf81e4843cf7e`  
		Last Modified: Wed, 26 Feb 2020 15:56:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b22ca9418e38d0bc9645b4a38384c803470818c41d3a853cf761905ce51474`  
		Last Modified: Wed, 26 Feb 2020 15:56:18 GMT  
		Size: 12.2 MB (12195164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eda60b2082f4b113726088fb8a8eeb5528fb5461e84ebbc5286774c806e188a`  
		Last Modified: Wed, 26 Feb 2020 15:56:14 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe919b4f84be19e3cabc726b186ffaae6a94344a7c97e5b1edf4d288e7ce252`  
		Last Modified: Wed, 26 Feb 2020 15:56:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86270bfac429a0bcba8b220b945037c1922cd8d9cfad0e7f33ea3f7a96230b7`  
		Last Modified: Wed, 26 Feb 2020 15:56:14 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f45df413be8bf0411165e0d4d5304b980830b472655105646104065df0fbc4`  
		Last Modified: Thu, 27 Feb 2020 01:33:14 GMT  
		Size: 3.1 MB (3074332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446902dcb76080595ed6c0832fb80a17a786f320072893343a320b8ad3b581a3`  
		Last Modified: Thu, 27 Feb 2020 01:33:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9646551cff13f32ee1570767743cdf97d482b18faeae32255830bd72765595`  
		Last Modified: Thu, 27 Feb 2020 01:33:21 GMT  
		Size: 15.4 MB (15449960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9a28ab525b7ce2717a0ad5b22ebb4da6232d589b48feb8402b59f70b327339`  
		Last Modified: Thu, 27 Feb 2020 01:33:13 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f531155a4cf7d21a54dd8a4269a2a3282507052dd2b58038149dd80ce442ec`  
		Last Modified: Thu, 27 Feb 2020 01:33:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:3-apache` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:65fca2dddcb092f5621e3d6c99e6ce4e815b159ec095642e61f38a66082c0623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157722730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8f18ce46d784ad024fd4a9076da163973187a7a597d47e48b8a53f1570233e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:46:51 GMT
ADD file:a93818b0ffcb2823807811dffd78092a3e3f4981aabf48c3cb75f2fa319ac055 in / 
# Wed, 26 Feb 2020 00:46:55 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 11:55:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 26 Feb 2020 11:55:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 26 Feb 2020 11:56:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 11:56:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Feb 2020 11:56:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Feb 2020 12:00:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 26 Feb 2020 12:00:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 26 Feb 2020 12:00:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 26 Feb 2020 12:00:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 26 Feb 2020 12:00:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 26 Feb 2020 12:00:43 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 26 Feb 2020 12:00:45 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 26 Feb 2020 12:00:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 12:00:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 12:00:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 26 Feb 2020 12:00:53 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 26 Feb 2020 12:00:55 GMT
ENV PHP_VERSION=7.4.3
# Wed, 26 Feb 2020 12:00:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Wed, 26 Feb 2020 12:00:59 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Wed, 26 Feb 2020 12:01:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Feb 2020 12:01:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Feb 2020 12:04:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 26 Feb 2020 12:04:35 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Wed, 26 Feb 2020 12:04:37 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Feb 2020 12:04:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Feb 2020 12:04:38 GMT
STOPSIGNAL SIGWINCH
# Wed, 26 Feb 2020 12:04:39 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 26 Feb 2020 12:04:40 GMT
WORKDIR /var/www/html
# Wed, 26 Feb 2020 12:04:41 GMT
EXPOSE 80
# Wed, 26 Feb 2020 12:04:42 GMT
CMD ["apache2-foreground"]
# Thu, 27 Feb 2020 03:18:54 GMT
LABEL maintainer=pierre@piwik.org
# Thu, 27 Feb 2020 03:21:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:21:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 27 Feb 2020 03:21:07 GMT
ENV MATOMO_VERSION=3.13.3
# Thu, 27 Feb 2020 03:21:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 814E346FA01A20DBB04B6807B5DBD5925590A237; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:21:32 GMT
COPY file:5a36d7fba12e383595e7235267e54c5714dbf865acd4c4596c92ac0f17d139b3 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Thu, 27 Feb 2020 03:21:33 GMT
COPY file:5a7e05d095f2d5d960fd43fac9e7317ffe1cd3fb9251933251a337b583272d45 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:21:34 GMT
VOLUME [/var/www/html]
# Thu, 27 Feb 2020 03:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:21:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f338bc35613f66cfaad272234de7b77a91d6c5422855bf6239f2b0ff9d73f0a4`  
		Last Modified: Wed, 26 Feb 2020 00:56:15 GMT  
		Size: 25.9 MB (25851563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe4ded10aa84b08ce645b2a064c692746e119bd7bdbeb50d004635ceec99237`  
		Last Modified: Wed, 26 Feb 2020 13:27:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a0cd710bad4e7ac9d5be343f0970fef306eeb91d1a80f7ad1849724764c4bc`  
		Last Modified: Wed, 26 Feb 2020 13:27:20 GMT  
		Size: 70.3 MB (70334994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4988beed3268a0092cad73bf3915a3dd39e2d730a4d549bb9c333b6bcc9cba6`  
		Last Modified: Wed, 26 Feb 2020 13:27:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc30c8501c0e3a4b5a426b2a6c45f8983ada2b381ad4d0a04176bde5e40fba47`  
		Last Modified: Wed, 26 Feb 2020 13:27:52 GMT  
		Size: 18.6 MB (18577731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b336db5f954338dd131a8f39e8ab21b9fc15388d0a0a55810c6189bc630eff50`  
		Last Modified: Wed, 26 Feb 2020 13:27:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc6705a5b21871b470803bcf2ecb06da02f9567cf7399546bfd562e3e587397`  
		Last Modified: Wed, 26 Feb 2020 13:27:47 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3188cdd5e8f621d472727306b28c0c60d35da074f0b8ec3086257359c6fd4f22`  
		Last Modified: Wed, 26 Feb 2020 13:27:48 GMT  
		Size: 10.6 MB (10597547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b298cddb1a258c4a93630d46a0d0f41838645c1a08cf0ddfb85956c0f3567c9`  
		Last Modified: Wed, 26 Feb 2020 13:27:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f86f1a69374b3b73b4a409e0f2f61ecc9abe7805602896e611942c38658ee1`  
		Last Modified: Wed, 26 Feb 2020 13:27:50 GMT  
		Size: 13.6 MB (13573826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b25c8060dec3d65bb5108ec351933b1b22071e720dc2a0a0debcb6ed0e8a0bc`  
		Last Modified: Wed, 26 Feb 2020 13:27:46 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86edf0ef20ee7117057a81f4d9caed837a91f2e99a73e06c7991147abb2c834a`  
		Last Modified: Wed, 26 Feb 2020 13:27:46 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5591a1f8ef692abc21c59068dad23736e9e13b4a817889b9cfe507f5e7341005`  
		Last Modified: Wed, 26 Feb 2020 13:27:46 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa417cea1629f8d117b82805776cdc6521486608481943a8fca77d1c8aee66c`  
		Last Modified: Thu, 27 Feb 2020 03:25:15 GMT  
		Size: 3.3 MB (3330127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7297e3ac22830fcafe0103fb89a5898886496cd2c5f70ef294cb988f4463707`  
		Last Modified: Thu, 27 Feb 2020 03:25:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07991001b22a52ac3439c5055d1f7ae6d06cc8456432dcde90dc5a910f7453c4`  
		Last Modified: Thu, 27 Feb 2020 03:25:19 GMT  
		Size: 15.5 MB (15450732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01cc32bed6f9c1c6aa7c76a6058d62c323034dc80de7dadc1b6a1d8597f1db4`  
		Last Modified: Thu, 27 Feb 2020 03:25:13 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f5540d228b1d36d7eb243fac69c10e54f1ec86e428dcd90dfb9bbd2faf8e07`  
		Last Modified: Thu, 27 Feb 2020 03:25:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:3-apache` - linux; 386

```console
$ docker pull matomo@sha256:0fb8301525c1e0d729169cf16985ea7e1abdc8fabf5cbbaa2fe2f4f1d4844758
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171663073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a268ad1c5d654ad83dd2283667c734177e20e2adce295faa70f4328771a942`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 00:32:17 GMT
ADD file:08977fa54555a1ed2ae44a3aec04df157092a6c1c1b70ce0407cc2dc2f8bcd76 in / 
# Wed, 26 Feb 2020 00:32:17 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 17:09:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 26 Feb 2020 17:09:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 26 Feb 2020 17:10:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 17:10:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Feb 2020 17:10:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Feb 2020 17:17:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 26 Feb 2020 17:17:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 26 Feb 2020 17:17:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 26 Feb 2020 17:17:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 26 Feb 2020 17:17:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 26 Feb 2020 17:17:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 26 Feb 2020 17:17:30 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 26 Feb 2020 17:17:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 17:17:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 17:17:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 26 Feb 2020 17:17:31 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 26 Feb 2020 17:17:31 GMT
ENV PHP_VERSION=7.4.3
# Wed, 26 Feb 2020 17:17:31 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Wed, 26 Feb 2020 17:17:31 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Wed, 26 Feb 2020 17:17:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Feb 2020 17:17:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Feb 2020 17:21:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 26 Feb 2020 17:21:41 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Wed, 26 Feb 2020 17:21:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Feb 2020 17:21:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Feb 2020 17:21:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 26 Feb 2020 17:21:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 26 Feb 2020 17:21:45 GMT
WORKDIR /var/www/html
# Wed, 26 Feb 2020 17:21:45 GMT
EXPOSE 80
# Wed, 26 Feb 2020 17:21:45 GMT
CMD ["apache2-foreground"]
# Wed, 26 Feb 2020 21:43:08 GMT
LABEL maintainer=pierre@piwik.org
# Wed, 26 Feb 2020 21:45:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 21:45:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Feb 2020 21:45:46 GMT
ENV MATOMO_VERSION=3.13.3
# Wed, 26 Feb 2020 21:46:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 814E346FA01A20DBB04B6807B5DBD5925590A237; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 21:46:02 GMT
COPY file:5a36d7fba12e383595e7235267e54c5714dbf865acd4c4596c92ac0f17d139b3 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Wed, 26 Feb 2020 21:46:03 GMT
COPY file:5a7e05d095f2d5d960fd43fac9e7317ffe1cd3fb9251933251a337b583272d45 in /entrypoint.sh 
# Wed, 26 Feb 2020 21:46:03 GMT
VOLUME [/var/www/html]
# Wed, 26 Feb 2020 21:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Feb 2020 21:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1de10f1ae2a5bfd5f34f19421ebd282580e443321e4947cdf5f943875782b018`  
		Last Modified: Wed, 26 Feb 2020 00:38:34 GMT  
		Size: 27.7 MB (27747667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63da883d1acf485a7b1cc92daec610b51a3619bad1c74646d2349d702e66678`  
		Last Modified: Wed, 26 Feb 2020 19:26:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6194ab862f4a0b8d6069fe53227b0a99ede3c9572bdd3a7a53f1c345933b00e`  
		Last Modified: Wed, 26 Feb 2020 19:27:12 GMT  
		Size: 81.2 MB (81198469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3174e482c145c56e48af068bfededb0f4176a4d233274aba6343c48fb2a056`  
		Last Modified: Wed, 26 Feb 2020 19:26:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb27e395c764f0a3f9ca49eef31ccb24f7377992fcad9029712199a1d534f6b1`  
		Last Modified: Wed, 26 Feb 2020 19:27:37 GMT  
		Size: 19.1 MB (19111905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d40ce7d32639c19d1581dd9c9188e567ef2cee34ea4b58599f1af4176db1ad`  
		Last Modified: Wed, 26 Feb 2020 19:27:31 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6162014f44f172cc8fc99b9f701119b8a665a64373699f9fcbde48f91d0a5e`  
		Last Modified: Wed, 26 Feb 2020 19:27:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569784587c3a0f75734d76f55f827edc8fd49cad2d9a874e6eb7ef24662842ab`  
		Last Modified: Wed, 26 Feb 2020 19:27:32 GMT  
		Size: 10.6 MB (10598012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7271d3bc01cfe76cf547959feed89d00483d23f086dc5a64e041c467bf2a60`  
		Last Modified: Wed, 26 Feb 2020 19:27:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30622ffb21f1965a87950cb945f57572e82b678dbd57ff21069867e31e630285`  
		Last Modified: Wed, 26 Feb 2020 19:27:36 GMT  
		Size: 14.1 MB (14133402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448530d65bd7a2b9ca1acbbcd5cba9da6c5212efe4aef161edfdf6b3ad5f7a03`  
		Last Modified: Wed, 26 Feb 2020 19:27:30 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaeee920fa37f280715478b2b86fb79f51049fcf09440a84766df6671b78e1c`  
		Last Modified: Wed, 26 Feb 2020 19:27:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625bec00f7b0123917c4557a15bf02b48eb7ef15f944b66162cedd1aeacad397`  
		Last Modified: Wed, 26 Feb 2020 19:27:29 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754709a40c657f21f2edb011fd2fdd25af122f82819c395e8840dbf3f11548e1`  
		Last Modified: Wed, 26 Feb 2020 21:49:00 GMT  
		Size: 3.4 MB (3416537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449dac011155747521df0b131b69e0d808ff81a51e12fdb8c270f433bea15dd2`  
		Last Modified: Wed, 26 Feb 2020 21:48:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da018a30df5865d2282655bb3d270db01bcd3a242c53e04e99d384fc41cb773`  
		Last Modified: Wed, 26 Feb 2020 21:49:12 GMT  
		Size: 15.5 MB (15450994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92080e16da230e1d8b3684543228c32e0a565b889feb0bdb71dd25c5bbaa7d4a`  
		Last Modified: Wed, 26 Feb 2020 21:48:58 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c9c17e3b2e814f868e544f0d34024aa562dccce33815d46d910c17d298a7d6`  
		Last Modified: Wed, 26 Feb 2020 21:48:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `matomo:3-apache` - linux; ppc64le

```console
$ docker pull matomo@sha256:1d8d18b759a9c39f69cf16d58e3f563127c6da5584a6f55e3343bcfebefd1e4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177091460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92629c3946b3b2f17e0aef795bc3a7fa8f7368e41d0b7c9ed714b838786949c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 26 Feb 2020 01:31:23 GMT
ADD file:430f1f769b86c60db1b8d2f96ed26c24837b3ff5730264be42a9c0cd8e43df7f in / 
# Wed, 26 Feb 2020 01:31:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 13:39:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 26 Feb 2020 13:39:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 26 Feb 2020 13:40:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 13:41:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Feb 2020 13:41:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Feb 2020 13:46:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 26 Feb 2020 13:46:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 26 Feb 2020 13:47:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 26 Feb 2020 13:47:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 26 Feb 2020 13:47:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 26 Feb 2020 13:47:51 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Wed, 26 Feb 2020 13:47:55 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Wed, 26 Feb 2020 13:47:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 13:47:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Feb 2020 13:48:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Wed, 26 Feb 2020 13:48:04 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 26 Feb 2020 13:48:06 GMT
ENV PHP_VERSION=7.4.3
# Wed, 26 Feb 2020 13:48:08 GMT
ENV PHP_URL=https://www.php.net/get/php-7.4.3.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.4.3.tar.xz.asc/from/this/mirror
# Wed, 26 Feb 2020 13:48:11 GMT
ENV PHP_SHA256=cf1f856d877c268124ded1ede40c9fb6142b125fdaafdc54f855120b8bc6982a PHP_MD5=
# Wed, 26 Feb 2020 13:48:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Feb 2020 13:48:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Feb 2020 13:52:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 26 Feb 2020 13:52:56 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Wed, 26 Feb 2020 13:53:01 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Feb 2020 13:53:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Feb 2020 13:53:06 GMT
STOPSIGNAL SIGWINCH
# Wed, 26 Feb 2020 13:53:08 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 26 Feb 2020 13:53:12 GMT
WORKDIR /var/www/html
# Wed, 26 Feb 2020 13:53:14 GMT
EXPOSE 80
# Wed, 26 Feb 2020 13:53:17 GMT
CMD ["apache2-foreground"]
# Thu, 27 Feb 2020 03:32:36 GMT
LABEL maintainer=pierre@piwik.org
# Thu, 27 Feb 2020 03:35:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		ldap 		mysqli 		opcache 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:35:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 27 Feb 2020 03:35:10 GMT
ENV MATOMO_VERSION=3.13.3
# Thu, 27 Feb 2020 03:36:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 814E346FA01A20DBB04B6807B5DBD5925590A237; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 03:36:32 GMT
COPY file:5a36d7fba12e383595e7235267e54c5714dbf865acd4c4596c92ac0f17d139b3 in /usr/local/etc/php/conf.d/php-matomo.ini 
# Thu, 27 Feb 2020 03:36:34 GMT
COPY file:5a7e05d095f2d5d960fd43fac9e7317ffe1cd3fb9251933251a337b583272d45 in /entrypoint.sh 
# Thu, 27 Feb 2020 03:36:37 GMT
VOLUME [/var/www/html]
# Thu, 27 Feb 2020 03:36:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Feb 2020 03:36:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:975241fcd2057cc8f4cb8f066d68ed18877152b88da11e682911ccc3bc3da7c4`  
		Last Modified: Wed, 26 Feb 2020 01:52:57 GMT  
		Size: 30.5 MB (30518427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57d9b8bc2eac5c6f4f9993a4c4b7bd08403a98d069eb7b3678d6fe8396f488`  
		Last Modified: Wed, 26 Feb 2020 15:58:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420ef5ae09970b307979254c32570cf02e8b0979b1bc6df0941e38eb670262a5`  
		Last Modified: Wed, 26 Feb 2020 15:59:12 GMT  
		Size: 82.3 MB (82259740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72af4000b0056d6328c78e7b5aa5de14c173ffd361612045bc4e3013bcb0fa8f`  
		Last Modified: Wed, 26 Feb 2020 15:58:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13063450f1fae407e2f5dfdaed0b40346c05f6a566b8261e9ec40c87da0a99ec`  
		Last Modified: Wed, 26 Feb 2020 16:00:17 GMT  
		Size: 19.8 MB (19811388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a750c8efaa8db87f2ee0ca169c14c7c764305e2a1f42ea0d221317adba5575a0`  
		Last Modified: Wed, 26 Feb 2020 16:00:05 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97334fa51526e6efd5eb2ef129e6f2af39c1b0d21c418ccf2559d7922a53522`  
		Last Modified: Wed, 26 Feb 2020 16:00:07 GMT  
		Size: 521.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cc6687c77c9db68ce7bfd8a89bd7ce7c765fd861c8fea48aeb7d635eda3bda`  
		Last Modified: Wed, 26 Feb 2020 16:00:06 GMT  
		Size: 10.6 MB (10598480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209d902e7985f874d2893c2cfc222e3462a79878932c25cbc8616f6d7542d840`  
		Last Modified: Wed, 26 Feb 2020 15:59:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8654e018bb5fa1aa349c54d418c86cda5633d3b4b2e6012e531d60ad7b6c3ec`  
		Last Modified: Wed, 26 Feb 2020 16:00:13 GMT  
		Size: 14.8 MB (14837699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b0325c993960faf35bd5841a5eeb0ac167a7a5e4dac8eef592836f19a70454`  
		Last Modified: Wed, 26 Feb 2020 15:59:59 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33798555876b2c843b34ce09282e43bb2c3dd1030fbe940a9cab02d3dfbadbee`  
		Last Modified: Wed, 26 Feb 2020 15:59:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ad19d0e6a96dc38da89bb5887de638e080a477b2cecc42cb2864965b65c05d`  
		Last Modified: Wed, 26 Feb 2020 15:59:59 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdef04a289208b779b7556b9c1990d1a0fdc4bdbb8f042cd187c07b585d0011d`  
		Last Modified: Thu, 27 Feb 2020 03:41:34 GMT  
		Size: 3.6 MB (3607371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca79b0ad6a80dc53a5b4c32ca79a8682c1ae65b38ecc26b3cb0023470bfde1f2`  
		Last Modified: Thu, 27 Feb 2020 03:41:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36409d6381a96f084e57507784f067104767490180f08dbfbd9a3b4cae89a8ce`  
		Last Modified: Thu, 27 Feb 2020 03:41:38 GMT  
		Size: 15.5 MB (15452139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f92cf09278c62abf75a1dcd16595b33092ab9623ee421fd3344e70075040acc`  
		Last Modified: Thu, 27 Feb 2020 03:41:33 GMT  
		Size: 305.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cb6e7b331484eb621ebce53a4f824eb862c479d9aae21fab1a385bdde6926b`  
		Last Modified: Thu, 27 Feb 2020 03:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
