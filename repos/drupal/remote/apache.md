## `drupal:apache`

```console
$ docker pull drupal@sha256:0d5fd3127b1cc8ab229c224ace08193db995adea3bd093863d79525817bcf8ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:apache` - linux; amd64

```console
$ docker pull drupal@sha256:a5173fdb1a84d3aef9dc101751692e795cd4b60bee5734d5fcad7130e4052f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199568985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe8714adac4e2aad5173b228dc05d1c7a414adc55529b7fd069677c531b1b97`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 08 Feb 2024 04:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 80
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c386db9cb1d87e70bc4655a9f464379178e6faec37925b32f481121cd1fd6b5`  
		Last Modified: Tue, 13 Feb 2024 07:32:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef1b237c949fbfc49af0024af5189a1feefff253e445a7b19ab4327ce5a5909`  
		Last Modified: Tue, 13 Feb 2024 07:33:11 GMT  
		Size: 104.4 MB (104355255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c66cb68b0ffb6ab95a1aa748b4012b5da8077a4a4c14a3f9bebcf9bf02f351`  
		Last Modified: Tue, 13 Feb 2024 07:32:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c790c1c009dd7204cac7a35fd9151636c23f96ae965fec6263addd5d366c547`  
		Last Modified: Tue, 13 Feb 2024 07:33:38 GMT  
		Size: 20.3 MB (20303944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055748d0b38a426b2cef949d76f35fc04c5a9a9a66a2d40449219a4853635cf`  
		Last Modified: Tue, 13 Feb 2024 07:33:35 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d72b3b895bccef06314fe3a5818d977b5b695a9e1a698eab278c1138790f8`  
		Last Modified: Tue, 13 Feb 2024 07:33:35 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a354636f862b01c059c1bfb98b1fb5690dee04607860bfcde46df979b83e0745`  
		Last Modified: Tue, 13 Feb 2024 07:42:05 GMT  
		Size: 12.4 MB (12408680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139fa831a3e6a192d9c34b51da2278bbc21b59818211cad69aa0afae9cd1732`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17106305d52519fd77cf6375c68dc5af30746038c372d15c8afb53bcdcb4c68a`  
		Last Modified: Tue, 13 Feb 2024 07:42:04 GMT  
		Size: 11.4 MB (11404904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b86f20916c18b1fb9b329b32e4f8701ebdc9191b17f4be6bc52fa3f3215e50`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa13ba4f6f48ae2301250cca77c42706fb9e7566d701084f7f9d5a3e498c2123`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2fe7754d476224d8cbaf01f8c02b87e12b08c9fbf6d6f19716d0e3b64e4e89`  
		Last Modified: Tue, 13 Feb 2024 07:42:02 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003dbe2ef75978bcdc18f00a252c8f9f3ac36be1debed8cbbaefa4cf41a91755`  
		Last Modified: Tue, 13 Feb 2024 08:58:09 GMT  
		Size: 2.0 MB (1997121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67069b968a6c5344d41264afb60c14dbdd720a8353d5a2eedbe5cddb1994363b`  
		Last Modified: Tue, 13 Feb 2024 08:58:09 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de54ec79694021db5c268cce1a433ffc2275bb6966acdac0e088112241d34366`  
		Last Modified: Tue, 13 Feb 2024 08:58:09 GMT  
		Size: 721.6 KB (721578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a62b1c4debbb460594b533c062b84fdbc0102746f55eade09095500d1886b1`  
		Last Modified: Tue, 13 Feb 2024 08:58:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6053ac54d0024cc7c4484534b6bbdc85fa787be61d61accf56976c678808c30a`  
		Last Modified: Tue, 13 Feb 2024 08:58:11 GMT  
		Size: 19.2 MB (19247415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:8b00bd90d91e7b700326a5d849bb19df2cc116e3b7987690be311a5e62cc7b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6489029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4d80524b5ca80a169e8123e423258ec6e6f787fcba47273176811213779e34`

```dockerfile
```

-	Layers:
	-	`sha256:71d000543773a577e5361a18dfe5f3729afb73f9b58a71c4670719e9962b1729`  
		Last Modified: Tue, 13 Feb 2024 08:58:09 GMT  
		Size: 6.4 MB (6443418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a67a2eafb45c0875937a772ec43e7370d3651dca77e3fd340a7839a14359aa`  
		Last Modified: Tue, 13 Feb 2024 08:58:09 GMT  
		Size: 45.6 KB (45611 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5bebe7ca0fb402c5bceffcb33e92c430b96a11ef036989ee84ed5a25ae150876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163514313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbe18ccbd994735937779b3860144f17b95798945a0cd660ac4cec4400c126d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:07:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 03:07:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 03:07:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:07:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 03:07:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 03:10:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 03:10:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 03:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 03:10:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 03:10:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 03:10:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 03:10:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 03:10:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 03:36:10 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Feb 2024 03:36:11 GMT
ENV PHP_VERSION=8.2.15
# Thu, 01 Feb 2024 03:36:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 01 Feb 2024 03:36:11 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 01 Feb 2024 03:36:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 03:36:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:39:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 03:39:33 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:39:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 03:39:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 03:39:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 03:39:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 03:39:34 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 03:39:34 GMT
EXPOSE 80
# Thu, 01 Feb 2024 03:39:34 GMT
CMD ["apache2-foreground"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391138267e710c3afd1b13ba20349432d550fbb6ca24d5c03c761feae22b88ee`  
		Last Modified: Thu, 01 Feb 2024 04:24:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc30a445c6e4bf057f6d7fb3a4548be66cef938aca0884681b2602cf7807923`  
		Last Modified: Thu, 01 Feb 2024 04:25:04 GMT  
		Size: 76.2 MB (76169686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2abab10a7e661e57eca65741d4ee689ebb206370db90b4c05c93aa3b7afce10`  
		Last Modified: Thu, 01 Feb 2024 04:24:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c27433b27de38bd46689c5ab4ea8a423bc343feebaea73d1d20d2aa314da3e`  
		Last Modified: Thu, 01 Feb 2024 04:25:49 GMT  
		Size: 19.0 MB (19046603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1fd23f93df4e6bcc7adb049f7e12804c6313798f3ceec63da7db141eed10a8`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649568d520a69772a79a3e5c4ce6031b6f2f7e274993c07bb783e481941066ff`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe2c127a46474022cc69e7ab8271858708631787a77ab94ffaa600e5eb352f2`  
		Last Modified: Thu, 01 Feb 2024 04:29:27 GMT  
		Size: 12.4 MB (12407860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1daa5547ed933b4460fa4dfe771b898e2f3e75ce7f99cb3a200a8c54748266e`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463e5207c526ebce9c5b4cf701e473e1199d310fbeb4787cd93619db99743a0`  
		Last Modified: Thu, 01 Feb 2024 04:29:27 GMT  
		Size: 9.8 MB (9819710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289557b5f69d251afef4200ff3e54c5f77a41457acd92715e7c9c1b0b0312de2`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60bbf7f7b83cf61f052a2eca634b228db210099d4ed918b0bac7e6db940fe27`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeee08a95fa2936e7413f4697356510c2b22ad55b9a16f5f769be6124a50f3f`  
		Last Modified: Thu, 01 Feb 2024 04:29:24 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be284d71b4c5ad9c1a7d5992ae599c79aafb706796588bb378a01cdf1c5d5ad`  
		Last Modified: Fri, 02 Feb 2024 15:34:10 GMT  
		Size: 1.4 MB (1354080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caedbf490ef9c9f3ce0921b07ed39041fdb63e33718e840500c3aa7e3f68ff1a`  
		Last Modified: Fri, 02 Feb 2024 15:34:10 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbb565c887f1e6af1d445a8c076be295b9884ed65f05d8f2c4d4efe06c53f59`  
		Last Modified: Mon, 12 Feb 2024 22:18:57 GMT  
		Size: 721.6 KB (721586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aba86857a693c7b356610129bf9ef956a9387acbf1047ee0f3e885cf12baac`  
		Last Modified: Mon, 12 Feb 2024 22:18:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d741e9f00f6e613366f4a2c894a400816c9e1f367a82fca4bef47c96f2942a`  
		Last Modified: Mon, 12 Feb 2024 22:18:58 GMT  
		Size: 19.2 MB (19247234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:2655f1a8cac262c7ba2c3770aed1df46e254f77a3ebb45736b0a72771ad55938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6324614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe27b3faa86dfd3f7d3095d28937e8c664b0a80cf3bd78e39e62d5e5156bdf5`

```dockerfile
```

-	Layers:
	-	`sha256:f07234b934d96668d0a0e553d7c5914405f948cdcba7456fb990b7474d546486`  
		Last Modified: Mon, 12 Feb 2024 22:18:57 GMT  
		Size: 6.3 MB (6283125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88470c53611d1b331c3518d61222796e5bb31b8c87741e337c777be09afc6cce`  
		Last Modified: Mon, 12 Feb 2024 22:18:56 GMT  
		Size: 41.5 KB (41489 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:bbc9439b8f1f95492f9d2694818f18d2495718a73d4233888205ed5dd77e4ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193635370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db0ad7e1c782ceed1a6a917dfb6941f1f66d4263544ab747c7673524e3cfbb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 08 Feb 2024 04:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 80
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7a340515b48e1c129ae5f32a9749bddee1f8e8329b7598fcbf4d08bbd6fb1`  
		Last Modified: Tue, 13 Feb 2024 07:00:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290f914abd180febe4ca21f26e7dbd62a7d47b3e0c2bb607b502ef0420c26a39`  
		Last Modified: Tue, 13 Feb 2024 07:00:29 GMT  
		Size: 98.1 MB (98125913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa77fec9d8935ca4f47917fa1800499aeb09f491467b65b0914b9598f905ab`  
		Last Modified: Tue, 13 Feb 2024 07:00:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e32a81172311d82a21a8c59c44a19943264d56868424bc14043cf6100b2fd`  
		Last Modified: Tue, 13 Feb 2024 07:00:54 GMT  
		Size: 20.3 MB (20305132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4064de42914748cf75888bc76bce8469dc92ae858893c597ede2741b140c622`  
		Last Modified: Tue, 13 Feb 2024 07:00:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1ed550d4635090d82d30c08e1d408806bfba8c24fffe9004f3b0837df191b`  
		Last Modified: Tue, 13 Feb 2024 07:00:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29386a07b0fb38b6f26a5a8c069cad0296b4554cee7ca6d835d589aba41462c`  
		Last Modified: Tue, 13 Feb 2024 07:09:04 GMT  
		Size: 12.4 MB (12408227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6a0d2ccf9bb28e54c8b6e5ad86add1a87bfb22761da9eb7ea8bdf4b7ebdd8e`  
		Last Modified: Tue, 13 Feb 2024 07:09:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec30c4cb990f53b935a7f8bd9190a5c37fb2d7c7427b6c7b14e3e1ec73ba2a56`  
		Last Modified: Tue, 13 Feb 2024 07:09:02 GMT  
		Size: 11.4 MB (11411295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da02d12faeeddd5da284c9bf92ff195f1105bef826ab21ba909db967793c03c8`  
		Last Modified: Tue, 13 Feb 2024 07:09:00 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de9da0d9fb698f29b8b078b7b96bc86b5456666d456c2606fa10d22b4b8d94a`  
		Last Modified: Tue, 13 Feb 2024 07:09:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe3329f8e7716983d4634d2eb72f9a31acf2b043ffec645c05faad08bb47cab`  
		Last Modified: Tue, 13 Feb 2024 07:09:01 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e420d1beb619d5d9fe069037e74c55da92474e117b20c160b98222cea6f759`  
		Last Modified: Tue, 13 Feb 2024 16:22:44 GMT  
		Size: 2.3 MB (2255203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fb1c87f379efa899c82110076efc2b8d35840fe6c5380e070d72809de33692`  
		Last Modified: Tue, 13 Feb 2024 16:22:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ff9ec6bf36e9c2a9ee2e3ed5205f8930e74fbe435aa86a0b1258f9940bf79d`  
		Last Modified: Tue, 13 Feb 2024 16:22:44 GMT  
		Size: 721.6 KB (721584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bbaa5c3add8cb941598e2057a9ee9e886f0788dff2f9e2b4b5fa4754ea37be`  
		Last Modified: Tue, 13 Feb 2024 16:22:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26823a815a1698a08fc4c1d90c3ecf10c279a358546abcff1a8b47db8b62c935`  
		Last Modified: Tue, 13 Feb 2024 16:22:45 GMT  
		Size: 19.2 MB (19245660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:e329524694367bdc075e118fe8036ef4adc6433aa40bc2b81cf3b064f7c494db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a71e7c4c77cdd93bc26ccd571ccaa6cb4592ee782e255b0094677e98d2dee65`

```dockerfile
```

-	Layers:
	-	`sha256:044d89563138dc0d41f544b8006f182d1e2e44358ba3cf0281a1f73b35fe5a0a`  
		Last Modified: Tue, 13 Feb 2024 16:22:42 GMT  
		Size: 6.5 MB (6468465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a190dec3ac789885c61f0cb855f9f8d970f54663b88ac7264f901e6b0227be9e`  
		Last Modified: Tue, 13 Feb 2024 16:22:42 GMT  
		Size: 43.4 KB (43381 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; 386

```console
$ docker pull drupal@sha256:0ac508ff5f0f39c0284e3dddb9616ff51ea1767f2d894d406a2f3e7b1d210823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198558940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b33bc7a48406c4454f66ef9fad4524e819e60d7ff2d421897a6aaf2ac2b0425`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 08 Feb 2024 04:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 80
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfde49385a90835b9c1612c002c49650aa228e709c6bec76329576d154acf40`  
		Last Modified: Tue, 13 Feb 2024 09:08:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ed10d21879c841ec1dc9f3c51bfc996313547be9838dd0871e0c090e9db93`  
		Last Modified: Tue, 13 Feb 2024 09:09:19 GMT  
		Size: 101.5 MB (101519769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0108a981d683eb4695cf1efac3357088358d8bd27fafb095510dcdc689e9270f`  
		Last Modified: Tue, 13 Feb 2024 09:08:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa94a6b92707cb45a0ff3ab809cb18c5a53cfcaad6fb553c591ef3b376088a1e`  
		Last Modified: Tue, 13 Feb 2024 09:09:47 GMT  
		Size: 20.8 MB (20826088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ba0ea043787178dd74139db437ce2498a8d3bf85e4eed296ea8e55a598f5a`  
		Last Modified: Tue, 13 Feb 2024 09:09:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ec064cfc067a6de6b378be145b2249b472d81b6fbf511d5f614fdf9909cad5`  
		Last Modified: Tue, 13 Feb 2024 09:09:42 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f319fd9049ee21eccbb2c23231019d3746d7634ea0bfd69993f02efcf8997c`  
		Last Modified: Tue, 13 Feb 2024 09:19:17 GMT  
		Size: 12.4 MB (12407595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58504e4335c41bed822efa4ad7b25f791c5cc6d9083b99d25943fed18891bf68`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19276e3afb9f25daf34037f4d19ea0302b5350ded9a2d2a89bde7ad1c08bd7b7`  
		Last Modified: Tue, 13 Feb 2024 09:19:18 GMT  
		Size: 11.6 MB (11638109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f11b92ecacf55e1b3d78edbf5baccea90e44bbc062a77468ce5f01aae4ce53d`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de8b000ea1dc85d6489a771eacacc0b89a42714ac3564896f2a0f87ec18647`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec0f7e99cf4670b71f0f0410acde2e2986034b5cca05650e313a5afebcfdf52`  
		Last Modified: Tue, 13 Feb 2024 09:19:14 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef8b5846d80c0f716db3d0238aedb4eff27662dfba863e6bc4c050c39262c6`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 2.1 MB (2050648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a7650125ccc199e64d77e122aeacf5d91833e00ec430b0f30ea1ebfd13c499`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f302478d1f570ca34d2ed7e3eb2b3d77fcbd76721b4d6c49e66e5f92fd4785d`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 721.6 KB (721579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4208391196c2039bda315fbe6ef2b03d4dba8246d4b991f89964c08c0663d362`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f62c3255a75c1b794a0f65b831e1eb026dab6dc6a436498dc8ffa2c0acba1e5`  
		Last Modified: Tue, 13 Feb 2024 09:58:18 GMT  
		Size: 19.2 MB (19247346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:fba5576c56e86b3aaba2c50b40662b1712ab799fd19a4a569a31389c8e00666e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6470926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6212fddf0a911d6c6f35c2d7feecaeb09099ab8b06c025d58f1668a3624660da`

```dockerfile
```

-	Layers:
	-	`sha256:71228d9b67ec8c58ca09390cc4ab940cc796711a47b625bd6edb6e15507ef92d`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 6.4 MB (6425454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51d4a443d56844a1adf3d3a0e1437d9cd5e43fa8fb63bcc8e86534f950919b03`  
		Last Modified: Tue, 13 Feb 2024 09:58:17 GMT  
		Size: 45.5 KB (45472 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:3f7b3a360af6776c8d364786f5b92e6a3f4a926f213ac8f16fc657f9b2405325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203974005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df4b52055700066ee100edd1f2cd7d5cbe7e23509b919fb3cb53e95c69280d7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 08 Feb 2024 04:27:17 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["bash"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 08 Feb 2024 04:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 08 Feb 2024 04:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Feb 2024 04:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_VERSION=8.2.15
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Feb 2024 04:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Feb 2024 04:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Feb 2024 04:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 08 Feb 2024 04:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Feb 2024 04:27:17 GMT
EXPOSE 80
# Thu, 08 Feb 2024 04:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f1023e69b0297ca1b43f02b0de9f2700c16c9f3bc3cd4d532dce1fed98a82`  
		Last Modified: Tue, 13 Feb 2024 06:43:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c21152df6e3694f2bd61235e4c23ee7e24735cd91cfff9f6dca5abb307a801`  
		Last Modified: Tue, 13 Feb 2024 06:43:58 GMT  
		Size: 103.3 MB (103313095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0608cc469fd017def730be29629f988d7db21971cb60c627d4043f3f4ff24e3d`  
		Last Modified: Tue, 13 Feb 2024 06:43:40 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c86cd418ad9f36395f647795ce8a6ee67f8cc57ee87b45a13e843c0d2209c3f`  
		Last Modified: Tue, 13 Feb 2024 06:44:28 GMT  
		Size: 21.5 MB (21489555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82afa6fa26cbb0b105f3ff50f1bb25a7743b2fb1e1e56092bf210cfd7a63d9ae`  
		Last Modified: Tue, 13 Feb 2024 06:44:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20423759eec7201d4e061fab44ae4f2be21b3cf195ccf90ecac69aa7ff61e45`  
		Last Modified: Tue, 13 Feb 2024 06:44:25 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42550739b7f48af716ac832fad1934c3cd65a3af5c7b62a26902f47601927316`  
		Last Modified: Tue, 13 Feb 2024 06:54:14 GMT  
		Size: 12.4 MB (12408126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46df924d7eef2bd9e70044d4446be91fcdefdf371aace2a0259973ccc336aca8`  
		Last Modified: Tue, 13 Feb 2024 06:54:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167aa1659e64fadc6152357b3e6abc6d28f56a25b8076d22275d7bd36a9e03cc`  
		Last Modified: Tue, 13 Feb 2024 06:54:13 GMT  
		Size: 11.8 MB (11813243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8043b9d3bd33a06672fd37521b2445df2f9f85b8b52d9cc56969e67c45fb2d`  
		Last Modified: Tue, 13 Feb 2024 06:54:11 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1dfca68d509a1142b3fb23a5a6367e0ae0cb5474e4830eb706f009e87c99c3`  
		Last Modified: Tue, 13 Feb 2024 06:54:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ecf1b755b47018e22491beb51c9f16a806520903e77beea5834e58b541781`  
		Last Modified: Tue, 13 Feb 2024 06:54:11 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b2152b82db0166f33f5e101583cd23e2d2396e09aa7800269ea85c58d0333`  
		Last Modified: Tue, 13 Feb 2024 14:36:12 GMT  
		Size: 1.9 MB (1855994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c81eb21cb90f51556902eb814ce835b9cb3add072d84e52ec75670028d50bc8`  
		Last Modified: Tue, 13 Feb 2024 14:36:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a80122347f6dadd310852db0deb7cad0a48ff03f0607d12b26715e56fb6012`  
		Last Modified: Tue, 13 Feb 2024 14:36:12 GMT  
		Size: 721.6 KB (721584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ba1f32c27bcc9846b36552c5f69ad87b1b9ef552f6386258a6213b2df31044`  
		Last Modified: Tue, 13 Feb 2024 14:36:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ef52396a8cd1142da104ad547499e7d1656921d7e5b3fa47fb2d26cc6ac1fa`  
		Last Modified: Tue, 13 Feb 2024 14:36:14 GMT  
		Size: 19.2 MB (19247501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:bf20cf9bffba875cfee86f9f724bebd34660dd9e27ecac60d9851e71a27a04b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6468367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d70f62d21064d862f8318e6bd59a19ce88bd0b3004354b9358b3b4eea9b13e9`

```dockerfile
```

-	Layers:
	-	`sha256:7fc5babc936b342270e28d08237973d5c6535b202e270ee01646c0812f84baa3`  
		Last Modified: Tue, 13 Feb 2024 14:36:10 GMT  
		Size: 6.4 MB (6424865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aa13b980720162c7d72417d17b0fa7f69fbc22dead2e4b9a2d621414f5110de`  
		Last Modified: Tue, 13 Feb 2024 14:36:09 GMT  
		Size: 43.5 KB (43502 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; s390x

```console
$ docker pull drupal@sha256:514a2a60ba5fd0d0f78b1c9dc7e30bdbfae6d86ad3c540b1f1fbcc7aefdea811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172803911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28884c1db4850b7a202037c780c5655ddf60e7972da16b044d8f89cf8e023cb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:58:51 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 22:58:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 01:17:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 01 Feb 2024 01:17:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 01 Feb 2024 01:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:18:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 01 Feb 2024 01:18:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 01 Feb 2024 01:22:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 01 Feb 2024 01:22:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 01 Feb 2024 01:23:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 01 Feb 2024 01:23:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 01 Feb 2024 01:23:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 01 Feb 2024 01:23:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:23:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 01 Feb 2024 01:23:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 01 Feb 2024 02:03:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Feb 2024 02:03:50 GMT
ENV PHP_VERSION=8.2.15
# Thu, 01 Feb 2024 02:03:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Thu, 01 Feb 2024 02:03:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Thu, 01 Feb 2024 02:03:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Feb 2024 02:04:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:06:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Feb 2024 02:06:36 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:06:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Feb 2024 02:06:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Feb 2024 02:06:36 GMT
STOPSIGNAL SIGWINCH
# Thu, 01 Feb 2024 02:06:36 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:06:37 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 02:06:37 GMT
EXPOSE 80
# Thu, 01 Feb 2024 02:06:37 GMT
CMD ["apache2-foreground"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fba508c7dad7497a6bbe373c417feff78e2fa3227a96337a55b59fcff9da5ae`  
		Last Modified: Thu, 01 Feb 2024 03:18:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59819a0dd4fd287d9e24157644eb1ff924fbb16ef9cf4e30d72908e1308d18a`  
		Last Modified: Thu, 01 Feb 2024 03:18:33 GMT  
		Size: 80.8 MB (80818276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdcf5b86b0e0f5aa0697cec9b64981a167285c1a2724d924a086a18d2918f20`  
		Last Modified: Thu, 01 Feb 2024 03:18:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ebd6cefe388bfe27d4a3bcf090a9de9f6c9aa33af40be2a2395ada6c5f097d`  
		Last Modified: Thu, 01 Feb 2024 03:18:58 GMT  
		Size: 20.1 MB (20084952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e4d9603325f9c8f157cc8090da6b4417fceb3c7a6a361860b8b52b4d64c9b`  
		Last Modified: Thu, 01 Feb 2024 03:18:56 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354950213319e1bb7f0f4e7adefdfafdf4e04ca12eb613e84acbaeadd3836a23`  
		Last Modified: Thu, 01 Feb 2024 03:18:56 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0102a161406a0521fca45d00343bd37d2d48b7194c66e781f50b683b261008`  
		Last Modified: Thu, 01 Feb 2024 03:21:40 GMT  
		Size: 12.4 MB (12408138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b8a30d53dae92b4ba19c3c334d8ff1ddf41cdc346a9ccd683060a546ebf7bd`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf3ba60882e47ed69aa7a680ac0026920e27ef8a56e54edce16c3a410bb1276`  
		Last Modified: Thu, 01 Feb 2024 03:21:39 GMT  
		Size: 10.5 MB (10450085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa51cd076b6bb332388f0c8ce8590fc455e1da472165a84176be54858a15ca1c`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e28100cd16736ce346da1727d5e46972524539e3119ad3b27c11e5115884582`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfb1c5076dcecc11fbc4c0174c55c7af4b87a17945cd2812db07815411518d2`  
		Last Modified: Thu, 01 Feb 2024 03:21:37 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ffcd5194ba9c4ffb855a2e55518002377b650702d667e3b523627780d7c30d`  
		Last Modified: Mon, 12 Feb 2024 22:54:26 GMT  
		Size: 1.6 MB (1554052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82ea90ade3cb9ded0a14a2bf0ec5fff48a46008be76dd91edece5e66658cb5e`  
		Last Modified: Mon, 12 Feb 2024 22:54:26 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aab33928c9f14c5114c41bd14a070458691f3ccf63913fe9b443b46f8b138bd`  
		Last Modified: Mon, 12 Feb 2024 22:54:26 GMT  
		Size: 721.6 KB (721586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee658d9995d43ccdc4fe949bbfce17c97bb9d9e8d27a4ec00cf82f4c1121fba4`  
		Last Modified: Mon, 12 Feb 2024 22:54:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774d90af6f682d07eefcefb9c8be1005bc61c4496a3071195adfb0db1466ad5b`  
		Last Modified: Mon, 12 Feb 2024 22:54:27 GMT  
		Size: 19.2 MB (19247351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:be9c3384de3fd5b6941a8f3efd27bf7a928d8e1539a705bb6e83703f4bf5d908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6348195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dc97b506bff9738c261ab6ffb2e2e7f6fc95c0649fd21a921d1f19284635d5`

```dockerfile
```

-	Layers:
	-	`sha256:2e6a5714e811ef1c5b63c9e5c405f2899f0f4e8f0f3ccab481e3bccec70cdd14`  
		Last Modified: Mon, 12 Feb 2024 22:54:26 GMT  
		Size: 6.3 MB (6304864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e0c8b86a70d7b60e4594181ea30baeea2701acb6392f99a9e8f45b440b4505`  
		Last Modified: Mon, 12 Feb 2024 22:54:26 GMT  
		Size: 43.3 KB (43331 bytes)  
		MIME: application/vnd.in-toto+json
