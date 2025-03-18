## `drupal:php8.4-apache-bullseye`

```console
$ docker pull drupal@sha256:564e5249b731d255721a25bc6c7267fa26907ebb9222d3ded5ce20885a845117
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `drupal:php8.4-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:07dc40931d7137f90842581041fd8fa770c3aa515975b6949ffeb87fbf25ce2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191450516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae72209243637bed7e4f077854c69f15b3c9f81ecf9d29edf98065d5c38ee36`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Mar 2025 22:53:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:53:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.4.5
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:53:13 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Mar 2025 22:53:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:53:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Mar 2025 22:53:13 GMT
CMD ["apache2-foreground"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714f06bc7863c57e375926cb29692675f6fb66fc16e71fef7b832fe8d30e430`  
		Last Modified: Mon, 17 Mar 2025 23:17:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c4e1b70e5e1c567a3261d5d6769a01b5ee1901a3755c9d3b3bee9a32efa187`  
		Last Modified: Mon, 17 Mar 2025 23:17:32 GMT  
		Size: 91.4 MB (91448528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5878794ee70cbdcc3c0197ef31e66c095601483f55f3eae5370177ea984c3115`  
		Last Modified: Mon, 17 Mar 2025 23:17:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc690edb25b8e856d907bc96dba047906008543d0422d2d37b507cad5325b23`  
		Last Modified: Mon, 17 Mar 2025 23:17:31 GMT  
		Size: 19.1 MB (19064229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f990cc1e421111416c62fb43e62d661fc79fad1885ab6b17ae0e4318c681664b`  
		Last Modified: Mon, 17 Mar 2025 23:17:31 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6620fc6d0be980600b970d7f1bacd37bf34e6093c6d360877f0773e0c52870`  
		Last Modified: Mon, 17 Mar 2025 23:17:31 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca531c98dafafb6e0efe0b00560b4b76eb33bcf02037c50d0616d4f5247fc60f`  
		Last Modified: Mon, 17 Mar 2025 23:17:32 GMT  
		Size: 13.7 MB (13730040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875a3f480929299f42b3606c9aa6278a9b9cc9ca7d6dcdf2a8c43244d72e35d3`  
		Last Modified: Mon, 17 Mar 2025 23:17:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9b1aeca8cacd2dbfdfb7b6975bdcc574f9298f28d1906a83aee98e44a9b49`  
		Last Modified: Mon, 17 Mar 2025 23:17:33 GMT  
		Size: 14.1 MB (14085808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb4f9866d1edcb2c3adbe807b48de223232f439c8444a1a0d9ec742ab7be73b`  
		Last Modified: Mon, 17 Mar 2025 23:17:33 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4bec24c93433930321e2af4ff44462035c70eb78fdb02aca1cd2028982659`  
		Last Modified: Mon, 17 Mar 2025 23:17:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc67e3e877fa1e291e7e3f2853a4fdcec21da5f16df3ca418c777b22156a47b`  
		Last Modified: Mon, 17 Mar 2025 23:17:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9659b3aae30a55953f299ca52554015e670a04aac4730cebbe938ebdb0d9`  
		Last Modified: Tue, 18 Mar 2025 00:20:13 GMT  
		Size: 2.1 MB (2059350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ccae1c31265a970f1d1134e296d2aed0b318336da5690867a496160beed010`  
		Last Modified: Tue, 18 Mar 2025 00:20:13 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab874d11ecf14933e0862233951b057394f5b66c3ee0f45aa8719822f448a8`  
		Last Modified: Tue, 18 Mar 2025 00:20:13 GMT  
		Size: 740.8 KB (740825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca572992b2141a2e457356bfe63b0dce5ed95266a7546b9b7dfa945a2a8d63b0`  
		Last Modified: Tue, 18 Mar 2025 00:20:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72620ad43aa1dbf5696c54e40302e16827e9b39347244c30836d375eac9430c3`  
		Last Modified: Tue, 18 Mar 2025 00:20:14 GMT  
		Size: 20.1 MB (20062008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:de91fca17a028c93f87a708c053c2e223a98e7e69191f36a0fe33fa0f806c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7071824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407cda9ead194932868c5e0bc9bed7111347fec2445e706e89cd21c513bc14af`

```dockerfile
```

-	Layers:
	-	`sha256:fa5a38b663b5d56608e5a96081ee4c568711d03945b2d3c66e2855c425f501e1`  
		Last Modified: Tue, 18 Mar 2025 00:20:13 GMT  
		Size: 7.0 MB (7035141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839e5abc3b3138397f0ff81c92992aa4cd69250ec12515df15e3288cbc91eac3`  
		Last Modified: Tue, 18 Mar 2025 00:20:13 GMT  
		Size: 36.7 KB (36683 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:8147dba68acab5c5a3ebd2db061634297be5768299eeb52447f6e800beb9048a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160589539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25103108e09a1630497eb83cacb1f0582d4703bf39e084443e00e98f795d974`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Mar 2025 22:53:13 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:53:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.4.5
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:53:13 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Mar 2025 22:53:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:53:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Mar 2025 22:53:13 GMT
CMD ["apache2-foreground"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3687c9079028ac9bf763326f4be55b4e440b37b5baf0c4529715d811c7ec1718`  
		Last Modified: Mon, 17 Mar 2025 22:19:22 GMT  
		Size: 25.5 MB (25535344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1025fe025af769b6936ee3ed06b13f60f6c4df2ea57a88d17e56f673ea45b6`  
		Last Modified: Tue, 18 Mar 2025 06:34:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c44daab001583fce063841032bb6ea652620064ab9fbf7d880588eaf67c75b`  
		Last Modified: Tue, 18 Mar 2025 06:34:43 GMT  
		Size: 69.1 MB (69119208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff841f7831550381d69a8f1bf31c3b5a47d736c2f6a95a57f029a70b9f2ba3ea`  
		Last Modified: Tue, 18 Mar 2025 06:34:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3820dfc98d59eecfc435663aeef071e4cd3a185c11c95fb306b3541f07ea6ca8`  
		Last Modified: Tue, 18 Mar 2025 07:33:39 GMT  
		Size: 17.8 MB (17817117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5693b515125ea6a0aa248f7e033223d4b2967f70f5cf1be77e196aaf38331d`  
		Last Modified: Tue, 18 Mar 2025 07:33:38 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a3e2077b9803e8dce2ee34a6c0340efb25d0a1243736af5195b1a593c69fc5`  
		Last Modified: Tue, 18 Mar 2025 07:33:38 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3882eb3f285fab662f58fe4536a479c64a162c98c87cd12b9c837faf31567d`  
		Last Modified: Tue, 18 Mar 2025 07:33:39 GMT  
		Size: 13.7 MB (13728416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4138d7383b4a67fc87578d2eaebe265d094c9bea9aad9970061d32a3df62658a`  
		Last Modified: Tue, 18 Mar 2025 07:33:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cadbee26019caa34302c1996e6dd522f7fb498bb9ff946b58fe07dd9d264dce`  
		Last Modified: Tue, 18 Mar 2025 07:33:40 GMT  
		Size: 12.3 MB (12260859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f1305e99b6351ad520062270cab9ac3183a899a0d4bdfc271715582fb9a8c2`  
		Last Modified: Tue, 18 Mar 2025 07:33:40 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3409db61116400af88acfa88718757a376a8436eff35de284777364aa1770318`  
		Last Modified: Tue, 18 Mar 2025 07:33:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32133a579c7e5b18bceb0e0ad9cdd26c814d2e93d323766e5146c637d1d93b1`  
		Last Modified: Tue, 18 Mar 2025 07:33:40 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9874b2dce42ae70ae630564821c444087f8988ca30803a8960773463903b2f7d`  
		Last Modified: Tue, 18 Mar 2025 15:44:24 GMT  
		Size: 1.3 MB (1319148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7747be8de02a38028ca446afe22dd2ab6f04e7cf7745e6de4ac65bca5379201b`  
		Last Modified: Tue, 18 Mar 2025 15:44:24 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58222cadf04427e704ee3b4eb37c51a08fe13c9656f0583d207e423152297b7b`  
		Last Modified: Tue, 18 Mar 2025 15:44:24 GMT  
		Size: 740.8 KB (740824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3553d5c6ff93ad9f759399b92dcdddc4289bbf0ad88cbd3f5e4d948c6ed509`  
		Last Modified: Tue, 18 Mar 2025 15:44:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bea7a2ec5f358d3d387d410ecc6fef26d1360c909b726cae739d75fee20dc1`  
		Last Modified: Tue, 18 Mar 2025 15:58:14 GMT  
		Size: 20.1 MB (20062712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:456126b7e4ca88af534e9bb577ddbd3b25c2f0aebf4f3358a6e7b81df0f949e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6880844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e89f869b0260242cfc19f09b0b724be00e64cc916b0d99df78ce69aa988689`

```dockerfile
```

-	Layers:
	-	`sha256:4ef9d2b547fd6d81e5d483aae50f550e9e9b39b535fab8589c53c354e9ea7fed`  
		Last Modified: Tue, 18 Mar 2025 15:58:13 GMT  
		Size: 6.8 MB (6844037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2d0255abde8dd5d35ddf47dc6e7efbf1931ec442014357d30cba69c8ccfaf5`  
		Last Modified: Tue, 18 Mar 2025 15:58:12 GMT  
		Size: 36.8 KB (36807 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:b9574870c6a0c45881b95390677edefb3de5a16c314a87ae1e891b584b8479b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184733411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c087bd0a5ac75b51151b382e5ecf062e09c47ee922017797e2d38b16cdae38`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Mar 2025 22:53:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:53:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.4.5
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:53:13 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Mar 2025 22:53:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:53:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Mar 2025 22:53:13 GMT
CMD ["apache2-foreground"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30a4b98d6d9d341325155385916d7532526ea08768653b48f2722f278a8d43`  
		Last Modified: Tue, 18 Mar 2025 05:31:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb0e83a8ad79344475695e51f2489c2d8cf5877a26fcded29b10154759542f1`  
		Last Modified: Tue, 18 Mar 2025 05:31:09 GMT  
		Size: 86.7 MB (86734007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80f21d828c5691e64bf7ff33432f2bc2b409ac5eb2fbbdd42b81f7c20557c38`  
		Last Modified: Tue, 18 Mar 2025 05:31:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577adf86a70349470def3c36906fb60b4b5ddfffb961d43ffa7ac9aa4404c094`  
		Last Modified: Tue, 18 Mar 2025 05:31:08 GMT  
		Size: 19.0 MB (18981509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cd473bc5275ce03133dbd2c85f8a58dd5605e869a74f6730992e65b5e2db03`  
		Last Modified: Tue, 18 Mar 2025 05:31:08 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4e8c4c72476e5f880737fb14a8a595975239ef8ad6a2ea5c6d4a25b73fe7b`  
		Last Modified: Tue, 18 Mar 2025 05:31:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707944d9cd5286a9403157e4ea92330f6f886c38788c80e8ff45ec3269213ec4`  
		Last Modified: Tue, 18 Mar 2025 06:23:16 GMT  
		Size: 13.7 MB (13729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aedd008c85077acba66f2fa07572f50d0d2f16dcccd0bb432b76bc596c78f7b`  
		Last Modified: Tue, 18 Mar 2025 06:23:15 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fd595836e57fb70cecde3c0340bca6eed0e88857492ca884341ade8a15adc9`  
		Last Modified: Tue, 18 Mar 2025 06:23:16 GMT  
		Size: 13.8 MB (13775729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca58e227dc2f41db99a52798919a7de2d652d915ed8cdb1ac94db66790ad84`  
		Last Modified: Tue, 18 Mar 2025 06:23:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e56843cf379def0d44d1dbe375b26b991215fc6b2d2bdb42e69a04d8c8570f`  
		Last Modified: Tue, 18 Mar 2025 06:23:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26246b14264be1309b6ede42b248bbe83f21493e87bacecd1fa227a4437ffa82`  
		Last Modified: Tue, 18 Mar 2025 06:23:16 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb41640396e31f97dbc7dbb55f54edb51ab2074a08a224a2ff57eba0078042d`  
		Last Modified: Tue, 18 Mar 2025 13:16:43 GMT  
		Size: 2.0 MB (1958103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b67bfd4bb3fd82f17d6d1e5c016a2d041ef46241c0d2782ec707bebe8a62d5`  
		Last Modified: Tue, 18 Mar 2025 13:16:43 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4db8376680ed049d0c07eb6f3b5a6a25f92c1c9421f38d53b9ddd7c3a7e6da`  
		Last Modified: Tue, 18 Mar 2025 13:16:43 GMT  
		Size: 740.8 KB (740824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c517c5625c6d8c00f907cc945ce4a42f77b3e6e84ba506b066eeacc492e937c8`  
		Last Modified: Tue, 18 Mar 2025 13:16:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a870fd6952b3a041eea407566c07f09f3f0d880603479edb4aee2328485610f9`  
		Last Modified: Tue, 18 Mar 2025 13:24:47 GMT  
		Size: 20.1 MB (20062161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:267fe5b69fe6dea947dadfe30dbe18a026893354a3020cac9e353a2038191c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7074780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308fcabb89a0e7fb3526ba44b9fa29db9e37bc88110ae59552fac51b9b334e73`

```dockerfile
```

-	Layers:
	-	`sha256:6173aea2c33d857cf7e9db91924b0606fa9e519616f85967aa0d09d86c164c24`  
		Last Modified: Tue, 18 Mar 2025 13:24:46 GMT  
		Size: 7.0 MB (7037937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a14f9ad338ba809e3def19bb7988b489fa3ba1bf9a0f7a5a657ef78b14bb050`  
		Last Modified: Tue, 18 Mar 2025 13:24:45 GMT  
		Size: 36.8 KB (36843 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:00181bc77ff6a2001420870f7a11c8cce50910e46dc6aa15881f32c072700cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194332391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9495757448048aae60279e1691eb15dbd85d6807a491b707f9a02cbee500d258`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 05 Mar 2025 22:53:13 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 05 Mar 2025 22:53:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:53:13 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.4.5
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:53:13 GMT
STOPSIGNAL SIGWINCH
# Wed, 05 Mar 2025 22:53:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:53:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Mar 2025 22:53:13 GMT
CMD ["apache2-foreground"]
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV DRUPAL_VERSION=11.1.4
# Wed, 05 Mar 2025 22:53:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:53:13 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:53:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2d1b54a8c4ae00795db4c06d288dd9a516dd08d1d002fe1f9817d872d5228c`  
		Last Modified: Mon, 17 Mar 2025 23:30:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d92aba006d69619a61b3eeffa178b1b831757db6635cb10b7799100ecf534a8`  
		Last Modified: Mon, 17 Mar 2025 23:30:16 GMT  
		Size: 92.5 MB (92521353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616b21176145736007345c67b3cd429464c323ce0d479ec916868624912cfdf7`  
		Last Modified: Mon, 17 Mar 2025 23:30:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c539a677f1892c0cff55fd8c6d868359396a19784ed53764e5edc2c25fcb8acc`  
		Last Modified: Mon, 17 Mar 2025 23:30:14 GMT  
		Size: 19.6 MB (19552727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd27570d4121deac2fc98c514b5bb742ef00dd5de2d908616fab32fcea6306`  
		Last Modified: Mon, 17 Mar 2025 23:30:14 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f790dc4c74e49d5c0c859f89113c06b165bdbf4e83f0a486f486cc9fb573699c`  
		Last Modified: Mon, 17 Mar 2025 23:30:14 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e34d970d2e33028676a126d0569c313692cc0e87c2073742418a43dcab0087`  
		Last Modified: Mon, 17 Mar 2025 23:30:15 GMT  
		Size: 13.7 MB (13729244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df9cc8f0bea1aef93b2973282c701413d1f23b17579b5f1d3553ce6b73e997f`  
		Last Modified: Mon, 17 Mar 2025 23:30:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae078f506c4478f275c871b2cc8559d0cee2c5586dcaabe3089c185d2820a86`  
		Last Modified: Mon, 17 Mar 2025 23:30:16 GMT  
		Size: 14.4 MB (14378483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b7579a8bb07e63122be61bf4e3dbdc50de9bc5ebc35d4bcb032bc451b28e42`  
		Last Modified: Mon, 17 Mar 2025 23:30:16 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd82d1f3a943fc12360bfd375361e3949cc84b5e5bec14ee19a1ddb4b85725`  
		Last Modified: Mon, 17 Mar 2025 23:30:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f4f1887c579ff8eeb445834470d333e1fb7dc8821f6fa9d6532a60dc6e42d8`  
		Last Modified: Mon, 17 Mar 2025 23:30:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502ced0db3e96e94ac1ca0800d6648edb5091ee4809842b8a2f837141bb7e49`  
		Last Modified: Tue, 18 Mar 2025 00:20:46 GMT  
		Size: 2.2 MB (2161555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b7eb94cbb2a3116a12ddd5413145b5f1b67e74255b69ad064880566ed017b5`  
		Last Modified: Tue, 18 Mar 2025 00:20:46 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea6c79c155c93a7d5fd2c1c4d3bf2a3ad348370241e081851507a8bc77dee76`  
		Last Modified: Tue, 18 Mar 2025 00:20:46 GMT  
		Size: 740.8 KB (740824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1819faea5ae917ac148a05506b9a158c76f27fd4349e8d12cc44812e0c4462`  
		Last Modified: Tue, 18 Mar 2025 00:20:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a04dffa9b9558ac5b3fc0aae9ea02d519031195fa728049ea81ec64a69cf89`  
		Last Modified: Tue, 18 Mar 2025 00:20:47 GMT  
		Size: 20.1 MB (20061978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:3fd7f908cb1a0cae7e68f7c5fc113191da9765cec3dad2d5253051a23bbf52a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109505fa284e75aa7b1047abf154895e2d4034b1216443b352cf52736126f3ec`

```dockerfile
```

-	Layers:
	-	`sha256:c9c0154bb5e00fd8a06e19af19ef617bf9858065155fe47eef7e42924fe2cb53`  
		Last Modified: Tue, 18 Mar 2025 00:20:46 GMT  
		Size: 7.0 MB (7025743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2f6844c5720bf322638b9bf565763087a3a91fc605a9447bd84e3f81f9d7ce`  
		Last Modified: Tue, 18 Mar 2025 00:20:46 GMT  
		Size: 36.6 KB (36638 bytes)  
		MIME: application/vnd.in-toto+json
