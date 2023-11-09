## `drupal:9-php8.2`

```console
$ docker pull drupal@sha256:9c1a930411f5eab5cd81a249e337a618e96c97fe3345f83dd09bd7db3e065c28
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

### `drupal:9-php8.2` - linux; amd64

```console
$ docker pull drupal@sha256:6cccc4e5b2a81a0dfc04d662200cbe8bebea68820819d51cd74095b9a2108b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203210723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25550772fb383eeb485f5a1168feeb0a8824d4859ccab291e2e64ebd0a380a7d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 22:07:44 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 22:07:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 22:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_VERSION=8.2.12
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.12.tar.xz.asc
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_SHA256=e1526e400bce9f9f9f774603cfac6b72b5e8f89fa66971ebc3cc4e5964083132
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 22:07:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 22:07:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 22:07:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
EXPOSE 80
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV DRUPAL_VERSION=9.5.11
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /opt/drupal
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053f6f43c122d10a9ed41f0b4fee4f12737d55a220a275d58bd89a57754e3fb`  
		Last Modified: Wed, 01 Nov 2023 07:10:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cebbf4d847e8ee87513e58c95b420844aff691e0d07e4a6d76246c9e0c685d`  
		Last Modified: Wed, 01 Nov 2023 07:10:24 GMT  
		Size: 104.4 MB (104353572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34045bc939601f7e76df95a46ca7bf42e99dcdb879b149a6c705a8924a707d9a`  
		Last Modified: Wed, 01 Nov 2023 07:10:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da31f94fbeef57a5035b3f90c4128531c28059dc206c1ede76a6bdbea6089c8a`  
		Last Modified: Wed, 01 Nov 2023 07:10:53 GMT  
		Size: 20.3 MB (20305084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c755cb948935c20aca0d800bd380ee8d1f6a354a22ebe9bcc932a77fd647e022`  
		Last Modified: Wed, 01 Nov 2023 07:10:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47863fce0cd3df8ca85ef1300f854bd99373bd00d3a30be040e074a7cd1fb7b3`  
		Last Modified: Wed, 01 Nov 2023 07:10:49 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a5ef80cfbe92612488bab2cdda1322071f3052549ea48c39ba9b9d690d5466`  
		Last Modified: Wed, 01 Nov 2023 07:13:45 GMT  
		Size: 12.4 MB (12383955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d0b71510d8df982c6cedae4a4705d4523cfcc84995d2e06ab0e4f270136785`  
		Last Modified: Wed, 01 Nov 2023 07:13:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbb724fde8514946ff319d6312569c1c3897e3fc057590acebde708267d3d70`  
		Last Modified: Wed, 01 Nov 2023 07:13:43 GMT  
		Size: 11.4 MB (11431814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf0df499623a6de569c2345d662adb40757d2143cf166d7b46bfc08d712a1d`  
		Last Modified: Wed, 01 Nov 2023 07:13:42 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4393adcb56390b1224646c878852fd06e0dc80ef4b424d8e61ef40ce77599dc9`  
		Last Modified: Wed, 01 Nov 2023 07:13:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c926c0a40b480ff3e6675b35673bfc073aa1532f541b823ab72b9e0ca6a257ac`  
		Last Modified: Wed, 01 Nov 2023 07:13:42 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff05df8160fde763256035a33c381b0206f9ade091b5d353f5d0a9557754a39`  
		Last Modified: Wed, 08 Nov 2023 20:26:31 GMT  
		Size: 2.0 MB (1996951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c002013aebdcd116569f577f320e7440369fd388513820ace7256d4906a147`  
		Last Modified: Wed, 08 Nov 2023 20:26:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049efe98af4251752b305cf8fa10151467120172b04854e441b259ceba21ab7d`  
		Last Modified: Wed, 08 Nov 2023 20:26:31 GMT  
		Size: 705.0 KB (705009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbd8dbcf35775c83690376fcd7973a64232be71b4688d25155341059b323534`  
		Last Modified: Wed, 08 Nov 2023 20:26:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104cf7f05e3d53123dc7b62d74ed9034c19f1dea728631bcff94c978ede57dba`  
		Last Modified: Wed, 08 Nov 2023 20:26:34 GMT  
		Size: 22.9 MB (22878487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:9-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:717b2dde18cd760cbab2a7d4dcde8a62f09c7154b412b56fbf0dbe43479adf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5954615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c71afdb6827d7a88dec29e5b4a228f121b26b2c6cb72e0652b0be2ae4b5cae`

```dockerfile
```

-	Layers:
	-	`sha256:981da33f5635e1eed41a1e984b958bc308ec183601ec16609ed469d096e0cd46`  
		Last Modified: Wed, 08 Nov 2023 20:26:31 GMT  
		Size: 5.9 MB (5913938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e67fc7895cbeb43486edd76d4cd34d05c49ec36516b9b849ac3e8918a5b041`  
		Last Modified: Wed, 08 Nov 2023 20:26:31 GMT  
		Size: 40.7 KB (40677 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:9-php8.2` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f3b8d201cb71df62800161b98c8e74923390904657610a7a5bc1ea111aa3e2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167192553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a26bf39d3e9e4c588badfeccc751d84dd1ccccc31eb261b3b4ddda6a9413bf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 22:07:44 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 22:07:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 22:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_VERSION=8.2.12
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.12.tar.xz.asc
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_SHA256=e1526e400bce9f9f9f774603cfac6b72b5e8f89fa66971ebc3cc4e5964083132
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 22:07:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 22:07:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 22:07:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
EXPOSE 80
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV DRUPAL_VERSION=9.5.11
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /opt/drupal
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59be9e284034d86ac38a94e851d999a8112b2981519e9ed43accdd42ea745b1`  
		Last Modified: Wed, 01 Nov 2023 14:26:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f819d872da6fd4c3abad62cb8f0e6f6ca3ef25dd1c5f9ecd790c7425416de028`  
		Last Modified: Wed, 01 Nov 2023 14:27:05 GMT  
		Size: 76.2 MB (76225678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2375ec6f596fcb0f8e9129d3ec03d7fb09ff1452cd48d5362413ed8fd146004c`  
		Last Modified: Wed, 01 Nov 2023 14:26:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18abaff3e43b1ae4164338bf14ac450d805fb5fb4c17c7603ceb956b15d2e9`  
		Last Modified: Wed, 01 Nov 2023 14:27:34 GMT  
		Size: 19.0 MB (19046556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9850741c09988073912d6a34bf642c5920e2e90e97e3c14209d755b42587906f`  
		Last Modified: Wed, 01 Nov 2023 14:27:31 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebca3b2280935675a7b6f5cd190ea980f8ef8c34a0691345d218e3668106dedd`  
		Last Modified: Wed, 01 Nov 2023 14:27:31 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ddc761e174676b622e6dafdf6e93b74af00e8d93b532697c3d57e67aa9bc90`  
		Last Modified: Wed, 01 Nov 2023 14:30:31 GMT  
		Size: 12.4 MB (12381739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d97572de22cfa2510b0c834176f5fa41bf9fe1582e632d139f3e6fb2974e4f1`  
		Last Modified: Wed, 01 Nov 2023 14:30:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f658c8456d8869320f78bf8c30896023aa9687fa42077ddab224b824feba2be`  
		Last Modified: Wed, 01 Nov 2023 14:30:30 GMT  
		Size: 9.8 MB (9845718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd8bbd59985ed4a1c487ddc3a4bfcb5c1125ca9372ee9dd6bc4ba56733b46c1`  
		Last Modified: Wed, 01 Nov 2023 14:30:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cff3c3803deabf6be3a74d3fc622bee1ae57f99d2d701d91fa59235fd9a7cd4`  
		Last Modified: Wed, 01 Nov 2023 14:30:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a52d94d5fd7a14c0b563468a6d16ec608769d6f41e1bd64bd2afa9b1c5ca8b`  
		Last Modified: Wed, 01 Nov 2023 14:30:27 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330a4a358f1ed12d106146f4ebebc4de7594141454af6f260d35b2da07ed801e`  
		Last Modified: Wed, 08 Nov 2023 20:33:43 GMT  
		Size: 1.4 MB (1353832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21402cd7382d47c4a6bee021590fe711f8781cbd3327ea218c68e40d25779e4c`  
		Last Modified: Wed, 08 Nov 2023 20:33:43 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4874cbca682bb3ce586ed44ba7b52b68db9df9297bf6694a5ecec4b9e03893`  
		Last Modified: Wed, 08 Nov 2023 20:33:44 GMT  
		Size: 705.0 KB (705007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7476250772523a0d639027acd74fcf5efea302098eb537758fdf8d1032f35c8`  
		Last Modified: Wed, 08 Nov 2023 20:33:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc94b6ae0ca05a428c7ad9e469e7e7aee65255c130cf9d6b69a2bb5df09868f0`  
		Last Modified: Wed, 08 Nov 2023 20:59:02 GMT  
		Size: 22.9 MB (22879120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:9-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:08bf4a3b275687d598d4b088d0f45c405890bfdf53a6358727846279e5851160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb6c8294598c37da7a79f9a4a5cbd626e408bdcd970979363e859f61e1f51db`

```dockerfile
```

-	Layers:
	-	`sha256:5c82cbe329a3ced78a169a93e198d68a30e3ae59b5b1c69cb6fbd3881543fb99`  
		Last Modified: Wed, 08 Nov 2023 20:58:59 GMT  
		Size: 5.8 MB (5753581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5841cec1cae7978f0329916641952d5e20e54ef0bd7fdbaa0149b39a252eb6`  
		Last Modified: Wed, 08 Nov 2023 20:58:58 GMT  
		Size: 36.4 KB (36435 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:9-php8.2` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:749b79537196b080d0278f51fb929cd896c626cb3a3d65889530598c39d36f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197283149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ce1aa9bd5d249845c69b22262924ea09dfdae1101851f739b4980bf5760bd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 22:07:44 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 22:07:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 22:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_VERSION=8.2.12
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.12.tar.xz.asc
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_SHA256=e1526e400bce9f9f9f774603cfac6b72b5e8f89fa66971ebc3cc4e5964083132
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 22:07:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 22:07:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 22:07:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
EXPOSE 80
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV DRUPAL_VERSION=9.5.11
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /opt/drupal
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a1d4347681dafacc4fd7807e0fd4250100fd23d88a3a5bb93ba9de6ebfa853`  
		Last Modified: Wed, 01 Nov 2023 13:32:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c9f838d23f8118bfd5cbaf969e6781ce721288fdbf4811d4613b8c94a0acb`  
		Last Modified: Wed, 01 Nov 2023 13:33:10 GMT  
		Size: 98.1 MB (98131824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb23c56d5c248ab07de2c65e6805408398ad24b9e7f68b76a772fd923a541f0`  
		Last Modified: Wed, 01 Nov 2023 13:32:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d3602892ec55ef6fa41b79e63f381805cacfdd794280d67a0b4babd0bec43b`  
		Last Modified: Wed, 01 Nov 2023 13:33:38 GMT  
		Size: 20.3 MB (20306772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339958c8b19db06ee2019751c64cb419ac60d5e696023999e381ac3d84a8511f`  
		Last Modified: Wed, 01 Nov 2023 13:33:36 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663bea60fafb0c6c43b3bf486910e7685edaa95e7b4794a8b5f952cc546ca561`  
		Last Modified: Wed, 01 Nov 2023 13:33:36 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c8c40d92731fe9bbc9c766e20842a07779d52fd14a045756620a9862ebd25a`  
		Last Modified: Wed, 01 Nov 2023 13:36:26 GMT  
		Size: 12.4 MB (12383590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578de21b35da228ae89c8021e1f70562c2c0dd06db7fff821a6ed0130b87e039`  
		Last Modified: Wed, 01 Nov 2023 13:36:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0d18fbe0d585938f57091bb1ec2014cd2feb04eefcccc6f6a4dd74f99b4a5`  
		Last Modified: Wed, 01 Nov 2023 13:36:24 GMT  
		Size: 11.4 MB (11437437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0bd6e2c0b0ba18ea4544d636013887e7e598599c66bd5bc1458811b40062a8`  
		Last Modified: Wed, 01 Nov 2023 13:36:23 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0765cf432f51cda8d1f53c97027d48fe6d6446173041684d0fd8440127560c0`  
		Last Modified: Wed, 01 Nov 2023 13:36:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee43e6cfd2216da55f68717de496a15678cd226c8abf05a02d8b1ec22519c611`  
		Last Modified: Wed, 01 Nov 2023 13:36:22 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3683a1f1d030df02cdf1aec16db310ee66f25b49b9c9eaf5275318d838af062`  
		Last Modified: Wed, 08 Nov 2023 20:52:28 GMT  
		Size: 2.3 MB (2253949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b0708300444e42ec4595d2474532fb43a1de9a6d7b89f28836a9ba012743e`  
		Last Modified: Wed, 08 Nov 2023 20:52:28 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3592209440ec6db7b1876095329806ad29155df71b81b9a950b8fcd4ccee12e`  
		Last Modified: Wed, 08 Nov 2023 20:52:29 GMT  
		Size: 705.0 KB (705008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210bce6d06e5fc2c4e30e40c593827184f618c6ccc310d085a609be3ed297fe9`  
		Last Modified: Wed, 08 Nov 2023 20:52:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4168d03150f141ca06b60b92b27dfee7660af50f036c82b77863733427cfb2cb`  
		Last Modified: Wed, 08 Nov 2023 21:39:41 GMT  
		Size: 22.9 MB (22879435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:9-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:2b7c299eb2d7312492ee0c913b89878dd60b8b54bc1c80dd7e8fda07aa94e126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54ee1fdf5a7746812942716402fb951af9376cdede509694e0a81d3585f19d`

```dockerfile
```

-	Layers:
	-	`sha256:78d01aab9e077f3bc0db539919bd3723f2f40f52ab20fb39ad682261750a362e`  
		Last Modified: Wed, 08 Nov 2023 21:39:39 GMT  
		Size: 5.9 MB (5938955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade3cd72badae2460ddd15075dbcbe6f11752287e26b21bce03ac4411f73a9ec`  
		Last Modified: Wed, 08 Nov 2023 21:39:38 GMT  
		Size: 36.3 KB (36308 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:9-php8.2` - linux; 386

```console
$ docker pull drupal@sha256:dec3fac0c149b6f2644d8ee26be40e1604adbdf73fe48efea02ea8bc02629443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202208968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c67a88ce2c4f8b30f72bbac97d829fb1967b8020bac6b03311139cb6fc7cea`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 22:07:44 GMT
ADD file:0c94521fdd9c0a4fdeeb9aad23e68cd053fba0dcd7c3af550aefa79377816e31 in / 
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 22:07:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 22:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_VERSION=8.2.12
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.12.tar.xz.asc
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_SHA256=e1526e400bce9f9f9f774603cfac6b72b5e8f89fa66971ebc3cc4e5964083132
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 22:07:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 22:07:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 22:07:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
EXPOSE 80
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV DRUPAL_VERSION=9.5.11
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /opt/drupal
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:98bdfce9af831c2a0d0bfcca812d0039cd1666986550f552b4b4c625bd5aa31c`  
		Last Modified: Wed, 01 Nov 2023 00:43:26 GMT  
		Size: 30.2 MB (30164042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3eaf1aecfb03c29cd0e5dc1ffbb067aa9f508574afba6695a026da3e199ad`  
		Last Modified: Wed, 01 Nov 2023 04:23:32 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c175ffb8b9413a37c9b489b7f83d2390868a05059afc258494d5af78e1b7647e`  
		Last Modified: Wed, 01 Nov 2023 04:23:55 GMT  
		Size: 101.5 MB (101532383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91b69c37dae718c719e57d3c1921435873a7f2090b92730c4c12a2cf19fa963`  
		Last Modified: Wed, 01 Nov 2023 04:23:32 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1e86618e905ad9e7a4b0fbb6154fc10ee39c6b4e4ffb5ae8e7e8c1cc9f0022`  
		Last Modified: Wed, 01 Nov 2023 04:24:27 GMT  
		Size: 20.8 MB (20826860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee47d31c6c00f6809f7e2513a4bc2f06d5539f25d70aeaa8f7b02140a79312ea`  
		Last Modified: Wed, 01 Nov 2023 04:24:22 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ec57bfff647f3ff0a2cf495fb87b134656c416ffa0335f2c16f01e6bf7134d`  
		Last Modified: Wed, 01 Nov 2023 04:24:22 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a0001fc011201c959eecc21080fc666e1b0e51e07430db8f3e776cdcf8630f`  
		Last Modified: Wed, 01 Nov 2023 04:27:46 GMT  
		Size: 12.4 MB (12382866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64e8a3b3eb7da4b9dabf414d401fc1b20e62907f4fb41ee2660efda2bec52ce`  
		Last Modified: Wed, 01 Nov 2023 04:27:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56b46ff0a4a74c39eb4487565ed9501d1b5e0914c8125b4e6673cf0d2f1a273`  
		Last Modified: Wed, 01 Nov 2023 04:27:46 GMT  
		Size: 11.7 MB (11664196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29b24e5dc3ceef3a563991ae343c8d570287ef023fa16bf72e5ac48dcfc5afd`  
		Last Modified: Wed, 01 Nov 2023 04:27:43 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35298df5edd8cf78fd85c52f8c7a05b1077c833432029041c966fb6ad507b17c`  
		Last Modified: Wed, 01 Nov 2023 04:27:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ee5a52615d3016a31bf26480858ab98b50b712ba3bbec775f5e117a055ad3`  
		Last Modified: Wed, 01 Nov 2023 04:27:43 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f20e81d992626a0e362b79de774634ef37f1c21e7ebf100b4ba869b121de2`  
		Last Modified: Wed, 08 Nov 2023 20:26:22 GMT  
		Size: 2.0 MB (2049178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c201ae3f6f8ef160d37f53a4e06c364d8deb4d2d7f9dc241e6e5a4bab36bbd5c`  
		Last Modified: Wed, 08 Nov 2023 20:26:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d940e6286979b1a298da5250f3451eddbcad266e3a6bbd137e3f0fc699af17`  
		Last Modified: Wed, 08 Nov 2023 20:26:22 GMT  
		Size: 705.0 KB (705010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8464576f31745916f99220953c62b30a8678eeeee8453691bc5f971a1ebd1c`  
		Last Modified: Wed, 08 Nov 2023 20:26:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f53c890ef1e9627028aab6bd394e53fd7f7151814efbf1be81121ac3b494c36`  
		Last Modified: Wed, 08 Nov 2023 20:26:25 GMT  
		Size: 22.9 MB (22878423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:9-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:f7bbacbb9fbfa9f38c38e8798f5c850415c4f94cfd2ce46e70a8c0fbd859ba08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 KB (40400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b56fd93cffed976841fcb1ea692fc073150aeaa658475e45e8902136702e38`

```dockerfile
```

-	Layers:
	-	`sha256:67a19f3988f442bedeab17b55c1c99a761c44188d583599839ea59349b6f2506`  
		Last Modified: Wed, 08 Nov 2023 20:26:21 GMT  
		Size: 40.4 KB (40400 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:9-php8.2` - linux; ppc64le

```console
$ docker pull drupal@sha256:8010164d577ae7f487794ce8fc053775d951598363869be47690aa1a533289c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207626921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcddfdca14f70e82404aaeb86519c18f26bbeba923a9682f995e7b5002d5e251`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 22:07:44 GMT
ADD file:f36d600ab8508979b5763875a75f35555fa0a83d2656cbcdfa50978c6ae97353 in / 
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 22:07:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 22:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_VERSION=8.2.12
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.12.tar.xz.asc
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_SHA256=e1526e400bce9f9f9f774603cfac6b72b5e8f89fa66971ebc3cc4e5964083132
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 22:07:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 22:07:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 22:07:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
EXPOSE 80
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV DRUPAL_VERSION=9.5.11
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /opt/drupal
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e56c8f20d7d119ff87eb044f21bfd5a4b30bf8436fc5fac12871095a6bd1517c`  
		Last Modified: Wed, 01 Nov 2023 00:26:10 GMT  
		Size: 33.1 MB (33141482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb7b50c4cec9d8b3ee3151f113d0850c38d425f2639a138998aff22db608fac`  
		Last Modified: Wed, 01 Nov 2023 13:33:59 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968d29dbdb5dd47033622464c3cbf5e5596c763ada6b126f0ed7b0ec2afeb267`  
		Last Modified: Wed, 01 Nov 2023 13:34:17 GMT  
		Size: 103.3 MB (103321469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478e8d8d847bcc715ab4bd09f60dc99a221fa87763dd700c618de14e6bef737`  
		Last Modified: Wed, 01 Nov 2023 13:33:59 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143f8e1485bd91cf3953173702e97444c71d3a99b5a6f1cb1706b65403b838c`  
		Last Modified: Wed, 01 Nov 2023 13:34:54 GMT  
		Size: 21.5 MB (21490272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6099c7ede4a09559d335e5803c512e1112dba09d5cb63a7c802337f1a49807eb`  
		Last Modified: Wed, 01 Nov 2023 13:34:46 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d81833d78283a8af447ef46394e1ce7c82b3441ca52363b242640514de8788`  
		Last Modified: Wed, 01 Nov 2023 13:34:46 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d479d159d0304b1e504d56d85cc180384414d33aa47fea4de1b661fa51b5cb`  
		Last Modified: Wed, 01 Nov 2023 13:38:09 GMT  
		Size: 12.4 MB (12383164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c5a371675a38c36f2a59b62940d612bf11aef6660731a7037767a9582b425`  
		Last Modified: Wed, 01 Nov 2023 13:38:05 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d69c4ab5e9e3de6bdb51820efb996a44c39a3254c56eb55b721929dde30af`  
		Last Modified: Wed, 01 Nov 2023 13:38:08 GMT  
		Size: 11.8 MB (11845411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09de39ec027142b04d1e8b4fd00ce8f637bdfdd46a9255f12a18a4575509a85`  
		Last Modified: Wed, 01 Nov 2023 13:38:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22b60ce71d6aa548ab6a734eb409d6b35254a7f70f104c40a37b1a93b765ed5`  
		Last Modified: Wed, 01 Nov 2023 13:38:06 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4cfceaa54e63efb66cfa2d6594fdb8f6982799ae9dff72c6e0c06b136693d1`  
		Last Modified: Wed, 01 Nov 2023 13:38:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c48b9d6e091f819a456b6e506ad4c18323c8479fb409091a36d3040fefd5c5`  
		Last Modified: Wed, 08 Nov 2023 20:36:49 GMT  
		Size: 1.9 MB (1855440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f795352e72c0c6d597d33b20e1046dc344e33e6746fb265fdfa3600a18fd38a`  
		Last Modified: Wed, 08 Nov 2023 20:36:49 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f58b5a7c484b6fb2830361b39763dd2ad4ad17e47a738ea5d9c19e58fe831d`  
		Last Modified: Wed, 08 Nov 2023 20:36:50 GMT  
		Size: 705.0 KB (705006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f247130d5c503d8d1581ca1b4a6244ac434e7b8e72b14852a2872728404d90`  
		Last Modified: Wed, 08 Nov 2023 20:36:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e44e0af056a9b2accad5ecbdd6b3dec0ead2dfb4ae1da94be48bf4b9a4fecc`  
		Last Modified: Wed, 08 Nov 2023 21:12:41 GMT  
		Size: 22.9 MB (22878671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:9-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:dbf0626ede75210c2104fb98855862fd7ac3c2be6ec3e580b21bebb34d80bea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5931665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3339a508724a356cb1e03740d7bbaa1d42c7d4368dc823f2b959c2834fb003ac`

```dockerfile
```

-	Layers:
	-	`sha256:cd16d85409bf50ad8634a145f84cc3f490bb0f2e9624d1c9bc40366c5e4b5630`  
		Last Modified: Wed, 08 Nov 2023 21:12:37 GMT  
		Size: 5.9 MB (5895295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915b43fff8866d20df9e8d16c2e17c35472ce49e721de2700802c1ee42991850`  
		Last Modified: Wed, 08 Nov 2023 21:12:36 GMT  
		Size: 36.4 KB (36370 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:9-php8.2` - linux; s390x

```console
$ docker pull drupal@sha256:f9cb29c8d69cf94cb1f048ded2cc18b1f3bc7813d794a89dabdb93a1db872977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176423905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33202d2b2f792783f72f95905d1f7b8f4db11d7df8a8caef394fd5301cf4d21`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 22:07:44 GMT
ADD file:2764e93c5bba50564937cce7bcaa7c7d3bdc3fd0d53a7bb09e6955e6fda8d7c2 in / 
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 22:07:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 22:07:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 22:07:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_VERSION=8.2.12
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.12.tar.xz.asc
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PHP_SHA256=e1526e400bce9f9f9f774603cfac6b72b5e8f89fa66971ebc3cc4e5964083132
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 22:07:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 22:07:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 22:07:44 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 22:07:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 22:07:44 GMT
EXPOSE 80
# Wed, 20 Sep 2023 22:07:44 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV DRUPAL_VERSION=9.5.11
# Wed, 20 Sep 2023 22:07:44 GMT
WORKDIR /opt/drupal
# Wed, 20 Sep 2023 22:07:44 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Sep 2023 22:07:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ac72f5406002214602d5a625a21b606af78a78e99e377d3140a83021f7edd666`  
		Last Modified: Wed, 01 Nov 2023 00:48:04 GMT  
		Size: 27.5 MB (27512766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54135d8976184e19a2569172c7c79dc6befeedf2c784e00866cfe8dec03e7711`  
		Last Modified: Wed, 01 Nov 2023 08:23:33 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b969a0a7ebbecf571ec12c4173870ac90683ba053048cec911dbd6620d8c4`  
		Last Modified: Wed, 01 Nov 2023 08:23:45 GMT  
		Size: 80.8 MB (80819510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a91eacd7477a3a5a47ac5e25912035a19b77ff3dabc01f6b2c9688591d74846`  
		Last Modified: Wed, 01 Nov 2023 08:23:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d890e8f265fe8e487dcd13d88a3a78a5795aeb22078a5aa1ca183f9e472343`  
		Last Modified: Wed, 01 Nov 2023 08:24:05 GMT  
		Size: 20.1 MB (20084755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f653517f54d6b5a016cdedd28fb52ced5c6416b56815cb06c23c5e144e38dc8c`  
		Last Modified: Wed, 01 Nov 2023 08:24:02 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296aac3478f39a2f5f28ad0b8a7cdd3a11bbe4a5c874ac0d6f758f1b06175125`  
		Last Modified: Wed, 01 Nov 2023 08:24:02 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5be3ce040a33a3a42542245d11a8db5eb1ce6e3be30b8673a8e8645ee44f09b`  
		Last Modified: Wed, 01 Nov 2023 08:26:26 GMT  
		Size: 12.4 MB (12382079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f30b52d521b70481626cd359db46250b65e86558ea51742e4bdb0f8cc702a`  
		Last Modified: Wed, 01 Nov 2023 08:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9800d6a5ea3edb02261291cb0aaf447531376608c1e7d56c2294c8b0c049ba7d`  
		Last Modified: Wed, 01 Nov 2023 08:26:25 GMT  
		Size: 10.5 MB (10480731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa698a456a8031c55ffba03f96d3ae8ca2fd02a336c226d20225001ee23aad3`  
		Last Modified: Wed, 01 Nov 2023 08:26:23 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1acff9693ac90558eed3dd4f87887f1515ee6bdba30666a79f1e63eb887322`  
		Last Modified: Wed, 01 Nov 2023 08:26:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a243a19a799de0b87c7e6c3dd45e7a0635eccc318da803d13e1584904bf1b3`  
		Last Modified: Wed, 01 Nov 2023 08:26:23 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026ef47488c77a2fe4a2d5c3aaedc6bb54d77eb254c4292113acf23fbe27673c`  
		Last Modified: Wed, 08 Nov 2023 20:31:11 GMT  
		Size: 1.6 MB (1554110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfe867afd18a8c57b76b9d05a57c9eeb0fbbaccd6aad93ff6884878d1820ae7`  
		Last Modified: Wed, 08 Nov 2023 20:31:11 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b04017d7c943fd8877a747eb067ce5a99c5aac154bb3c0cd6fbe41c59230b7`  
		Last Modified: Wed, 08 Nov 2023 20:31:11 GMT  
		Size: 705.0 KB (705008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e850e1fa3742f6056ebdb8db8c14fc6efae9b179d4a2878ec811c2f5bd4db78e`  
		Last Modified: Wed, 08 Nov 2023 20:31:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbbea85533148dfbfd8f2aabeb5ed328d13b32cbe3033ec29e38e4c0f90b2e6`  
		Last Modified: Wed, 08 Nov 2023 20:57:30 GMT  
		Size: 22.9 MB (22878942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:9-php8.2` - unknown; unknown

```console
$ docker pull drupal@sha256:87041a2cdeeedc9f65cd26cd9d24267fcd5d112301aef65b92e10a8a047dbe14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5811728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04529dbd81249beb6712b56848dc8b6b900b6ecacac358fa96a36ec7399b73ba`

```dockerfile
```

-	Layers:
	-	`sha256:a7300b1e8b92ebdb96753d36538a86f16c3a9f45c3b14861bdf7de85ae296427`  
		Last Modified: Wed, 08 Nov 2023 20:57:28 GMT  
		Size: 5.8 MB (5775440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791fe91bebd766d0992f5d8ed65c6d23828a2473b1066a7e2228c662895caba4`  
		Last Modified: Wed, 08 Nov 2023 20:57:28 GMT  
		Size: 36.3 KB (36288 bytes)  
		MIME: application/vnd.in-toto+json
