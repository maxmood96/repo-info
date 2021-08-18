## `joomla:php7.4`

```console
$ docker pull joomla@sha256:d01c1fd8f1c9d9476292ff9edecbe6b55394528f39deb57d46ca6221b630c22e
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

### `joomla:php7.4` - linux; amd64

```console
$ docker pull joomla@sha256:5d59acf170139835238e7b8d85095bc7185ad6eacf406482266165a125b170dd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159861263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35898a7fbd0299a4f496bcbca67ccda55f501f996378e54710d8c23f5e8bdddb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:35:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 22 Jul 2021 01:35:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 22 Jul 2021 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:36:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Jul 2021 01:36:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Jul 2021 01:45:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 22 Jul 2021 01:45:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 22 Jul 2021 01:45:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 22 Jul 2021 01:45:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 22 Jul 2021 01:45:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 22 Jul 2021 01:45:26 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 22 Jul 2021 01:45:26 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 22 Jul 2021 01:45:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 01:45:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 01:45:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Jul 2021 02:56:09 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 30 Jul 2021 01:23:26 GMT
ENV PHP_VERSION=7.4.22
# Fri, 30 Jul 2021 01:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Fri, 30 Jul 2021 01:23:27 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Fri, 30 Jul 2021 01:23:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 30 Jul 2021 01:23:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Jul 2021 01:26:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Jul 2021 01:26:25 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 30 Jul 2021 01:26:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Jul 2021 01:26:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jul 2021 01:26:27 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 Jul 2021 01:26:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 30 Jul 2021 01:26:27 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 01:26:27 GMT
EXPOSE 80
# Fri, 30 Jul 2021 01:26:28 GMT
CMD ["apache2-foreground"]
# Fri, 30 Jul 2021 03:23:20 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 30 Jul 2021 03:23:21 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 30 Jul 2021 03:23:22 GMT
RUN a2enmod rewrite
# Fri, 30 Jul 2021 03:24:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Jul 2021 03:24:59 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 03:24:59 GMT
ENV JOOMLA_VERSION=3.9.28
# Fri, 30 Jul 2021 03:25:00 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Fri, 30 Jul 2021 03:25:04 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 30 Jul 2021 03:25:05 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 30 Jul 2021 03:25:05 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 30 Jul 2021 03:25:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 03:25:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03c99d34ed5eef03bd9b50e93e7c4ef428d351bc473dbc5af6b35e3b38ca23`  
		Last Modified: Thu, 22 Jul 2021 04:14:30 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f637ed06e1a5cbebe59f7e1102e78d40b788c8ff3143b1c6e6e2d1fda3b8554`  
		Last Modified: Thu, 22 Jul 2021 04:14:43 GMT  
		Size: 76.7 MB (76681016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd84713df3e0b309ebfe29910fd6efc5803314e93a7866d1e5e31b458f719d`  
		Last Modified: Thu, 22 Jul 2021 04:14:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75835d9b84b3757d1deb834824a4479ed9d423cd4593672e9cbbed7a777aff31`  
		Last Modified: Thu, 22 Jul 2021 04:15:18 GMT  
		Size: 18.7 MB (18679369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514983ec064c16e8f52a86598455ddeddf91ff2842c474059e4bba4c1fe25ca`  
		Last Modified: Thu, 22 Jul 2021 04:15:15 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec742b42e20a7b9594a3277ab8c630885e93558bdffdd3c85e13627d84a9a9a6`  
		Last Modified: Thu, 22 Jul 2021 04:15:15 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec0037df356a6abca694cde784862c7941ac2775c6e7168dd23c6635f482623`  
		Last Modified: Fri, 30 Jul 2021 02:24:40 GMT  
		Size: 10.7 MB (10686686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12533b9aae46469f7241c21186b1e784b001dd2d62ad16765987e666e8b14163`  
		Last Modified: Fri, 30 Jul 2021 02:24:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35321669eeaa955cde37eae5036022fe6e1ae7cc4f72d12538b4a8839d08e744`  
		Last Modified: Fri, 30 Jul 2021 02:24:39 GMT  
		Size: 13.8 MB (13842918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b13b2730b4a24871433d66bcdf00cae089dbc5feaa31882488279e61f4bc3a`  
		Last Modified: Fri, 30 Jul 2021 02:24:37 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fbc18466a3b04fb62d55d8c5d1ca91e8619b9936f0cfa49ba4f08d9ab328dc`  
		Last Modified: Fri, 30 Jul 2021 02:24:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1db32813f924c9d18ea7af90cc54a1e0dc13c86c976c57e9085c1265163e086`  
		Last Modified: Fri, 30 Jul 2021 02:24:37 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98307d27c968a75cd44be4cd6262a0adeca48eb72ad350ab2955ed07c51e891e`  
		Last Modified: Fri, 30 Jul 2021 03:30:08 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599b3d0b521ed98452ba94672fd87c2ac94b0af86ca80887dda9af5482a2b6b`  
		Last Modified: Fri, 30 Jul 2021 03:30:09 GMT  
		Size: 3.2 MB (3172809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d68c1890cace2b4b91f7e59ce48f5d71be014e62c9fad48f44a1d794a54aa1`  
		Last Modified: Fri, 30 Jul 2021 03:30:11 GMT  
		Size: 9.6 MB (9645156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fefc65c28b86a3c81f4f3a0ac046914acac4f76fa8e992c9a04259050fde33`  
		Last Modified: Fri, 30 Jul 2021 03:30:08 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2048f843b82f786c189144f3f0455df9875d1e52011efc375dd5823477d169b`  
		Last Modified: Fri, 30 Jul 2021 03:30:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; arm variant v5

```console
$ docker pull joomla@sha256:4bbff3f3d8a1d161f132fa3b8596b2133659adbff81618f98b3d1107673892e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137982809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dba108191822ba8ec70ac748b9392d13307d97311f3719224c118efd005270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:50:06 GMT
ADD file:885454a996e63d5eb93f1f365a3be77a441f368d7f5a77a7fd1636edf5d0b8cd in / 
# Thu, 22 Jul 2021 00:50:07 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:06:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 22 Jul 2021 12:06:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 22 Jul 2021 12:06:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Jul 2021 12:06:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Jul 2021 12:12:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 22 Jul 2021 12:12:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 22 Jul 2021 12:13:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 22 Jul 2021 12:13:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 22 Jul 2021 12:13:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 22 Jul 2021 12:13:11 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 22 Jul 2021 12:13:12 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 22 Jul 2021 12:13:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 12:13:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 12:13:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Jul 2021 12:57:10 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 30 Jul 2021 00:08:31 GMT
ENV PHP_VERSION=7.4.22
# Fri, 30 Jul 2021 00:08:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Fri, 30 Jul 2021 00:08:32 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Fri, 30 Jul 2021 00:08:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 30 Jul 2021 00:08:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:13:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Jul 2021 00:13:05 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:13:07 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Jul 2021 00:13:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jul 2021 00:13:07 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 Jul 2021 00:13:08 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:13:08 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 00:13:09 GMT
EXPOSE 80
# Fri, 30 Jul 2021 00:13:09 GMT
CMD ["apache2-foreground"]
# Fri, 30 Jul 2021 02:18:22 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 30 Jul 2021 02:18:23 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 30 Jul 2021 02:18:25 GMT
RUN a2enmod rewrite
# Fri, 30 Jul 2021 02:22:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Jul 2021 02:22:54 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 02:22:55 GMT
ENV JOOMLA_VERSION=3.9.28
# Fri, 30 Jul 2021 02:22:55 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Fri, 30 Jul 2021 02:23:07 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 30 Jul 2021 02:23:08 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 30 Jul 2021 02:23:08 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 30 Jul 2021 02:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 02:23:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2b96a0a1ddfe4fab89025b13e583392414251af73361434f28af076c3db77100`  
		Last Modified: Thu, 22 Jul 2021 01:02:11 GMT  
		Size: 24.9 MB (24879093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861382e8dbbd820d9a4538ddaf29e0b0c0f515fd90639c058287fa2019743660`  
		Last Modified: Thu, 22 Jul 2021 14:08:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e4ad6d85e91d0126ac6accc3d3b3547c140b899b07c20d2c87902e712437ce`  
		Last Modified: Thu, 22 Jul 2021 14:09:18 GMT  
		Size: 58.8 MB (58820397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439bf04f412bbb2a80ba86c2de602f373457faad3f7b80124b562f47d6cdb43b`  
		Last Modified: Thu, 22 Jul 2021 14:08:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe412a5712e333b44d6b1b8dceb3529d0a67d781e92609f7c795ecbfc8c383`  
		Last Modified: Thu, 22 Jul 2021 14:10:11 GMT  
		Size: 18.0 MB (18025970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e55f2e42cb9f14e5ad99de21becff215ea7ac4ba2a8ecc168bfb10c08bd1a3e`  
		Last Modified: Thu, 22 Jul 2021 14:09:58 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0bca6f16c2d923262c2864bb98880465bcaa6524489f3754d41d093589dc2c`  
		Last Modified: Thu, 22 Jul 2021 14:09:58 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd8eb9e020eaffd0fafab486ccf1d202083ea66c4476568eeb06588274fb3f4`  
		Last Modified: Fri, 30 Jul 2021 00:40:09 GMT  
		Size: 10.7 MB (10684776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5d2e0fd124404fc7f08b9881f238949915ad87796a11f8c5362b7b4c7b37b8`  
		Last Modified: Fri, 30 Jul 2021 00:40:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a45519840859629d87ab773aff241870b4ec92c2dac3d77878b2b509765fad`  
		Last Modified: Fri, 30 Jul 2021 00:40:14 GMT  
		Size: 12.9 MB (12925322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ff7d6aa5d6383fc40dd51a99a342f44ad8ab68430d16fb6162e1f334fcf0f3`  
		Last Modified: Fri, 30 Jul 2021 00:40:04 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef81ac9eef724671647cad63943ba19dde4f37bc463e3ddfe0c4a997e16b6213`  
		Last Modified: Fri, 30 Jul 2021 00:40:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a1462210a4b827a782c3cbc4977261f54cf687e36426db7efed7aecd804665`  
		Last Modified: Fri, 30 Jul 2021 00:40:04 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423f033b3a62de84248c8308c64483cec9527f86d8547092e4690b920d017f96`  
		Last Modified: Fri, 30 Jul 2021 02:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1bdfdf73ed8ce421fefa48bd2fd2ab177400701e8db17aea7f939100f53ff7`  
		Last Modified: Fri, 30 Jul 2021 02:31:41 GMT  
		Size: 3.0 MB (2994564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c27d756efead2f46716a2c7700074ddac923b32fc81b5649b1e448a9c0da3b`  
		Last Modified: Fri, 30 Jul 2021 02:31:49 GMT  
		Size: 9.6 MB (9645164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8068f443a80a202314be1bf4ee9f2c4fa9453c908a7343a1a314a55c9a1bff`  
		Last Modified: Fri, 30 Jul 2021 02:31:39 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfed11368d32a2d7db9d92e2454daf22487906b747aac30d02fcf46070adce5`  
		Last Modified: Fri, 30 Jul 2021 02:31:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; arm variant v7

```console
$ docker pull joomla@sha256:198326ce047d2fd820c107ef7094d218823f2824c143f6b7b941ce1f4491723b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135201557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba1556455a98ae12b10a9279ba088e01799dee39f508524d46c283f16d65fa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:36:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 22 Jul 2021 14:36:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 22 Jul 2021 14:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:37:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Jul 2021 14:37:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Jul 2021 14:42:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 22 Jul 2021 14:42:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 22 Jul 2021 14:43:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 22 Jul 2021 14:43:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 22 Jul 2021 14:43:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 22 Jul 2021 14:43:05 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 22 Jul 2021 14:43:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 22 Jul 2021 14:43:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 14:43:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 14:43:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Jul 2021 15:26:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 30 Jul 2021 00:40:19 GMT
ENV PHP_VERSION=7.4.22
# Fri, 30 Jul 2021 00:40:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Fri, 30 Jul 2021 00:40:20 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Fri, 30 Jul 2021 00:40:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 30 Jul 2021 00:40:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:44:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Jul 2021 00:44:33 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:44:35 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Jul 2021 00:44:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jul 2021 00:44:36 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 Jul 2021 00:44:36 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:44:37 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 00:44:37 GMT
EXPOSE 80
# Fri, 30 Jul 2021 00:44:37 GMT
CMD ["apache2-foreground"]
# Fri, 30 Jul 2021 05:07:47 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 30 Jul 2021 05:07:47 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 30 Jul 2021 05:07:49 GMT
RUN a2enmod rewrite
# Fri, 30 Jul 2021 05:12:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Jul 2021 05:12:01 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 05:12:01 GMT
ENV JOOMLA_VERSION=3.9.28
# Fri, 30 Jul 2021 05:12:02 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Fri, 30 Jul 2021 05:12:14 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 30 Jul 2021 05:12:15 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 30 Jul 2021 05:12:15 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 30 Jul 2021 05:12:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 05:12:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a6f750d4cc5b551e031499e5ced2f4e1692c17f980e3f3e9761851b1387df6`  
		Last Modified: Thu, 22 Jul 2021 16:43:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f840bf7e69f6fe9bd4011a2183f851a5cc6fc624d56bc9b46591cd2e53e0a944`  
		Last Modified: Thu, 22 Jul 2021 16:44:11 GMT  
		Size: 59.5 MB (59513541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee71535876e5795780f7bfcbfe8f27f77aa6f23604c136eca44283630cee1f2e`  
		Last Modified: Thu, 22 Jul 2021 16:43:33 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321c322abb00aaa1a1a9361dcc1b844d07f4a778a2740fda143e67b56903c197`  
		Last Modified: Thu, 22 Jul 2021 16:45:03 GMT  
		Size: 17.5 MB (17481720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b52be569cf1523c6fbe4bac9eb505e674557de2cb5e9225816da32d8412d43`  
		Last Modified: Thu, 22 Jul 2021 16:44:53 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6740a92d88c8a3cd252177314eb2726ed2630987afbdb2aa24475b31394a4ff7`  
		Last Modified: Thu, 22 Jul 2021 16:44:53 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4d688217fda9b0b98d360dff1ac30ce43b81a1bbfb24a6912c1e6b96110925`  
		Last Modified: Fri, 30 Jul 2021 01:51:27 GMT  
		Size: 10.7 MB (10684812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948d3097f492b6365352ccd497a20686898389fa04935977f3084a74b4c6ca4e`  
		Last Modified: Fri, 30 Jul 2021 01:51:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd12d0c11aff22c6de4ba9080094a52d465b7fd2f246bd058f2b99d68846d584`  
		Last Modified: Fri, 30 Jul 2021 01:51:30 GMT  
		Size: 12.2 MB (12225041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c10b70269fea247b479d05137fcfaa96208b77cc56f6db005715a1c3192630b`  
		Last Modified: Fri, 30 Jul 2021 01:51:22 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b18229b01945980566d61dbf04b99eb20438cf37fa4362cab3153448547a0e`  
		Last Modified: Fri, 30 Jul 2021 01:51:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09190746c068a9430fb61968bf10d6895b32c157d3207bdcf7198216fa8f472`  
		Last Modified: Fri, 30 Jul 2021 01:51:22 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a86a2f5edf63c580098bc6b48bcf854d4eee90d95aa950c039023007840627`  
		Last Modified: Fri, 30 Jul 2021 05:26:03 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0c447d8bdcb0e05c2df224351b92b47634491fdee380f888b760f2d35b5172`  
		Last Modified: Fri, 30 Jul 2021 05:26:05 GMT  
		Size: 2.9 MB (2897785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1713e9e90997646405982b2af630545494fa30ad26cbf739eb9403c354b8a01f`  
		Last Modified: Fri, 30 Jul 2021 05:26:14 GMT  
		Size: 9.6 MB (9645155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce64f8017c37098b6b894f06ee914386dc5006e8bd96ba82bb01eb693723b7b1`  
		Last Modified: Fri, 30 Jul 2021 05:26:04 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdd6e91423afee5623e5e2efebaa103f53e6aa79716d1618997195c63008c35`  
		Last Modified: Fri, 30 Jul 2021 05:26:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:666e2d9330495f91102c24554da6d3677573e190eb6bea02a3a24795d24f03a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151943333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d17f4764ef607abc40a369f13d6120f7d0bceb54d381ada434165c1b61c2da9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 07:59:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 22 Jul 2021 07:59:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 22 Jul 2021 08:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 08:00:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Jul 2021 08:00:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Jul 2021 08:05:20 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 22 Jul 2021 08:05:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 22 Jul 2021 08:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 22 Jul 2021 08:05:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 22 Jul 2021 08:05:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 22 Jul 2021 08:05:30 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 22 Jul 2021 08:05:30 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 22 Jul 2021 08:05:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 08:05:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 08:05:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Jul 2021 08:39:14 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 29 Jul 2021 23:21:44 GMT
ENV PHP_VERSION=7.4.22
# Thu, 29 Jul 2021 23:21:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Thu, 29 Jul 2021 23:21:45 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Thu, 29 Jul 2021 23:21:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 29 Jul 2021 23:21:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 29 Jul 2021 23:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 29 Jul 2021 23:24:03 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 29 Jul 2021 23:24:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 29 Jul 2021 23:24:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 29 Jul 2021 23:24:04 GMT
STOPSIGNAL SIGWINCH
# Thu, 29 Jul 2021 23:24:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 29 Jul 2021 23:24:05 GMT
WORKDIR /var/www/html
# Thu, 29 Jul 2021 23:24:05 GMT
EXPOSE 80
# Thu, 29 Jul 2021 23:24:05 GMT
CMD ["apache2-foreground"]
# Fri, 30 Jul 2021 01:09:46 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 30 Jul 2021 01:09:46 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 30 Jul 2021 01:09:46 GMT
RUN a2enmod rewrite
# Fri, 30 Jul 2021 01:11:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Jul 2021 01:11:21 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 01:11:21 GMT
ENV JOOMLA_VERSION=3.9.28
# Fri, 30 Jul 2021 01:11:21 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Fri, 30 Jul 2021 01:11:25 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 30 Jul 2021 01:11:26 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 30 Jul 2021 01:11:26 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 30 Jul 2021 01:11:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 01:11:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44bf6e1c2ffecd0cb804c5c9724b0f855bd48677407824a7b027d09146df1f0`  
		Last Modified: Thu, 22 Jul 2021 09:24:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b532f48bc4e6d89cb03d2540f7ae329af87d635ed865265a2023fbfe1fc232a`  
		Last Modified: Thu, 22 Jul 2021 09:24:23 GMT  
		Size: 70.4 MB (70356654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d305caec4584e49bc16aba430471ac6c8598af8fb0933c75aa4a3a4878de283`  
		Last Modified: Thu, 22 Jul 2021 09:24:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb3e27aa26a5cde375a6ee13ebc068fdc5ea10c6b69e68813bccf4e57bb58bf`  
		Last Modified: Thu, 22 Jul 2021 09:25:09 GMT  
		Size: 18.6 MB (18580237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a36074e496498c75c5a91a44760892c6a3e932e1e66a6c4219c041d5a55051d`  
		Last Modified: Thu, 22 Jul 2021 09:25:06 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413dbd802a98657ce5e9315ad03e87712a6be4b628a68c0cf805c0b59d90f2a5`  
		Last Modified: Thu, 22 Jul 2021 09:25:05 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fea15f4afff0553b356cb7e9543f807519c664c1ae16204463db945b685184`  
		Last Modified: Fri, 30 Jul 2021 00:18:56 GMT  
		Size: 10.7 MB (10685441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0b80c96668f3891789050131a268c868a842d66d11d070ae74cae5f34b1467`  
		Last Modified: Fri, 30 Jul 2021 00:18:53 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ab31cd0419853d38d537d0bf6a9f09be59c4ef01647c60f291905460e831fe`  
		Last Modified: Fri, 30 Jul 2021 00:18:55 GMT  
		Size: 13.6 MB (13627697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf8ee06b746ad0adf028f001523967cfc7bdb39fa09411b2fb8e5c947d300b`  
		Last Modified: Fri, 30 Jul 2021 00:18:53 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b30a35379f1ca9a5a3f4d0cce70531ea82c6b8ca2b3123213f23e0fa169550`  
		Last Modified: Fri, 30 Jul 2021 00:18:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6d9729c9a684a6b7563e92fceafdede63ac6866b89aded8ef91955e562f3d9`  
		Last Modified: Fri, 30 Jul 2021 00:18:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc7f8b636a0fc822057e8b883b7e627897c800e320f56d3f653745084d81c22`  
		Last Modified: Fri, 30 Jul 2021 01:17:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8b6ebc5f2d5160cee06eea6028ca6ff51ef91353e3a40035e6a59e51b98207`  
		Last Modified: Fri, 30 Jul 2021 01:17:38 GMT  
		Size: 3.1 MB (3125839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980df3c57066c74027d206c17c03b5dd7865076f78ba8a21dfca7ccc5a156293`  
		Last Modified: Fri, 30 Jul 2021 01:17:40 GMT  
		Size: 9.6 MB (9645167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e4fbc69445d68b7d8846af6254dcf68e95215a8aca003ca02300d2580b10ef`  
		Last Modified: Fri, 30 Jul 2021 01:17:37 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41ff8bc1a471b434ebe7403d53c6e68542341766c2c7cec0017c016a3ac17e4`  
		Last Modified: Fri, 30 Jul 2021 01:17:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; 386

```console
$ docker pull joomla@sha256:363388960f209ee7f53722680d65f7e1b54b1c34fa3e77de470f9225387f1aad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182361151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b794f2af46cc711482e245fc8bd43f9da911ce865262bc2c0dd25fb2b4b0977f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:40:28 GMT
ADD file:9afc107c0880864c9f16852bb6cc272a068f2c82a2df7c3444bbbc533f377156 in / 
# Tue, 17 Aug 2021 01:40:29 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 21:52:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 21:52:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 21:53:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:53:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 21:53:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 22:02:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 22:02:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 22:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 22:02:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 22:03:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 22:03:01 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 22:03:02 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 22:03:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 22:03:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 22:03:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 23:17:58 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 17 Aug 2021 23:17:58 GMT
ENV PHP_VERSION=7.4.22
# Tue, 17 Aug 2021 23:17:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Tue, 17 Aug 2021 23:17:59 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Tue, 17 Aug 2021 23:18:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 23:18:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:22:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 17 Aug 2021 23:23:00 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:23:01 GMT
RUN docker-php-ext-enable sodium
# Tue, 17 Aug 2021 23:23:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Aug 2021 23:23:01 GMT
STOPSIGNAL SIGWINCH
# Tue, 17 Aug 2021 23:23:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 17 Aug 2021 23:23:02 GMT
WORKDIR /var/www/html
# Tue, 17 Aug 2021 23:23:02 GMT
EXPOSE 80
# Tue, 17 Aug 2021 23:23:02 GMT
CMD ["apache2-foreground"]
# Wed, 18 Aug 2021 02:03:09 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 18 Aug 2021 02:03:09 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 18 Aug 2021 02:03:11 GMT
RUN a2enmod rewrite
# Wed, 18 Aug 2021 02:06:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Aug 2021 02:06:03 GMT
VOLUME [/var/www/html]
# Wed, 18 Aug 2021 02:06:03 GMT
ENV JOOMLA_VERSION=3.10.0
# Wed, 18 Aug 2021 02:06:04 GMT
ENV JOOMLA_SHA512=cf08194582bc7c88708200ecf664f6146e3244bca1e004deeb26c7459ebc3dab28da3b54d6f5e27bd3a12fe5defb3fe25266f4243f80e141f337a3d7a5e959fa
# Wed, 18 Aug 2021 02:06:14 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 18 Aug 2021 02:06:15 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Wed, 18 Aug 2021 02:06:16 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Wed, 18 Aug 2021 02:06:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 02:06:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6edd81381c438b83d2749dc056d46cd53320e27fb010b3e931ca1f0a752ddc07`  
		Last Modified: Tue, 17 Aug 2021 01:49:56 GMT  
		Size: 32.4 MB (32375657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde02ea43ea712182954343ee01b737ca6911ebdd1527d70da58d27b7a783340`  
		Last Modified: Wed, 18 Aug 2021 00:29:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75e82c83c65eda18ff4d7179d4b89c554a2792d4c36b04e03c2b9ede6515962`  
		Last Modified: Wed, 18 Aug 2021 00:29:45 GMT  
		Size: 92.7 MB (92712724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de8bb8fa63c86a9b01ad32ac4d7d10c7c3908efd8781160574009a46d9ec957`  
		Last Modified: Wed, 18 Aug 2021 00:29:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5020b8eb36c1dc1fdc847b0f9e27801ed927145025fa69137fd038e46f734cb`  
		Last Modified: Wed, 18 Aug 2021 00:30:31 GMT  
		Size: 19.7 MB (19691617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75db0c00c48f5a0fb6ca36f599e66882fbf1cb0a0ebccdfeb6c8df7d16448874`  
		Last Modified: Wed, 18 Aug 2021 00:30:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a535ab9a73ebe90cfb772df39ddb9b18ce3f36465cdc40ad268b1aebe247ff78`  
		Last Modified: Wed, 18 Aug 2021 00:30:24 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d3bb4f3f32fef0884297ebc9265b8149bf69aebf62e967ac9d0f9de69ec2d2`  
		Last Modified: Wed, 18 Aug 2021 00:39:15 GMT  
		Size: 10.7 MB (10688132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf55f0ed6d6a4152d3404cbd31c1c0bbe3bea2f45da121ea17d213d080861ee`  
		Last Modified: Wed, 18 Aug 2021 00:39:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d74832073247f5b027114d72105615aaed9d06c74e4f13cdf21195e51a63e4e`  
		Last Modified: Wed, 18 Aug 2021 00:39:17 GMT  
		Size: 14.2 MB (14236812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d960f1eae1e771eb71c2f4d25ab112792723ff85612f436cbd77feaa28a24ab0`  
		Last Modified: Wed, 18 Aug 2021 00:39:10 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4c8cf6c81b2ecffd8dd7b56c6c532b712c3978cf9b8f664ffe0af25046bcce`  
		Last Modified: Wed, 18 Aug 2021 00:39:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be7dcb8d904be03971456c7e0238a887d34f716245a91095008ae9840bd9115`  
		Last Modified: Wed, 18 Aug 2021 00:39:10 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214ee13273f8d656d371d2f0ee3b0d82141de0a7c935554246565ca9634fc5e`  
		Last Modified: Wed, 18 Aug 2021 02:12:27 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df241da87ef76bd3c4251888d5301d2e066e330b75d5288788511e8cde95fbf7`  
		Last Modified: Wed, 18 Aug 2021 02:12:28 GMT  
		Size: 3.0 MB (2971827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aca95c323648bf52bc8468dc678153f40d8cad7896a2616699b3fbcebb73900`  
		Last Modified: Wed, 18 Aug 2021 02:12:31 GMT  
		Size: 9.7 MB (9676857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1793ee65fef84ad2eb9655d5fdce60264b70cb3238704050127b96b7c0b5a9`  
		Last Modified: Wed, 18 Aug 2021 02:12:27 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf1ae9a39129d9ad9eb4bd8027d36bb9b83392111f47afe7a9c90eae1ff68c`  
		Last Modified: Wed, 18 Aug 2021 02:12:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; mips64le

```console
$ docker pull joomla@sha256:5aaff2eedeae6a74cd5b2be728ab91488c2a88e93533c7209e5e270283ac7e55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142425870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7cad0a0b44f142fbf141bec8a4866a98402fc0a36d888f42c8eeb2ea32baa6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:09:45 GMT
ADD file:1f77b9001c4977ba733be674fc5eb4b85130f1dea8a7b39d545b70f9c107695f in / 
# Thu, 22 Jul 2021 00:09:46 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 06:26:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 22 Jul 2021 06:26:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 22 Jul 2021 06:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 06:27:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Jul 2021 06:27:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Jul 2021 06:40:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 22 Jul 2021 06:40:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 22 Jul 2021 06:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 22 Jul 2021 06:40:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 22 Jul 2021 06:40:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 22 Jul 2021 06:40:51 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 22 Jul 2021 06:40:52 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 22 Jul 2021 06:40:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 06:40:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 06:40:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Jul 2021 08:20:52 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 29 Jul 2021 22:08:16 GMT
ENV PHP_VERSION=7.4.22
# Thu, 29 Jul 2021 22:08:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Thu, 29 Jul 2021 22:08:17 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Thu, 29 Jul 2021 22:08:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 29 Jul 2021 22:08:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 29 Jul 2021 22:16:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 29 Jul 2021 22:16:28 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Thu, 29 Jul 2021 22:16:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 29 Jul 2021 22:16:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 29 Jul 2021 22:16:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 29 Jul 2021 22:16:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 29 Jul 2021 22:16:32 GMT
WORKDIR /var/www/html
# Thu, 29 Jul 2021 22:16:32 GMT
EXPOSE 80
# Thu, 29 Jul 2021 22:16:32 GMT
CMD ["apache2-foreground"]
# Thu, 29 Jul 2021 23:25:44 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 29 Jul 2021 23:25:44 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 29 Jul 2021 23:25:46 GMT
RUN a2enmod rewrite
# Thu, 29 Jul 2021 23:30:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Jul 2021 23:30:42 GMT
VOLUME [/var/www/html]
# Thu, 29 Jul 2021 23:30:42 GMT
ENV JOOMLA_VERSION=3.9.28
# Thu, 29 Jul 2021 23:30:42 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Thu, 29 Jul 2021 23:30:56 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 29 Jul 2021 23:30:57 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Thu, 29 Jul 2021 23:30:57 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 29 Jul 2021 23:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Jul 2021 23:30:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:99ee621d0b0485e9de65aa19604aa2453d19ea7fc86b22c5b77c1bab74e3cb42`  
		Last Modified: Thu, 22 Jul 2021 00:16:11 GMT  
		Size: 25.8 MB (25812771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb76462e8360f1f5fff3b0d7916c87ab70e0bbd21e9c5d8bd295d716e936d11`  
		Last Modified: Thu, 22 Jul 2021 09:42:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec5c433242b6ed428599424c77a781f34a977b90bea14ac3510767faa7f11ee`  
		Last Modified: Thu, 22 Jul 2021 09:43:04 GMT  
		Size: 61.4 MB (61404113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6864500bb103f2e00dfcdfde3d5550d0f3d21a02b6cbd85a051712f0fcd37d2`  
		Last Modified: Thu, 22 Jul 2021 09:42:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebae74a74e418a6b26a8685a9f30d65e043f71e5c14665534532d7d717808e2f`  
		Last Modified: Thu, 22 Jul 2021 09:43:50 GMT  
		Size: 18.6 MB (18612034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd18bae59cc21c5192cd6ebcf87aca7d61db0d09f9ee65db01244796cfb953f`  
		Last Modified: Thu, 22 Jul 2021 09:43:36 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491f65ee045108657ab9827d2b775a68bfa8481b5936c92bddbbed07a4048630`  
		Last Modified: Thu, 22 Jul 2021 09:43:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edfe6dc444405ebddaf209cef723760c6034ce4da887c7dff7d0e0dd6b7a5b2`  
		Last Modified: Thu, 29 Jul 2021 22:49:31 GMT  
		Size: 10.7 MB (10684073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b18d905fa5e14a11617db97460b2cb6c7d4c60b524bb71b301f4898ed3745c0`  
		Last Modified: Thu, 29 Jul 2021 22:49:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4415c12c4eef524270e759f0d184990d3f3633717d64dd80da3a899f03e1c472`  
		Last Modified: Thu, 29 Jul 2021 22:49:42 GMT  
		Size: 13.1 MB (13148278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5903465635930c538a048a72cb866e5d0387bd1739a132f3dc59370d2107af86`  
		Last Modified: Thu, 29 Jul 2021 22:49:25 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7265af4c8a588a4cf438cff04c8f3bc83016d3ebd4e5ab3e78387429f4e04ac0`  
		Last Modified: Thu, 29 Jul 2021 22:49:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ced67693a1cef5c1c71722b967333debb78cbe6c292e8468eafd70351563489`  
		Last Modified: Thu, 29 Jul 2021 22:49:25 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b1de36f589a80f4b923e91f5383888cb21c9fe59097d44443a5eda48145607`  
		Last Modified: Thu, 29 Jul 2021 23:36:55 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12356814b6f476f24509f8a7aa42e275bde1c0f2c87fbefe2c789b9ec4ea6e1`  
		Last Modified: Thu, 29 Jul 2021 23:36:58 GMT  
		Size: 3.1 MB (3112020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da756d9833b5a494a37a5afcc5705106931053ffd9cd66a8693022ccece13347`  
		Last Modified: Thu, 29 Jul 2021 23:37:05 GMT  
		Size: 9.6 MB (9645164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9462399ee89e10cae3dfcc476dc36a29e23ad2802dd7d9a4f09ddde26438866`  
		Last Modified: Thu, 29 Jul 2021 23:36:55 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c3dc558da5151a58e1c8bfeae2b30ac1adf81fba1a8899272d61b0c6cbbc5`  
		Last Modified: Thu, 29 Jul 2021 23:36:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; ppc64le

```console
$ docker pull joomla@sha256:d312223ed68fd75752e7fd1b6a72fe335f5f8cc67a10410358a39a4c827eea91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171258122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e3429569d4c6089c536a1e87b4f1a13323c59fa965f59501e95d8715137607`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:19:04 GMT
ADD file:3a6bd6ce3eff98b88a13de5d0f26cff0b026f876674204dbad6f84fafcf145b1 in / 
# Thu, 22 Jul 2021 00:19:13 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:19:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 22 Jul 2021 12:19:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 22 Jul 2021 12:21:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:22:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Jul 2021 12:22:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Jul 2021 12:30:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 22 Jul 2021 12:30:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 22 Jul 2021 12:32:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 22 Jul 2021 12:32:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 22 Jul 2021 12:32:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 22 Jul 2021 12:32:58 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Thu, 22 Jul 2021 12:33:01 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Thu, 22 Jul 2021 12:33:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 12:33:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Jul 2021 12:33:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Jul 2021 14:30:33 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 29 Jul 2021 23:55:15 GMT
ENV PHP_VERSION=7.4.22
# Thu, 29 Jul 2021 23:55:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Thu, 29 Jul 2021 23:55:20 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Thu, 29 Jul 2021 23:56:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 29 Jul 2021 23:56:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 30 Jul 2021 00:01:56 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:02:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 30 Jul 2021 00:02:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jul 2021 00:02:10 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 Jul 2021 00:02:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 30 Jul 2021 00:02:14 GMT
WORKDIR /var/www/html
# Fri, 30 Jul 2021 00:02:17 GMT
EXPOSE 80
# Fri, 30 Jul 2021 00:02:22 GMT
CMD ["apache2-foreground"]
# Fri, 30 Jul 2021 04:05:56 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 30 Jul 2021 04:05:58 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 30 Jul 2021 04:06:08 GMT
RUN a2enmod rewrite
# Fri, 30 Jul 2021 04:11:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 30 Jul 2021 04:11:16 GMT
VOLUME [/var/www/html]
# Fri, 30 Jul 2021 04:11:23 GMT
ENV JOOMLA_VERSION=3.9.28
# Fri, 30 Jul 2021 04:11:27 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Fri, 30 Jul 2021 04:11:47 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 30 Jul 2021 04:11:54 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Fri, 30 Jul 2021 04:11:56 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 30 Jul 2021 04:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 30 Jul 2021 04:12:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1130517d52da84a09f9465006bddab5e49afd398860890eab6274fd0bff32371`  
		Last Modified: Thu, 22 Jul 2021 00:27:49 GMT  
		Size: 30.6 MB (30553709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c744aca669d54986809be1e2a67eb9e2f0c23ad48ab4da67e0c595bf97a76a`  
		Last Modified: Thu, 22 Jul 2021 16:07:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69949ff352dba1d2e0826d16d0b93a1105fece06120256646f820ca4e023a19`  
		Last Modified: Thu, 22 Jul 2021 16:08:59 GMT  
		Size: 82.3 MB (82290779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d27c09515bc1d70dc3cb8a856c0db0ce76de299c9919d580eb32f61a7ea517`  
		Last Modified: Thu, 22 Jul 2021 16:07:47 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884ffb9dee9d233677c4afa7cb1496169fa44e71d2a70f415e43eadd584ed49d`  
		Last Modified: Thu, 22 Jul 2021 16:09:54 GMT  
		Size: 19.8 MB (19818437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9b1c84d470f3cfc4ab9e253cfb3be6a0c76557d11e98658835e703c9f9e879`  
		Last Modified: Thu, 22 Jul 2021 16:09:49 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb570758ef2a62add994aa1b2640d417d903c0d8bcc489f347a9157ab906df1a`  
		Last Modified: Thu, 22 Jul 2021 16:09:47 GMT  
		Size: 520.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0d7dbc8fce9dfee0e3adf08621039f5e847f339c9628bebae409b05496545b`  
		Last Modified: Fri, 30 Jul 2021 01:08:22 GMT  
		Size: 10.7 MB (10686634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef335160e8381e12e047fd326f7d28c38c81e471264b940642c73ba169b9bcbe`  
		Last Modified: Fri, 30 Jul 2021 01:08:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aae1751681b7e83fa17865e272313c90e0e1bbc9aea5ec89db176cdd7c95049`  
		Last Modified: Fri, 30 Jul 2021 01:08:18 GMT  
		Size: 14.9 MB (14882432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ee72b35ea5c3170f73ecc37feac7e95b73c1300d4622ecd94bdcc27b16068a`  
		Last Modified: Fri, 30 Jul 2021 01:08:14 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea40b73d0bfff97b3ecd95a4bca3ac1fd01de7a9e1a5417e1f0df9f989620cb`  
		Last Modified: Fri, 30 Jul 2021 01:08:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587868979b89dd326d143582f3b251cb39dce356259b92ad7f32ebd564715511`  
		Last Modified: Fri, 30 Jul 2021 01:08:14 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f35cb12a96077b18201f9ac1344d672d63989411efa9a602eaa31279fa91341`  
		Last Modified: Fri, 30 Jul 2021 04:23:27 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216cbafea6b1746897073795b2a795250b585e0ec0e06d021828523a92751bf5`  
		Last Modified: Fri, 30 Jul 2021 04:23:28 GMT  
		Size: 3.4 MB (3373434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695b0db811cb0482a45afd097ff7daa0df71c3f3132f9e44417a9d64f3229bbe`  
		Last Modified: Fri, 30 Jul 2021 04:23:30 GMT  
		Size: 9.6 MB (9645163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fca30dd22b55e9a44410b2049bc74dcbffedf0e3b74408a35a02a6732350149`  
		Last Modified: Fri, 30 Jul 2021 04:23:27 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c1fbc611a0865dd4a02f82690473ab6c45ae66cbe48ace5b042c951a44acd3`  
		Last Modified: Fri, 30 Jul 2021 04:23:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php7.4` - linux; s390x

```console
$ docker pull joomla@sha256:c4857062736022e20fe50351e4a043d5a3c75f325c673059f028c6cf46550668
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145520768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b906b3d89910f4586fc168a99b0106b20ec58337256105245827152d8baaa7f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:14:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 17 Aug 2021 08:14:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Aug 2021 08:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 08:15:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Aug 2021 08:15:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 17 Aug 2021 08:18:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Aug 2021 08:18:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Aug 2021 08:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 17 Aug 2021 08:18:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 17 Aug 2021 08:18:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 17 Aug 2021 08:18:36 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Tue, 17 Aug 2021 08:18:36 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Tue, 17 Aug 2021 08:18:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 08:18:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Aug 2021 08:18:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Aug 2021 08:58:05 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 17 Aug 2021 08:58:06 GMT
ENV PHP_VERSION=7.4.22
# Tue, 17 Aug 2021 08:58:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.22.tar.xz.asc
# Tue, 17 Aug 2021 08:58:06 GMT
ENV PHP_SHA256=8e078cd7d2f49ac3fcff902490a5bb1addc885e7e3b0d8dd068f42c68297bde8
# Tue, 17 Aug 2021 08:58:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 17 Aug 2021 08:58:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 17 Aug 2021 09:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libonig-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 17 Aug 2021 09:01:17 GMT
COPY multi:e4407f0002276f00cc93b01e48696c1f677a5f7d3d194b3a84bec1cc5e733bcb in /usr/local/bin/ 
# Tue, 17 Aug 2021 09:01:19 GMT
RUN docker-php-ext-enable sodium
# Tue, 17 Aug 2021 09:01:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Aug 2021 09:01:20 GMT
STOPSIGNAL SIGWINCH
# Tue, 17 Aug 2021 09:01:21 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 17 Aug 2021 09:01:21 GMT
WORKDIR /var/www/html
# Tue, 17 Aug 2021 09:01:22 GMT
EXPOSE 80
# Tue, 17 Aug 2021 09:01:22 GMT
CMD ["apache2-foreground"]
# Tue, 17 Aug 2021 21:36:37 GMT
LABEL maintainer=Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Aug 2021 21:36:37 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Aug 2021 21:36:38 GMT
RUN a2enmod rewrite
# Tue, 17 Aug 2021 21:38:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libjpeg-dev 		libldap2-dev 		libmcrypt-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 		libzip-dev 	; 		docker-php-ext-configure gd --with-jpeg; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		gmp 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.20; 	pecl install memcached-3.1.5; 	pecl install redis-5.3.4; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 21:38:02 GMT
VOLUME [/var/www/html]
# Tue, 17 Aug 2021 21:38:02 GMT
ENV JOOMLA_VERSION=3.9.28
# Tue, 17 Aug 2021 21:38:03 GMT
ENV JOOMLA_SHA512=0751036475d9b527bd6da5f5a0c67e0c728449bf02ba9d508f206b4b2f35697093c938a4350b6e9412b16f5eabb8700575268b564fd8db451308ae4cfe4d882e
# Tue, 17 Aug 2021 21:38:09 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 17 Aug 2021 21:38:10 GMT
COPY file:f6b7a1c96cc89593a2b9ce4c68af350ae02f2e0c654cd5e842ff6c03641d470e in /entrypoint.sh 
# Tue, 17 Aug 2021 21:38:11 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Tue, 17 Aug 2021 21:38:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Aug 2021 21:38:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b509377d804e99fd3d8c5eb11fdcb06ac0592b467e1a5d34f296426a6cec6a14`  
		Last Modified: Tue, 17 Aug 2021 09:47:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef8dd0e3b36bc333683aafc6e422e5b3a9294feb703deb0a71a749175c45da6`  
		Last Modified: Tue, 17 Aug 2021 09:47:10 GMT  
		Size: 64.7 MB (64710852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b280bc6a9cfb9647c076d519d4cb4187708961862386bd0840ea7453ef0e7992`  
		Last Modified: Tue, 17 Aug 2021 09:47:00 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de4b54aaf5dd53ad2ac62707dd4c5c8030890b676fbe5c7823d8f12bf768e2c`  
		Last Modified: Tue, 17 Aug 2021 09:47:35 GMT  
		Size: 18.5 MB (18524602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0abae072b87dfb79496fadfb5eb3277ce9996738210dbe9512ab90c3a6928cf`  
		Last Modified: Tue, 17 Aug 2021 09:47:32 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a36783568b3bb0a138246be89ef9fa42f2fea6526495960bcdaa1ab8f15c8f3`  
		Last Modified: Tue, 17 Aug 2021 09:47:32 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fdc7193604ef181fb670e3340eb48bb99195c80229816769ae0d09ad87c782`  
		Last Modified: Tue, 17 Aug 2021 09:51:10 GMT  
		Size: 10.7 MB (10685107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39e885a0f859eddfb637426a761b40e09a5e16f8359b4f095236269e48dad35`  
		Last Modified: Tue, 17 Aug 2021 09:51:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e14913997f081dcc827553f6e333e3dc78353f965783c6d2f253c8dd9ea190e`  
		Last Modified: Tue, 17 Aug 2021 09:51:10 GMT  
		Size: 13.1 MB (13058646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a062312c01e8512d51deb0479a8a2d5d99e567626cfabea332f57b90e756f7b`  
		Last Modified: Tue, 17 Aug 2021 09:51:08 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0777bd88a545785586fe5a4d48d7f6b396731c0b12cb25af82f56c396a65c6f`  
		Last Modified: Tue, 17 Aug 2021 09:51:08 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662784841910f15a3f7c67f9c37835775ed253fba46a3b77fbe2a8e723e0d24c`  
		Last Modified: Tue, 17 Aug 2021 09:51:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135936155abb84329e819f5304ca3f2981aeb3aa021bd1425be4261166a370b7`  
		Last Modified: Tue, 17 Aug 2021 21:43:08 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b64c526ee007bdf5b04202e381bec88200635870bc7595fecd1e8392c470af`  
		Last Modified: Tue, 17 Aug 2021 21:43:08 GMT  
		Size: 3.1 MB (3128035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7865364d0817ba62f0a178facbe80ee059c9d6390203035dd30c71c5259aea9`  
		Last Modified: Tue, 17 Aug 2021 21:43:10 GMT  
		Size: 9.6 MB (9645153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5977cc94935fa899d17647a0a54e0e3a613499d9028dbd1fefcf6750d98bf5f8`  
		Last Modified: Tue, 17 Aug 2021 21:43:08 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94572ca8be1a9615850ab13a7c211cf8d6d2d7e6bc6f40d9541b8bfbf35405cc`  
		Last Modified: Tue, 17 Aug 2021 21:43:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
