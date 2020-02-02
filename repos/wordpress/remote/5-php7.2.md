## `wordpress:5-php7.2`

```console
$ docker pull wordpress@sha256:6fa421cbf9acc1ff6115377ff7bb803e447c8a0e4b6de6da3e0711d6203867df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `wordpress:5-php7.2` - linux; amd64

```console
$ docker pull wordpress@sha256:9c1e3af8c53b42238b9d634a27eafdebc83ddb29f57c2d65d8823bd560f62d29
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187355480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7744d23afc42f17fe124368ae4e03d30c6f40fee7fa8ff1566cbd9deec1c24`
-	Entrypoint: `["docker-entrypoint.sh"]`
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
# Sun, 02 Feb 2020 12:21:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 12:23:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 12:23:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 02 Feb 2020 12:23:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sun, 02 Feb 2020 12:23:57 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sun, 02 Feb 2020 12:23:58 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 12:23:58 GMT
ENV WORDPRESS_VERSION=5.3.2
# Sun, 02 Feb 2020 12:23:58 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Sun, 02 Feb 2020 12:24:04 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Sun, 02 Feb 2020 12:24:04 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Sun, 02 Feb 2020 12:24:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 12:24:05 GMT
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
	-	`sha256:f6ebb87ff2f5ae8b17371305ba5d35b6e07cf3c19e9b548965b016c9c83f058a`  
		Last Modified: Sun, 02 Feb 2020 12:36:23 GMT  
		Size: 16.7 MB (16704462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cc2251ba93f7a3d2716cadc93827464b97d0d00b1d9094d161c753d3e3932c`  
		Last Modified: Sun, 02 Feb 2020 12:36:22 GMT  
		Size: 9.5 MB (9486778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324b0b73c50a15ec85d06a53cf9b8def270da27ca1a0b2c30b7d33954842baef`  
		Last Modified: Sun, 02 Feb 2020 12:36:17 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f86b05a1639b2013aee7c26370295cbd8f7a7f2b16189c8b43d99ff9f860d0`  
		Last Modified: Sun, 02 Feb 2020 12:36:17 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22bdbd87890a940355736dd5851d444a265d13e7c4f86e6d8557768b10ca3f2`  
		Last Modified: Sun, 02 Feb 2020 12:36:17 GMT  
		Size: 19.5 KB (19478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19160827fb4377d43704912a3d21d2d077d8c3c6652adae4a1bb8fa1d36d17a7`  
		Last Modified: Sun, 02 Feb 2020 12:36:21 GMT  
		Size: 12.2 MB (12227880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd82ff2c6e0e6d0969e527bd09488ef7294f1ecaad4ccd8039c05fc19adede2`  
		Last Modified: Sun, 02 Feb 2020 12:36:17 GMT  
		Size: 3.9 KB (3894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-php7.2` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:245b711f5ddef92b0a9e09989c6ea3419518154c2d0f3158531a3aaeb8683379
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164102687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9e8910169fd794246d916c21f76c514f1b2250079fc0180d4a2d72099e7fa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
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
# Sat, 01 Feb 2020 21:51:49 GMT
ENV PHP_VERSION=7.2.27
# Sat, 01 Feb 2020 21:51:50 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Sat, 01 Feb 2020 21:51:50 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Sat, 01 Feb 2020 21:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 01 Feb 2020 21:52:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:55:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sat, 01 Feb 2020 21:55:32 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:55:34 GMT
RUN docker-php-ext-enable sodium
# Sat, 01 Feb 2020 21:55:36 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sat, 01 Feb 2020 21:55:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 01 Feb 2020 21:55:37 GMT
STOPSIGNAL SIGWINCH
# Sat, 01 Feb 2020 21:55:38 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:55:39 GMT
WORKDIR /var/www/html
# Sat, 01 Feb 2020 21:55:40 GMT
EXPOSE 80
# Sat, 01 Feb 2020 21:55:40 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 08:25:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 08:29:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 08:29:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 02 Feb 2020 08:29:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sun, 02 Feb 2020 08:29:26 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sun, 02 Feb 2020 08:29:28 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 08:29:28 GMT
ENV WORDPRESS_VERSION=5.3.2
# Sun, 02 Feb 2020 08:29:30 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Sun, 02 Feb 2020 08:29:36 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Sun, 02 Feb 2020 08:29:37 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Sun, 02 Feb 2020 08:29:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 08:29:40 GMT
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
	-	`sha256:0b7d7b1c4a21aea0a469d44f029bf6c5d1db823c4fb8ee705ffee9f6f29ec8eb`  
		Last Modified: Sat, 01 Feb 2020 22:28:04 GMT  
		Size: 12.6 MB (12643160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11da19b0fa8cd7f623d96f1f70d608f89a84190c5574938b71db695ec4dac790`  
		Last Modified: Sat, 01 Feb 2020 22:28:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c2ef509e29a94b1e00dd53858c5e7ddbddec32841de8bf4965a65d62d1cb6`  
		Last Modified: Sat, 01 Feb 2020 22:28:05 GMT  
		Size: 12.9 MB (12916522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c865585d5992c2df0cc36086ed076ce01c575717569b8c7314f821e120db406d`  
		Last Modified: Sat, 01 Feb 2020 22:28:00 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995f102acdda7f69f4f08f8e5093c430f26f11da1584e76978abf74295272337`  
		Last Modified: Sat, 01 Feb 2020 22:28:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38af5d9bdc5ff23a3702861ec3ac8c1eb56ce08674fdc61d779d31c8cdf81652`  
		Last Modified: Sat, 01 Feb 2020 22:28:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbcd64d877c8b57356f11e4b2aa2740ad08736444d2b6faa70c134e40435146`  
		Last Modified: Sat, 01 Feb 2020 22:28:00 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202cf8c16674e11dca3e0078803d441f8323ebb1296c6627e9bfe6a82db30ade`  
		Last Modified: Sun, 02 Feb 2020 08:53:01 GMT  
		Size: 16.3 MB (16279199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c86a868be0441efe13991446935aaa79397e9af91245bdde5b8ed51bb673b`  
		Last Modified: Sun, 02 Feb 2020 08:52:58 GMT  
		Size: 8.4 MB (8352649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f263816e66f0c3f54e7a22b932ee8e1f25aeebdbb4e570351a84437ee56df37`  
		Last Modified: Sun, 02 Feb 2020 08:52:52 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee36845f5c77a72dfa797ddb4085eaf920b219071bb034be7725629d579ba741`  
		Last Modified: Sun, 02 Feb 2020 08:52:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e46a120179270427b796edb455bc96ede5af7606ae4d7b76c31baabb3a24e4`  
		Last Modified: Sun, 02 Feb 2020 08:52:52 GMT  
		Size: 19.5 KB (19491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f998b0eaffd719e61843142e2dcfdce5f33879fd5b49e97b0ca6a9602741619`  
		Last Modified: Sun, 02 Feb 2020 08:52:58 GMT  
		Size: 12.2 MB (12227883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52665ad7dff1377aa22e0759be0372d081c5ee84e9844f09abcfdb5b72ef511`  
		Last Modified: Sun, 02 Feb 2020 08:52:52 GMT  
		Size: 3.9 KB (3896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-php7.2` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:60055f2aff0bd90c4e8482405494ff2f50677fcb498c310429f9e38717921297
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160137984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5c2ee2541d1ad28d69ac679773ab6af9a13001ac8f02f3eb950da86b33226b`
-	Entrypoint: `["docker-entrypoint.sh"]`
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
# Sun, 02 Feb 2020 01:55:58 GMT
ENV PHP_VERSION=7.2.27
# Sun, 02 Feb 2020 01:55:59 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Sun, 02 Feb 2020 01:56:00 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Sun, 02 Feb 2020 01:56:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sun, 02 Feb 2020 01:56:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sun, 02 Feb 2020 01:59:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Sun, 02 Feb 2020 01:59:49 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Sun, 02 Feb 2020 01:59:52 GMT
RUN docker-php-ext-enable sodium
# Sun, 02 Feb 2020 01:59:54 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sun, 02 Feb 2020 01:59:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 02 Feb 2020 01:59:55 GMT
STOPSIGNAL SIGWINCH
# Sun, 02 Feb 2020 01:59:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sun, 02 Feb 2020 01:59:57 GMT
WORKDIR /var/www/html
# Sun, 02 Feb 2020 01:59:58 GMT
EXPOSE 80
# Sun, 02 Feb 2020 01:59:59 GMT
CMD ["apache2-foreground"]
# Sun, 02 Feb 2020 16:40:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:43:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 16:43:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 02 Feb 2020 16:43:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sun, 02 Feb 2020 16:43:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sun, 02 Feb 2020 16:43:40 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 16:43:41 GMT
ENV WORDPRESS_VERSION=5.3.2
# Sun, 02 Feb 2020 16:43:42 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Sun, 02 Feb 2020 16:43:47 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Sun, 02 Feb 2020 16:43:48 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Sun, 02 Feb 2020 16:43:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 16:43:49 GMT
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
	-	`sha256:75fa62c85c7efd91d72e83cbab94a745b73bb6e469de8dee7c2618d509a8a320`  
		Last Modified: Sun, 02 Feb 2020 02:33:38 GMT  
		Size: 12.6 MB (12643216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb95ed566f3a4d63df6cda76b22f399669b4bf2dadf67923b81f7f38341dc0d`  
		Last Modified: Sun, 02 Feb 2020 02:33:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a6e15f8b40eeb975787fff828e9c76f4779010a6587c02b6d3cae78216f6d8`  
		Last Modified: Sun, 02 Feb 2020 02:33:37 GMT  
		Size: 12.2 MB (12186050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8841f7ffdafa5981a29a906525d29f87b57b56bdfc986edff6e6e5b2ce8802bd`  
		Last Modified: Sun, 02 Feb 2020 02:33:33 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937f8cf7a7089ce03b390bb4e740c0037f7942113980c931736cfc8ca9907826`  
		Last Modified: Sun, 02 Feb 2020 02:33:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993c749504c7d0061e00637a3256e8f445ae818bdce2688683cc024a75d8651a`  
		Last Modified: Sun, 02 Feb 2020 02:33:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f006a30d9988760930421865c04379e76b4db1f624a5021ae2bb5aee3f738675`  
		Last Modified: Sun, 02 Feb 2020 02:33:33 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2038af42b9fc6e985413e896944d01ce93a8c00f4d19d9db1d5136a710a870d6`  
		Last Modified: Sun, 02 Feb 2020 17:03:26 GMT  
		Size: 15.9 MB (15854777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481f48caa5af257cd8196c55043c7a0177854773d933802bf66b82cd244eba2a`  
		Last Modified: Sun, 02 Feb 2020 17:03:21 GMT  
		Size: 7.5 MB (7514013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdd9e432d8e980a55efa92b6a0840a926793180900fc4735d9f86d2b4db7a69`  
		Last Modified: Sun, 02 Feb 2020 17:03:17 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769cffbd9383626450d953701329fd389b84bbd1c940b77c97e5309fc270eda3`  
		Last Modified: Sun, 02 Feb 2020 17:03:17 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acd2f6d8a3050c4fb65a480d65f59c34a3ed5aec0e1404f1380f627a3c264f3`  
		Last Modified: Sun, 02 Feb 2020 17:03:17 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f021c4729c25e44f8497a83f0c95d6683ff6e66b41128920c62a694b9b452d`  
		Last Modified: Sun, 02 Feb 2020 17:03:23 GMT  
		Size: 12.2 MB (12227884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a91fd9f65cc12d05651c8cfc0210fef1666f26d46549f3f646e1267e4d5fcd`  
		Last Modified: Sun, 02 Feb 2020 17:03:17 GMT  
		Size: 3.9 KB (3894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-php7.2` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:65a27800006d597b443e558a66a648fa81275297a88453d72a370afd6d15f7a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177746070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c23456d71b95a5c22d051599fad8508d45cb643082b04b842520ce0a824aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
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
# Sun, 02 Feb 2020 18:56:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:59:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 18:59:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 02 Feb 2020 18:59:16 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sun, 02 Feb 2020 18:59:20 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sun, 02 Feb 2020 18:59:20 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 18:59:21 GMT
ENV WORDPRESS_VERSION=5.3.2
# Sun, 02 Feb 2020 18:59:21 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Sun, 02 Feb 2020 18:59:26 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Sun, 02 Feb 2020 18:59:27 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Sun, 02 Feb 2020 18:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 18:59:30 GMT
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
	-	`sha256:9d44c205ad7b6124d736782459842c9e914f15fa2171162cc16b6f0d36206a66`  
		Last Modified: Sun, 02 Feb 2020 19:18:48 GMT  
		Size: 16.6 MB (16649359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d044d86c24c79931fca8db8e0fb8e10a72ef86f683ae6e5eea70ce21ab921f`  
		Last Modified: Sun, 02 Feb 2020 19:18:44 GMT  
		Size: 7.9 MB (7895950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4871148c86a088858c1c2a53709c9aa41840e2e351b0ad79446b88ec24ae36e9`  
		Last Modified: Sun, 02 Feb 2020 19:18:41 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b1e43dcd8630a56dd18a8636d6df600659a6cdf610848ba4aaa7c36c55eeaa`  
		Last Modified: Sun, 02 Feb 2020 19:18:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458dfc90a06aa7647518ce060a067fb28cf045592a2851e021336236cbac2b47`  
		Last Modified: Sun, 02 Feb 2020 19:18:41 GMT  
		Size: 19.5 KB (19498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dd2a28d57c145e7e53c39396015d0d8b8f30a5b0c27e77c2c1c31b6128f456`  
		Last Modified: Sun, 02 Feb 2020 19:18:45 GMT  
		Size: 12.2 MB (12227881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2886e3b6696fa426d83993f50663a1773014f3583255ee01e9267851d727b`  
		Last Modified: Sun, 02 Feb 2020 19:18:41 GMT  
		Size: 3.9 KB (3891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-php7.2` - linux; 386

```console
$ docker pull wordpress@sha256:d1b16bd9b0cd766ec49d587ebca3e05b0fba664bbc3e6cac474b1f21dab9e5f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192879477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b034d21905788602f55a959d0776984716e4c6c087da14d5a7394bd0e55d44d`
-	Entrypoint: `["docker-entrypoint.sh"]`
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
# Sun, 02 Feb 2020 12:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 12:27:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 12:27:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sun, 02 Feb 2020 12:27:41 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sun, 02 Feb 2020 12:27:42 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Sun, 02 Feb 2020 12:27:43 GMT
VOLUME [/var/www/html]
# Sun, 02 Feb 2020 12:27:43 GMT
ENV WORDPRESS_VERSION=5.3.2
# Sun, 02 Feb 2020 12:27:43 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Sun, 02 Feb 2020 12:27:53 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Sun, 02 Feb 2020 12:27:54 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Sun, 02 Feb 2020 12:27:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 12:27:54 GMT
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
	-	`sha256:ea40153ec91b190f919e492ef5d66253b03d6610a1014e77585b74fec34a6020`  
		Last Modified: Sun, 02 Feb 2020 12:41:46 GMT  
		Size: 17.0 MB (17022261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78da899e2f3c0872ab1a13729416f960491998d25408ce1f65e592ad13cd55ed`  
		Last Modified: Sun, 02 Feb 2020 12:41:43 GMT  
		Size: 8.7 MB (8728426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a475ba1a2b7e13ef1a0f5510039e4b3282478e53453642b9c42bb9c1475f51ba`  
		Last Modified: Sun, 02 Feb 2020 12:41:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126961742e080557cfd51bac60d355fa7773c597d56edd82e6dc0d2a0625e67b`  
		Last Modified: Sun, 02 Feb 2020 12:41:38 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d986cb18a4981ec83b93c798fdebc1b922e9f5a0ca2816f5f7edc468cc43b4`  
		Last Modified: Sun, 02 Feb 2020 12:41:38 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5936ee465d8606fa779e54715d6d1caa30735ccd660a8dce94188115fe7a4a`  
		Last Modified: Sun, 02 Feb 2020 12:41:44 GMT  
		Size: 12.2 MB (12227873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc46bd3d3e35862361b9df62a5a6454f1c73344d673733ca6d39cc792d52635d`  
		Last Modified: Sun, 02 Feb 2020 12:41:38 GMT  
		Size: 3.9 KB (3896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:5-php7.2` - linux; ppc64le

```console
$ docker pull wordpress@sha256:e3e149b21af27279995b163d250a0b968e58aabf7bae3d397c2680e01ec2bf26
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199176323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9200353cce70248c489940aad8e31c527eca356ebfdb9000d9608b25fb0e0fa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:39 GMT
ADD file:abec4f3d6a54bb0725560d826d07e99da3d6b582433c6dd95605626c67d7c2d6 in / 
# Sat, 28 Dec 2019 04:20:43 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 18:07:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 Dec 2019 18:07:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 Dec 2019 18:09:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 18:09:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 Dec 2019 18:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 Dec 2019 18:15:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 28 Dec 2019 18:15:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 28 Dec 2019 18:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 28 Dec 2019 18:17:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 28 Dec 2019 18:17:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 28 Dec 2019 18:17:22 GMT
ENV PHP_EXTRA_BUILD_DEPS=apache2-dev
# Sat, 28 Dec 2019 18:17:24 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--with-apxs2 --disable-cgi
# Sat, 28 Dec 2019 18:17:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 Dec 2019 18:17:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 28 Dec 2019 19:27:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Jan 2020 01:17:53 GMT
ENV PHP_VERSION=7.2.27
# Fri, 24 Jan 2020 01:17:57 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.27.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.27.tar.xz.asc/from/this/mirror
# Fri, 24 Jan 2020 01:17:59 GMT
ENV PHP_SHA256=7bd0fb9e3b63cfe53176d1f3565cd686f90b3926217158de5ba57091f49e4c32 PHP_MD5=
# Fri, 24 Jan 2020 01:18:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 24 Jan 2020 01:18:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Fri, 24 Jan 2020 01:22:39 GMT
COPY multi:3ab587b19c9ec9c9b34bacbe7fa0911462d0bafd50179d8808e207ed9b82b0b9 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:22:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 24 Jan 2020 01:22:53 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 24 Jan 2020 01:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 24 Jan 2020 01:22:58 GMT
STOPSIGNAL SIGWINCH
# Fri, 24 Jan 2020 01:22:59 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 24 Jan 2020 01:23:01 GMT
WORKDIR /var/www/html
# Fri, 24 Jan 2020 01:23:03 GMT
EXPOSE 80
# Fri, 24 Jan 2020 01:23:05 GMT
CMD ["apache2-foreground"]
# Fri, 24 Jan 2020 09:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jan 2020 09:50:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 	; 		docker-php-ext-configure gd --with-freetype-dir=/usr --with-jpeg-dir=/usr --with-png-dir=/usr; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		opcache 		zip 	; 	pecl install imagick-3.4.4; 	docker-php-ext-enable imagick; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jan 2020 09:51:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jan 2020 09:51:09 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 24 Jan 2020 09:51:14 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPTrustedProxy 10.0.0.0/8'; 		echo 'RemoteIPTrustedProxy 172.16.0.0/12'; 		echo 'RemoteIPTrustedProxy 192.168.0.0/16'; 		echo 'RemoteIPTrustedProxy 169.254.0.0/16'; 		echo 'RemoteIPTrustedProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' +
# Fri, 24 Jan 2020 09:51:17 GMT
VOLUME [/var/www/html]
# Fri, 24 Jan 2020 09:51:21 GMT
ENV WORDPRESS_VERSION=5.3.2
# Fri, 24 Jan 2020 09:51:24 GMT
ENV WORDPRESS_SHA1=fded476f112dbab14e3b5acddd2bcfa550e7b01b
# Fri, 24 Jan 2020 09:51:31 GMT
RUN set -ex; 	curl -o wordpress.tar.gz -fSL "https://wordpress.org/wordpress-${WORDPRESS_VERSION}.tar.gz"; 	echo "$WORDPRESS_SHA1 *wordpress.tar.gz" | sha1sum -c -; 	tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 	chown -R www-data:www-data /usr/src/wordpress
# Fri, 24 Jan 2020 09:51:33 GMT
COPY file:d93be233af180b81b8838a1d00e9f930eb82172c751ffaafb4732db4a09a7534 in /usr/local/bin/ 
# Fri, 24 Jan 2020 09:51:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jan 2020 09:51:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37e6f4d596ea5c3cc92914bd95508a4192c8834c4edaff414734885929b07800`  
		Last Modified: Sat, 28 Dec 2019 04:28:05 GMT  
		Size: 30.5 MB (30517529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253f3f96795b9e74581686a5867b34cf3ecd5456bb7932c9ec497837086b036c`  
		Last Modified: Sat, 28 Dec 2019 20:11:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077abe7f19b79a3a23bfa7192e160eec857b8a062f0a13f4bf6bbce92bee057`  
		Last Modified: Sat, 28 Dec 2019 20:12:16 GMT  
		Size: 82.3 MB (82259503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565c1c236ff11a718b8647ec9809cbe25c526a10c71b8062301809806c2d05bd`  
		Last Modified: Sat, 28 Dec 2019 20:11:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1372dfcd0e5e6d2bb1596fd6d6b76343945db2d38c2bf250246fb8cd3d5a2c1`  
		Last Modified: Sat, 28 Dec 2019 20:13:20 GMT  
		Size: 19.8 MB (19811373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324fd437fe3df3006e8a7a6aefd39c9ccc10c1b57193917c4e4cee049076d29b`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6942ad65b54758c147c0578b07c2458a0ac935892e3591c3222ad3085b3cb8`  
		Last Modified: Sat, 28 Dec 2019 20:13:10 GMT  
		Size: 519.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f4261eade962bad58ec7f712615d695dfba3bc49174e5dec74a9d33b136ad`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 12.6 MB (12645005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4cb21bfc01fd93a9e418cf7bc2327e279bb2df4649a3da6db84f72bb408c5`  
		Last Modified: Fri, 24 Jan 2020 02:44:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0996209acd92ef0fa07ed86c14082220cb0f713b198ba2a941b223fe0cf753d0`  
		Last Modified: Fri, 24 Jan 2020 02:44:05 GMT  
		Size: 14.9 MB (14882858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131065afee7c0bee89bbc44fb4436e2b58ff0e21c79130e156400c68e26df4e`  
		Last Modified: Fri, 24 Jan 2020 02:44:01 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e21322eb9a58aa48fa2c039c10045f27a8fd47d1f96e160a76658eacd6829`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b79d68cb91344e97e77178c1de2c78953eed938b075a8ebb62b710a51c5801a`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c034275e5ae4c2f35342f8f011f4369f4352a24db20dc39abee71d8e7b8cbc4d`  
		Last Modified: Fri, 24 Jan 2020 02:44:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18db1b573da68bc58fd842f91e107166e6b76e9f1fce5f302799a6891f03c43e`  
		Last Modified: Fri, 24 Jan 2020 10:45:34 GMT  
		Size: 17.5 MB (17455226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23318d5e8c931bae90de1e256402aef78730e70774680f43b3059f995b7e3c4d`  
		Last Modified: Fri, 24 Jan 2020 10:45:27 GMT  
		Size: 9.3 MB (9347262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ef350bdfdedf3ae847ed7c006f8ed90f68cfa52a8efcc6bd1fc4650f55f429`  
		Last Modified: Fri, 24 Jan 2020 10:45:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d67fc1f6cbc962a3c44362113a85dfda0cfb329a49e356990834af9ba025391`  
		Last Modified: Fri, 24 Jan 2020 10:45:18 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a865fdbd5884c04aaeb1a3572078e63813ba3d5bc5961fa5f68f0cbb5f1c77bd`  
		Last Modified: Fri, 24 Jan 2020 10:45:18 GMT  
		Size: 19.5 KB (19497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3e4301dbd44fc022dda0c4a1c645cb0b9c5c29a756f22a6a3a7063ae435b1`  
		Last Modified: Fri, 24 Jan 2020 10:45:26 GMT  
		Size: 12.2 MB (12227875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791fda2367405717d279197dafbee5ed657108431240e4f5b9430e7f6735a923`  
		Last Modified: Fri, 24 Jan 2020 10:45:18 GMT  
		Size: 3.9 KB (3895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
