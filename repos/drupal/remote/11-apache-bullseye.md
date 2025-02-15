## `drupal:11-apache-bullseye`

```console
$ docker pull drupal@sha256:72e97d7cc4feaa3463282e581aea9177598a449043118e896ca0cbec74844158
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

### `drupal:11-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:931b34a017f46ca0e22e9b2f27635b6c7ddbbb3de823296d16088ca93884bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187764950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef286e3a654b047a3f2f2cb9c1abce002893c539e80c4e41cef7eef951118136`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 05:02:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 05:02:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 05:02:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 05:02:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 05:02:24 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9e246d5aaea0fc69685b5aea207f2a16838519cf7892ce4df249a06f7a96f9`  
		Last Modified: Fri, 14 Feb 2025 05:09:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d418715d9a3f9d8e7ccc4401fa223b74d1e5a01d8d825c8fd8967887b02644ba`  
		Last Modified: Fri, 14 Feb 2025 05:09:11 GMT  
		Size: 91.4 MB (91448796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe151abc6d942eb1d891a141c273902a3caf3941cf65dd785a303571fd4dd8ff`  
		Last Modified: Fri, 14 Feb 2025 05:09:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c326e668a50af3bc8ba29989cffeb38c833ec443c8bf03b000c57a610745cf9`  
		Last Modified: Fri, 14 Feb 2025 05:09:04 GMT  
		Size: 19.1 MB (19064369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67db1d647814105a8545f0987221bf8bf6b6ec1c17349b57d5326a5a32de1fb`  
		Last Modified: Fri, 14 Feb 2025 05:09:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b37c3a634ca5326cadd7400ba975b52b7f16bd4b8b5567d63a1047eaef1c54`  
		Last Modified: Fri, 14 Feb 2025 05:09:00 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5475812d779b7b1cd1cc3b6a25b755e53e8f1b9e13ce1b378e85121872b07e`  
		Last Modified: Fri, 14 Feb 2025 05:09:01 GMT  
		Size: 12.7 MB (12666623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57600eeb45a9c63eff55ec6521d6c169fc095dab16320b0857f297052ad5331`  
		Last Modified: Fri, 14 Feb 2025 05:09:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9340f5552afe2b3ed33b8719a4d87b6803b6c01205dce56b12382b908265a3`  
		Last Modified: Fri, 14 Feb 2025 05:09:01 GMT  
		Size: 11.6 MB (11593109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f78a35f38bdc65e06053ce24b513b775d154e20c8cefb2cd756cfec27c1586f`  
		Last Modified: Fri, 14 Feb 2025 05:09:00 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f2b1cabde8981d627f727cfdf7dd033126af11061ad83be94c341a7599da29`  
		Last Modified: Fri, 14 Feb 2025 05:09:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911582984f6f644bebdf4356162cdb375401c0d830bb80f73312005e16e71689`  
		Last Modified: Fri, 14 Feb 2025 05:09:00 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c1ec73d228ab7b206321cea4e93d1ff2e1e7dd0615f6de7a7987e09d998fbf`  
		Last Modified: Fri, 14 Feb 2025 21:12:56 GMT  
		Size: 1.9 MB (1932984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19f315b72c7fbfd5a188551e3e19c34c7c918a652ba20f0ab49bac01f710abf`  
		Last Modified: Fri, 14 Feb 2025 21:12:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90f7ba7008d9e282e768927d131766d5e4798ff6cad54be9230d53fa549cfa7`  
		Last Modified: Fri, 14 Feb 2025 21:12:56 GMT  
		Size: 740.4 KB (740352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de63b6126043b50af8fdbc6ee306e1d5f39813082ef07612d95da5e2ce337047`  
		Last Modified: Fri, 14 Feb 2025 21:12:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ec2147d7369bbfd8d9334aa487e0a49d71f537e51f9dde9d2f4c6cf19b3e3b`  
		Last Modified: Fri, 14 Feb 2025 21:12:57 GMT  
		Size: 20.1 MB (20060227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:774b3ccdfadfe445db9cbec3411003e4225a3f2e693d75f547c3681f8c570734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7063127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc49594bb6cf606c9866f6580720d8de6e9d38a0e92fdab18ae6ea8d2cc95f6`

```dockerfile
```

-	Layers:
	-	`sha256:8e96e7d23008995bc5cb8f9d4deba3f1324f2511d80afc760596637be68e13cd`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 7.0 MB (7025141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10e1bd580a9124897e97285ad401836bf3c14a9eee3f75cdc7a2e32febaa232`  
		Last Modified: Sat, 15 Feb 2025 00:01:55 GMT  
		Size: 38.0 KB (37986 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:611c9b39ef57735ca74dacb89ee835d581ec4799a5dbacd62716fe5753fe3e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157277710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c8f3ab780a97cdf903c8c040e999b7c1c31eead78ab2d815566ccda122fd77`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 05:02:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 05:02:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 05:02:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 05:02:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 05:02:24 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 08:24:31 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9f22afe418a45c031cf43983b6e05c8ed9b386411bd488f375251dc4089c49`  
		Last Modified: Wed, 05 Feb 2025 04:33:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20b645f918db98d26680f3077f4791bf599ff64dcf689b13a40c8243399e230`  
		Last Modified: Tue, 04 Feb 2025 20:06:32 GMT  
		Size: 69.1 MB (69119296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03588c4764681ba1b285def08d8bf43afd148e8bc56a103b85f5ac8fd68cd75`  
		Last Modified: Wed, 05 Feb 2025 05:50:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011d0e07a08551756fc0d9251dd7d8adcb43b54b55f862230c27cb52281d3c0b`  
		Last Modified: Thu, 06 Feb 2025 05:50:25 GMT  
		Size: 17.8 MB (17816973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e5d87506fe5f9d0f2478db889ed9a97ded17fd651aa1775559280fe1356590`  
		Last Modified: Wed, 05 Feb 2025 05:50:29 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723307e39c6c36865316265914b7178ea59e979eaa4e029b7a48851b408e44a7`  
		Last Modified: Wed, 05 Feb 2025 09:57:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174803f82b42d38fe342260e702f0853adc566c96b12f00d5e419a6c5a8ed74a`  
		Last Modified: Fri, 14 Feb 2025 12:56:20 GMT  
		Size: 12.7 MB (12665279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81af66c3cdbdcdbed5122a62e5260e38d14ef8a1d866c17aacdc97b4413bea1c`  
		Last Modified: Fri, 14 Feb 2025 12:56:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c79f20ff8b29d632dc7b8ea9312e8446e3d67d7791fa9891bbe3b391e39d811`  
		Last Modified: Fri, 14 Feb 2025 12:56:23 GMT  
		Size: 10.0 MB (10022663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee128a62fc61cc7a055da41e3d5e019e20137e0826df2771c76dfec58efd114`  
		Last Modified: Fri, 14 Feb 2025 12:56:25 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee52cba0d3a2b83468bc595bcfc47528e600247ddca3e4db72aac2a7d11cfd2d`  
		Last Modified: Fri, 14 Feb 2025 12:56:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9835ec5e6ad19ff4f16e2a69336b327919ca77213ca7b6529188b52f9e5e7f`  
		Last Modified: Fri, 14 Feb 2025 12:56:26 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89fa5111c23e8bd8680e1193306c9ce8f50f8e72a1a10264b61c2a7480a831`  
		Last Modified: Fri, 14 Feb 2025 08:19:24 GMT  
		Size: 1.3 MB (1312075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4ff9a6d55a642f6ca6edd99325076bd5f024cfec8797a724dd69c3085c5c0a`  
		Last Modified: Fri, 14 Feb 2025 08:19:23 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd9a3ea1bdb665acb2b47204914914e3e888b6b48178bfa64bc59eed6b93a25`  
		Last Modified: Fri, 14 Feb 2025 08:19:24 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2574442c4324a53cf272f66f4febd7db9bcc56dc7f2165163ad8c0d8ec0d42`  
		Last Modified: Fri, 14 Feb 2025 08:19:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfce73d7dac4f96a3565ac3c8a84374452f5092a96c0c60890347b0bde3b3e42`  
		Last Modified: Fri, 14 Feb 2025 08:19:25 GMT  
		Size: 20.1 MB (20061277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:3e5b66b6b7f11a5867c6e9bf10a65950cab8fd3950812cbece530d7c0fd567ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6883510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc5a2ae9770ec3b2219f0b15a825bad86431163de3070171c3f74a82f617beb`

```dockerfile
```

-	Layers:
	-	`sha256:aeb5aa58a9ebddcd774830cd44d28821e0e9823bee707d6878c3c5615c40e164`  
		Last Modified: Fri, 14 Feb 2025 09:13:13 GMT  
		Size: 6.8 MB (6845367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beed2666db13067d80435a8ab00d1d0c86df57cd1c0e10d03912ad89b4870197`  
		Last Modified: Fri, 14 Feb 2025 09:13:14 GMT  
		Size: 38.1 KB (38143 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:341c29c8d460b75629c8ee636001d0fa2fb0a8f838246d28561fa940a797172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181788332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d22587a607db092229f9bd2a1d158f32cded6bca1d3a7f03585da33e3b1096`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 05:02:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 05:02:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 05:02:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 05:02:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 05:02:24 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f170b18fc37f37ecc87975e5944875fd3d007167024e0f8a586c70f59364c2`  
		Last Modified: Fri, 14 Feb 2025 06:05:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9877a67bcea947fd28896ce8ce4388d08d8eae5ea20fe294649dcd55f6253c`  
		Last Modified: Fri, 14 Feb 2025 06:05:11 GMT  
		Size: 86.7 MB (86734370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4bff070cb9c3aa82cac65e78d2b37dc73ac5f5518d9eef698f9ef5c2dc618`  
		Last Modified: Fri, 14 Feb 2025 06:05:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07124adb1d9b97db6d688feed5df86faaa1d4e336db6f7eb6286181761eeb742`  
		Last Modified: Fri, 14 Feb 2025 06:05:08 GMT  
		Size: 19.0 MB (18981147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d92e0cfe925cb5172c8c47b5b8748909ce3ba205a61e1b822bc1098f0acd5d`  
		Last Modified: Fri, 14 Feb 2025 06:05:08 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe9521d4d77bd33c8dec7224d364cbac56032849b7ea68a92683a653b4aa551`  
		Last Modified: Fri, 14 Feb 2025 06:05:07 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec254ce14b748b0346202a305c293c45c86dc591b6905b4c7d83c04c1e23610`  
		Last Modified: Fri, 14 Feb 2025 06:05:08 GMT  
		Size: 12.7 MB (12665998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab5639009b5288d3e7fdf0677e134d6f6d6e86a93eea74d8b1d338b1f3ec5a4`  
		Last Modified: Fri, 14 Feb 2025 06:05:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9a89d3e0b1d909eaa76a1048f5f01aa35ce3af3f36a66adfeab1afad86185d`  
		Last Modified: Fri, 14 Feb 2025 06:05:08 GMT  
		Size: 11.7 MB (11658079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3044c8862c85850f1fb84382938a8d214e4a945a86a83ef913770b62edccae83`  
		Last Modified: Fri, 14 Feb 2025 06:05:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e149769c7e24bfc7c004560e1801c7b6de847d40763ae399def1f65bc1b195`  
		Last Modified: Fri, 14 Feb 2025 06:05:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4e46a2015f30ce4dad93c33d78cbda938149edc2b8617a2e342257cba3c8eb`  
		Last Modified: Fri, 14 Feb 2025 06:05:07 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbd67d00243b5230a25642e55ec83606d055d5091d6561e716c8f3adc70cb93`  
		Last Modified: Fri, 14 Feb 2025 08:39:51 GMT  
		Size: 2.2 MB (2196398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2138132614e4c007784f493ea29108d9d157979f1b46b8974d13285066686618`  
		Last Modified: Fri, 14 Feb 2025 08:39:51 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef02728a89810bb69117a4f6270d10a3d5b1a470d8b6f80fcb78f935a8e8142`  
		Last Modified: Fri, 14 Feb 2025 08:39:51 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6aaefe2681a52c7e3f2bca1539f67520243cf457badcad973eb2071d263ac8`  
		Last Modified: Fri, 14 Feb 2025 08:39:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8af0b0fdebe22d8549ff53e83555a3dcdf6363ca3a072bf8ce204b0948ab49`  
		Last Modified: Fri, 14 Feb 2025 08:39:53 GMT  
		Size: 20.1 MB (20061276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5594381dcff7260d549011bba594167acfc792c5e32038c2b8e9b7b5894b0f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be058e57f5e315ee6ee888bd8778ea7131a184f339d32b5a850a0f4ed82c7f81`

```dockerfile
```

-	Layers:
	-	`sha256:aab3c5281423f1f184457e9249554d023c3a315bfacf5d9b70053e42813bf874`  
		Last Modified: Fri, 14 Feb 2025 09:04:25 GMT  
		Size: 7.0 MB (7039283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e928a109a870801ab4e1c1734549768289208b134c9965de4647c4eabc61f9e9`  
		Last Modified: Fri, 14 Feb 2025 09:04:25 GMT  
		Size: 38.2 KB (38195 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:927067264e3e5403be7a9ee450d10282f06e0a8c3294e8248486459e63f2f0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190536112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff393c223e9640d49a1e0af55f9021c7ca0a8b403c23834ff37dbbd3426b29d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Feb 2025 05:02:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_VERSION=8.3.17
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Feb 2025 05:02:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Feb 2025 05:02:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /var/www/html
# Thu, 06 Feb 2025 05:02:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 06 Feb 2025 05:02:24 GMT
CMD ["apache2-foreground"]
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV DRUPAL_VERSION=11.1.2
# Thu, 06 Feb 2025 05:02:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Feb 2025 05:02:24 GMT
WORKDIR /opt/drupal
# Thu, 06 Feb 2025 05:02:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Feb 2025 05:02:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 05:05:20 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9219b052f79b2567c8318f800af7a67e79373912b9a18406039c49abcf25f6b`  
		Last Modified: Fri, 14 Feb 2025 05:09:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37797d529fd6cc198576ceb7126399349927b037480fae1196e5ed8c12414fc5`  
		Last Modified: Fri, 14 Feb 2025 05:09:08 GMT  
		Size: 92.5 MB (92521702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a629f3cb2ad6182d3f5bb708fa1b665a8ee0f0f69659b07cdb9a10a46e1d867`  
		Last Modified: Fri, 14 Feb 2025 04:09:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc7d6fd95125964198fcdb54e6175a8a0d153303b8787cf17de23dba33f2382`  
		Last Modified: Fri, 14 Feb 2025 05:09:03 GMT  
		Size: 19.6 MB (19552810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb72f4499321dc467af2e473aa88bb63b95bf61b499cf2fd4fc93bfd708459`  
		Last Modified: Fri, 14 Feb 2025 05:09:02 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0584b9e1c8166a53155ad76afcc15e1a4eed84a6495d3c703bffc27d3267a00`  
		Last Modified: Fri, 14 Feb 2025 05:09:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c552e6035484043b658cb97cc36e8593836c81b390b12469454b99526c3e3b2`  
		Last Modified: Fri, 14 Feb 2025 05:09:04 GMT  
		Size: 12.7 MB (12665971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207f91dfd312e1568d89fe49c47fae3bc58e269f9faa0f0d8c476e568645c453`  
		Last Modified: Fri, 14 Feb 2025 05:09:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6d478bf6c7c0ea43599b5af2360ccad678f16cb0303050f3d4b0eee150587b`  
		Last Modified: Fri, 14 Feb 2025 05:09:03 GMT  
		Size: 11.8 MB (11811171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6965f4a46c9156f9de002d64d84d318cea549f64365b0217543ea9fc3de38993`  
		Last Modified: Fri, 14 Feb 2025 05:09:03 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623d1768a0203c77d63e666d3793dba7df8d7b843bc14224a1debdefc8e21cc7`  
		Last Modified: Fri, 14 Feb 2025 05:09:03 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39722546f08233dcbca6e7a221e7077af09dca2ff846745658738137f179a861`  
		Last Modified: Fri, 14 Feb 2025 05:09:02 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b306597ea6e83aef134e81cf2539a94cb4b4e5789fa1ab7246a6e616162c105`  
		Last Modified: Fri, 14 Feb 2025 21:13:02 GMT  
		Size: 2.0 MB (1998181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645f8b49f67b2e6aad92ab01d8be380bd9fda6a09db0788b94b239e13d286c79`  
		Last Modified: Fri, 14 Feb 2025 21:13:02 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f30bfd1a452f1c08a4721d075b3344a06bb4fbe797cc5b99ddcf60ddeb63f4`  
		Last Modified: Fri, 14 Feb 2025 21:13:02 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcb172af38d4b87fc06af369ede96af0dd8403ba535b1b467c5b9c0b0ee6a29`  
		Last Modified: Fri, 14 Feb 2025 21:12:53 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37164688c091c1efc88417bb79699a4d827efdaba2c8d2b53ae696e5924b3e1e`  
		Last Modified: Fri, 14 Feb 2025 21:13:04 GMT  
		Size: 20.1 MB (20061144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:1e81e049bef5072bc23b631b818bad9ac49ec0b012b3c76360f032915ffc9019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7053646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014faf91dff3be7150f3f389db264aba8017414608e30ed932265e1f5a50c49f`

```dockerfile
```

-	Layers:
	-	`sha256:b47aa03cc6c90f5db621e7091390caad78a5a4d5d284861f8e8bb4b0c978b2bb`  
		Last Modified: Sat, 15 Feb 2025 00:02:06 GMT  
		Size: 7.0 MB (7015723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be551ffb7d25fa72060bcdd03a52f33aedda327bd155491abf9852e6727ca40`  
		Last Modified: Sat, 15 Feb 2025 00:02:07 GMT  
		Size: 37.9 KB (37923 bytes)  
		MIME: application/vnd.in-toto+json
