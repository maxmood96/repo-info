## `drupal:php8.4-apache-trixie`

```console
$ docker pull drupal@sha256:adc48c2627696e1a010bcc42671051fbb44b501026495c6c727b00981684ea61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:php8.4-apache-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:e3082e95925c5045e82bed07e5ecb6338285a126434e736f81e035feb8dc4f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (206017109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97247fb23b189e55242f9441535cbc7e1aaa93940c4f5f05d5f42d72433034d7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:15:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:16:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:16:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:16:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:16:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:16:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:16:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:16:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:16:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:16:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:18:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:18:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:18:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:18:54 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:18:54 GMT
CMD ["apache2-foreground"]
# Wed, 15 Apr 2026 22:13:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:13:14 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:13:15 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:13:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:13:15 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 22:13:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 22:13:15 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 22:13:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 22:13:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffb7e1d7f94860f5b3a9e2df478da8a2661498b38db3222d9490e0e63fd1e07`  
		Last Modified: Thu, 09 Apr 2026 22:19:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd73acf43b8d72c9dce9d17f01a9fc96884e893fc0702b8be4ba1e9b39945ca4`  
		Last Modified: Thu, 09 Apr 2026 22:19:17 GMT  
		Size: 120.8 MB (120798321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e27b2414675d618ef8d63b7faf256eda9fb801f17c768ca2b063c97843fa451`  
		Last Modified: Thu, 09 Apr 2026 22:19:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc31bb8e9d4fc68dce9e7c72545b026b8586fcc7b7d99976a216777b9b33fe`  
		Last Modified: Thu, 09 Apr 2026 22:19:14 GMT  
		Size: 4.2 MB (4227183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95eebb2f652d3f8bc58d02c8f368f5be63a1f67390fe9de93e6baba1956a99`  
		Last Modified: Thu, 09 Apr 2026 22:19:15 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf8294cbce8072b8bef494170ec4e214049a03390ca4d566e00156e38f30e18`  
		Last Modified: Thu, 09 Apr 2026 22:19:15 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c151ee09453b87c82f5735f7018d15ed5d30c6041dc559bc10bb7d30f0d7afe`  
		Last Modified: Thu, 09 Apr 2026 22:19:16 GMT  
		Size: 13.9 MB (13852862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f6373c27c3d7dd9b7e77fed7edc59b8be02efab451f8d8ba326a7490553753`  
		Last Modified: Thu, 09 Apr 2026 22:19:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9737d96107ee92514e5d96eeb1a70a902de902fd2ed8001a3805160ec1d84f5d`  
		Last Modified: Thu, 09 Apr 2026 22:19:17 GMT  
		Size: 13.6 MB (13557848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48126b155e192ea24076e34fbca93a8b1c6291af2f36f25d9a0cf5fc5aee768`  
		Last Modified: Thu, 09 Apr 2026 22:19:18 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2952872e255d2257f7578c14704e67ae49e1be9cf71b56b1ee7dd00650fcb77`  
		Last Modified: Thu, 09 Apr 2026 22:19:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305ee441fb9d0e7a2339b25d3413b213db2965089b29aee05d045863217b97`  
		Last Modified: Thu, 09 Apr 2026 22:19:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e170750ef23969459ae184cc5b350c055501327c889084b0d23dc8c77ab3c`  
		Last Modified: Thu, 09 Apr 2026 22:19:19 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc95fefdbbdc0cd4b3b0246dcd763016b2082b1c51295c3698f8deafbb4c4a`  
		Last Modified: Wed, 15 Apr 2026 22:13:42 GMT  
		Size: 1.7 MB (1658767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb37493acd20e99fe344df81057bfabd0e4e7c56905d8632081f3dd8203f7ed`  
		Last Modified: Wed, 15 Apr 2026 22:13:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5f5b7468f308056fbb5bf7ff8ed6360cffe3e8944e2dc1b36595d12a4f8df4`  
		Last Modified: Wed, 15 Apr 2026 22:13:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5699bb800306e0c70c9914f90d7028d8e61a3039cd816d500d965f4dfed64d4b`  
		Last Modified: Wed, 15 Apr 2026 22:13:42 GMT  
		Size: 790.8 KB (790771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd00c6bbea464a1704893a61fbb4413eecce84608a522c63517acba170e2a7`  
		Last Modified: Wed, 15 Apr 2026 22:13:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93b5661509305bb0c6ecaabbb41228a81552f256523c31f0ce8b67c012d0a77`  
		Last Modified: Wed, 15 Apr 2026 22:13:44 GMT  
		Size: 21.3 MB (21349299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:ab2b16327556142968dfdebe726220a74a1936a5725b3b920a6f0371b188c323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158435a76dea1a4f0cd5e0922c9efed70727a958e15c0b4b05456f699231cdbc`

```dockerfile
```

-	Layers:
	-	`sha256:e4a37630c25b593258711966acc50ba7e52fc3898c28b8ea1663a03ed88fa892`  
		Last Modified: Wed, 15 Apr 2026 22:13:42 GMT  
		Size: 7.3 MB (7342289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a058ca108debf5b44054cde02dc4b1a077d788ac1c48cf771462ccd2e7f51ec`  
		Last Modified: Wed, 15 Apr 2026 22:13:42 GMT  
		Size: 48.8 KB (48787 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d6cd8e45c39ec8aa26d9ee067e8f2007eedf3882b95f684d21a642f421fcdaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167413605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0496f6561eebaaab0917f471626b7f299149b0165e774571b136f187692b04`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:23:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:24:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:24:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:24:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:24:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:24:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:24:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:24:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:24:23 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:24:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:24:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:27:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:27:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:27:25 GMT
CMD ["apache2-foreground"]
# Wed, 15 Apr 2026 22:21:01 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:21:01 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:21:01 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:21:01 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:21:01 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 22:21:01 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 22:21:01 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 22:21:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 22:21:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0128c6517e22ae07a90d2d53d482b1ccf7b914707f39c4b40d9e304ae6ec4cb5`  
		Last Modified: Thu, 09 Apr 2026 22:27:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d854cffdaee5fd297d469b8963aebb247498d83a49a7c5deb26d68f1ca7c1e`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 88.5 MB (88463301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd78e7b03a1506505ff4e2357beba6c4855c1e762463f1262aeaaba547d4b`  
		Last Modified: Thu, 09 Apr 2026 22:27:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fd66de35fc4b6b762abfe39a9442a2d4efa944581b0a7eb7033c21ac84d157`  
		Last Modified: Thu, 09 Apr 2026 22:27:42 GMT  
		Size: 3.8 MB (3757405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c13ed7dc08209d20d334187f9a51c2cefd9a568d2519f095e1dc912a853a0`  
		Last Modified: Thu, 09 Apr 2026 22:27:44 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd003c675d84dba2ce06cc80ceeb1992de569cc5d18f6d7f551f1feb3a2bcc`  
		Last Modified: Thu, 09 Apr 2026 22:27:44 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac37e47d191b62e7f6e43458346d6f3355a25b461964bd0ed801a4ba679dcac`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 13.9 MB (13850372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cb6d95e03404421d8eb92e7a8a2fc508d5c9e783e0d209d20108f234083c2e`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e11293b6092bafa94f6c635f63a063f53445de6c79c42486e077a8a7b331bb`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 11.6 MB (11617794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d8282280582efe36635d2dcbcc9d09807c4d617ea798fdaf20a672500ff66`  
		Last Modified: Thu, 09 Apr 2026 22:27:46 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1925ff69bb29d6cea799781584b619aee1df1ebfbb7d0358d5edfb3c5829e43`  
		Last Modified: Thu, 09 Apr 2026 22:27:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcefb6170cb2f4cc0af2a8f801e8b2bc784e377dcf4066936c1899fde82f17e`  
		Last Modified: Thu, 09 Apr 2026 22:27:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6453786394b4d850905bf56d93207bd709039503ce5b4dd85574e3b10ad46833`  
		Last Modified: Thu, 09 Apr 2026 22:27:47 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f387c3638c84b9456146b7e864a9a4b06c819a9d053b45d296b7d526819156ee`  
		Last Modified: Wed, 15 Apr 2026 22:21:27 GMT  
		Size: 1.4 MB (1371474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2d3ae1d2b0bfbd23467c276e6f01f5ce2a32ea4892ed0afaf44d1427be6192`  
		Last Modified: Wed, 15 Apr 2026 22:21:27 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f4924ef24c0aa934df8de133a984474ca449aba7008321d3f52c642d7db357`  
		Last Modified: Wed, 15 Apr 2026 22:21:27 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21772161e620eab625341f8d98cfbf34a552068f2da5d663344289abf0f1b92e`  
		Last Modified: Wed, 15 Apr 2026 22:21:27 GMT  
		Size: 790.8 KB (790767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c5660944c7e0ccc9baf3f891bcfe4960f84706ca3457cb317059c179ab5eb4`  
		Last Modified: Wed, 15 Apr 2026 22:21:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b7217eefccca2d8017b5bf08b233be0c220afedb721a20d4f8526412547b7`  
		Last Modified: Wed, 15 Apr 2026 22:21:29 GMT  
		Size: 21.3 MB (21346412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:2038a43349e8eb3ea4c2828502cfda987ab7d43124a21be2f6f54a6f3d7de56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fa958321eb2f2cec655566fe603693f976fd41c6e8da752224b6359fc960ce`

```dockerfile
```

-	Layers:
	-	`sha256:250724dc56f5ca949a5ac6e490419e30b15aa6a344c9a87f7880e8077268aa7b`  
		Last Modified: Wed, 15 Apr 2026 22:21:27 GMT  
		Size: 7.1 MB (7146298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c4073a238dabb31f2fb90565cc9df7f34d5929f96f5d6884c04673980119e01`  
		Last Modified: Wed, 15 Apr 2026 22:21:26 GMT  
		Size: 49.1 KB (49081 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:36c66033a92dfd8f66ab628d08f3f9354674c669b9e39f02110b4f1eaa978e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.8 MB (198772594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a0878730b162ca32ccfc589eb8d264bb8191396b901ef1ed71559ab4d9da59`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:16:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:16:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:16:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:16:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:16:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:16:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:16:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:16:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:16:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:16:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:16:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:20:01 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:20:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:20:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:20:01 GMT
CMD ["apache2-foreground"]
# Wed, 15 Apr 2026 22:25:07 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:25:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:25:07 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 15 Apr 2026 22:25:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:25:07 GMT
ENV DRUPAL_VERSION=11.3.6
# Wed, 15 Apr 2026 22:25:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 15 Apr 2026 22:25:07 GMT
WORKDIR /opt/drupal
# Wed, 15 Apr 2026 22:25:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 15 Apr 2026 22:25:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338ea32ccb6710f9a682185fd06ae9ec4f900b61387416169639d8ea6c2cc0b`  
		Last Modified: Thu, 09 Apr 2026 22:20:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc88cb1f79996d45df348bb492317d64532bd42f62297aa7bea02d90003a9be`  
		Last Modified: Thu, 09 Apr 2026 22:20:26 GMT  
		Size: 113.5 MB (113507428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fed35923d21dc60ad69bc693d326331e0a0c7073e561b4a44d5ba25504166c`  
		Last Modified: Thu, 09 Apr 2026 22:20:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a06a2c5945814b4e74d4f46092aeecf8c2de9e39a6ab51d0e25c3f569f24f4`  
		Last Modified: Thu, 09 Apr 2026 22:20:23 GMT  
		Size: 4.3 MB (4305799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ec882417cf6b7335d4f14a8abdb39fac07521db952fddacf1ef75e9d16ceb`  
		Last Modified: Thu, 09 Apr 2026 22:20:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731768ee0f6fb461e3600410b457fbc6bbe938ebaf5275067ba9912aabeb1f3`  
		Last Modified: Thu, 09 Apr 2026 22:20:24 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8881a242eb81a0565a768bdcc648a7147149c032b758e29cc4039b5914b295`  
		Last Modified: Thu, 09 Apr 2026 22:20:25 GMT  
		Size: 13.9 MB (13852382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fccd83ca47a53cb0d9f8e783cef04bd25f0506ea44ee9dfcdd1717eb9f5aaa1`  
		Last Modified: Thu, 09 Apr 2026 22:20:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea7ac474f047296270655a2dd8c8175c85ebfc9d7d983c0737933d479ee6b2`  
		Last Modified: Thu, 09 Apr 2026 22:20:25 GMT  
		Size: 13.2 MB (13206297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31a0f1b8754c4d349dbfeda5eb674bb6939768c0036f19ae26c4a19e042549`  
		Last Modified: Thu, 09 Apr 2026 22:20:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7266fa89a433a670a82c0e0744a4bdf11227ce5865a30269c8a41353ac6d2d09`  
		Last Modified: Thu, 09 Apr 2026 22:20:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c46f206b133b93ea1e49cfa9e70c50747d808b8938b0dc73ba86015fae98c`  
		Last Modified: Thu, 09 Apr 2026 22:20:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edcfc2b7d3dbe1ff7618369da15633d8e17cbd51e7fce9a81d6f9d622e63bb9`  
		Last Modified: Thu, 09 Apr 2026 22:20:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4f7b1fc48cefe731e29b7d75c7cbe970b6601276845c602dedac9d7e89660`  
		Last Modified: Wed, 15 Apr 2026 22:25:33 GMT  
		Size: 1.6 MB (1615403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f3cf9a070fb78562109eab057d58891e59cd80244c66516ffb396a894310d5`  
		Last Modified: Wed, 15 Apr 2026 22:25:33 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef02f934453afa32bcef9dcbda27b530c376b7be2f867b0fbebf0697f6e81b6`  
		Last Modified: Wed, 15 Apr 2026 22:25:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f89e64c98dbf3150a5dfb2077c445e9cf35bcadc963cfdcc3918edf3037eb4`  
		Last Modified: Wed, 15 Apr 2026 22:25:33 GMT  
		Size: 790.8 KB (790771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec89fad30e04aa13025dd0288b930ce7bb2d0fa84b3e6556bb5cee19030a9fd`  
		Last Modified: Wed, 15 Apr 2026 22:25:34 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a13ed540f186777ef66dee8aafc57e28298cc7e96f84d78d748a7e33348fa6`  
		Last Modified: Wed, 15 Apr 2026 22:25:34 GMT  
		Size: 21.3 MB (21349539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:845cfc19e75046e446e1b67cb18451022daca09063025fdd853b44f903dda5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c78d600facbb46c0ebeb9d499d5156aa91133956279cf168010260464fefe3`

```dockerfile
```

-	Layers:
	-	`sha256:78e727d62ad29a2f126535674c8ff078c16b4729ac5ca6abc564e8f7cf4b0c20`  
		Last Modified: Wed, 15 Apr 2026 22:25:34 GMT  
		Size: 7.4 MB (7439831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d516be64d289e0c7959e0929f8a4f3d7d5c421ec2881a777169b369c3b17191`  
		Last Modified: Wed, 15 Apr 2026 22:25:32 GMT  
		Size: 49.2 KB (49202 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-trixie` - linux; 386

```console
$ docker pull drupal@sha256:8e7b627fb2f1971516a935d80786ce614f6ccfa150ab0f7cfcf4684c4a805615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206373717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6359147e60b356cab1774cf02322f0364dbbc0942cd6edf1ecaeacee0fde40`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 10 Apr 2026 00:13:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 10 Apr 2026 00:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 10 Apr 2026 00:13:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Apr 2026 00:13:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Apr 2026 00:13:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 10 Apr 2026 00:13:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 10 Apr 2026 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 10 Apr 2026 00:17:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 10 Apr 2026 00:17:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 10 Apr 2026 00:17:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:17:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Apr 2026 00:17:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Apr 2026 00:17:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 10 Apr 2026 00:17:17 GMT
ENV PHP_VERSION=8.4.20
# Fri, 10 Apr 2026 00:17:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Fri, 10 Apr 2026 00:17:17 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 00:17:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 00:17:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:20:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 00:20:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:20:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 00:20:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 00:20:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 00:20:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 00:20:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:20:13 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 00:20:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 00:20:13 GMT
CMD ["apache2-foreground"]
# Thu, 16 Apr 2026 00:14:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 00:14:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 00:14:11 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Thu, 16 Apr 2026 00:14:11 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:14:11 GMT
ENV DRUPAL_VERSION=11.3.6
# Thu, 16 Apr 2026 00:14:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 16 Apr 2026 00:14:11 GMT
WORKDIR /opt/drupal
# Thu, 16 Apr 2026 00:14:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 16 Apr 2026 00:14:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a92f446b809c904945a411bb67902b0fcb804dcda8f8530399a048c8d97d42`  
		Last Modified: Fri, 10 Apr 2026 00:17:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe65c199e5e12fd285c1fdf06f8db50e8751916ca67a06fea5299982f2e4d443`  
		Last Modified: Fri, 10 Apr 2026 00:17:03 GMT  
		Size: 119.0 MB (119028544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853284a3a27de8c8fa9a97529af03ba23f69a93608379868f50ee59e7e2bc66`  
		Last Modified: Fri, 10 Apr 2026 00:17:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca576676b87eb9db8fbe10b125ce6d96f8308f91f939ac7d95b83d9f8c9124b`  
		Last Modified: Fri, 10 Apr 2026 00:20:23 GMT  
		Size: 4.5 MB (4458590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62b183fba032246b7d8c27a1afcaf87b34bf5e9a37e6c412940cf7296f8feb3`  
		Last Modified: Fri, 10 Apr 2026 00:20:23 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc5fc03205d3ad7ead12e7590bdc0901a118749993b98bbdbbb41a0ecc35819`  
		Last Modified: Fri, 10 Apr 2026 00:20:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3c56d241949ef57e2cc0c2e7c7eeaaabc78ab3438d18cba7fc606beb2f27b8`  
		Last Modified: Fri, 10 Apr 2026 00:20:23 GMT  
		Size: 13.9 MB (13851799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb65be09d625f703f6ba916e419dd449ee3e55d1654c0bf37222784a21ab17f`  
		Last Modified: Fri, 10 Apr 2026 00:20:24 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0088c54638dbaca78ba5b0c7d80130b91c444b112a0433579314e66a8b3ed877`  
		Last Modified: Fri, 10 Apr 2026 00:20:24 GMT  
		Size: 13.9 MB (13858661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efde10b8a0121242527de07ccaa6c37e6dbfeec8c8dd001c76fc963bc4b843d9`  
		Last Modified: Fri, 10 Apr 2026 00:20:24 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0feed1df77199f6aba1e3eed14fe442c5a10afb54ee586577ff1fac2bfe4a5`  
		Last Modified: Fri, 10 Apr 2026 00:20:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b1110e6aa1b0ea3e9b2d611c2cafca7ba4bf3116a2ab03e897df1b02a0837`  
		Last Modified: Fri, 10 Apr 2026 00:20:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4663a865880911de827e46c618ecc0f010f4384dcccc337311c16d41e9b9c059`  
		Last Modified: Fri, 10 Apr 2026 00:20:25 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab51d04e1229d87fb9dff868a03285a7ed92eb337be8a68890face61cfd6e0a`  
		Last Modified: Thu, 16 Apr 2026 00:14:33 GMT  
		Size: 1.7 MB (1737924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9838fc97bbbbb3a20fc4af426206d46644e6c926acc8b1c7f24fca8964daad8`  
		Last Modified: Thu, 16 Apr 2026 00:14:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4ba1d1ad357ea50b95c28868f8e73b37957e77c2ec8d7ead9956aad8d2a334`  
		Last Modified: Thu, 16 Apr 2026 00:14:33 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fe14137037679036f322687ec225bac833b2a9c6330be1fd73ab4e72d49c77`  
		Last Modified: Thu, 16 Apr 2026 00:14:33 GMT  
		Size: 790.8 KB (790775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0e686d473f00e31088e3a5a8776aa36a475fc4c58c304062e2ad564cdd6ed9`  
		Last Modified: Thu, 16 Apr 2026 00:14:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93005e266e29606b323f42e0ac3f9dfa37a0c2da8097280fd05776c61b1d74b`  
		Last Modified: Thu, 16 Apr 2026 00:14:35 GMT  
		Size: 21.3 MB (21349742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:78f270e50a80c83d5e7320a54ac8ca86524659b3efd88a701bebd1986228a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62b420401ee340af7b3efee1fabc9da1709f17c1b81e9b1339a191616ec87ce`

```dockerfile
```

-	Layers:
	-	`sha256:f571a48c8005da0af21d7e1a0e1dfa70342ddbfb8d09b8300ef46b6ff6559af0`  
		Last Modified: Thu, 16 Apr 2026 00:14:33 GMT  
		Size: 7.3 MB (7316041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697198c1b260f9759f78cf8110038b8f644d0f4ec0c2581beb4e27d6440b39d7`  
		Last Modified: Thu, 16 Apr 2026 00:14:32 GMT  
		Size: 48.6 KB (48641 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:ed67d6b595a16facb82f14b6ff717873c64ae3998b6a09896b26510f99c192d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203563184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a25641840c6a41c0ac53f3a817dccae5d00ea906f6066a32348d16455b34be8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:52:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:53:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 02:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 02:15:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 02:15:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:50:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:55:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:55:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:55:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:55:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:55:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:55:37 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:55:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:55:37 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:55:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:55:37 GMT
CMD ["apache2-foreground"]
# Fri, 10 Apr 2026 01:19:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Apr 2026 01:19:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 10 Apr 2026 01:19:12 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:58:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:58:09 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:58:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:58:09 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 18:58:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 18:58:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9146bf73c8a452f415773cc4d7b28152e6a0132b4872c062036e93ceda4a1`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f4a0e07fb6454284581cfcdd933b1a8aeaf834a24a8768bd1bdee7fe76ac43`  
		Last Modified: Tue, 07 Apr 2026 01:58:49 GMT  
		Size: 109.6 MB (109599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e4f5187124bd689202e1c0b532dcdbfed0adfcf45354b5dcc246a80a88c8e`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c2826d5bd7597d2bc055cec74a30953477482f418eb99bc191b54a5657bea0`  
		Last Modified: Tue, 07 Apr 2026 02:22:07 GMT  
		Size: 4.9 MB (4881630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4711f0a1e700d515af14d521ed74bc330dbff10a897db0c88f1da3017c82e`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea076c7d43b09b2edeb333274a93e4615a067914cc9eb5a71e39816735581b`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dec351a1ea0e9f8260db0fe7f5d544d413ead98aa6f93faf52f5156bb42d56`  
		Last Modified: Thu, 09 Apr 2026 22:56:06 GMT  
		Size: 13.9 MB (13866829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f754301576436903c98219c1253480fba798fa000796d9db4f6011448f5160`  
		Last Modified: Thu, 09 Apr 2026 22:56:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b357d4da30965de24a959c63bc4844d6f6f5beb41154aab5e98cb072cd32d1ca`  
		Last Modified: Thu, 09 Apr 2026 22:56:07 GMT  
		Size: 17.6 MB (17628234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17fe5d72f918a62b30ed32340ee8d5cbbd95d30d46fd2d9f868466d9e98dfa2`  
		Last Modified: Thu, 09 Apr 2026 22:56:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd59e22820a87e6bdc0facc2a3223bc3c80db8152bfef03f17ea6d6137c1be3`  
		Last Modified: Thu, 09 Apr 2026 22:56:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8543dcddba6ccd9c73c4c19848d0c9fccd12afdd8e85a282bf1cd6198558483f`  
		Last Modified: Thu, 09 Apr 2026 22:56:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1582253340f81d8245e092973d69ddd30341420233cde15f2aa9bc04b2d52f7`  
		Last Modified: Thu, 09 Apr 2026 22:56:08 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2426d1f834b27198f98281169bca096c3e1ae0a28418b16e65bc169d4bcd13d7`  
		Last Modified: Fri, 10 Apr 2026 01:20:12 GMT  
		Size: 1.8 MB (1847790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3279074232a66cd13d527b5f0d32853c1ab1d3f56c000cd342b35d2faab352f9`  
		Last Modified: Fri, 10 Apr 2026 01:20:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85e1a192db0249a352861427486791481010ec1ea48ea98e87ba95cb1ef4c1e`  
		Last Modified: Fri, 10 Apr 2026 01:20:12 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71427b718b7f00f8f97c3def039846e508137241ebcf84c362ce82b9a2b7426b`  
		Last Modified: Tue, 14 Apr 2026 18:59:08 GMT  
		Size: 790.8 KB (790770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f993f2ec0725ef4424631b090be2fcb67eeb27494b57c8ab267cf33cc5c77050`  
		Last Modified: Tue, 14 Apr 2026 18:59:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6314867bf8241dd0671f6df09e57660f674bca3a5d1f984f9b687fd899f873`  
		Last Modified: Tue, 14 Apr 2026 18:59:09 GMT  
		Size: 21.3 MB (21349402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:83c74927fb0270adba33e6603a8b99b750bea0d8ef8ba784cff0ab796f9d03e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a049cc97dc50d35d3abd67c401d6fada93fffb8c13ab876900a6b82be29a4792`

```dockerfile
```

-	Layers:
	-	`sha256:053d7b65a7bfffe51c4b3007d1049bd1f40d645a74ac46790b50e448d8b276f5`  
		Last Modified: Tue, 14 Apr 2026 18:59:08 GMT  
		Size: 7.3 MB (7342234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b290a389a64bf7989c4e11eec07693f221b81fff0661ddd1f80897859317978`  
		Last Modified: Tue, 14 Apr 2026 18:59:08 GMT  
		Size: 49.0 KB (48968 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:2419c58446d454abd72747a282c3c18468c5e248aa3b80d1dd6071007da2307f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232488080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104eee791ee5fff00c1b57d322049bd6771090afe392df74e83c7996d4f4c52b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 11:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 11:52:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 11:52:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 16:36:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 16:36:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 17:30:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 17:30:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 17:30:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:53 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 17:30:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 17:30:53 GMT
CMD ["apache2-foreground"]
# Sun, 12 Apr 2026 23:58:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 12 Apr 2026 23:58:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 23:58:20 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 14 Apr 2026 19:16:41 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 19:16:41 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 19:16:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 19:16:41 GMT
WORKDIR /opt/drupal
# Tue, 14 Apr 2026 19:17:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 14 Apr 2026 19:17:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1748d653b8c3ed98b870438732aa56def2ef4f267a38a228a8d4e1a775744da`  
		Last Modified: Tue, 07 Apr 2026 12:53:25 GMT  
		Size: 4.0 MB (4031244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79c952e0710b8d660c2b70f3e9f2716a16833b628e3b2dd090af31c1cf7438`  
		Last Modified: Tue, 07 Apr 2026 12:53:24 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe6480453dd1cec4db695c1e657272ce31a8c86abec42383da6aa9846d7dc4`  
		Last Modified: Tue, 07 Apr 2026 12:53:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dacce83cf82615cd1d4a6c1a86cea6e40883d3a42ad8656c9b8763530155814`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 13.9 MB (13866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3323b96cffff08af8f445b80f611ebe68799371d01077775a0c3f4567380bd`  
		Last Modified: Fri, 10 Apr 2026 17:34:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e4e9e187467f7ffbcfe1cdf4d10ee90f6ee36da3b522274275365cc718ee0`  
		Last Modified: Fri, 10 Apr 2026 17:34:06 GMT  
		Size: 16.0 MB (16013910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb761f6a2a209495608bb857bb80d3d0d0aa4de2fb075e52945a24da89addada`  
		Last Modified: Fri, 10 Apr 2026 17:34:01 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ced9f37602f905311a1e2a29a005c079a57757cdbf7e7fb075022b1a0f660b`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494a5659332e0f15ed2f4d61e062b27c51744e0fa85863035bb125c624a2ad0`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6cee257162c3d59f0cd7d2be13c20ecd7f6bf71c712eecacc44cc33a5fec83`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1ec1dcabb72fdf1fff1899e95cc28eeeb080a92202265393c30e998755f38c`  
		Last Modified: Mon, 13 Apr 2026 00:03:48 GMT  
		Size: 1.6 MB (1574702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cc5d13f405029f9ccb37f237b3febd6e19ce6b4ee6a642406a790be72e6a01`  
		Last Modified: Mon, 13 Apr 2026 00:03:48 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6ebc987c3bf77987507513cc22dc6d877338860f15e35bc574f8c3d480e16b`  
		Last Modified: Mon, 13 Apr 2026 00:03:48 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa970d92091989717169fbb8f48967e4ca4184c702272acc7ca6b2605a73363`  
		Last Modified: Tue, 14 Apr 2026 19:22:18 GMT  
		Size: 790.8 KB (790773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12e0c83ace679a84802a9e3ac97381cbde2a63c4ee8f0544c31d490f8f5b0bd`  
		Last Modified: Tue, 14 Apr 2026 19:22:17 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e7a5237b1514d80ad863d4eecc4e76bcbd343e31e8ee6982a1c8727feab679`  
		Last Modified: Tue, 14 Apr 2026 19:22:21 GMT  
		Size: 21.3 MB (21349457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:10590d023009651bc16caaf61ba6c5d2134a3207d11e443eb008e6a64ae209b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541a4b8503034395b2eed4131ece704964ae39ad2125cfab7f4f080131209237`

```dockerfile
```

-	Layers:
	-	`sha256:a577b0fd0699f3d0d3f57839af39d1212e6eae52c88ba8466adae2e5fa70023b`  
		Last Modified: Tue, 14 Apr 2026 19:22:19 GMT  
		Size: 7.4 MB (7414231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05d8ddf887abcb59817cd5565f2e6fe6276dbbbd3d0c82b9dccbc8eaf9653476`  
		Last Modified: Tue, 14 Apr 2026 19:22:17 GMT  
		Size: 49.0 KB (48967 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:a5f57f1f463393406ce74c20f6c41e70acd13371161829e95b4ba783847bfa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180807940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac94a292cc4d2f608b3abf68ff732432ee8f05fb6901829dd88fc7ba0614bc1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:26:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:26:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:26:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:26:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:26:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:26:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:28:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:28:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:28:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:28:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:28:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:32:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:32:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:32:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:32:31 GMT
CMD ["apache2-foreground"]
# Tue, 14 Apr 2026 18:58:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 18:58:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:58:18 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 14 Apr 2026 18:58:18 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 18:58:18 GMT
ENV DRUPAL_VERSION=11.3.6
# Tue, 14 Apr 2026 18:58:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Apr 2026 18:58:18 GMT
WORKDIR /opt/drupal
# Thu, 16 Apr 2026 01:00:10 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 16 Apr 2026 01:00:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba7c97d634db0bf7b04319d896d93eb13e70bc5e2a5daf23b3c4b5710f3acc`  
		Last Modified: Tue, 07 Apr 2026 01:29:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f5aba2e62a8aff95377ba1541ebda00e243f039e8a96124c4029b535783f4`  
		Last Modified: Tue, 07 Apr 2026 01:31:18 GMT  
		Size: 92.6 MB (92573092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1830f35178a510aae66fa242c825ad8540d4f3add9ceb7ccacf66e1bb9da043f`  
		Last Modified: Tue, 07 Apr 2026 01:31:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b301ccb75c77960806c0ea37e92e1b99243e9a8d687bfc6db319970ac91f9c`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 4.3 MB (4344650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf23a194a95511e11697de8599bd15c2e7d23e82439849817ff4ee0545a6810`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f2358fea68d2f11fcbcec43f2eb9742f1eadd4a93ce25b7e68f23cfb85aa8c`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991dd16132fc94a6d52d5107f9776c86dcf8caae024f764f06bc885d575cee`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 13.9 MB (13851076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87d5a1b93460e311218f5ac3e87631522b4433142da175d424f6bd320df4e94`  
		Last Modified: Thu, 09 Apr 2026 22:32:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb95cde67f1742edb7cccfde71f78bbbe935107625ddb21ba1724d38435a99a`  
		Last Modified: Thu, 09 Apr 2026 22:32:50 GMT  
		Size: 16.4 MB (16380506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97d4a74df6527bcd960fce4094c8e1c27291528451064ea3faa896ac2c1c1b0`  
		Last Modified: Thu, 09 Apr 2026 22:32:50 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefc446184137fe33299c034d9cf46ba3572475c9efe360f211417e8e418bb9c`  
		Last Modified: Thu, 09 Apr 2026 22:32:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724e29eb6c04410dbb77ffce8a97ab6d3df5233bc2227d951d39d5f0a9c94cfe`  
		Last Modified: Thu, 09 Apr 2026 22:32:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885828dad5e6c28eee98a5b07f7316a15c2969bd0a4c4e961e0ddd32c0ff6aad`  
		Last Modified: Thu, 09 Apr 2026 22:32:51 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524e622c69aac60880e07fb3ad21d0f11d5e8325ffc410e78689979c731099b4`  
		Last Modified: Tue, 14 Apr 2026 18:58:58 GMT  
		Size: 1.7 MB (1676511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec1432b2a8ee544b0bcdb86386981c8e483760575ab281324bc35e7695fdb08`  
		Last Modified: Tue, 14 Apr 2026 18:58:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1110c33ed936e937a18c68eb66ce52fe8b3d514d9f3a866d31d38f3ec181e89`  
		Last Modified: Tue, 14 Apr 2026 18:58:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfacc41738f2b4316cdc0964d12db94fad8868e6c6378e9fb2f2c9fcd7074743`  
		Last Modified: Tue, 14 Apr 2026 18:58:58 GMT  
		Size: 790.8 KB (790769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5d72d38990a10d34d90b3eb1aebaca541dbe882197305bd3aac7d1912d258`  
		Last Modified: Tue, 14 Apr 2026 18:58:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acce8a420cdb0af96bdcd05b9a9a78ef69dc6a91cc3b193fc4a85775685bb35`  
		Last Modified: Thu, 16 Apr 2026 01:00:41 GMT  
		Size: 21.3 MB (21349487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:c2fd66ffba17ba7312cd0151d3c50ef5942aea31d81d2c92a733a4974dc8ed5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cebb6380173cc9c29a943f01a4e221da033a560d87a792306c3bd37481c8e3`

```dockerfile
```

-	Layers:
	-	`sha256:cd6947ea18eeaab74a5845fc84eee6d00543533b1f2f79b8eada8e4971f5370e`  
		Last Modified: Thu, 16 Apr 2026 01:00:41 GMT  
		Size: 7.2 MB (7159539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c35de87e32493ea499d01ba7e2cf1c2b899379dce412d2939b4d809135cd7ad9`  
		Last Modified: Thu, 16 Apr 2026 01:00:40 GMT  
		Size: 48.8 KB (48780 bytes)  
		MIME: application/vnd.in-toto+json
