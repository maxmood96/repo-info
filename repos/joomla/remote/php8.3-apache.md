## `joomla:php8.3-apache`

```console
$ docker pull joomla@sha256:a43239e5d04d7044dad484283c0e5a906fcbaef41a75b22f8e3f4d57aabc93d7
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

### `joomla:php8.3-apache` - linux; amd64

```console
$ docker pull joomla@sha256:aa9a3703c7fa5a4b47e48a82a9cc5bea06a2f0d4ae1376074922926fb861065e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260694879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a379af236dae7e4cdb87c50e2326674872d00fbf073af41ee107663e7f0cc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:55:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 01:55:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 01:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:56:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 01:56:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 02:00:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 02:00:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 02:00:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 02:00:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 02:00:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 02:00:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 02:00:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 02:00:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 02:00:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Jun 2024 02:00:25 GMT
ENV PHP_VERSION=8.3.8
# Thu, 13 Jun 2024 02:00:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 13 Jun 2024 02:00:25 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 13 Jun 2024 02:00:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 02:00:36 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:04:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 02:04:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:04:20 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 02:04:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 02:04:20 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 02:04:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:04:20 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 02:04:20 GMT
EXPOSE 80
# Thu, 13 Jun 2024 02:04:21 GMT
CMD ["apache2-foreground"]
# Thu, 13 Jun 2024 09:45:56 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 13 Jun 2024 09:45:56 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 13 Jun 2024 09:46:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 09:48:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 13 Jun 2024 09:48:41 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 13 Jun 2024 09:48:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 13 Jun 2024 09:48:42 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 13 Jun 2024 09:48:43 GMT
VOLUME [/var/www/html]
# Thu, 13 Jun 2024 09:48:43 GMT
ENV JOOMLA_VERSION=5.1.1
# Thu, 13 Jun 2024 09:48:43 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Thu, 13 Jun 2024 09:48:47 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 14 Jun 2024 20:34:34 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 14 Jun 2024 20:34:34 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Fri, 14 Jun 2024 20:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Jun 2024 20:34:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c187ab622ce6623bfc28e291735e4d79466116c66b38ea155d2e56e503980c`  
		Last Modified: Thu, 13 Jun 2024 03:29:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4382a8829fff65dc205865ad03b19117fdcea939ac1f8d5ab37309ad641e4c3d`  
		Last Modified: Thu, 13 Jun 2024 03:29:37 GMT  
		Size: 104.4 MB (104357495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43046b340e345aef56c4f6f9a15ed3640207000305855ed512de8f87b1ac602b`  
		Last Modified: Thu, 13 Jun 2024 03:29:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199ce03f09e669bb973f45a400011e83c67287af6af8dd48aeaefb315757fc4a`  
		Last Modified: Thu, 13 Jun 2024 03:30:19 GMT  
		Size: 20.3 MB (20329570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f77a5a3aeda716a8cd4d1929a8fa2f60b6f2eaa5d2c8d26323ee46c8440525`  
		Last Modified: Thu, 13 Jun 2024 03:30:16 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60517e1132d4cc458c2c216ef3855fd33cca2d86202108874776e6220b7e7e06`  
		Last Modified: Thu, 13 Jun 2024 03:30:16 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5d0afba05b8048d89a7a67f4be59b395844201271fdc6c80419b78d4b04206`  
		Last Modified: Thu, 13 Jun 2024 03:30:17 GMT  
		Size: 12.8 MB (12815820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dd271e18d65f84c7df2b1096d538e79577f54d18d40ef40f2d231765bee046`  
		Last Modified: Thu, 13 Jun 2024 03:30:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e00a793d3c47fc3b6ad774e7564bbca488f0a62c7edb6efab3d07fb155b9a3`  
		Last Modified: Thu, 13 Jun 2024 03:30:16 GMT  
		Size: 11.6 MB (11640613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81fc1b7e3b9c59204262f30d3191d4c9d71ace1c74dfefd08af1e3a7036420`  
		Last Modified: Thu, 13 Jun 2024 03:30:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f84ad6a3718b6a89a7eaec74a8589c2a9fe1337530f972740266b1008535c1`  
		Last Modified: Thu, 13 Jun 2024 03:30:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf5601c77e2fe2034b988bc568f94f72ceb6a563bda43f43a510583e416a852`  
		Last Modified: Thu, 13 Jun 2024 03:30:14 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b749080acb78c5268e96d27e3ada232059d69af5cd3f000257fc8be870a5f273`  
		Last Modified: Thu, 13 Jun 2024 10:06:35 GMT  
		Size: 27.2 MB (27166379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8999259ddc74278f33109e97ba5f38aff79023545910c4537535b7b9786bde8c`  
		Last Modified: Thu, 13 Jun 2024 10:06:36 GMT  
		Size: 31.5 MB (31488861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0d074a59768832bdbeb87009a9e43498d4e20c322898ee2de4ab9ef1047a0e`  
		Last Modified: Thu, 13 Jun 2024 10:06:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4db92a96e5eaa657acace19b872939fd3bebf8453c984b1d3d2f67b2c819580`  
		Last Modified: Thu, 13 Jun 2024 10:06:29 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bc062cd310d162b3e38932015d64b41053bb9eb9d3389d351c0e03badd1276`  
		Last Modified: Thu, 13 Jun 2024 10:06:29 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd024d6a223afce714c02e1ed8541543412b3ebe10608af2dfed95217ff1c2e`  
		Last Modified: Thu, 13 Jun 2024 10:06:33 GMT  
		Size: 23.7 MB (23715619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41150f988d5b5a788e0f4e86d0c3a29a15ef145972d1be1bbe4072c912b2c1ac`  
		Last Modified: Fri, 14 Jun 2024 20:37:37 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f35994351d8810e7baec1bb55fd41ad21bdfd8c56b19e95a5b083c081437ef3`  
		Last Modified: Fri, 14 Jun 2024 20:37:37 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:c0c608a63224e13b4161922e34dab8b7a7cfa3194b924e8b6c57e9b3b4f73af4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230485085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c0b76819d311288da0032cc67535195bb736647a556939f6707476c2f7bed1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:27 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Tue, 02 Jul 2024 00:48:27 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:27:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:27:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:27:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:27:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:30:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:30:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:30:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:30:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:30:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:30:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:30:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:30:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 01:55:52 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 01:55:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 01:55:53 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 01:56:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 01:56:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 01:59:29 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:59:30 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 01:59:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 01:59:30 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 01:59:30 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:59:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:59:31 GMT
EXPOSE 80
# Tue, 02 Jul 2024 01:59:31 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jul 2024 05:28:46 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 02 Jul 2024 05:28:46 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 02 Jul 2024 05:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:31:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 02 Jul 2024 05:31:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 02 Jul 2024 05:31:41 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 02 Jul 2024 05:31:41 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 02 Jul 2024 05:31:41 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 05:31:41 GMT
ENV JOOMLA_VERSION=5.1.1
# Tue, 02 Jul 2024 05:31:42 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Tue, 02 Jul 2024 05:31:46 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 02 Jul 2024 05:31:47 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Tue, 02 Jul 2024 05:31:47 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 02 Jul 2024 05:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 05:31:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fa7b963844d7a531cf61bfa69bbb8429c9b28bbc6fa8908e9ac1418cef4458`  
		Last Modified: Tue, 02 Jul 2024 03:41:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6337430e42acedb06f4a615a62ef8175ddb93248b8558778019f70a0977bb9`  
		Last Modified: Tue, 02 Jul 2024 03:41:20 GMT  
		Size: 82.0 MB (81997556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52929959fae16599e8f6edc0be4d23c98f1b9c9bc53e232dd6b029a1f0c2421`  
		Last Modified: Tue, 02 Jul 2024 03:41:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab47bc327c2f621a15e696a06a22e7954434b1eba7a6917a220d76b315aa652`  
		Last Modified: Tue, 02 Jul 2024 03:41:45 GMT  
		Size: 19.6 MB (19620495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff5cd1bf38c523b7094f7e3b241caa94d68265f5645e113fef2d23af5f9a74c`  
		Last Modified: Tue, 02 Jul 2024 03:41:41 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0699d1b86522ccca00a70a4cf12296e520df5cd2cc365da7e6cc2a5e55197e`  
		Last Modified: Tue, 02 Jul 2024 03:41:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291f51f4622ca13c6ea25bda53c05ceeaf5ae1b91f1e103a21ce486b43158ffe`  
		Last Modified: Tue, 02 Jul 2024 03:44:28 GMT  
		Size: 12.8 MB (12812173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b29021fea0811c8ecf67cef1eed9e56619d1797cc1164f3e3e57f39e3a1ff8`  
		Last Modified: Tue, 02 Jul 2024 03:44:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ddac81bb09cd2e70f9c84a19ffc1ba3bd6324fd11e0bc10d5082babc5631c`  
		Last Modified: Tue, 02 Jul 2024 03:44:28 GMT  
		Size: 10.6 MB (10606256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279d36140ca64c2e4ad010e8c0d84837329e1c78177f1c762661bdf6fe620aa`  
		Last Modified: Tue, 02 Jul 2024 03:44:25 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b309e43265a4d0af50d0966efa74531d9944c51f388028d0918e226f51956d7e`  
		Last Modified: Tue, 02 Jul 2024 03:44:25 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c5c97d1c40991a790a1614c08febfd4cac3c76dd1629f8bf82cbd8de54ab94`  
		Last Modified: Tue, 02 Jul 2024 03:44:25 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1944eeed1ece9ae4cda38e52232aa161548f962c25172ecf3186dd0fe69096`  
		Last Modified: Tue, 02 Jul 2024 05:50:11 GMT  
		Size: 26.6 MB (26614467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2172c38ca0ccf31cf9931f6593d21a6398ad3b9aae3775c7f63c0f809f1ab775`  
		Last Modified: Tue, 02 Jul 2024 05:50:11 GMT  
		Size: 28.2 MB (28201156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a4ed08570d55765dc021ff70000a00f075fd536e1331092c09952656072e0e`  
		Last Modified: Tue, 02 Jul 2024 05:50:06 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e10c1bbe12266064ad5a99e336ec326b06a48d172e015a0da4efcdc06fb164`  
		Last Modified: Tue, 02 Jul 2024 05:50:04 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfb3082e402c30f595d5c4728279603d4c2c1c62ba820a076307c9d337ac840`  
		Last Modified: Tue, 02 Jul 2024 05:50:04 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540034bc38b9c1b77428570b9170f87074d2756ba3d712d34c9fd4f83aecd865`  
		Last Modified: Tue, 02 Jul 2024 05:50:09 GMT  
		Size: 23.7 MB (23715623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c00f4f68d569eca83921c80b65d7bf3bf31dfe74c7780864181d875d0420d90`  
		Last Modified: Tue, 02 Jul 2024 05:50:04 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc718f29fca866c40056e9095074fe8f993a082f22544592c07217853f295e9f`  
		Last Modified: Tue, 02 Jul 2024 05:50:04 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:39ee62b25c6cfa5f9a6e160a81985e583d90c4ad2348bff6ba95aec043802dc0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218980053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfc45ae623aee52e273729005821fa780c45ea5d21559af7f1babbdfbac32b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:47:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:47:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:51:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:51:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:51:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:51:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:51:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:51:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:51:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:51:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:17:25 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:17:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:17:26 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:17:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:17:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:20:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:20:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:20:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:20:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:20:23 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 02:20:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:20:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 02:20:23 GMT
EXPOSE 80
# Tue, 02 Jul 2024 02:20:23 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jul 2024 06:09:07 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 02 Jul 2024 06:09:07 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 02 Jul 2024 06:09:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:12:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 02 Jul 2024 06:12:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 02 Jul 2024 06:12:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 02 Jul 2024 06:12:12 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 02 Jul 2024 06:12:12 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 06:12:12 GMT
ENV JOOMLA_VERSION=5.1.1
# Tue, 02 Jul 2024 06:12:12 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Tue, 02 Jul 2024 06:12:17 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 02 Jul 2024 06:12:18 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Tue, 02 Jul 2024 06:12:18 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 02 Jul 2024 06:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 06:12:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98f2ea35903ab22a64a0b9429586e5ebf253d8f30160f658c9a3e91506b6b4f`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed99c1553b06b60dc38f501a723427469be3c7f305f660c2d3f5c4826636db6`  
		Last Modified: Tue, 02 Jul 2024 03:57:17 GMT  
		Size: 76.2 MB (76166316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ff1c809dc06de95648d78a0490826dc9afc53a05c01d001be86b39ec6903ec`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751f0125442586c37682f7ec34b710b4ab71ddc530c91fea2cf2af4901d2a1a4`  
		Last Modified: Tue, 02 Jul 2024 03:57:42 GMT  
		Size: 19.1 MB (19057874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016198828fa6032df9c10ec2e792db92c6a8b19d35a884387328ccb4cb68f19d`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b6f3e158190277e0f0f214b0dc62c26057875ebd2af19ac0a15534c73fb171`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f32c3cff2a03027048be884bf66786a52a1a6839e373f5d73eb7e67831bceb`  
		Last Modified: Tue, 02 Jul 2024 04:00:28 GMT  
		Size: 12.8 MB (12812086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1584640ffafbde934a7679551b3702cb84d574de31b261a9542d1f9087406f0`  
		Last Modified: Tue, 02 Jul 2024 04:00:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aead8cff0b4a3c8e600dbd12cdacda6ca1fc6355041ae52eeba9cc4d049d424`  
		Last Modified: Tue, 02 Jul 2024 04:00:28 GMT  
		Size: 10.0 MB (10030643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c819aeab246273128570ad8c480c16215828983d034be32ad0efe1dea542c7e2`  
		Last Modified: Tue, 02 Jul 2024 04:00:25 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e699bb8eebaf2c15b1a2809f436e32f2c5d9e2cc037008374a22c1a226dda4`  
		Last Modified: Tue, 02 Jul 2024 04:00:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b6db48584730dbff8a84fa0d768891c247d38058c34b8e61c3b5fd7d2147c2`  
		Last Modified: Tue, 02 Jul 2024 04:00:25 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eee6d915102cafa0e4c0eb137d869dc2c4573614de974df4b0d9766448a21d4`  
		Last Modified: Tue, 02 Jul 2024 06:30:59 GMT  
		Size: 25.9 MB (25850411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b46ee86d39f648912ad4b8e1143089147073008f2b73aec26f9464c05e1b5`  
		Last Modified: Tue, 02 Jul 2024 06:30:59 GMT  
		Size: 26.6 MB (26598845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776a7f2c06a7e70175aab8779048945e8b3ea2cfd2f3cf3d834c9298cb57bffc`  
		Last Modified: Tue, 02 Jul 2024 06:30:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e41b08cbf63819cbdfc550fe2ce98208f5bca3b87a6cb4cadff6a0fdfd4547b`  
		Last Modified: Tue, 02 Jul 2024 06:30:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd9166234789988b0f6676be1edd025fd4f8789c4ea3f82d7a4103bc68e28b5`  
		Last Modified: Tue, 02 Jul 2024 06:30:52 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6832d46a1087e4c9f8956ed8396cc404fa633e06399eda91b57ff2b463a0c8`  
		Last Modified: Tue, 02 Jul 2024 06:31:01 GMT  
		Size: 23.7 MB (23715617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cd2310aa196ea890e3e64d7b346466aaf606b2447597e35e14cd273955bb3c`  
		Last Modified: Tue, 02 Jul 2024 06:30:52 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce9269325aae7167afeef47bc215ecf230a5a13feb218229c9fdda51831eff8`  
		Last Modified: Tue, 02 Jul 2024 06:30:52 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:9e8561340fd9085613a118badebd96a1026515e3cfd11efa6d0e8e28565954ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61907f93abcb657358040582585179d3f3f4f32f80e030ac2f80da98c34e7406`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:18:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:18:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:18:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:22:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:22:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:22:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:22:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:22:39 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 01:51:30 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 01:51:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 01:51:30 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 01:51:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 01:51:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:55:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 01:55:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:55:11 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 01:55:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 01:55:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 01:55:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:55:11 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:55:11 GMT
EXPOSE 80
# Tue, 02 Jul 2024 01:55:12 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jul 2024 06:57:41 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 02 Jul 2024 06:57:41 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 02 Jul 2024 06:57:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 07:00:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 02 Jul 2024 07:00:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 02 Jul 2024 07:00:09 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 02 Jul 2024 07:00:09 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 02 Jul 2024 07:00:09 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 07:00:10 GMT
ENV JOOMLA_VERSION=5.1.1
# Tue, 02 Jul 2024 07:00:10 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Tue, 02 Jul 2024 07:00:13 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 02 Jul 2024 07:00:14 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Tue, 02 Jul 2024 07:00:14 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 02 Jul 2024 07:00:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 07:00:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d168c82669385a88cb2d49927f5d97a9fd361459c5ba221ade1b4833b14530`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be59d5943ae49be3e4ff309c07ef79eacf2bf161b53590db30e1227422f98601`  
		Last Modified: Tue, 02 Jul 2024 03:36:42 GMT  
		Size: 98.1 MB (98131121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702846940aedcd56970bc052b4e64fa8ff21b12b0a6ba8ca8273f4e256aaedc2`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8911daeb05e620d4f86e6e1800ae61553a08eaf29667c22d5a6bdae9461cada3`  
		Last Modified: Tue, 02 Jul 2024 03:37:07 GMT  
		Size: 20.3 MB (20321495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4028ee2076616a6cf681ab5e49658e589a2d0b1918e9213d61a41938d6b4299b`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 438.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4d03e54d8a1108c589658f102c0afa22f96cd422f05ace79e1ae3b68741d06`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fd0cbd6509a2d306d2ec4d8e0e7aae2ce92cb9c9a8fb9f27bc087c8c5985d2`  
		Last Modified: Tue, 02 Jul 2024 03:39:35 GMT  
		Size: 12.8 MB (12813781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3566e1cffe5fccc92789df865101993fa2f64b2c89f67e6e5ad97aac357ea028`  
		Last Modified: Tue, 02 Jul 2024 03:39:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a78ea83b294c43f176881b04d1cab12890b9cbc3eb4d3ce8f7897b54740a702`  
		Last Modified: Tue, 02 Jul 2024 03:39:35 GMT  
		Size: 11.6 MB (11633874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c171382a6056783256c3b72893af5befa26f40ed0599fc1f9a4380c56610363`  
		Last Modified: Tue, 02 Jul 2024 03:39:33 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798e1bd3b79d54fd633874b4272931288d506c3e8a33d8db24b9b696298acb42`  
		Last Modified: Tue, 02 Jul 2024 03:39:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d703d02c1edb86b69ea7181a34036a1cf1da4328b9d163b128b8c02416e657c5`  
		Last Modified: Tue, 02 Jul 2024 03:39:33 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c869a32c65925a304b1da690c564740198e1156745ed9eb7bc42ccc3bde7b074`  
		Last Modified: Tue, 02 Jul 2024 07:15:40 GMT  
		Size: 27.0 MB (26996989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a561637b9523c1c1c4bc9a0f47ea18b726d81b7957c558a3c7769cb2e5af51c`  
		Last Modified: Tue, 02 Jul 2024 07:15:40 GMT  
		Size: 29.1 MB (29088438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc763bc8df900bb4299668fe6b72d79405ed655adb3511e3d6791eeb95d924d`  
		Last Modified: Tue, 02 Jul 2024 07:15:37 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66785be72f6d1cce31dc3868d74a6ea0673511621e26dbeaefcf8e91fe497024`  
		Last Modified: Tue, 02 Jul 2024 07:15:35 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ca2650a94bfa5b83d9ccac98b1542e082dbb34289adbc6effd94f2da2dc5ca`  
		Last Modified: Tue, 02 Jul 2024 07:15:35 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe1a4d210f8dee056bb72147bc6de0aecdc2c1a194c1b122d2141dbadf1c9fd`  
		Last Modified: Tue, 02 Jul 2024 07:15:38 GMT  
		Size: 23.7 MB (23715631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cf91bdb77aa9e2ec5f6faef8f70bcfe175033804ebf7022d98ad3a06bd0ed5`  
		Last Modified: Tue, 02 Jul 2024 07:15:35 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151e5d561f4514aac58f2084565b31c2519c0056ff5007f0c009a050ef6e784a`  
		Last Modified: Tue, 02 Jul 2024 07:15:35 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; 386

```console
$ docker pull joomla@sha256:7367ec1311c657dc9f65fc46bb0ff90c20b63979c624b8e83ccb5827d89fe0c6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259244805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8011a56771fdd0affa102e12f8bc162d0d0037e229139117e6cc2f385a85c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:42:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:42:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:42:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:42:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:49:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:49:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:49:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:49:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:49:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:49:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:49:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:49:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:49:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:36:52 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:36:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:36:52 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:37:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:37:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:43:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:43:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:43:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:43:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:43:12 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 02:43:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:43:12 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 02:43:12 GMT
EXPOSE 80
# Tue, 02 Jul 2024 02:43:13 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jul 2024 06:34:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 02 Jul 2024 06:34:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 02 Jul 2024 06:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 06:37:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 02 Jul 2024 06:37:32 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 02 Jul 2024 06:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 02 Jul 2024 06:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 02 Jul 2024 06:37:34 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 06:37:34 GMT
ENV JOOMLA_VERSION=5.1.1
# Tue, 02 Jul 2024 06:37:34 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Tue, 02 Jul 2024 06:37:39 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 02 Jul 2024 06:37:40 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Tue, 02 Jul 2024 06:37:40 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 02 Jul 2024 06:37:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 06:37:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6daa048202ff5a552b6eacd27b84297ac780821f0730574f9bb61ed3a6996e20`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d876e28acd3b5f3038bdfb0fb8fe720824179dc347e25e6d745ae512376fa6`  
		Last Modified: Tue, 02 Jul 2024 05:39:40 GMT  
		Size: 101.5 MB (101516977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe24ff1fc83352bac36eafb7daa5d32e7ea2232fe6fef612107fdbd1f81e7c8`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087987d024f8b2145282ca5bfbb784c34ed054bbc454fc96a25334882be4e1fe`  
		Last Modified: Tue, 02 Jul 2024 05:40:06 GMT  
		Size: 20.8 MB (20843476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8723ec10434fcdc00676902f705fe56081a8fb0a774cb1a3a00894a4be83d8bf`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 436.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f856f33b11561e423f77df5f979a60b6dd4042c3f53df3d21647a29b671248`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b85e93cf20edc3a74338b3e76862967ce00db8edc95b80b225532ff96e0a81`  
		Last Modified: Tue, 02 Jul 2024 05:43:01 GMT  
		Size: 12.8 MB (12813175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563f24447dbb940aed06e6cbd3925fc83469da6fe26a8a5278139e07a43619c5`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa92b71a357d6cb4cd2b2ff75daf50f105c5b4862295d8f23059b0889279c68`  
		Last Modified: Tue, 02 Jul 2024 05:43:01 GMT  
		Size: 11.9 MB (11862314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7237f03a3d2814de9df424c01e8bb410509d39ade80450711ccd7517e8987745`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d7609802db7bd708d6cc8af552d1cdbff6c9f77315a1c1f21f85fce58be838`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c666f6279f00f518eaa5fcd4cfd3f5cdfbbdb17dd10fd1bd12018cc756e135a2`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1021d7ef588bbc98bfaaf00f7cecfc22f0e8c8d70d8792fdc0543720e2fa9f4`  
		Last Modified: Tue, 02 Jul 2024 06:57:40 GMT  
		Size: 27.5 MB (27526018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a663c4ff71c060f5012d7356a3a0abd0e54e20d98280b43554753863aa1438`  
		Last Modified: Tue, 02 Jul 2024 06:57:41 GMT  
		Size: 30.8 MB (30792879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fe5d9acd5c9f59838e0512754467088d55b6e8a2f5a592c9d12eeda8c1e37d`  
		Last Modified: Tue, 02 Jul 2024 06:57:32 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4215846737f27a1a4c04d95cbba4bca73e1c0e528629f4a467839450fb26bf52`  
		Last Modified: Tue, 02 Jul 2024 06:57:30 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69923f99bfd2047fdc70ffa4397812ca34668e07e108510401dd82c29be482b0`  
		Last Modified: Tue, 02 Jul 2024 06:57:30 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b7ad9b89c315a3f151a7f27d4c1e92ce77f953ee6cc8b9ad5723f453fd3e78`  
		Last Modified: Tue, 02 Jul 2024 06:57:38 GMT  
		Size: 23.7 MB (23715622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2f7dd10767acce9ff2f31ec4a49a182dfea2d074a75925a98e8a06ffadd5e4`  
		Last Modified: Tue, 02 Jul 2024 06:57:30 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35135d31fbed679063ee2d7f71ab48ec214d767ac57c0b7763e6309b8858c0a`  
		Last Modified: Tue, 02 Jul 2024 06:57:30 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; mips64le

```console
$ docker pull joomla@sha256:16f90fecc9a20684b84cbcffc64da2f622c6bfe1ddfeade5fd12d4431e335b9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232239466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63a07f9eb9db6e7d9aa538ee241febd8dd15c4bda21297a5db76f7b408facf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Jun 2024 01:10:34 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Thu, 13 Jun 2024 01:10:39 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 04:38:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 13 Jun 2024 04:38:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Jun 2024 04:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 04:40:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Jun 2024 04:40:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 13 Jun 2024 04:56:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Jun 2024 04:57:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Jun 2024 04:57:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 13 Jun 2024 04:58:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 13 Jun 2024 04:58:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 13 Jun 2024 04:58:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 04:58:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Jun 2024 04:58:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Jun 2024 04:58:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 13 Jun 2024 04:58:25 GMT
ENV PHP_VERSION=8.3.8
# Thu, 13 Jun 2024 04:58:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Thu, 13 Jun 2024 04:58:33 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Thu, 13 Jun 2024 04:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 13 Jun 2024 04:59:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 13 Jun 2024 05:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 13 Jun 2024 05:14:58 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 13 Jun 2024 05:15:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 13 Jun 2024 05:15:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Jun 2024 05:15:12 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Jun 2024 05:15:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 13 Jun 2024 05:15:20 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 05:15:23 GMT
EXPOSE 80
# Thu, 13 Jun 2024 05:15:27 GMT
CMD ["apache2-foreground"]
# Thu, 13 Jun 2024 13:08:48 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 13 Jun 2024 13:08:52 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 13 Jun 2024 13:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 13:22:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 13 Jun 2024 13:22:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 13 Jun 2024 13:22:32 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 13 Jun 2024 13:22:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Thu, 13 Jun 2024 13:22:45 GMT
VOLUME [/var/www/html]
# Thu, 13 Jun 2024 13:22:49 GMT
ENV JOOMLA_VERSION=5.1.1
# Thu, 13 Jun 2024 13:22:54 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Thu, 13 Jun 2024 13:23:25 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 14 Jun 2024 19:57:35 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Fri, 14 Jun 2024 19:57:41 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Fri, 14 Jun 2024 19:57:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Jun 2024 19:57:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705f642d228b7653cb0773a864d5251e0be042ebc63ba123f76a2ee96d99f0cd`  
		Last Modified: Thu, 13 Jun 2024 10:55:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7e656a5f67cd261b9639f19da875eb3bfb3f267ee1019dc4147fc3051f3428`  
		Last Modified: Thu, 13 Jun 2024 10:56:37 GMT  
		Size: 80.5 MB (80474931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85627c8d9ca80056d763e9a846c0a5ad6d1f4d99cbfd5394306de302d3126cf4`  
		Last Modified: Thu, 13 Jun 2024 10:55:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eae8ba09be0609884c62ca9dde575c2b43d5477c438e0c31c248995beceb8e2`  
		Last Modified: Thu, 13 Jun 2024 10:57:38 GMT  
		Size: 20.1 MB (20064190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d04f2bb3a32ce8eb7e8d8b20e7a211525218391a48d0a82d77b91c41850b0a8`  
		Last Modified: Thu, 13 Jun 2024 10:57:24 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b0d3a6994847794b9a5124e40369c3b1b12455ac518c8ac05b97e7f687bb71`  
		Last Modified: Thu, 13 Jun 2024 10:57:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec980500db6653d038952d4c05c61d55f09b39b1d258ae18e8667fc8f92bf562`  
		Last Modified: Thu, 13 Jun 2024 10:57:28 GMT  
		Size: 12.6 MB (12606914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67af80399a4a461a0e8e8dd0f1c9c949ae96343ecfbf21442b7d42f2336ca6ca`  
		Last Modified: Thu, 13 Jun 2024 10:57:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8389ff8650153d59a88c96049f00c8d031131167963896c66427099652be054`  
		Last Modified: Thu, 13 Jun 2024 10:57:32 GMT  
		Size: 10.7 MB (10709618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436a720d3519abcbb4585c72ea4588fd8d857bc0816197cc2275ab7ea58a91ef`  
		Last Modified: Thu, 13 Jun 2024 10:57:21 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd1f27be70bce6a23c730b8d92fb29a3d122679429c900c9a4ab04322b704ff`  
		Last Modified: Thu, 13 Jun 2024 10:57:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a060bbe2cf06722fb878202e0c4474a86eb21e2ecbdb10e99ebfdf5b32f0b5`  
		Last Modified: Thu, 13 Jun 2024 10:57:21 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f2ffff2ab6877a851b3841cc3818821ad40c9e364d314e9140012e9e8b58bc`  
		Last Modified: Thu, 13 Jun 2024 14:45:05 GMT  
		Size: 26.9 MB (26921517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffea06dab7d71f9d3530e789c1ded13e7ef54306bd6373ec7caecf821c6ac28a`  
		Last Modified: Thu, 13 Jun 2024 14:45:13 GMT  
		Size: 28.6 MB (28571004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e278e2f3f4ec3ca32a9292c7bad938bd98f994c9d5a2ccd87e48acfbbed1394`  
		Last Modified: Thu, 13 Jun 2024 14:44:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a15d5c4256320eba2bbf1ecd56b2cca8b4ba08e8d22aa7395fe167e629ff8d`  
		Last Modified: Thu, 13 Jun 2024 14:44:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20ad534f6eb71a2e5c16ddb381c13959d0433a29ac2e383fa1370eb8807eb1e`  
		Last Modified: Thu, 13 Jun 2024 14:44:38 GMT  
		Size: 19.2 KB (19180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83e1923d36da22f5fb707db2633fac43bfe58928fa33239ec2ea4fd231af4d`  
		Last Modified: Thu, 13 Jun 2024 14:45:12 GMT  
		Size: 23.7 MB (23717339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1717c4f5af37a1339c0c24b847887542235d9640f13d2a3c20881932abde1696`  
		Last Modified: Fri, 14 Jun 2024 20:03:49 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf17e9026757650d484f398b6cb5d98d9bb0576258b6f64e0cf0d55fcce4eb3`  
		Last Modified: Fri, 14 Jun 2024 20:03:49 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:72003eab750d4a31bc263a1ef61d2f2f805bc1730041fdaf396c4d8d99eae835
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266498476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348be6cf0cecf5dd5c9d0fb0f8e039fd136531c1be1f784c072c12fa9dab2074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:35 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 02 Jul 2024 01:17:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:10:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:11:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:11:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:14:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 02:14:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 02:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 02:14:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 02:14:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 02:14:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:14:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:14:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:14:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 02:40:24 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 02:40:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 02:40:24 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 02:40:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:40:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:43:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:43:34 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:43:35 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:43:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:43:36 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 02:43:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:43:37 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 02:43:37 GMT
EXPOSE 80
# Tue, 02 Jul 2024 02:43:37 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jul 2024 05:41:45 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 02 Jul 2024 05:41:46 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 02 Jul 2024 05:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:45:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 02 Jul 2024 05:45:42 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 02 Jul 2024 05:45:43 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 02 Jul 2024 05:45:45 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 02 Jul 2024 05:45:45 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 05:45:45 GMT
ENV JOOMLA_VERSION=5.1.1
# Tue, 02 Jul 2024 05:45:46 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Tue, 02 Jul 2024 05:45:52 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 02 Jul 2024 05:45:55 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Tue, 02 Jul 2024 05:45:55 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 02 Jul 2024 05:45:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 05:45:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609eb2596342a8a7f536a9dbbffcfccaaadff4bcd99626d15c588274979eaf2a`  
		Last Modified: Tue, 02 Jul 2024 04:14:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b9e2e6a6e6ca971bb68e9cd39a2e7d46e2bacfa5a93def5ea728e84f1553a4`  
		Last Modified: Tue, 02 Jul 2024 04:15:02 GMT  
		Size: 103.3 MB (103317721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8703185de8bbe987d67d7808f74a14a5bcb767eadd604f0096503f998496675`  
		Last Modified: Tue, 02 Jul 2024 04:14:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bfa1030b231350ace419a1b1cb2251a16babac7f828c4850f38366b1a7319a`  
		Last Modified: Tue, 02 Jul 2024 04:15:27 GMT  
		Size: 21.5 MB (21511668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ed004f3d7d188c082021564296cd592b4b41057f3e2a33679c35c3e7bb1a2c`  
		Last Modified: Tue, 02 Jul 2024 04:15:25 GMT  
		Size: 442.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacb72cfc9dd2acb981ca25b9f1f57e62d7bf82694d0a3219b604b104ba52cab`  
		Last Modified: Tue, 02 Jul 2024 04:15:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee019b9c004127f837b9d2c7226e82ce292df62dd64d3519f65887ba0e610832`  
		Last Modified: Tue, 02 Jul 2024 04:18:11 GMT  
		Size: 12.8 MB (12813507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e766d42fda63ef67eed68be47d5f50878afdd1b4e4e880845c906520ea95410`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be12d2bf092f77e4d7fbbc8801fd8d7ed07ec2660abc9c5c2ba4037e37580a7f`  
		Last Modified: Tue, 02 Jul 2024 04:18:10 GMT  
		Size: 12.1 MB (12053279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2560c21f83acf49f4b81440045271ad23b81a4d67d6cc274297d909bc8459f4`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560bba3b36fb7d576c2975e69ceff7c67a7e861bfa9aff093cd913d759d6aa32`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa870c08d564e55bdd62cc1ac5d7bcddbd0cdba2a0ff9324091b67358d77e23f`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9796c632f2e8f8153138f6fb5be320f64e1389d6be1fa897f480a00019253d09`  
		Last Modified: Tue, 02 Jul 2024 06:10:10 GMT  
		Size: 28.3 MB (28323326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50fc065bde39dd479f91f1d9b98595b2e8e1bf30b2ef644beac1e4a1988404d`  
		Last Modified: Tue, 02 Jul 2024 06:10:11 GMT  
		Size: 31.6 MB (31610966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2981637f4db1feea6cfec8bf591163829b2b3db4200c8a5a62bf4f90ef3afc`  
		Last Modified: Tue, 02 Jul 2024 06:10:06 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7649b651273e2ddb31c692793eb2a6dc3c55f7eb9433715f655a1cafa6125`  
		Last Modified: Tue, 02 Jul 2024 06:10:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69a574b9df1fb8f439f4b504185d0a095a1782d9c2134b2ed73c8f10c152c5a`  
		Last Modified: Tue, 02 Jul 2024 06:10:04 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb3283ddf29bb9560590d0826d9404ec2aa82ba52db6b1f7142a85029ae93b0`  
		Last Modified: Tue, 02 Jul 2024 06:10:08 GMT  
		Size: 23.7 MB (23715622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193cdb715b962af7d05412163944b9e4bfe224a1a80343c8917d8707485305d5`  
		Last Modified: Tue, 02 Jul 2024 06:10:04 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85959c288b26999c5dfab38ae3b9fdfc5045c216e22ba89c616c6143ea0d1a07`  
		Last Modified: Tue, 02 Jul 2024 06:10:04 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.3-apache` - linux; s390x

```console
$ docker pull joomla@sha256:37e8d2a7308366b431fcacec6d06d44c57747dead69cf660acd237dd3c81b5c2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230708484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71015a27dcdc6c62c2526abd611d48938066690dd88131b1aaf783fdb9906f4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:14:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:14:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:14:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:14:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:17:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:17:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:17:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:17:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:17:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 01:17:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 02 Jul 2024 01:40:15 GMT
ENV PHP_VERSION=8.3.8
# Tue, 02 Jul 2024 01:40:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Tue, 02 Jul 2024 01:40:15 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Tue, 02 Jul 2024 01:40:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 01:40:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 01:42:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:51 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 01:42:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 01:42:52 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:52 GMT
EXPOSE 80
# Tue, 02 Jul 2024 01:42:52 GMT
CMD ["apache2-foreground"]
# Tue, 02 Jul 2024 04:58:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 02 Jul 2024 04:58:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 02 Jul 2024 04:58:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:00:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 02 Jul 2024 05:00:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 02 Jul 2024 05:00:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 02 Jul 2024 05:00:49 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Tue, 02 Jul 2024 05:00:50 GMT
VOLUME [/var/www/html]
# Tue, 02 Jul 2024 05:00:50 GMT
ENV JOOMLA_VERSION=5.1.1
# Tue, 02 Jul 2024 05:00:50 GMT
ENV JOOMLA_SHA512=e99aa94b5b455eeb3f3ce1fc330c83fda3d1ac1688e269351355692171705a1f7947005f62375345a62166cee46840bd8090b541301768466fc4e603bafa4c7b
# Tue, 02 Jul 2024 05:00:54 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.1.1/Joomla_5.1.1-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 02 Jul 2024 05:00:56 GMT
COPY file:09d039f2ed0d8991a914126098661c6156e603362c75d72887a3d64c1ce9f866 in /entrypoint.sh 
# Tue, 02 Jul 2024 05:00:56 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 02 Jul 2024 05:00:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jul 2024 05:00:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9251ecd224e15bee1af8e5d8ed06b4583727d21c25571b0841308fa40637020`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de732a471a32b9581046aa3735f5891fa36c8dc024c7c7a007087dd77b0bd3a`  
		Last Modified: Tue, 02 Jul 2024 03:05:16 GMT  
		Size: 80.8 MB (80817736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f9b6de1c71adae007cab6934b2b7dfe2155be5d6b7fecfea770f4dca1aa159`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac393ffa46cdbdd309e76835caefc39b9a5f28208a5117719850422e50cd1830`  
		Last Modified: Tue, 02 Jul 2024 03:05:34 GMT  
		Size: 20.1 MB (20101995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b9ac198003d25e1ae488b290fbd759f674d87fea5692596dc85177b0ad0014`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 435.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe10d7b17a1f1937efded756698b3791c41a781a95ad1f5b3436f29993e08d6`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5bbfc0b19cefb721f67756afcade67a54ba2d2fcbc2be7462481103cd2fe8`  
		Last Modified: Tue, 02 Jul 2024 03:07:35 GMT  
		Size: 12.8 MB (12812458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a65017c5fff5bdbf4e6ed2ef891894e6e82ba8ee7e78aa4be1bc5dc840309a`  
		Last Modified: Tue, 02 Jul 2024 03:07:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858861860c883ad9bbd0b4d9890b7f5da952f5b355b6ac3d8837192f66931a49`  
		Last Modified: Tue, 02 Jul 2024 03:07:35 GMT  
		Size: 10.9 MB (10855256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a7e452349b7a3c7288686b98c22cb60a21684ed1e692e41246ff28042ec963`  
		Last Modified: Tue, 02 Jul 2024 03:07:33 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fb2532b04431089c3ee00e57c184cfbbac0425c2fd1da833583dd29a7a3d6b`  
		Last Modified: Tue, 02 Jul 2024 03:07:33 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d38afdd93df871fb4749fddfea9c92d2c5ba5b201e11d2e63187726fa83ee9`  
		Last Modified: Tue, 02 Jul 2024 03:07:33 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01939ebd3b71e52cb3c21a28fefedfa2e303870a45e88ab79a0422c0570b4aa5`  
		Last Modified: Tue, 02 Jul 2024 05:14:55 GMT  
		Size: 26.7 MB (26701032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c50fea02f1e03b8c01bb9ded3311683cec940a100898fcf0f0c60e9419a01f`  
		Last Modified: Tue, 02 Jul 2024 05:14:55 GMT  
		Size: 28.2 MB (28184240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876193100ff8c3df65b5e0f4b3a794af1c4c23aa6620b6b0e05067b2c73a29e4`  
		Last Modified: Tue, 02 Jul 2024 05:14:51 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b42e012baebc0dfbd65b6a5124bad44779c703661848ab13c89b39972081f`  
		Last Modified: Tue, 02 Jul 2024 05:14:50 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c691ee6aaa5f8a9a8a007b8c6e0409bd20199a8dd92e4f31fc7695943b9d085c`  
		Last Modified: Tue, 02 Jul 2024 05:14:50 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6356eb0ba7fc6f6f2b10d9ba1cd90bbd2286742801f64414c7cab28cc85489`  
		Last Modified: Tue, 02 Jul 2024 05:14:53 GMT  
		Size: 23.7 MB (23715620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a315024b8a1afa7673d3aacaabeaacdf33bfad9e05296142fdd588fb9fac6a1f`  
		Last Modified: Tue, 02 Jul 2024 05:14:50 GMT  
		Size: 3.7 KB (3657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c45c9a2cb1a9eaf7639a32312150ac3e4bea2ec18a452e6e8a1ee901e16aba6`  
		Last Modified: Tue, 02 Jul 2024 05:14:50 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
