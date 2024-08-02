## `drupal:apache`

```console
$ docker pull drupal@sha256:483796e5220bc5c3e590fc016d83b3ebb13f5841bfac0d842827b65edf31b47f
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
$ docker pull drupal@sha256:27b991f4fb71f028a0b2fb638656a3448ae371373e05b7951b385f232fa741e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201452543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced309296f411d0b4605b25b34fb55917694b6ff2a2503304484a985d2d8a816`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 04 Jul 2024 15:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 80
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a83fa76a2b6c79f2ceb6a3ac1d705844e9f1b13544b372353738d852317d8a`  
		Last Modified: Tue, 23 Jul 2024 09:35:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3cd9e6b429af5419fe7f9a9d1ebd1b80eec307fb1eb50d85e9ce901775300`  
		Last Modified: Tue, 23 Jul 2024 09:35:51 GMT  
		Size: 104.3 MB (104349191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41714dd6e6a02a12b553a69607d296b4acfe06ebfd34170e47f89ce43f2fd09`  
		Last Modified: Tue, 23 Jul 2024 09:35:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e362d14d0b88a76a0df065fd31bfc25b16f4f2afc88ecb30273c08bd21d1ab60`  
		Last Modified: Tue, 23 Jul 2024 09:36:16 GMT  
		Size: 20.3 MB (20327898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b475c73fa4cd4c57941308b5448392792620bdb6654ebde07c1856ea462830`  
		Last Modified: Tue, 23 Jul 2024 09:36:12 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1c872d3db8284d29f89158d5ecb0ff14ebbc08e78834d499468496a1232bd9`  
		Last Modified: Tue, 23 Jul 2024 09:36:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97876285719a3926791dae6daf617f442ad6ebd72bb6aadcd6e75a057763ceb4`  
		Last Modified: Thu, 01 Aug 2024 22:24:35 GMT  
		Size: 12.4 MB (12433177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fb4d37a6c21f19658c9b8cc1982937978535910681835832fbaaf18b589681`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35e4747e8da8a8a230df17fac175b1ca1e8fb00ee40e7bd2f15b2e22788bd72`  
		Last Modified: Thu, 01 Aug 2024 22:24:34 GMT  
		Size: 11.4 MB (11404388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdab7abc93847315c1bae86b3fff17e155d13c34e0bf39d8a2ae70fbcd7ac4d6`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d1509706696990e5b9e9a56a46b6b6271be377112ec6f5a2a31d0c46f60c11`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096b0161e32fdfd3684d3735197d451eac28ea855cde552dbafe1f1167c97d1e`  
		Last Modified: Thu, 01 Aug 2024 22:24:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9386a61cd0793a340341dd3e9bf8154f8e2d835fcf4d947bd4453f7a1adb9cde`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 2.0 MB (1996795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8985b282337db9d2dfeb47f51669f8ce81fda6d10021dba5beae10dcb6f79d7`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52d9a19cb2ecc79181e37c37d76cfd686d32d8be20cf08e6c2e01b92b3c913c`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 726.3 KB (726342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caa48ba54751ad7c6d961ecae3716f2164d6dd78703a4783e29c2e10ab97283`  
		Last Modified: Fri, 02 Aug 2024 14:54:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb992628818a48b9f56f9288da382f1145d71648de5f14204aed19fffcf3c3cf`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 21.1 MB (21082574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:2d8b08f4137e7475aba5b40a0543345cc53e82713aeef613cb9b8d4cf0543fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6880015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4df5f2c309bc12e80d24559e747d010c2ec56d9cc243a82075904488b8fadcd`

```dockerfile
```

-	Layers:
	-	`sha256:2ff127cbd0030178d363211cc38d6eb0a99f04d46e60bb22d52fbbfc6f850e27`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 6.8 MB (6838053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042ef727fe95a5384393615085728858b17cf5c3f22d94ae04c35e3f92a23858`  
		Last Modified: Fri, 02 Aug 2024 14:54:55 GMT  
		Size: 42.0 KB (41962 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:0eb3d8540ee7b07d1b73f9fe6e794b2fb480c606c01261f22f1f8a3d92822d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165367470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0f1f87e0c72dcda8a148859560974ccd6f42bcd1dbce19ba49abd8777e2529`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 04 Jul 2024 15:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 80
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d3ec06c5e0e90071038fdee9232ba4133360411125844bff1e22a52304e3c5`  
		Last Modified: Tue, 23 Jul 2024 08:33:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd846de240ae9bfefaac5899b068df5455a7f31a27e33777e570ad4672b5f483`  
		Last Modified: Tue, 23 Jul 2024 08:33:38 GMT  
		Size: 76.2 MB (76166096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ba38eb3f2eb6eb3d8dc7fb73ec6839277b5fa128f0e76530300b9b2c7ea11b`  
		Last Modified: Tue, 23 Jul 2024 08:33:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d3a944b3fc7ab92bd394ccbe902f5a1849f8040bc6b87bb71c55a597806ad4`  
		Last Modified: Tue, 23 Jul 2024 08:34:04 GMT  
		Size: 19.1 MB (19062695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074c49465f19a38077840c8da574714fb625678c76cd49a611c4baf44c5b8da2`  
		Last Modified: Tue, 23 Jul 2024 08:33:59 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563d18616929af33d314b6f921c8aebd71dcf275575b6ac1bf44317795ff3d83`  
		Last Modified: Tue, 23 Jul 2024 08:33:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6974b4d6b3ce5aa536ab97f47b866d6236919d6e14d700c04948aeb92ab3a49d`  
		Last Modified: Thu, 01 Aug 2024 22:45:36 GMT  
		Size: 12.4 MB (12430923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd695692fb928af41d52b8d10a1c7db2ebd2b91ee498f2f528ab20615e5b87a`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00b386f4be24366cac12f857922bda09e317afc726794d08751ae34ab7f6cc3`  
		Last Modified: Thu, 01 Aug 2024 22:45:36 GMT  
		Size: 9.8 MB (9821208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50f3abd5887bf2342b87de8e5f972208175961d9ebd3f158857481caa94dd8`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd37c8754f0cc3db455ee6cc34ae9b0bc46167ea392edfd0d6889b0139484503`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf67375f400392804df9d50f3b046491c521731b84233bb2349e1ae45dc8139`  
		Last Modified: Thu, 01 Aug 2024 22:45:33 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f90c298725d37d740829887cc6c94030b61be9ebd6bb86eb12bacd83f9238`  
		Last Modified: Fri, 02 Aug 2024 00:50:14 GMT  
		Size: 1.4 MB (1352960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29faf82c3152e0df28e5504d464b5450e375ed3eb4b795e041b0144d6f7df9ce`  
		Last Modified: Fri, 02 Aug 2024 00:50:14 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1950c3788be291ff3aecdba43a2847cce6bf12e842b21aa742efca2617dea5d8`  
		Last Modified: Fri, 02 Aug 2024 02:48:10 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c153651c46e21b7d0ce1810912b9ae8c196867db36f395722a4d5182af37f2`  
		Last Modified: Fri, 02 Aug 2024 02:48:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8d336dc18987742652b1fc586d317868db12e92090f09ef918f7de66977995`  
		Last Modified: Fri, 02 Aug 2024 02:57:49 GMT  
		Size: 21.1 MB (21083141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:732b5f70ee40178f48392f5759f63a9998feede7fb682f8ddae9da72be10dab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6695852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb5c5061f7437dbcf6efb5177674e71eac2a6e5ab8bed2ea1987f26495a3492`

```dockerfile
```

-	Layers:
	-	`sha256:ceb8b55e90d8ae3a52655904a7ea7570c886a649545e8e95e7be9ab05fec8d1b`  
		Last Modified: Fri, 02 Aug 2024 02:57:48 GMT  
		Size: 6.7 MB (6653569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327035eb7868c6194cffd018fefd4394e4941383a7babe98395bb988d2c8f277`  
		Last Modified: Fri, 02 Aug 2024 02:57:47 GMT  
		Size: 42.3 KB (42283 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:0465a9f68766cfdbe2390ce6d2099bc7daac4972f17b6a0695050601b53dcb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195529743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a7c1c0dbe1578075556ba5b6d3f2e040623597c9a2745654d8d3ab186ecf3c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 04 Jul 2024 15:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 80
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb57d14375011cadb1425f6530fb6a23e2f97cc0ccd6ce600b387796d09b6b4`  
		Last Modified: Thu, 01 Aug 2024 22:46:06 GMT  
		Size: 12.4 MB (12432709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39b2ab2d4dbeb01af65f4e26ea8b6dc08c42116a32407d9d5dde0ffb9d19d3d`  
		Last Modified: Thu, 01 Aug 2024 22:46:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8ed9c0d97624457fea31353db9846e1bfcc6db53724052a83f379142a61a0f`  
		Last Modified: Thu, 01 Aug 2024 22:46:05 GMT  
		Size: 11.4 MB (11415586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f772d30c25f084365844471f325a8725e11c8a4b82ccc5ab18c719d6a41ffbd5`  
		Last Modified: Thu, 01 Aug 2024 22:46:03 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ff2b3ecb6636d36b21fd2bf898bae0846d228aa26af91fd4a482bc3267b67`  
		Last Modified: Thu, 01 Aug 2024 22:46:04 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ed996fa9043a7271019d19116f9c491c392c55ba17f631ddd472bfdd0d973f`  
		Last Modified: Thu, 01 Aug 2024 22:46:03 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b253501cee7a1d6860af3a3725a04c014cca3c54d9f701db6c99f83b3615e46e`  
		Last Modified: Fri, 02 Aug 2024 03:35:28 GMT  
		Size: 2.3 MB (2253433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4652b63c882328ecdac40f3828f4e4600d33e845665156e0abd792abd6698`  
		Last Modified: Fri, 02 Aug 2024 03:35:29 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93da1b98f34dfcc77b7ae54c0ace2c20512f1d0a861b4909dd5baa67d6fada60`  
		Last Modified: Fri, 02 Aug 2024 05:19:35 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ae4c0c9686b1405c747311a5039b471e553c137bd5a8f7f5693803a8e90571`  
		Last Modified: Fri, 02 Aug 2024 05:19:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3561b6bc629642888e478462cb2c041cb431b18f3f89b0bbd41ce39d5ba2592`  
		Last Modified: Fri, 02 Aug 2024 05:27:59 GMT  
		Size: 21.1 MB (21082984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:1214ae8bd5b8b9ddb44d54a8493c3ad29583b071cb419221b9af8f21fe74de02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6909622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d36d5736d5f0037343bf4cf3f192fd2b527ecbde5de64de8daba208b3a4f1f`

```dockerfile
```

-	Layers:
	-	`sha256:d284e5eeb0e2c1ea2ffacf8c3b4f9b259cf66f07b9a1156ac57d9d3036ec6b10`  
		Last Modified: Fri, 02 Aug 2024 05:27:58 GMT  
		Size: 6.9 MB (6866737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433322440fc4a59d67615f10050037bdea727cd18a786393ea62b76c3d6b3045`  
		Last Modified: Fri, 02 Aug 2024 05:27:58 GMT  
		Size: 42.9 KB (42885 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; 386

```console
$ docker pull drupal@sha256:bb9661bc9c55eb581359d139c32a8963439b6402874fb0036a590ac1d166b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200439728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ddb13cadd8c008825f78d16865e54564dbaa644b4cabc17217ef000b94b9ec`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 04 Jul 2024 15:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 80
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34caeeb2ec9b0a871c2808cc5cad03c85e3775d863522099238ac68eda5e4073`  
		Last Modified: Tue, 23 Jul 2024 09:41:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee053233ee4b919aa7cfb9d47b5f6760be8d3ec7f62e66dd4fe9e6c60e99a7`  
		Last Modified: Tue, 23 Jul 2024 09:41:49 GMT  
		Size: 101.5 MB (101517599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc19e49f8d18ecebf1bf4f346d396cf87df4d75ee7b99b43a0f051717b7a5a`  
		Last Modified: Tue, 23 Jul 2024 09:41:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fda610fbfb0250b0d7e6b2430595f61c3dad96ed4a2536f3469b9de80d5f57`  
		Last Modified: Tue, 23 Jul 2024 09:42:15 GMT  
		Size: 20.8 MB (20843275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa63e9eb0f2b2ad20ff051c8efa62397470384f5c75a9dbd4d774b6028e8647`  
		Last Modified: Tue, 23 Jul 2024 09:42:11 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1608ceaa879e01156cb06283c35d1871d0cb91db35e47cc469b3da6547a360f`  
		Last Modified: Tue, 23 Jul 2024 09:42:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc1bec97e1d66dce19d5b7186ab0ea8e8191f3b9ff0b4b6f4f565867ef4622`  
		Last Modified: Thu, 01 Aug 2024 23:40:34 GMT  
		Size: 12.4 MB (12432133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e558ef9c36ef71dac0174b02389c50c788902a6c9dd3a5e8867d1de325c900`  
		Last Modified: Thu, 01 Aug 2024 23:40:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7f888fac46693254239774da24685e75c562bb8ec15bf142b6ffea90a451b7`  
		Last Modified: Thu, 01 Aug 2024 23:40:34 GMT  
		Size: 11.6 MB (11638659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca936a5f9ef66f7c4c2b900a5da6bbc81f6c60a933422bc35a1d6dd2ba66e0da`  
		Last Modified: Thu, 01 Aug 2024 23:40:31 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385e6dfadd95d1d775065c2cd1c7c753bfcf309f5def11c3a524127962508bc8`  
		Last Modified: Thu, 01 Aug 2024 23:40:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4da37a746bac5aaa53f8dd01d0534d8c90372d3f66a29d3d4f9103ca12344`  
		Last Modified: Thu, 01 Aug 2024 23:40:31 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b3a3f763b5a4d90fbb45d36e1cc9c092deabcbf29b3bc4b1edf39e3c2a0057`  
		Last Modified: Fri, 02 Aug 2024 14:54:59 GMT  
		Size: 2.0 MB (2048246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baf036bda2596926f6fa4b0f19cfdd993f0aec015208b212e89fce37db01ae6`  
		Last Modified: Fri, 02 Aug 2024 14:54:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf6a675e5465c654d3916448417e741700a8f21616829630f9a0ec2e073b2e1`  
		Last Modified: Fri, 02 Aug 2024 14:54:59 GMT  
		Size: 726.3 KB (726348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272c5eeba0d1e7e24dbbdbcb4a542b5f15600f23b395e5035fca6446c32fe760`  
		Last Modified: Fri, 02 Aug 2024 14:54:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ce08138957268059fc59d4d25def02e5639a9cbfa3ca3c6b0684e00992ef4`  
		Last Modified: Fri, 02 Aug 2024 14:55:00 GMT  
		Size: 21.1 MB (21083257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:8a6f23101f0f12514bbcf6887ba065f03d2dfc9e46a2c084a00a83ce97fb8519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6860248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19141c78f4938be45e00872d31aecd38f99712111b89066b51f61553821868ad`

```dockerfile
```

-	Layers:
	-	`sha256:dc26e657077a03bd35bd149e871c6c9e6921e39b372bf0505b3d6039dfd7873f`  
		Last Modified: Fri, 02 Aug 2024 14:54:59 GMT  
		Size: 6.8 MB (6818425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee71cff46e167d8dd74d1e7dc94d5a4fd74db6e445276f3faa74648a17cae1c`  
		Last Modified: Fri, 02 Aug 2024 14:54:58 GMT  
		Size: 41.8 KB (41823 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:78818b1aeccaaeb84189d8d41f66e87e1e73a5713aa43f4a23c1ad3f46ef7db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205882236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bff261d2ab94eaea0b066edb937ec367d3a9efabbbeb4d0997dde7646f28d3d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 04 Jul 2024 15:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 80
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679744addd25c44b49c10b6d0881679a0285af40dabbd99b4006332b338823e3`  
		Last Modified: Tue, 23 Jul 2024 05:17:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0c4608463aeeae784b14fc3e81ca8b4b81bd60e1b7a34823399adca9b770d5`  
		Last Modified: Tue, 23 Jul 2024 05:18:13 GMT  
		Size: 103.3 MB (103319086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f792a79caaf61b5ad5c6975df0f029f85e03b8e4560339110102763bde450248`  
		Last Modified: Tue, 23 Jul 2024 05:17:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbcbd591db67cc93879717462625294983b0ea984ec7daeb3ce7a2f84b49a60`  
		Last Modified: Tue, 23 Jul 2024 05:18:38 GMT  
		Size: 21.5 MB (21511417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe64cbce59d87195b9dab5e2f77c18dd42c43726b1d403e26b4aae6195ecdb7`  
		Last Modified: Tue, 23 Jul 2024 05:18:34 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b032e6ddf45fcdb0a5bcb1a93b94de425b9b38e0283696ffca9b79b528f7bbca`  
		Last Modified: Tue, 23 Jul 2024 05:18:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb04ab356a9cbf43bb5cae924cb21b65bcb872255f05ddfb0498dc302d77c78`  
		Last Modified: Tue, 23 Jul 2024 05:28:44 GMT  
		Size: 12.4 MB (12439479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deadc2f0947522843c0db43b8a4eb62444195ac333fc460b8c3490fdd11f047`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7901e2964f1a5ff1439d30a37e1aa375cd500e7fa5c58288daf7dfe0ca078b`  
		Last Modified: Tue, 23 Jul 2024 05:28:43 GMT  
		Size: 11.8 MB (11819426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696f569d5bb5396488646a76b13c9129a720e5721059c3e2a7c0f35bb8cb7345`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb2fc48d2b2ec1e727ade89c70d20b49837fa895e31fc8f69b5d861b77e7a96`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82caf1c6b06f7c22c75e0f9a203b324b948aeb0260334cce4dfed3e83d9058ca`  
		Last Modified: Tue, 23 Jul 2024 05:28:41 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16e0d7aa0e89f4310c5ef66d99ca2c4b5b13a290412a444ff0cc59ea70c14c7`  
		Last Modified: Fri, 02 Aug 2024 06:19:27 GMT  
		Size: 1.9 MB (1854936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752c41d6017d04f83df09ab0e1faff0b8b3af30be0cce8c6d3d9bd87198ce3d4`  
		Last Modified: Fri, 02 Aug 2024 06:19:26 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a56432bdb2763d278d4a1601ef3ba578628ec9f4be6e49b0250da4e51e373f`  
		Last Modified: Fri, 02 Aug 2024 06:19:27 GMT  
		Size: 726.3 KB (726346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17475a2965f63c779ec1fee761481a532d5d9164aadbe6323505cfd6b74977f3`  
		Last Modified: Fri, 02 Aug 2024 06:19:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aeb4d489b6c57863858ff16f761fe765b3b934eb4429029820776d0996e840`  
		Last Modified: Fri, 02 Aug 2024 06:32:42 GMT  
		Size: 21.1 MB (21083366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:a0508174ce318a76eebb58f994f2c6620677fc71b70611ffd0e6493071deb611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87db5e7bfa4166f1e78bf933eeec2ae8200ce14817c227be247e1650fb8ca3cf`

```dockerfile
```

-	Layers:
	-	`sha256:c44ee92441453dc5705ae3f1e2f51d924bf49f80fa928913864431c16cc2c279`  
		Last Modified: Fri, 02 Aug 2024 06:32:41 GMT  
		Size: 6.8 MB (6815329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3ea3fc230cb1ed02a558635c2bec23891abf2d197fa88973863ec04890c3ba`  
		Last Modified: Fri, 02 Aug 2024 06:32:41 GMT  
		Size: 42.2 KB (42188 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache` - linux; s390x

```console
$ docker pull drupal@sha256:52efea3b2917c78e7a2aa2eda4a86010cbf30a1209af363492287dd2754fc39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174853604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1730409be9cd5d505dfb186e942180122558b4c7118f7cdea9e72922fc851690`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 04 Jul 2024 15:27:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 04 Jul 2024 15:27:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 80
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["apache2-foreground"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cfba21730315054a9974bd81d57f4a0af83b3bce0ec602a8f39389526bc2a1`  
		Last Modified: Tue, 23 Jul 2024 06:11:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd83f19e63f8d7e6b0b418799c2fb3484a9b57681a15bb5c58dce953d894962`  
		Last Modified: Tue, 23 Jul 2024 06:11:47 GMT  
		Size: 80.8 MB (80816895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be2e88b5706d13997a405886ca83d6ee622ee824201de072a4e20126cf86513`  
		Last Modified: Tue, 23 Jul 2024 06:11:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb79cf9c2bd490848a9ac73af98b8cefb3d122a50b2cbb486d0fb3ae2a8db97f`  
		Last Modified: Tue, 23 Jul 2024 06:12:04 GMT  
		Size: 20.1 MB (20100185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4025c7bae49c61bc1bff1636e41c0224459752e9c72ebe99611290e1666f6e46`  
		Last Modified: Tue, 23 Jul 2024 06:12:01 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86355c71c575018477f6144acf0b48c2c5ab63f1264d4aeaa532f87ef04b7b08`  
		Last Modified: Tue, 23 Jul 2024 06:12:02 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f84dd80b1feb7eb73ab08093900e12c30566afc03c54416082a8379efb56f`  
		Last Modified: Tue, 23 Jul 2024 06:19:36 GMT  
		Size: 12.4 MB (12438611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bbca816bc846117ddd76ea0db88deee30f219514f268e7458e7c4489e61d9c`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e00239342e2e2d95cd4a2a1fd94a3aaaccaaa8e5ea86c40a32f4d2514430ab6`  
		Last Modified: Tue, 23 Jul 2024 06:19:36 GMT  
		Size: 10.6 MB (10639853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0e80beddd1b6cc0f0d3021338d8a05ce0ffaaa003754b62683ab4903690c7`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af6b58d4a7c6dc9f0d3c45e50f102d26d519e8eee83ae22ff07a379fc05867e`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2189971768087d257369eaf7c8f4422424b497302bf1a537f4e8d672314f0`  
		Last Modified: Tue, 23 Jul 2024 06:19:34 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947379d9b791e330adfd2de8d40680a432a4b24f7e51c70c36331e58e70dc797`  
		Last Modified: Wed, 24 Jul 2024 12:31:00 GMT  
		Size: 1.6 MB (1552479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e5514e0c0528bb68fff8ff829781cc6db8b0737bdaf7086ed38f4d465feaa9`  
		Last Modified: Wed, 24 Jul 2024 12:31:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6362fa486d4b6db16741b2e365c3323a30164bb38d2f09720a91e17bd4abdd0b`  
		Last Modified: Wed, 24 Jul 2024 12:31:00 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca007124b74551d9db5a5fb63ff33109e932e8159a7947242ce360a0812e6848`  
		Last Modified: Wed, 24 Jul 2024 12:31:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798d388fd2513f3405aa735523063e7bc2e29596b5df850bc25988be0e1f6391`  
		Last Modified: Wed, 24 Jul 2024 12:54:19 GMT  
		Size: 21.1 MB (21083264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache` - unknown; unknown

```console
$ docker pull drupal@sha256:9b8df719f61cac590259abec18539ff5787f8b92093889bbbd0d4765fe225405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6721914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebe5fad99cdadcca77ac0f60abfbd30d7f6add45aa358cdec30677c831cce15`

```dockerfile
```

-	Layers:
	-	`sha256:fba7ae69bb7029f03b66380df86011fb8ea66c49ba3305d81d5dd341aef09bf5`  
		Last Modified: Wed, 24 Jul 2024 12:54:17 GMT  
		Size: 6.7 MB (6679903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b07358f94890f5f1d4b89a1d5fefa8e0d2223cf3c342f47225136a1adb02db`  
		Last Modified: Wed, 24 Jul 2024 12:54:17 GMT  
		Size: 42.0 KB (42011 bytes)  
		MIME: application/vnd.in-toto+json
