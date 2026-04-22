## `drupal:php8.4-apache-bookworm`

```console
$ docker pull drupal@sha256:aeb6a9fcea346bf3225a1537bdb8257b81bf63bccefc711b47f52491d9f862da
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

### `drupal:php8.4-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:28903cf21804a869030f9307043e766f25b09f1832a9fe5e8ad4793949f62bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.8 MB (203783404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4b40d2e27641bb81e7b3eee49b49c2f2d3fc2b5459694c1eaa20d3f1460567`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:22:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:23:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:26:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:26:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:26:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:26:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:26:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:26:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:26:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:26:10 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:26:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:26:10 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:26:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:26:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:28:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:35 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:28:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:28:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:28:35 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:28:35 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:35 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:28:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:28:35 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:46:26 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:46:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:46:26 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:46:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 04:46:26 GMT
ENV DRUPAL_VERSION=11.3.8
# Wed, 22 Apr 2026 04:46:26 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 Apr 2026 04:46:26 GMT
WORKDIR /opt/drupal
# Wed, 22 Apr 2026 04:46:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 Apr 2026 04:46:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b008fb61610738e3c65f8b09bcc9b6b8515b801784cbe80e9fc049249ed0f48a`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d94c6a71161072fb0fcfc81621dd65ee173ca53f39ea933298318764b330e`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 104.3 MB (104337480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089f7f311938490a3dc2e97c430055eb5d7f9ee88e8de854b49d67a60161c5d3`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d603da4bf717be339399b29a0d40993917dc6b5beaaf4baf16d70080ea3476a5`  
		Last Modified: Wed, 22 Apr 2026 01:28:47 GMT  
		Size: 20.1 MB (20141842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1dda83f767aa4f9a9617740be56267a0b7942f1b65f878e5548bc4a5b9ce7e`  
		Last Modified: Wed, 22 Apr 2026 01:28:45 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01482a89adcca3a4dc31d8247553c26a6c3d3620c1bf4301c23412ba508d5863`  
		Last Modified: Wed, 22 Apr 2026 01:28:45 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458612cea2df86899fa23e863a09940b2576aec5911dfaf81bfb5d223c56f04f`  
		Last Modified: Wed, 22 Apr 2026 01:28:46 GMT  
		Size: 13.8 MB (13815117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5c526968db17fbedfb95c011e1e5736a2bf800f08d4a1046f0dcb55a0c1494`  
		Last Modified: Wed, 22 Apr 2026 01:28:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb621b046323db38cce8567ecfa01dbd157f4af38679a345af9764abceae763a`  
		Last Modified: Wed, 22 Apr 2026 01:28:47 GMT  
		Size: 13.5 MB (13528877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1c6a2a7342561255355f6ac5c3921c6030fdb2bdb39cce8cb410a1c252c7c3`  
		Last Modified: Wed, 22 Apr 2026 01:28:48 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0856a9673cf6a28e24ff5929d70b542f345426504b2593629a21ef0c99e25`  
		Last Modified: Wed, 22 Apr 2026 01:28:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ad7f1dda421992916189b9eb0ae44418bf5cec4aa1ebac322705179e025837`  
		Last Modified: Wed, 22 Apr 2026 01:28:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41128a54a0a0ba366aa87b8ab082305df70a1de441f1d68159d48840318e9cbb`  
		Last Modified: Wed, 22 Apr 2026 01:28:49 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6bb2b85c37e52d69745591dbd692e3d26b39cb303f6759a103c3651289181d`  
		Last Modified: Wed, 22 Apr 2026 04:46:48 GMT  
		Size: 1.6 MB (1575801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccabbd8e974d9c4a49c42436597ea736bfe82bd4833f6d01b1e742b101c81e31`  
		Last Modified: Wed, 22 Apr 2026 04:46:48 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8955201c0193e58bc3a92f78594498a5197dbb688984d37225d6f5102693fe`  
		Last Modified: Wed, 22 Apr 2026 04:46:48 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd9382ba72e9d9836ae4439a421787b0a2dda73d29fc634b7ebead540cbca4`  
		Last Modified: Wed, 22 Apr 2026 04:46:48 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89ca936464acade9f9153d5f6aced67725fdb9164b1c3bd4d93eb9aff8c17a1`  
		Last Modified: Wed, 22 Apr 2026 04:46:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e358566855693790bdaf554730d358d1ad6bdceccfdbd6d1dd0aca02adb26c6`  
		Last Modified: Wed, 22 Apr 2026 04:46:50 GMT  
		Size: 21.4 MB (21350861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4320ea4fa83e5cfe43648f7e864baac05847f3ee29acf91962e27cc1a9b3ca40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3c342d371bac5e2617a9f5e5290453c0930dda753aa3a0a6e80e25b33bf9ed`

```dockerfile
```

-	Layers:
	-	`sha256:bc1168080d606f80c841d71051215b53bd8d4c856e185255ab32e67dbd3468ec`  
		Last Modified: Wed, 22 Apr 2026 04:46:48 GMT  
		Size: 7.1 MB (7052202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4062916d6d85b05ce7c33b4942fe5c86993715178781863ed67bfb12347abb81`  
		Last Modified: Wed, 22 Apr 2026 04:46:48 GMT  
		Size: 43.9 KB (43930 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6757748b928528d4fdc3f59d0efaa0a797396523df105e1ae8fcad4ed3dc6789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167809643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ceab4b1cb24cebf827148e3da06eb81161b0cd7ca0ef63a9000532d6ae8199`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:32:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:32:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:32:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:32:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:32:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:32:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:32:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:32:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:32:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:32:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:32:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:32:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:32:40 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:32:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:32:40 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:32:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:32:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:35:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:35:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:35:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:35:32 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:35:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:32 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:35:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:35:32 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 03:53:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:53:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:53:24 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:53:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:53:24 GMT
ENV DRUPAL_VERSION=11.3.8
# Wed, 22 Apr 2026 03:53:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 Apr 2026 03:53:24 GMT
WORKDIR /opt/drupal
# Wed, 22 Apr 2026 03:53:31 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 Apr 2026 03:53:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289aece76337b7b43cf268666a62568b6ab7dd670985e6939690cee3c1daa3a3`  
		Last Modified: Wed, 22 Apr 2026 01:35:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086661eaf715af15fecf61aa4d202e8780f3efb6775b636e9731c88d6b565ab`  
		Last Modified: Wed, 22 Apr 2026 01:35:51 GMT  
		Size: 76.2 MB (76156394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bb1d52b88f3b582b6e72dacd14215e93559e3c0344c90f3088182caaa03dff`  
		Last Modified: Wed, 22 Apr 2026 01:35:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c63cca69d6dfb74a827beaedad416c618f85433db8e75192a3e4093920aa1ed`  
		Last Modified: Wed, 22 Apr 2026 01:35:50 GMT  
		Size: 18.9 MB (18850606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0850324ee1e805cde047d5c29d0d08b2a6f94d94b09f55cbb8677ff7bdf46741`  
		Last Modified: Wed, 22 Apr 2026 01:35:50 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad2f5f02a374b47aeaa2f41b8aaa3b4e379ec5492d3795801a1c18f7072c855`  
		Last Modified: Wed, 22 Apr 2026 01:35:50 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe6432d7bf105de9200f7518709ea6cfa65590942cc2edeb5e10df4f8e84588`  
		Last Modified: Wed, 22 Apr 2026 01:35:51 GMT  
		Size: 13.8 MB (13813260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7cdfcb2c186f946142852d78199f5a708f6acd02af1b2aeeb3835c92355fea`  
		Last Modified: Wed, 22 Apr 2026 01:35:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144ef36bafa23fa1c6eba962aa4bc3cb1494c31cdd09eebe1a03a6a950d77d3b`  
		Last Modified: Wed, 22 Apr 2026 01:35:52 GMT  
		Size: 11.6 MB (11604221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080e89e88dbbe9b79394931ae74c556152b6aef6482664a7efe9f2dabf5f0965`  
		Last Modified: Wed, 22 Apr 2026 01:35:53 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccffcae17a8118931c0f7ab9e9d80f5eb941e59505921558d8783ed820fe00b`  
		Last Modified: Wed, 22 Apr 2026 01:35:53 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01a5d240100473e084d2459d189a4d284baafa22151cbee972d6b8f0ae1b346`  
		Last Modified: Wed, 22 Apr 2026 01:35:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12806e0d19f88b167e93dc4ba406af59d3619e4ac43fa9aba392e36532c995e3`  
		Last Modified: Wed, 22 Apr 2026 01:35:54 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de173a5c0f4c93b1808d052e861606f409a4f0cf441762bb895c4b2d6b1412a`  
		Last Modified: Wed, 22 Apr 2026 03:53:48 GMT  
		Size: 1.3 MB (1295596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae429ed5303af68e520b62dbcd5e2cdaab66836d7e32d7f71ce3101db7bfd9c`  
		Last Modified: Wed, 22 Apr 2026 03:53:48 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de0ecd8930f2fd9629612bb42b010cf2ea2a733635e1a95cd70db43b90a8ae`  
		Last Modified: Wed, 22 Apr 2026 03:53:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e80a293d89f4fc4d5d01ef483e62067aeaa9eb0516f8e79b972e500caac4403`  
		Last Modified: Wed, 22 Apr 2026 03:53:48 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c78691d39130790eb08d939d048c39747305b1dd8ce9428d68bd0fcaa92eba4`  
		Last Modified: Wed, 22 Apr 2026 03:53:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a49549f7821b9836de3bf2fedcd93775f6fdb230ba34544ec991f1b24ed48d`  
		Last Modified: Wed, 22 Apr 2026 03:53:50 GMT  
		Size: 21.4 MB (21350955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:611eeda1d175a9c00652f19f76fd3fe3631ad1466fd5b855be5420ef73664a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6909665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d88cae8195e07ec35b8802c74eae264c7a56d171279e29ed9f04e2414fe4dc5`

```dockerfile
```

-	Layers:
	-	`sha256:bcf1de4269f657ea4e792d892fa41177d4ea4836d2dcaccbfb20c5a90e17618a`  
		Last Modified: Wed, 22 Apr 2026 03:53:48 GMT  
		Size: 6.9 MB (6865570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a9168512e1e806d3a797180e436fbf660d7498847c0d0c812faa2061ca1b1d`  
		Last Modified: Wed, 22 Apr 2026 03:53:48 GMT  
		Size: 44.1 KB (44095 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ec25f9a07cf14782f4d57d68b23d7e5cf8b69a562195b75abbc2fb8901fa2d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197139658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b4160dc534ae5d3de03279e2ba2e01ec6e1729d008586dbfa98a3276cd9d87`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:26:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:27:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:27:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:27:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:27:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:27:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:27:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:37:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:37:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:37:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:37:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:37:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:37:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:37:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:37:58 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:37:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:37:58 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:38:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:38:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:40:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:41:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:41:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:41:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:41:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:41:00 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:41:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:41:00 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:41:00 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:41:00 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 02:33:31 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:33:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:33:32 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:33:32 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:33:32 GMT
ENV DRUPAL_VERSION=11.3.8
# Wed, 22 Apr 2026 02:33:32 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 Apr 2026 02:33:32 GMT
WORKDIR /opt/drupal
# Wed, 22 Apr 2026 02:33:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 Apr 2026 02:33:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990ef3ac49bfcc488a4603db16f5cbb17a1423e36a5107bdfd69ea3ca10bb00`  
		Last Modified: Wed, 22 Apr 2026 01:30:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344ebbe7af54368820dffb9c1765aaf75e2ee23313cb25fedcfa6c7500b08bb9`  
		Last Modified: Wed, 22 Apr 2026 01:30:35 GMT  
		Size: 98.2 MB (98170709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7231ffab18cb08332f844bd1f572746b5276c55ae55635cfc96b2460598abeab`  
		Last Modified: Wed, 22 Apr 2026 01:30:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679aeba930c2fd65021573e7e46e01df7cb152a13532a5714ecbe2561cc77f6d`  
		Last Modified: Wed, 22 Apr 2026 01:41:12 GMT  
		Size: 20.2 MB (20163662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ba14e0ca71979b06f73b8e4094e065e217ff3006fac5e837f8ee41384284d`  
		Last Modified: Wed, 22 Apr 2026 01:41:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c5a3e4bc88b54ec97618a33088f99b163591959207c0031b83653c101469fe`  
		Last Modified: Wed, 22 Apr 2026 01:41:11 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ff5f5cfdf8afd542032208c3a9ee3a73d626b4a12570cc82e6660f41e0aaf4`  
		Last Modified: Wed, 22 Apr 2026 01:41:12 GMT  
		Size: 13.8 MB (13814866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fe89951a7010c0295564c02ebc75dfe98e97407d5b85a0930e22aa8f3c9461`  
		Last Modified: Wed, 22 Apr 2026 01:41:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cc61417ea50b68af5f9a28fffb1ed0330df1d94d3457cfaf6eab6ee1a83941`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 13.2 MB (13163009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3128a7dfa61cf114d164c8b678c9bef8cc406753ef8553260343b0ebfc87f0`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f24b838cf38d0df10588e780bf2110563f8ac4122e3e2e106ece5188f391f2`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656032b3fac2a542677aac1a904fc9c9d028e3eb7cd31b423d08a6b0e6354640`  
		Last Modified: Wed, 22 Apr 2026 01:41:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e86876a823594fa35fafdd5019aaa5093f0524d65931aeb1ddbbd68b8c95ab4`  
		Last Modified: Wed, 22 Apr 2026 01:41:14 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997151f10141c68acc30e6693a637976fa8f51da927c50be9c99d8c1feee5392`  
		Last Modified: Wed, 22 Apr 2026 02:33:57 GMT  
		Size: 1.6 MB (1563633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10708ed6de4fa07c205d8c6ab848489d97b22a4490d39423b39b0fb9c84c80a`  
		Last Modified: Wed, 22 Apr 2026 02:33:57 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fdb8e32d5760e32f6a03969d2a700c259d0f3dd29c327453f29fc93bd3d406`  
		Last Modified: Wed, 22 Apr 2026 02:33:57 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764218c2d60cace2cc83bd21b079e9739f4ef2f1e3dcbc6f8a8dca33d8cef69c`  
		Last Modified: Wed, 22 Apr 2026 02:33:57 GMT  
		Size: 790.8 KB (790770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a47deb5486f52e172ba67912c5348db3b54e9a51123a3cba15ad7da3bc401f`  
		Last Modified: Wed, 22 Apr 2026 02:33:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeff79f191201ab61b1893139c47f3973be4e344bcca00fafa275afa7368e935`  
		Last Modified: Wed, 22 Apr 2026 02:33:59 GMT  
		Size: 21.4 MB (21350480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:0b6932252e37676b0d9442c63d352250ed26352a6458a6c031506b8767438d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e67841a4a0cfce52a83e4e76ad6527797ea2e55a1a274826fe77402bb16ed23`

```dockerfile
```

-	Layers:
	-	`sha256:96ab9239517563a487737bb876a2c459fe7df9d6566b6a75b4eac44b07e62497`  
		Last Modified: Wed, 22 Apr 2026 02:33:57 GMT  
		Size: 7.1 MB (7080663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a757e38fbafa14441e6d54da4cb1b8ecc95ae570f5c464292cec56e911036fcc`  
		Last Modified: Wed, 22 Apr 2026 02:33:56 GMT  
		Size: 44.1 KB (44146 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:6f51eb0647bf0ca55e4a0f86f215248c736302fc0fd670b9cfa4a3eecfd060cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202846716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e98e9820ee47b86149bb387a56d81849a20df080f01666a073441c815e9b7d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:18:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:18:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:18:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:18:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:18:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:18:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:18:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:22:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:22:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:22:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:32 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:32 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:32 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:23 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:25:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:23 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:23 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:25:23 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 05:04:04 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:04:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:04:05 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:04:05 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 05:04:05 GMT
ENV DRUPAL_VERSION=11.3.8
# Wed, 22 Apr 2026 05:04:05 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 Apr 2026 05:04:05 GMT
WORKDIR /opt/drupal
# Wed, 22 Apr 2026 05:04:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 Apr 2026 05:04:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d4fbc2e6dc8ab6dd6c0f4fc6dddc7cd1d8af53923812823367ef628728c552`  
		Last Modified: Wed, 22 Apr 2026 01:22:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990ee3b832cd698ba8d7237296cca6b847c244f888708b4c1ff3e7037dc285d6`  
		Last Modified: Wed, 22 Apr 2026 01:22:19 GMT  
		Size: 101.5 MB (101529778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bb6a0ad9dad6af32fdd0c6f2ce2a6fa9974fc1c60b96097d0f6d0092099e9e`  
		Last Modified: Wed, 22 Apr 2026 01:22:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d6572f2bc234a692a6a2d1108d378fada0e08767e91e45a2c9fbfe821adf5e`  
		Last Modified: Wed, 22 Apr 2026 01:25:34 GMT  
		Size: 20.7 MB (20665557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fb06dd3642e8a84747e211cc1ad364b78066dffeb22b1e974c2dc8d88ac728`  
		Last Modified: Wed, 22 Apr 2026 01:25:33 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71176b532ea07cf176e0aacea019732e7e7b4e1951d4f90bac6dde0516c26d28`  
		Last Modified: Wed, 22 Apr 2026 01:25:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1a5ebbb2e8a6fc7fa8cb8ce56482b8869e5ec63eca359a0c995500c2a99c5c`  
		Last Modified: Wed, 22 Apr 2026 01:25:34 GMT  
		Size: 13.8 MB (13814278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df6c377d37d55d05fcc96b4f515ef1be62b25b78f15d7c44ae14aa851d89b2f`  
		Last Modified: Wed, 22 Apr 2026 01:25:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e34176ea9c8bfb19ee4cd230597979bba61b69f12a8a514cff0dfaf7c51de6`  
		Last Modified: Wed, 22 Apr 2026 01:25:35 GMT  
		Size: 13.8 MB (13819718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0d62bb2d90bbc1e55c8ff9869a17711a46d8b87e25893755e791c8d4f1d1a8`  
		Last Modified: Wed, 22 Apr 2026 01:25:36 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa4ac81503cff03734b334083b3a11f9fe8f9825cd253d805b543f35b1bc993`  
		Last Modified: Wed, 22 Apr 2026 01:25:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347f6e55f8b2c51493f9f1f1e6679d0aa87f341ae2fe7b307d142dca7e527d0d`  
		Last Modified: Wed, 22 Apr 2026 01:25:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e561094cdadba33aeea5c1005daeb0a580c9bd502674893994df5c2041103f2`  
		Last Modified: Wed, 22 Apr 2026 01:25:37 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3891495f246291f406f1297adbc3c021b8e7494d93bbf623fb6e18a66eea6f3d`  
		Last Modified: Wed, 22 Apr 2026 05:04:25 GMT  
		Size: 1.6 MB (1647744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a332e99d0be44c0a7df2acc28ec056169f32f04f98fc9deb0f626348e640d3`  
		Last Modified: Wed, 22 Apr 2026 05:04:25 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82fc18113a1938cfa119489b2c3ea667d7a0312e16957acd678e3073ecf413e`  
		Last Modified: Wed, 22 Apr 2026 05:04:25 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a725d9afd0f16742096d5f9a39511b342773d4bb5e115e95325f435d3560c3`  
		Last Modified: Wed, 22 Apr 2026 05:04:25 GMT  
		Size: 790.8 KB (790769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259a224f0008a8c34f1cbb29eb5ab15b05443a012c64a094e214375f1474ac5b`  
		Last Modified: Wed, 22 Apr 2026 05:04:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedd121120f14635df0bdd262105014d883afaa6526d2d78ae4a5088ec170963`  
		Last Modified: Wed, 22 Apr 2026 05:04:27 GMT  
		Size: 21.4 MB (21350756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:e4f29feac673df36fdc62eccfb78578793e38a86609ff174d4dc96cf75f238cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e80a2b0d558c9a3d588f3167ed89edf51327014587f1f01b2f0a215a1d4366`

```dockerfile
```

-	Layers:
	-	`sha256:a5e826c82cd42836d3a40da0fd3c0b1878e711919a920e72b5f9c1c37b224b86`  
		Last Modified: Wed, 22 Apr 2026 05:04:25 GMT  
		Size: 7.0 MB (7031930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac8ebb9392fe6dd9d004f31853338bd42dbf1d62839937153f08ca7e42b0c2e`  
		Last Modified: Wed, 22 Apr 2026 05:04:25 GMT  
		Size: 43.9 KB (43865 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:ddeb67dd14ba344e95ba8bd54d8a3b8a19d7fabda99cf47002b4177ae5ddd3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211374964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ab2f8031bc34659e5443cdc6070edbc19f013a3553a75647764d7b492c0287`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 02:00:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 02:00:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:00:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 02:00:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 02:00:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 02:00:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 02:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 02:04:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:04:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:04:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 02:04:39 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 02:04:39 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 02:04:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 02:04:39 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 23:01:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 23:01:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:06:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 23:06:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:06:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 23:06:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 23:06:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 23:06:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 23:06:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:06:16 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 23:06:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 23:06:16 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 01:21:34 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 01:21:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 10 Apr 2026 01:21:35 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:59:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:59:20 GMT
ENV DRUPAL_VERSION=11.3.8
# Tue, 14 Apr 2026 18:59:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:59:20 GMT
WORKDIR /opt/drupal
# Mon, 20 Apr 2026 17:51:45 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 20 Apr 2026 17:51:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38fc39e5b1951092cd5d7d0c353c05fc46d54f99fc09075563b28fe3140233d`  
		Last Modified: Tue, 07 Apr 2026 02:05:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907375e2bc1671ecd7e842b7b97cbc7d4e818650b88036efb258c049d774eecb`  
		Last Modified: Tue, 07 Apr 2026 02:05:23 GMT  
		Size: 103.3 MB (103330301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b5c36d7ac6c0441c421dd303cfe1a4fd985d304a99be070da82c97ab2a3278`  
		Last Modified: Tue, 07 Apr 2026 02:05:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9c2111011dd642f99bd40809575f96ae6f3f4fecffa787d358ca0e78d82fe0`  
		Last Modified: Tue, 07 Apr 2026 02:10:28 GMT  
		Size: 21.3 MB (21332514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b06d2f576298b89ac5a7035b9404990844d097ef1f42bfa5ec8785e21f80df`  
		Last Modified: Tue, 07 Apr 2026 02:10:27 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe222ffbe2298a7a6213f5fc273d2c16858691ea5798a206c266bd5525a1086`  
		Last Modified: Tue, 07 Apr 2026 02:10:29 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a52dfeb29c08d65b1f2ce9b5b969be32c5ca05f669ec2e2f555df4d330dad0f`  
		Last Modified: Thu, 09 Apr 2026 23:06:42 GMT  
		Size: 13.8 MB (13814767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e2dd49422bfa8a5f3baed603b29ba7bdf20c716badbf9393080ee27d417a4`  
		Last Modified: Thu, 09 Apr 2026 23:06:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ebaaff6cfc165aec5bea8bad2c6398dae3261687cd54eebf39a66a0f86131`  
		Last Modified: Thu, 09 Apr 2026 23:06:42 GMT  
		Size: 16.9 MB (16893039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c2b418ab5a79b6a4f1d468d08632ede2dd61973e87268ea968f6914d28ea21`  
		Last Modified: Thu, 09 Apr 2026 23:06:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca59b11503a11e99fa68aefb7c2f2f75aab5c7bc40d906580e96e581db67057`  
		Last Modified: Thu, 09 Apr 2026 23:06:42 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09f8e3e591097f6e52ac8df6facd8ee60555ee58df061776d5c2927ebfcd8a3`  
		Last Modified: Thu, 09 Apr 2026 23:06:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828ce838910628f2b1172497133a7263768278147777628991153056d47d0a44`  
		Last Modified: Thu, 09 Apr 2026 23:06:43 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beddd3ac530a627b23ab31c1ef534685123c2aa8a8372836fde15a9354cb3666`  
		Last Modified: Fri, 10 Apr 2026 01:22:35 GMT  
		Size: 1.8 MB (1778509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0376d836a0516aaf6014abbe1c346e0541c8964f960a23bffe327ca81d25d72d`  
		Last Modified: Fri, 10 Apr 2026 01:22:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1415b5381ec20a5351baa658d5893c7f901b9e74ae3c9e93292779594583dc15`  
		Last Modified: Fri, 10 Apr 2026 01:22:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0dcda6c83d2abc36ec34ba27300d2b6d37e69a2f1c61b398c1a6b7be811f31`  
		Last Modified: Tue, 14 Apr 2026 19:00:23 GMT  
		Size: 790.8 KB (790771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa66e99af5223dc4d2b13773f1503743dbea2c10007abb79fa19301ae8ed584c`  
		Last Modified: Tue, 14 Apr 2026 19:00:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40c874cf96f58ec14e3e694624d61e41feadc185f6f23e7bdc2893139a12cac`  
		Last Modified: Mon, 20 Apr 2026 17:52:25 GMT  
		Size: 21.4 MB (21350162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:2724886c857995ffb26e187812660e5b9573bdd493ba1bf9ce90c205fa1d859e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7073076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5a993e9633b0ed5dfb97898f400ae2b1f7d9c6e33b8669c6fdcd0dabd2e48e`

```dockerfile
```

-	Layers:
	-	`sha256:26c794502ab4905f2469b2b84baf61c453be84118b1ca811f72ad9b39c479be3`  
		Last Modified: Mon, 20 Apr 2026 17:52:24 GMT  
		Size: 7.0 MB (7029062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e128ab00e67bb6e9f659dea5f31ec2f85fb942f6dc00f6d252d0568b7e50221`  
		Last Modified: Mon, 20 Apr 2026 17:52:24 GMT  
		Size: 44.0 KB (44014 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:07027087ce521c004e8d898288374622463c2aba836296aae04d8de9c2a97095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180079492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b4e74bdacc68e55db6f8194c9da7599b1440877023361e4eba3fbb4d9fbdca`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:35:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:35:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:35:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:35:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:35:39 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:35:39 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:36:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:36:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:36:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:36:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 01:36:29 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 01:36:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 01:36:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:33:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:33:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:38:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:38:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:38:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:38:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:38:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:38:17 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:38:17 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:38:17 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:34:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:34:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Apr 2026 23:34:17 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:56:45 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:56:45 GMT
ENV DRUPAL_VERSION=11.3.8
# Tue, 14 Apr 2026 18:56:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:56:45 GMT
WORKDIR /opt/drupal
# Mon, 20 Apr 2026 18:05:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 20 Apr 2026 18:05:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836e529738c3a4ccdd0b1dd95596d46abea966176beacc2742f11b3651592fae`  
		Last Modified: Tue, 07 Apr 2026 01:40:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3498b9f85e5cef550e2a5b12b10557ae540a5aa7f66491a036d6db8c5642e2b`  
		Last Modified: Tue, 07 Apr 2026 01:40:56 GMT  
		Size: 80.8 MB (80828298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d3aef64598ff4c058f1d1ab6c147ea9567ac449e4199e284837b62e90af7a`  
		Last Modified: Tue, 07 Apr 2026 01:40:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e458e23f2f37c66a3dbb8deada7cace1c24d7aaa31b96da6134c8ae2c7cd3048`  
		Last Modified: Tue, 07 Apr 2026 01:41:39 GMT  
		Size: 19.9 MB (19918805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6057a51944580af5f880bff947a1c4f378c0171c88f32b9b4e31bab4ba3e01b2`  
		Last Modified: Tue, 07 Apr 2026 01:41:38 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93b0c5128440a77994318103a3d756fe0af6eca954c172a51055a8ca1170cb`  
		Last Modified: Tue, 07 Apr 2026 01:41:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8f7e877c9f3b039367dae257c9583dc9516912cbda71743ddabb75fb258cd8`  
		Last Modified: Thu, 09 Apr 2026 22:38:36 GMT  
		Size: 13.8 MB (13813830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f88bb7c511dd60b3fa8030937c44b271605b6205b425a5c59873a42ad61a29`  
		Last Modified: Thu, 09 Apr 2026 22:38:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8fb7b3e37b34e2e1450df87850d437061c70f330e34c71b9ec9b4b0b4e274`  
		Last Modified: Thu, 09 Apr 2026 22:38:36 GMT  
		Size: 15.0 MB (14992785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e7adc52354ba720e5f848fb2755f2742d32ec17b5659d931645977519a7128`  
		Last Modified: Thu, 09 Apr 2026 22:38:36 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6320fa3a32b4745bc4f728adbbc4c26f3ef1fc27e3e9e22d9767c5b6674bb8a8`  
		Last Modified: Thu, 09 Apr 2026 22:38:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce77cd0660fcc3f89b7fd0bc67f9ab43a74a25f8f97e20881878beb99c99eda`  
		Last Modified: Thu, 09 Apr 2026 22:38:37 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a3c24ac95d91f13483496485af95a15dd8882f5c5b91d81ee5521b819d7780`  
		Last Modified: Thu, 09 Apr 2026 22:38:37 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c33c7a321136b7947a6a3339638c9e701d72ff186fd7783cb641add3719244`  
		Last Modified: Thu, 09 Apr 2026 23:34:51 GMT  
		Size: 1.5 MB (1486492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427d8183209a1e526267979553da79783be29a192062bca40ac4569a330cf5eb`  
		Last Modified: Thu, 09 Apr 2026 23:34:51 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fc5eae63d1a1a3631092b963243311511b7ceff66fed6a311ba4660bcecd89`  
		Last Modified: Thu, 09 Apr 2026 23:34:50 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1712fe91af53e978f5d73cf6ee3aa462ba2fcbb04046d602eefc02a2f0dde0`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 790.8 KB (790768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e119071ac42317dacc2854b5a33ebf15548b3bfb9737fe6cb2052b360b960`  
		Last Modified: Tue, 14 Apr 2026 18:57:25 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062b10684ca8bd7b3a2f0b46d56654341776129419ba730c66dabf5341249c75`  
		Last Modified: Mon, 20 Apr 2026 18:06:58 GMT  
		Size: 21.4 MB (21350467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:39ef57d9c1736670d9ba406abddbfa62931a78fa239b621f35cf5b581f125733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6933327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1ccfc4f0f074391daf0b6d2818b2ca36e3674b153a7927d5590f9bdc7a0a08`

```dockerfile
```

-	Layers:
	-	`sha256:01a74883b79554fabfb6697dcfae681343c05c5054d88742ff495c809f976b06`  
		Last Modified: Mon, 20 Apr 2026 18:06:56 GMT  
		Size: 6.9 MB (6889404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee6e8d1287abfb29a8f149b0fafeb2e9920b04e0739789552e2f6e9c2de600c0`  
		Last Modified: Mon, 20 Apr 2026 18:06:56 GMT  
		Size: 43.9 KB (43923 bytes)  
		MIME: application/vnd.in-toto+json
