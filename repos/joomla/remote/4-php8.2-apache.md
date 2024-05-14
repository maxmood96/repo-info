## `joomla:4-php8.2-apache`

```console
$ docker pull joomla@sha256:9297199d958906141c3916324a5f27cb5a0342e844d42899ac90b6c5acdd6ab1
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

### `joomla:4-php8.2-apache` - linux; amd64

```console
$ docker pull joomla@sha256:c6229a36856ebecd5f4f4b752e1a4a6e35c299a935d605f0c15ce559ac2b3bfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261623779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda038573714da1a9c63a04d4ced90371927dc0aaf3a64608b95e06ec162a4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:39:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 08:39:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 08:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:40:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 08:40:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 08:44:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 08:44:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 08:44:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 08:44:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 08:44:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 08:44:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 09:15:03 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 10 May 2024 22:24:00 GMT
ENV PHP_VERSION=8.2.19
# Fri, 10 May 2024 22:24:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 10 May 2024 22:24:01 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 10 May 2024 22:24:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 May 2024 22:24:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 May 2024 22:27:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 May 2024 22:27:39 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 May 2024 22:27:40 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 May 2024 22:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 May 2024 22:27:40 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 May 2024 22:27:40 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 May 2024 22:27:40 GMT
WORKDIR /var/www/html
# Fri, 10 May 2024 22:27:40 GMT
EXPOSE 80
# Fri, 10 May 2024 22:27:40 GMT
CMD ["apache2-foreground"]
# Fri, 10 May 2024 23:55:16 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 10 May 2024 23:55:16 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 11 May 2024 00:04:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 11 May 2024 00:06:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 11 May 2024 00:06:41 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 11 May 2024 00:06:41 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 11 May 2024 00:06:42 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sat, 11 May 2024 00:06:42 GMT
VOLUME [/var/www/html]
# Sat, 11 May 2024 00:06:42 GMT
ENV JOOMLA_VERSION=4.4.4
# Sat, 11 May 2024 00:06:42 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Sat, 11 May 2024 00:06:49 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 11 May 2024 00:06:49 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Sat, 11 May 2024 00:06:49 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Sat, 11 May 2024 00:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 May 2024 00:06:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93478d4793284c7a75389488e31ab45acb8ea56f8ba474bdb2359ecd2132177`  
		Last Modified: Wed, 24 Apr 2024 10:13:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74cc574d0d2183a964ea5880bba6308b7653c4cc7ff2010beb2c1b157168a3a`  
		Last Modified: Wed, 24 Apr 2024 10:13:18 GMT  
		Size: 104.4 MB (104357707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4782e138a9004836453694f515681a93d6635ab26f05b7f2dfea2baa4b761ad`  
		Last Modified: Wed, 24 Apr 2024 10:13:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeec87621aeb5b3bf8907398acc95a5e9b85a5f3faa6a68e0640e7d6653f850`  
		Last Modified: Wed, 24 Apr 2024 10:13:58 GMT  
		Size: 20.3 MB (20329716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1badcd002c0a773002eaf87724b5a303e17873ae752e7e69dfd6b22c05a7dea`  
		Last Modified: Wed, 24 Apr 2024 10:13:56 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d463a60cb62b1b64dd43c0defef018c6ab557e474c029d17824cc9d1b5d103`  
		Last Modified: Wed, 24 Apr 2024 10:13:55 GMT  
		Size: 515.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bce13a727be3ad7256f8b75af3d25c0a7bec550afe60b0a4714b164bbaa38b5`  
		Last Modified: Fri, 10 May 2024 23:19:45 GMT  
		Size: 12.4 MB (12428785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbeca1cab87b8da6e2d01bf831ca39eab38505949a395693195d5141b56bf57`  
		Last Modified: Fri, 10 May 2024 23:19:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9216544a8100ea19ea728dfe3ad2a7a299d940a64217866902b8fead28fcf864`  
		Last Modified: Fri, 10 May 2024 23:19:44 GMT  
		Size: 11.4 MB (11407462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3680ee4acbeaac93cf685d9521c50e8155d37083350a3b06b23f47f25c6f1b`  
		Last Modified: Fri, 10 May 2024 23:19:43 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fa048d3ad436b28b033ef7fc8c5ee8d9dc995bcd49c2cc9f77d44bfc5927d5`  
		Last Modified: Fri, 10 May 2024 23:19:43 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8be4124e519ada7e76d67f15ced6c1d7e0d3b2f31f7ecb2dd42e7c94f4cde36`  
		Last Modified: Fri, 10 May 2024 23:19:43 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3440ed3e165b63e8552f22dd933fdb115cb296112300b0fcdbc49e6b7829a4`  
		Last Modified: Sat, 11 May 2024 00:14:54 GMT  
		Size: 26.3 MB (26259560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9c88009834c81aea21eba915c193f06ba6e55653cda36dac76775695690d6e`  
		Last Modified: Sat, 11 May 2024 00:14:54 GMT  
		Size: 32.0 MB (32016664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4728839fa6e096a6736c05f9e114f1cc9aa262555d29a1cf475fe551f0dd5fd5`  
		Last Modified: Sat, 11 May 2024 00:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b82fe09d524525a44ec6f514c27004095701b573c6625f4fdee874f204a7ff`  
		Last Modified: Sat, 11 May 2024 00:14:48 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6009824da514a8d735e0298c0f1d01364d4e459c9bcc493e0e58a63d2fb821d0`  
		Last Modified: Sat, 11 May 2024 00:14:48 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69d02ff0f5badd00221095f2f2d423152c868d95d94671c9242e0c7300729af`  
		Last Modified: Sat, 11 May 2024 00:14:52 GMT  
		Size: 25.6 MB (25644132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4f96bb34af4f668be5cde9c142419191c15dfac8ad02972a7ed3084d90fee4`  
		Last Modified: Sat, 11 May 2024 00:14:48 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27ce55bda62a9c20afae8a8f7bd771db4eaa35787c1feb1d7cd1bfb3f87eeb8`  
		Last Modified: Sat, 11 May 2024 00:14:48 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:8152806d5b4fa4ef1530a1aca3db3b1b027ad1a899c485657b646d6139333580
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231437499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7d60e5fb1e022a4943e45027a5142c81bac8a460b5702692f48fbb39a8da42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:17:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 06:17:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 06:18:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:18:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 06:18:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 06:21:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 06:21:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 06:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 06:21:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 06:21:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 06:21:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 06:21:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 06:21:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 06:47:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 06:47:16 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 06:47:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 06:47:16 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 06:47:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 06:47:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 06:50:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 06:50:24 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 06:50:24 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 06:50:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 06:50:24 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 06:50:24 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 06:50:25 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 06:50:25 GMT
EXPOSE 80
# Tue, 14 May 2024 06:50:25 GMT
CMD ["apache2-foreground"]
# Tue, 14 May 2024 09:18:22 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 May 2024 09:18:22 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 May 2024 09:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:49:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 14 May 2024 09:49:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 14 May 2024 09:49:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 14 May 2024 09:49:30 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 14 May 2024 09:49:30 GMT
VOLUME [/var/www/html]
# Tue, 14 May 2024 09:49:30 GMT
ENV JOOMLA_VERSION=4.4.4
# Tue, 14 May 2024 09:49:30 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Tue, 14 May 2024 09:49:37 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 May 2024 09:49:38 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Tue, 14 May 2024 09:49:38 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 14 May 2024 09:49:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 09:49:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b283b382b2311252750e03cf28bb273177b1a644a513c67a0af84dc33bc0633`  
		Last Modified: Tue, 14 May 2024 07:33:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc40d9d7b09f9947ad3ebe49406fcf6ce7acb778623b45fcc96cebe1b4563f60`  
		Last Modified: Tue, 14 May 2024 07:33:21 GMT  
		Size: 82.0 MB (82002617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4db5c4a8625a25d7cecd1cc80936c109faf62308652fc85012e5a68f54d7372`  
		Last Modified: Tue, 14 May 2024 07:33:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b45579b8504eea68995af76de66f35d59d2e9ebe8389d7dd428ddebe1ecec2c`  
		Last Modified: Tue, 14 May 2024 07:34:04 GMT  
		Size: 19.6 MB (19622321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28ba7ac5fb1773d3617ca9bf789cb90fb8c23afe9fd53e6bd8dcc43b06478ec`  
		Last Modified: Tue, 14 May 2024 07:34:01 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd6f1599840943bf95f4f9fc58e6ece76c7a53b3b743b165633615cdf07e1c2`  
		Last Modified: Tue, 14 May 2024 07:34:00 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f651653ad680d69388e233633022099ed26500c524cffb7d0579f19d6c499`  
		Last Modified: Tue, 14 May 2024 07:37:20 GMT  
		Size: 12.4 MB (12426749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9bb448a18a9c5d7bb520f7ea0727d7132a5f5b500c77d533a8e94458e320c4`  
		Last Modified: Tue, 14 May 2024 07:37:18 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e1f89e164918e7fcbbdc83e85b27743eb6a792cb350eaff039244af911c6d6`  
		Last Modified: Tue, 14 May 2024 07:37:20 GMT  
		Size: 10.4 MB (10391929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75674d6e0316c5c39148436a657848562ce5d8978aba4c522f69b5dbae6276bd`  
		Last Modified: Tue, 14 May 2024 07:37:19 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac60bd3c69d7e558f5e7441e332894b4b8639c05a3447c4a9901411cffc8212c`  
		Last Modified: Tue, 14 May 2024 07:37:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec615a93cc2b5f252b3406e8f2ae2f7272b37a200c590c37a8810f05d410ac0a`  
		Last Modified: Tue, 14 May 2024 07:37:18 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10ed7651da0f544e9107241a71d46a36dc1b1bc14d994d4853d190189d10ab9c`  
		Last Modified: Tue, 14 May 2024 09:57:22 GMT  
		Size: 25.7 MB (25711496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a475eba0658eb9f81d4e51b1ecc96b6b4eb779e386924c4f05e811d205d3aa`  
		Last Modified: Tue, 14 May 2024 09:57:23 GMT  
		Size: 28.7 MB (28699094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a18ca81f7bb17e1035cb1702be6db7bf1c9373e6c4dd0c1c989290b6e74a7c`  
		Last Modified: Tue, 14 May 2024 09:57:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5308f8d195c1b732a3e153d6342113039631312206df9175bc8835be98ab69d4`  
		Last Modified: Tue, 14 May 2024 09:57:16 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55528cdc07b426721cda3d4140597b1d0a2d1f89138eaca6b51ade6a054c8f4`  
		Last Modified: Tue, 14 May 2024 09:57:16 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abef4fd23f5c19506c52b738bde8bdac7069a52e4651c3382e353b90affd547`  
		Last Modified: Tue, 14 May 2024 09:57:21 GMT  
		Size: 25.6 MB (25644099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc15b6c808157ff14ed60c147bd5764f9166c9487e2ea82c2ca063880caa454`  
		Last Modified: Tue, 14 May 2024 09:57:16 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ba4d9cafb61741d2d33470f3c85507e1ee74619361611d8c163092134bb53e`  
		Last Modified: Tue, 14 May 2024 09:57:16 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:ff75f81ffeb664c7e04607633761a809705c77b18ba609f5d278b1772b36bd1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220076959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e912842d2d04a7a733ba17130d674140b31d850028f4e6e6e1faf85b9f293f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:58:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 03:58:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 03:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:59:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 03:59:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 04:03:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 04:03:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 04:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 04:03:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 04:03:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 04:03:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 04:03:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 04:03:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 04:26:49 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 04:26:49 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 04:26:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 04:26:49 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 04:27:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 04:27:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 04:29:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 04:29:36 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 04:29:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 04:29:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 04:29:38 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 04:29:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 04:29:38 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 04:29:38 GMT
EXPOSE 80
# Tue, 14 May 2024 04:29:39 GMT
CMD ["apache2-foreground"]
# Tue, 14 May 2024 12:40:31 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 May 2024 12:40:32 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 May 2024 12:55:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 12:58:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 14 May 2024 12:58:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 14 May 2024 12:58:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 14 May 2024 12:58:26 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 14 May 2024 12:58:26 GMT
VOLUME [/var/www/html]
# Tue, 14 May 2024 12:58:26 GMT
ENV JOOMLA_VERSION=4.4.4
# Tue, 14 May 2024 12:58:26 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Tue, 14 May 2024 12:58:34 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 May 2024 12:58:35 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Tue, 14 May 2024 12:58:35 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 14 May 2024 12:58:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 12:58:35 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930fa116255ec27680b90a6ba22cc2c89d8749932a47c6d4e85670bd5f5895f`  
		Last Modified: Tue, 14 May 2024 05:10:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209a30fd2288462c9bd40bff3edad699d1f25378ba1f52a225423313692d28fb`  
		Last Modified: Tue, 14 May 2024 05:11:08 GMT  
		Size: 76.2 MB (76173233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f973b073d45c698f093d40ad07c6f3772965aec6d2ca899e4f939604ff77063f`  
		Last Modified: Tue, 14 May 2024 05:10:57 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a81ee217d111e55b42dacc84c4ea8a8b805f4b32ce08f913584fe3049432ba0`  
		Last Modified: Tue, 14 May 2024 05:11:54 GMT  
		Size: 19.1 MB (19059177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b244a7011bf77c7f6dbb7aeec8801541a4fcedc9b0d677e011ba3858486721`  
		Last Modified: Tue, 14 May 2024 05:11:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c308a4706893e3f7ca2cbb4a95bff0ddcb532c9ca5ee57e07ae406b7932dd2`  
		Last Modified: Tue, 14 May 2024 05:11:51 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207411a3fc351e4cd4dba4dc396802cd42ca26deaabe6592fb03eec3a94bd4f4`  
		Last Modified: Tue, 14 May 2024 05:15:35 GMT  
		Size: 12.4 MB (12426707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22896483e79b6b53e6f6524f5fa4d2f6c303c615384bae8c75f9492e5aff5ff2`  
		Last Modified: Tue, 14 May 2024 05:15:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde5dfa1efe02ba8930c1ee6983b1b4a6e805433936c3a0ecd3ba43afe87f5fa`  
		Last Modified: Tue, 14 May 2024 05:15:34 GMT  
		Size: 9.8 MB (9822182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc7ea2ba51377bccd06d804142a58cb19dba638d020993dd69053ccf8367268`  
		Last Modified: Tue, 14 May 2024 05:15:32 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5176d2149383ff89be494491e131c341136db4dcf4dfad7bf73b544cfef3cf7f`  
		Last Modified: Tue, 14 May 2024 05:15:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd844c572243e18bf237d8148b32b7c390f3e20985bdf3839c8ca27e43e32f`  
		Last Modified: Tue, 14 May 2024 05:15:32 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861c6cf147a35419b10f913bf52115ca6e40ed12c4856d6a6552c24d7c8859a6`  
		Last Modified: Tue, 14 May 2024 13:07:30 GMT  
		Size: 25.1 MB (25077671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d183f4304d27ba136713e4764ae59298d03e30264650abe8b375f1a5bfc150`  
		Last Modified: Tue, 14 May 2024 13:07:30 GMT  
		Size: 27.1 MB (27104385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144a4ad8980ce3357c99a339214b628bb7a09826d7f5e18469c2d4ddf794e9b0`  
		Last Modified: Tue, 14 May 2024 13:07:24 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e997e18f1a34c1ece783f2111c1fcd4fc063eb1f4ff4a415077881d7b0b832`  
		Last Modified: Tue, 14 May 2024 13:07:22 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612cbddcda865195ab095c9d38cd01a92b6484fa9544a69832cb7eb89f22a126`  
		Last Modified: Tue, 14 May 2024 13:07:22 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69b1bb7ec9be774d82506c32df34a0513cccdd5cdf5e011182eaddbed8b4aad`  
		Last Modified: Tue, 14 May 2024 13:07:28 GMT  
		Size: 25.6 MB (25644114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc113bd73ee16563cbfe3b44561b4f9e27eac86f7f7f9f8ee78ddc09b57bd985`  
		Last Modified: Tue, 14 May 2024 13:07:22 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf60ea4aabc0df27ed37d9529dd0bf0b747331c69e87b9a39e1b367141334e6`  
		Last Modified: Tue, 14 May 2024 13:07:21 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:2c5173b4f471507713dfe28af10a3e7c9c2028b3b5bf365816bb4b3cd5f3e2e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252931430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53f3be7b5f1154fa1a36f20e52fea9f520d0ddf8d2bf357be16226e474c9444`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:09:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:09:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:10:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:10:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:14:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:14:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:14:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:14:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:14:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:14:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:14:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 05:43:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 10 May 2024 23:20:41 GMT
ENV PHP_VERSION=8.2.19
# Fri, 10 May 2024 23:20:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 10 May 2024 23:20:41 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 10 May 2024 23:20:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 May 2024 23:20:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 May 2024 23:24:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 May 2024 23:24:02 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 May 2024 23:24:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 May 2024 23:24:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 May 2024 23:24:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 May 2024 23:24:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 May 2024 23:24:03 GMT
WORKDIR /var/www/html
# Fri, 10 May 2024 23:24:03 GMT
EXPOSE 80
# Fri, 10 May 2024 23:24:03 GMT
CMD ["apache2-foreground"]
# Sat, 11 May 2024 00:50:10 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 11 May 2024 00:50:11 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 11 May 2024 00:58:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 11 May 2024 01:00:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 11 May 2024 01:00:09 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 11 May 2024 01:00:09 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 11 May 2024 01:00:10 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sat, 11 May 2024 01:00:10 GMT
VOLUME [/var/www/html]
# Sat, 11 May 2024 01:00:10 GMT
ENV JOOMLA_VERSION=4.4.4
# Sat, 11 May 2024 01:00:10 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Sat, 11 May 2024 01:00:15 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 11 May 2024 01:00:16 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Sat, 11 May 2024 01:00:16 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Sat, 11 May 2024 01:00:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 May 2024 01:00:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246bb70e866bd7dd3dccad886145a828fb1a1323f17ef26ec181465dbcb0b28`  
		Last Modified: Wed, 24 Apr 2024 06:35:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d9cbc94d9e79c445b63152194f2f71247fc73f539ba2b78046fd04c59ff44b`  
		Last Modified: Wed, 24 Apr 2024 06:35:43 GMT  
		Size: 98.1 MB (98132015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760f776f4854c09ee785a8e7e0b102fbcd2483de52db872f8a92ce21e43cac04`  
		Last Modified: Wed, 24 Apr 2024 06:35:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a0ec8ef6bc2cde02f58dc81eeee21fde397e0ad51d4ab138f21b67b77c89c4`  
		Last Modified: Wed, 24 Apr 2024 06:36:24 GMT  
		Size: 20.3 MB (20322298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d170b72693bbaede3e95c7b3f669df38b31b21d3d1a25458e4153823999ceb1`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dda424ab92b122f202ae6b960aa32dd30bc2da243480399c10b1bb870e3342`  
		Last Modified: Wed, 24 Apr 2024 06:36:21 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcf27e9cf11cc19d9490533be7f869dae27f889eddc6f6437c006e2387f17fc`  
		Last Modified: Sat, 11 May 2024 00:13:36 GMT  
		Size: 12.4 MB (12428432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc4d463a2728065bbfd1a737d68e5ba7953a577da9390056bd7c2aea0b4f659`  
		Last Modified: Sat, 11 May 2024 00:13:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e33d10d18e7f056a379b32cc15b33e09244e2c320d0157d133d3b07a6a3ec7c`  
		Last Modified: Sat, 11 May 2024 00:13:35 GMT  
		Size: 11.4 MB (11414579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3759faaf4a9eab3b766b23928cf039298cba4317521ed4b532d0acef9b6225d0`  
		Last Modified: Sat, 11 May 2024 00:13:33 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ff3204e2861ce3d2f17dc3b313dcc2aceb4f8070ebea11b7fafa6d20bb1915`  
		Last Modified: Sat, 11 May 2024 00:13:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea66b9f88f3728305f34e7d304dff656e73e4cf80c1ebea60a490f92c8ea2eea`  
		Last Modified: Sat, 11 May 2024 00:13:33 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac91cb425838deb2973b1b751f1a542f4caa2daddb5e32f69a4fbf66db86c51`  
		Last Modified: Sat, 11 May 2024 01:07:46 GMT  
		Size: 26.2 MB (26184810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6773bbae73cddb3bc54be930c834bba98c498988de85b6a7ff4423f0d2fd9c6`  
		Last Modified: Sat, 11 May 2024 01:07:47 GMT  
		Size: 29.6 MB (29595955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6251d96332774a61b456aaa49c96d8eb378f1bde05800a2ddad8c59dae92db9f`  
		Last Modified: Sat, 11 May 2024 01:07:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ceabdb7f4272ec6df60654d1eee7070acd358aec1df48d418f87f87b76a4f`  
		Last Modified: Sat, 11 May 2024 01:07:41 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d79245dd426f05913376b82345f12d698b6a9cec281e36fb705ea9ae71496e1`  
		Last Modified: Sat, 11 May 2024 01:07:41 GMT  
		Size: 19.1 KB (19147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833d2cc5bf0fdea989f7f3ba003fbf88d2690b81d7057bfd1514b101d54747dc`  
		Last Modified: Sat, 11 May 2024 01:07:44 GMT  
		Size: 25.6 MB (25644132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a545f80772f981da6251d69ecfb964941a7262f6eba331d1c1eb4813eb22d223`  
		Last Modified: Sat, 11 May 2024 01:07:41 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ed8661d29ee4137f1e08efe060e4deaff6f2cf4bba3119ec520a7aa71519fd`  
		Last Modified: Sat, 11 May 2024 01:07:41 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; 386

```console
$ docker pull joomla@sha256:c9052d59f6282978ade347dbac42ef36ada25ed214b4fae7a11fb394e8374e84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260265604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b51e729cf5b07299870fdba300938703135fcda96d83dfae6c7f58fbe426f87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:02:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 05:02:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 05:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:03:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 05:03:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 05:10:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 05:10:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 05:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 05:10:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 05:10:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 05:10:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:10:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 05:10:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 06:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 10 May 2024 23:22:43 GMT
ENV PHP_VERSION=8.2.19
# Fri, 10 May 2024 23:22:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 10 May 2024 23:22:43 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 10 May 2024 23:22:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 May 2024 23:22:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 May 2024 23:29:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 May 2024 23:29:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 May 2024 23:29:11 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 May 2024 23:29:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 May 2024 23:29:12 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 May 2024 23:29:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 May 2024 23:29:12 GMT
WORKDIR /var/www/html
# Fri, 10 May 2024 23:29:12 GMT
EXPOSE 80
# Fri, 10 May 2024 23:29:12 GMT
CMD ["apache2-foreground"]
# Sat, 11 May 2024 01:22:12 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 11 May 2024 01:22:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 11 May 2024 01:34:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 11 May 2024 01:37:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 11 May 2024 01:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 11 May 2024 01:37:34 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 11 May 2024 01:37:35 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sat, 11 May 2024 01:37:35 GMT
VOLUME [/var/www/html]
# Sat, 11 May 2024 01:37:35 GMT
ENV JOOMLA_VERSION=4.4.4
# Sat, 11 May 2024 01:37:35 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Sat, 11 May 2024 01:37:44 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 11 May 2024 01:37:44 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Sat, 11 May 2024 01:37:45 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Sat, 11 May 2024 01:37:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 May 2024 01:37:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb1b3a226af34ddecc6d2893906c2c06039ad4a2e8de3b340d85dce69d80022`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492e3888464375d37ac47d192dc5edd8fa2a1146cc5b3542c21ca67bc5e080e6`  
		Last Modified: Wed, 24 Apr 2024 07:36:25 GMT  
		Size: 101.5 MB (101522095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a318120f6f010a0842e1a7d0c601c50a55f8f3822db28e6889a943b1e1c103`  
		Last Modified: Wed, 24 Apr 2024 07:36:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa961eb09ca3c9b99fc06b865a7a6fd8608a50684db856f6da97733cecb9c0e`  
		Last Modified: Wed, 24 Apr 2024 07:37:11 GMT  
		Size: 20.8 MB (20844719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8105c623b5e86209dc2d11e7aff7ae42685ea6efbd232f64750a7d2d42e817`  
		Last Modified: Wed, 24 Apr 2024 07:37:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c7989bc9f4db0aeee6f780bdfd90643adebf6585c505c8ba1cb7fdee8b4b7b`  
		Last Modified: Wed, 24 Apr 2024 07:37:06 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c178a245769d8df1210ed5a8d7228da9dfa2a2098389c0ab4638425d19810c32`  
		Last Modified: Sat, 11 May 2024 00:56:24 GMT  
		Size: 12.4 MB (12427795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6234debe7413d5618aa2b4da080630b648276fa8342461b3781fc5ef9603a0eb`  
		Last Modified: Sat, 11 May 2024 00:56:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0d9335a3183ba84e8ca15f7bfcd5bbc0bb20029a734a3fbfcde78c3f42289a`  
		Last Modified: Sat, 11 May 2024 00:56:25 GMT  
		Size: 11.6 MB (11639840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64b8917ffbc69528186f94ad45d6c353735967d20744eade755454c120bc93f`  
		Last Modified: Sat, 11 May 2024 00:56:21 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d73a9bbc8e05dface0e608bd6cfa75874a2e306cac4cf1ca8b7c295dadd06fc`  
		Last Modified: Sat, 11 May 2024 00:56:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bc7e2b63f91db3cb5db1880f3ae579c9dca795e243d125857e16c50cd8e8eb`  
		Last Modified: Sat, 11 May 2024 00:56:21 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93665c0e8ee59abac4a50bd0d9cf77e9037eafa8c1ec6d56613d21cee2235999`  
		Last Modified: Sat, 11 May 2024 01:47:51 GMT  
		Size: 26.7 MB (26701404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c1c601ed1a2c3f1b53deb58512f8262265014cd7ecbbf45c388f09d93664c`  
		Last Modified: Sat, 11 May 2024 01:47:53 GMT  
		Size: 31.3 MB (31293149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f441309e772e9c04d4ad2a5eb3d8f20972974e1964a80cd84d1d96171d666`  
		Last Modified: Sat, 11 May 2024 01:47:43 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128788895c42f202cb551aee15a5ddc036dc6ebb27c4ace817101267687eac59`  
		Last Modified: Sat, 11 May 2024 01:47:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7a6dfb5ab0b7c4907428ad27aa129fe6cd033a3d864aa3beef52f4b5090c62`  
		Last Modified: Sat, 11 May 2024 01:47:41 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3023908cdfa504eae8191c36ee5a4694d4a4b5a69ad23710492feb594cf4327`  
		Last Modified: Sat, 11 May 2024 01:47:50 GMT  
		Size: 25.6 MB (25644128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f076f2f5a7ffce1825cd7faf4a389cd64b162277c8dda38781da6da51e2c939b`  
		Last Modified: Sat, 11 May 2024 01:47:41 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0764cc582731ee83390d55dccaee5abc12b32acd46f57a21e3dbcbc1275e19`  
		Last Modified: Sat, 11 May 2024 01:47:42 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; mips64le

```console
$ docker pull joomla@sha256:31fe2a25434142be4419cfc219be0f35c56e40b8c2419a8c9b8752072636cd53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233190149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952ee7d5d9b5757df50015864f2838d6734f732694167aa82c5f28d2c1e3c650`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:50:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 24 Apr 2024 10:50:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Apr 2024 10:52:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:52:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Apr 2024 10:52:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 24 Apr 2024 11:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Apr 2024 11:09:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Apr 2024 11:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 24 Apr 2024 11:10:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 24 Apr 2024 11:10:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 24 Apr 2024 11:10:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 11:10:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Apr 2024 11:10:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Apr 2024 13:17:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 10 May 2024 23:36:18 GMT
ENV PHP_VERSION=8.2.19
# Fri, 10 May 2024 23:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 10 May 2024 23:36:25 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 10 May 2024 23:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 May 2024 23:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 May 2024 23:52:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 May 2024 23:52:39 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 10 May 2024 23:52:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 May 2024 23:52:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 May 2024 23:52:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 May 2024 23:52:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 10 May 2024 23:53:00 GMT
WORKDIR /var/www/html
# Fri, 10 May 2024 23:53:03 GMT
EXPOSE 80
# Fri, 10 May 2024 23:53:07 GMT
CMD ["apache2-foreground"]
# Sat, 11 May 2024 01:50:02 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Sat, 11 May 2024 01:50:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Sat, 11 May 2024 02:20:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 11 May 2024 02:32:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 11 May 2024 02:32:39 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 11 May 2024 02:32:45 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 11 May 2024 02:32:52 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sat, 11 May 2024 02:32:57 GMT
VOLUME [/var/www/html]
# Sat, 11 May 2024 02:33:01 GMT
ENV JOOMLA_VERSION=4.4.4
# Sat, 11 May 2024 02:33:06 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Sat, 11 May 2024 02:33:43 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Sat, 11 May 2024 02:33:51 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Sat, 11 May 2024 02:33:57 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Sat, 11 May 2024 02:34:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 May 2024 02:34:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2dfa3d36c21ae20eadd92525e61517d0277ef14398994b215d50f524e69655`  
		Last Modified: Wed, 24 Apr 2024 17:08:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a61fb25c010a33f1a3c4b6a08fb02be6a6c0b5d22d9b3ce52a1dd1c356a0024`  
		Last Modified: Wed, 24 Apr 2024 17:09:13 GMT  
		Size: 80.5 MB (80474735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239652ab0a80c5dad89154985f8ceec71b76e056f18e7dcb6ffaea27e8984b59`  
		Last Modified: Wed, 24 Apr 2024 17:08:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796fa395fb05e5a39254d0d9582b02b4121109eda21399913880a92cf308465f`  
		Last Modified: Wed, 24 Apr 2024 17:10:14 GMT  
		Size: 20.1 MB (20064275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a013e8397474ca02386b15a3f4275dd3bafea255c7d4a0473efdade3a7a35305`  
		Last Modified: Wed, 24 Apr 2024 17:10:01 GMT  
		Size: 440.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c13a0066263138d3939a9dbee014c328c5cff619f5a5e211581815e00aac8ae`  
		Last Modified: Wed, 24 Apr 2024 17:10:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46daba8c58c48abd846e81e6b2f6fe8d7968a64608a60263767b3497d2c4e7b`  
		Last Modified: Sat, 11 May 2024 01:30:18 GMT  
		Size: 12.2 MB (12220793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3a4b0697036d9ae5ab4e8cbc1f24f8be12287444f30dea7ab94bd77d028f23`  
		Last Modified: Sat, 11 May 2024 01:30:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712502d32d01645c885f724d11f2d5f8ef9606f9cd49185953c76125ed88907d`  
		Last Modified: Sat, 11 May 2024 01:30:21 GMT  
		Size: 10.5 MB (10486399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce80a1b7a679379833dc3a3037b77e0ae0da2b8be0b864d1d21fbb210bb78c41`  
		Last Modified: Sat, 11 May 2024 01:30:14 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6614bf6ad45d48475ea14cce5fd7b8b3aa483e48e3dc93f3dfb8bf3689520575`  
		Last Modified: Sat, 11 May 2024 01:30:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1156c254363074426c88b4bfb3a014cc4deb2f290688f2e1cc888f2574d5b5bd`  
		Last Modified: Sat, 11 May 2024 01:30:13 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588c04fc34e9667e4beaecb7570ea3599b255ba6516c6100f083875c76656751`  
		Last Modified: Sat, 11 May 2024 02:52:09 GMT  
		Size: 26.0 MB (26024125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6888b40a9c39e3d2068b3401c828f1b9ddbf975f676620e335ac6f0b6a1b62`  
		Last Modified: Sat, 11 May 2024 02:52:14 GMT  
		Size: 29.1 MB (29101523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e62993e749f4a258a6b3fb75f0dbdd66b3ebb120e6f703f774697575b50acd6`  
		Last Modified: Sat, 11 May 2024 02:51:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a864c7cbf48a568047ee6f5836e2b6f15724e76e122032a4452ab9b5481482`  
		Last Modified: Sat, 11 May 2024 02:51:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04860640cb05f3bb1cfd538c92c4151bf548bd9e3592a34a1c99efdb8a9d76df`  
		Last Modified: Sat, 11 May 2024 02:51:48 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e692379ea43b27042a4e7aab45df5a1ea9266ab0493213fed145e4c4942f28a4`  
		Last Modified: Sat, 11 May 2024 02:52:09 GMT  
		Size: 25.6 MB (25644920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b3903393c920c4f3fea70fb20086af3237f6bd8bb20784d89da494a7f461ff`  
		Last Modified: Sat, 11 May 2024 02:51:48 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d801ba40ae9e12d2c8678e9e8dad3207d9935ced22313adb0e4f3cc9db88e64`  
		Last Modified: Sat, 11 May 2024 02:51:49 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:63af8b21e3882a3cd6577c8327c5e09565fb74a65ba1048592ed503fa1dee90f
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267367715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9949709453082832f4fc79c722ead315aa0b6b215904a2af58833f84ce4c263`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 04:50:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 04:50:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 04:51:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 04:51:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 04:51:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 04:54:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 04:54:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 04:54:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 04:54:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 04:54:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 04:54:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 04:54:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 04:55:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 05:20:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 05:20:41 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 05:20:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 05:20:41 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 05:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 05:20:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 05:23:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 05:23:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 05:23:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 05:23:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 05:23:51 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 05:23:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 05:23:51 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 05:23:51 GMT
EXPOSE 80
# Tue, 14 May 2024 05:23:52 GMT
CMD ["apache2-foreground"]
# Tue, 14 May 2024 07:43:31 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 May 2024 07:43:31 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 May 2024 08:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 08:05:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 14 May 2024 08:05:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 14 May 2024 08:05:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 14 May 2024 08:05:20 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 14 May 2024 08:05:20 GMT
VOLUME [/var/www/html]
# Tue, 14 May 2024 08:05:20 GMT
ENV JOOMLA_VERSION=4.4.4
# Tue, 14 May 2024 08:05:21 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Tue, 14 May 2024 08:05:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 May 2024 08:05:32 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Tue, 14 May 2024 08:05:32 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 14 May 2024 08:05:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 08:05:32 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4562afaefe716a9177f3e8e143cb862a9bfd4980c33e8d63c6ee05392159f033`  
		Last Modified: Tue, 14 May 2024 06:06:44 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a34f2dfc8cfd4efefed6a22fdb6ea01ce29b2e88757603c3b87ec2670e08ee`  
		Last Modified: Tue, 14 May 2024 06:07:01 GMT  
		Size: 103.3 MB (103316796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f1895c9ef9f2875807d908e684ad9f88e7c676216f458fa417575822393e77`  
		Last Modified: Tue, 14 May 2024 06:06:45 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f971db6de5e64bf822ec5e73c39ac673c5d74f08aa9df057f97ff7372bc3346`  
		Last Modified: Tue, 14 May 2024 06:07:48 GMT  
		Size: 21.5 MB (21512862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae5f533e6fe915ffc514abafd184fbce626f3fd778cab04a40a1c2ddfe9b1ff`  
		Last Modified: Tue, 14 May 2024 06:07:45 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1748b46a6be93add11b123b2cdd6f88564c577026e664ba3d1cc389cd0ccfe`  
		Last Modified: Tue, 14 May 2024 06:07:45 GMT  
		Size: 516.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c7e3103de9aafb35be3a4c02be7f77ad077abf773f7e8afe17ad6043039ea2`  
		Last Modified: Tue, 14 May 2024 06:11:32 GMT  
		Size: 12.4 MB (12428087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0963c1dd5181b2e6216ab4a7655f3db050b7229cb4b63a03fb5dcf3ab926bcd`  
		Last Modified: Tue, 14 May 2024 06:11:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20535f1665a99a3c7eec9aa31955edae0af9648cdfbf290ba6ebe257bb5e6820`  
		Last Modified: Tue, 14 May 2024 06:11:31 GMT  
		Size: 11.8 MB (11819876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812f1b4a7dcda22e6bfda4b09c0479ad4e2ef250fb27f973f335172161b3c37b`  
		Last Modified: Tue, 14 May 2024 06:11:29 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dd48b6a1fbae269589bd7d1a896c95c941d2b43526360a2c106f8d26949fb0`  
		Last Modified: Tue, 14 May 2024 06:11:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abd0ac3a76545961cff9fe1882586bebf12ba993fc9a91900cc0ace18fcff25`  
		Last Modified: Tue, 14 May 2024 06:11:29 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ee6e8ccb3b5fd40e24b6bdb53ed43dfdfed68fcb29fb278514f2976031dbeb`  
		Last Modified: Tue, 14 May 2024 08:14:21 GMT  
		Size: 27.3 MB (27347766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd7c01183f1eba7b997813adac09d83650c96b0738afe8462b4c16873084bb2`  
		Last Modified: Tue, 14 May 2024 08:14:23 GMT  
		Size: 32.1 MB (32127785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fafe5d45e8aac2a88ee16c891543531d39b016a1f23bf09b1ceacba7f84954`  
		Last Modified: Tue, 14 May 2024 08:14:17 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772c93a282c93747aa7aaafd33a1237be126f8f4492bf0a5eb5924abd485b048`  
		Last Modified: Tue, 14 May 2024 08:14:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b76378f0422bce324a2470dccd39f4d3d4f9975f5a9a9acd7bf7da7e161309`  
		Last Modified: Tue, 14 May 2024 08:14:15 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042c8a4ed68ef01be5313b83cc475992950babff8d1e1caa1cc091b362c6ce6d`  
		Last Modified: Tue, 14 May 2024 08:14:20 GMT  
		Size: 25.6 MB (25644113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e2699b7263ca2323106f11c9b506be00ac80a32d9d537af4551bef6d4ce3b0`  
		Last Modified: Tue, 14 May 2024 08:14:15 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e737939fb1d09516eb3a0d1c42fa64867a7d44250ef797737e715920e560b2`  
		Last Modified: Tue, 14 May 2024 08:14:15 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:4-php8.2-apache` - linux; s390x

```console
$ docker pull joomla@sha256:6ecd6a2cdb741f336df65a472138d8dc82930bf7fab4b2d97836b48293973594
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231587183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3dd7b78ce573b7fb70c13d862c916a825683b41b7316b66d2943fad8efbcbe5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:33:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 01:33:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 01:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:33:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 01:33:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 01:36:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 01:36:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 01:36:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 01:36:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 01:36:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 01:36:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 01:36:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 01:36:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 01:59:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 01:59:18 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 01:59:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 01:59:18 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 01:59:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 01:59:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 02:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 02:01:52 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 02:01:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 02:01:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 02:01:53 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 02:01:53 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 02:01:53 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 02:01:53 GMT
EXPOSE 80
# Tue, 14 May 2024 02:01:53 GMT
CMD ["apache2-foreground"]
# Tue, 14 May 2024 07:52:30 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 May 2024 07:52:30 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 May 2024 08:02:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 08:04:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 14 May 2024 08:04:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 14 May 2024 08:04:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 14 May 2024 08:04:50 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 14 May 2024 08:04:50 GMT
VOLUME [/var/www/html]
# Tue, 14 May 2024 08:04:50 GMT
ENV JOOMLA_VERSION=4.4.4
# Tue, 14 May 2024 08:04:50 GMT
ENV JOOMLA_SHA512=782469e12a7e6ceb719e4fca5e839d1bd5e475b2b3a932a4262ecc51b2585e94dede017021b5075b2e36c2687b27a82350064b5cc74fb27761987cff55e8637f
# Tue, 14 May 2024 08:04:57 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.4/Joomla_4.4.4-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 14 May 2024 08:05:00 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Tue, 14 May 2024 08:05:00 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 14 May 2024 08:05:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 08:05:00 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76efe86e8656e714cf7aa1ba3a2e2da46d90970675eed1ac596d54341adef5fe`  
		Last Modified: Tue, 14 May 2024 02:40:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a302ff990e37602ffd001b5a58dd5fc8be32487aa37574380ee44c70387806f3`  
		Last Modified: Tue, 14 May 2024 02:41:02 GMT  
		Size: 80.8 MB (80813948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c59d05ef45c3b48efd12d56e4527110f6e50545c6dcd42a5376465a707080f`  
		Last Modified: Tue, 14 May 2024 02:40:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c784d095f4f30a10bc3c9cfe481a1224ebfdff0c616463ac2eff0c9d885d6f86`  
		Last Modified: Tue, 14 May 2024 02:41:33 GMT  
		Size: 20.1 MB (20103079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b50dbad61f09c3f73bf7969170063d97e466b1a12ae2ba7b43b6a1d27f63d1`  
		Last Modified: Tue, 14 May 2024 02:41:30 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b6cb9b940c0b50bb4e883c620c63521411fa8a580f8d65cb0b494da50a9013`  
		Last Modified: Tue, 14 May 2024 02:41:29 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c90a360939d698baf4e1dba6022d55d386f2ffb6087ff5689fe62dac0c460e`  
		Last Modified: Tue, 14 May 2024 02:44:26 GMT  
		Size: 12.4 MB (12427019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e98de2f19b654e4691c4cec1ab78e57176aeac3f7dcaca20f174118bc3f8074`  
		Last Modified: Tue, 14 May 2024 02:44:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f157edde0b3de22108235997578adb544070502c9d1853303057930b2390abd`  
		Last Modified: Tue, 14 May 2024 02:44:26 GMT  
		Size: 10.5 MB (10452799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a4112208e1829776a8c512dc05859cafa0e01d29e01d2748c09c6bd4f1332b`  
		Last Modified: Tue, 14 May 2024 02:44:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d3e13c3d0860126b08e265bf4cbaf46bafccfd05688049f28fcc7d5cd47a6c`  
		Last Modified: Tue, 14 May 2024 02:44:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aacad7a0cade283d0c933422b1de7bbcc197532a54e5e1b6404c74ecfe888d`  
		Last Modified: Tue, 14 May 2024 02:44:24 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf18e53c94a16b7129efd91ec80c9ee14a45b89a8d22f495ee4e6418df144fc`  
		Last Modified: Tue, 14 May 2024 08:10:46 GMT  
		Size: 25.9 MB (25899613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0220b51d9779e882ae70b21145e64ad57d067162e98f70f917ac4af9a527b3e4`  
		Last Modified: Tue, 14 May 2024 08:10:46 GMT  
		Size: 28.7 MB (28704963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3488a96bdd02ba91bf698a4af37df364c427fc4899f131ddf4214850a333622`  
		Last Modified: Tue, 14 May 2024 08:10:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e235bf85ed912ccce856b2aa866ea46340f41793bdeefb9109b26d8bb6e557`  
		Last Modified: Tue, 14 May 2024 08:10:41 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326a089822deb8644b9dc0a7810a96ab2d1dfb60cc5571af0d10351b31c4ab12`  
		Last Modified: Tue, 14 May 2024 08:10:41 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b5468b8a6571e5be8151da4ef3752ee581e1bad4eddca9e0938f85914f61e4`  
		Last Modified: Tue, 14 May 2024 08:10:45 GMT  
		Size: 25.6 MB (25644100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ffb84762799357612beedc51bcfc11f034df65d093ba865243f987abf94dca`  
		Last Modified: Tue, 14 May 2024 08:10:41 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1719545e0126aa5e40ff9ec17460ae09fe4261f17a9ebecfd840f4d9c27763`  
		Last Modified: Tue, 14 May 2024 08:10:41 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
