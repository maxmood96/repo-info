## `drupal:php8.3-apache-bullseye`

```console
$ docker pull drupal@sha256:786e924ff4e678599e523a4e79ba56ab32f34584c23040af4fb17823e1c653bc
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

### `drupal:php8.3-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:835f56340a2dc0d82400b6e3e6a981d598f46f3b293d2e06354b0a301e68404a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187792765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92929bfd971b98e18c4118311f39a8f6414e06a77b096803bd4d7bc777e9803`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c23d72c429f48e6473375f3e6f96d40094a206dd3f5f5e29df06b28fe6e79db`  
		Last Modified: Fri, 14 Mar 2025 00:12:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bec484a71128ef35e5df88153e1cd69a9f8bb0d9b9d21bdd09531a5c2f1bc19`  
		Last Modified: Fri, 14 Mar 2025 00:12:16 GMT  
		Size: 91.4 MB (91447959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0608c78a50b73f33585240f0fc48882392a49faedb733372be2d613525fe765c`  
		Last Modified: Fri, 14 Mar 2025 00:12:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671de327d8132633a460c4c4e7900acc646170d523c080b0017c8bd3beaf3c28`  
		Last Modified: Fri, 14 Mar 2025 00:12:14 GMT  
		Size: 19.1 MB (19064147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd12b5a4262421a4eb067eac7c352e924a4d52aef7da264bfe397d874faafb1`  
		Last Modified: Fri, 14 Mar 2025 00:12:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9240246bd12ecb704cad9813d833db1ed689c1609cc58e968a3eade1e59908`  
		Last Modified: Fri, 14 Mar 2025 00:12:15 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a1275b4802e748ad381202d409a7f5f7a36b9590145f399c409646e8580abc`  
		Last Modified: Fri, 14 Mar 2025 00:12:16 GMT  
		Size: 12.7 MB (12685572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04cdea19014754830059be42eeccc4eba77d090bdf4adfd855da0502fdc4b81`  
		Last Modified: Fri, 14 Mar 2025 00:12:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d711360abafa1a6075f1ebc77e061cfb7d7cdb32b6b78acbeddaad038e55ef`  
		Last Modified: Fri, 14 Mar 2025 00:12:16 GMT  
		Size: 11.6 MB (11599149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d589d7daa3ed12ec2c8f4ec91331f06729e9956f70fd276d0c5a2ee0e7ad7def`  
		Last Modified: Fri, 14 Mar 2025 00:12:17 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666f9efc41d4a2c3abb05e687cc69448d9b2addc24aa8329e078e2885348827`  
		Last Modified: Fri, 14 Mar 2025 00:12:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b607f4b11cb761d0a06597f3c9f951500666dbf849a591e4c7a2604e242038e`  
		Last Modified: Fri, 14 Mar 2025 00:12:17 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d4da364d565203ab6e8300ffe7e83c65d7f1d287616613b8f75d0c1102be72`  
		Last Modified: Fri, 14 Mar 2025 02:13:01 GMT  
		Size: 1.9 MB (1933088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c529529d775989a62a76859dd10312050cbee0a9ae496df9caa7b447d2aec658`  
		Last Modified: Fri, 14 Mar 2025 02:13:01 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb04d0e0eef81c66b5fac8f414d25725f5067f36e7ce0af6c304159a3aa226e1`  
		Last Modified: Fri, 14 Mar 2025 02:13:01 GMT  
		Size: 740.8 KB (740827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88234a12f48bcdca362c287e3752647b7be06903981f7a9a089de92eb1e174fd`  
		Last Modified: Fri, 14 Mar 2025 02:12:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c12f03546ccbf3780e4f4194583fec1e7fa7d53636dadec0e6f3268957c756`  
		Last Modified: Fri, 14 Mar 2025 02:13:01 GMT  
		Size: 20.1 MB (20062178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a7e87c3fa1082bfe59bde51287424f20cb5940102ed6dc7a247ac150be014f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7074425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d76eeccd1f5f25ef226c49fc20635700e0a841592fa7aa2f9ec21d3cc9213a7`

```dockerfile
```

-	Layers:
	-	`sha256:7c96173fd0d0569e6b840f1e23003b808e2b71ad91a4b7e42121e128fd26e8c2`  
		Last Modified: Fri, 14 Mar 2025 02:13:01 GMT  
		Size: 7.0 MB (7036439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d911c514629516b5ade4c9c84e4ef8c1d79199ff9dadfb1bfa771060326c0d81`  
		Last Modified: Fri, 14 Mar 2025 02:13:01 GMT  
		Size: 38.0 KB (37986 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f116612c329f4942e6492fa6e1a176017d58a6c59753aa6312060ebee15250c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157304801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e6f0bec05250a90240d614f8f1336975be35b29ed374ff1edd495e329a3ff`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
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
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6376edd46dda2c697c237efb83c17a91a0979b8e59e202d593f0446305d10167`  
		Last Modified: Tue, 25 Feb 2025 03:00:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29853446d3cd05c0eb401a13f07135f89a449ee487663701b45fb717b9b8e4e8`  
		Last Modified: Tue, 25 Feb 2025 03:00:39 GMT  
		Size: 69.1 MB (69119400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b785546b44d4e782b7e6d1ac072a5cb20d9e0432b17127beae71a8577c4cd2`  
		Last Modified: Tue, 25 Feb 2025 03:00:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeb99bd884dcbd5d6ffa37230eb214c6fcfa01c4209a7ed8a1b1770dd478f50`  
		Last Modified: Tue, 25 Feb 2025 03:04:14 GMT  
		Size: 17.8 MB (17817128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b649ad95fd42808118f2b9d9a28fedf901a4235cbce70922c327521bf824879`  
		Last Modified: Tue, 25 Feb 2025 03:04:13 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334502dc51a7b5349a8c3d03af32b92643c36810124976e7d092548a58d286e1`  
		Last Modified: Tue, 25 Feb 2025 03:04:13 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9745f7c4ce7ed807c6c966afac33957a7cd8b063b23877c8d1987a4ebd91f`  
		Last Modified: Fri, 14 Mar 2025 03:42:14 GMT  
		Size: 12.7 MB (12684249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5768474b97215949813285514f97411454047a3d1df5b3c86f1f3337589d6a`  
		Last Modified: Fri, 14 Mar 2025 03:42:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0e0a291000c0c7964c9ee059b5796b6b3ec0c24e4efdd829c9f50a1585a643`  
		Last Modified: Fri, 14 Mar 2025 03:42:14 GMT  
		Size: 10.0 MB (10027689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd2a69d99e50da7f406cd02a7661e332e349aa9cc2a6c6bb4f6ca427eacca0d`  
		Last Modified: Fri, 14 Mar 2025 03:42:13 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f646edf5e790e207fac19f49412443618b0c8d4ad14ee5c20974a65fa64132`  
		Last Modified: Fri, 14 Mar 2025 03:42:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4062d110d5fd7e479f0ddc3960ee9837d1b482d2fba5f9c8e6849a67b525d0e2`  
		Last Modified: Fri, 14 Mar 2025 03:42:14 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c613d6db559e5993ef0b96791c439c94ea32c892c90907bb8906dc4949986d`  
		Last Modified: Fri, 14 Mar 2025 16:22:18 GMT  
		Size: 1.3 MB (1312093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cad6f78a3f2f1850486d98868cec94f930ba171dd8d3b76df8c50820474cf1`  
		Last Modified: Fri, 14 Mar 2025 16:22:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00a681e2d1107f573a14b4ffd85049f2ebacb17cc3901c29818e6548aac9e08`  
		Last Modified: Fri, 14 Mar 2025 16:22:18 GMT  
		Size: 740.8 KB (740825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e074f7cbfbefecda965661fc91d10352d5ccaf13677d9d671d12a46fc6bdc98`  
		Last Modified: Fri, 14 Mar 2025 16:22:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e454fd8024a0bddfb6edb31c17c2351b50b93b51fad955747e032238db228069`  
		Last Modified: Fri, 14 Mar 2025 16:22:22 GMT  
		Size: 20.1 MB (20062071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:16511b4fa7076a13a5ac54f565f74cb7b04168dba72819158523cf783d54bd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6883509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f610c0d8201a10862e2153fdf85ec2f9988b186131dd4ada0079b932af0e7eb`

```dockerfile
```

-	Layers:
	-	`sha256:3fd7ce9a9c479abafd9799e4e1dbb9faf9ece5ed8b32da978a9e89f75b525cf6`  
		Last Modified: Fri, 14 Mar 2025 16:22:18 GMT  
		Size: 6.8 MB (6845367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f093df6ee317e0fa973327c717bdf2d74bc58bad382b1c56f4d2238936fc5c86`  
		Last Modified: Fri, 14 Mar 2025 16:22:17 GMT  
		Size: 38.1 KB (38142 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:08cc7199884333b953c69cb9b63a2aa1eb05e93cacb7dd6c1cf407a8acdea610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181807662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e784b69adc39633b5723886627191ff15708956b3b27353ddc8140cd2419dfba`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cac8d80438c7d8c825ba99a93071ef755fedf47f61ec6695e1a497258d4a6d`  
		Last Modified: Tue, 25 Feb 2025 03:17:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cf5e32e0b7c2e87599c9d64521fbaff9ea36e3fbfb51f931baef0cb2e19803`  
		Last Modified: Tue, 25 Feb 2025 03:17:38 GMT  
		Size: 86.7 MB (86734530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bd05e74457394c989762746be7fe63b0dbcf517102c6b331508270af1b04b`  
		Last Modified: Tue, 25 Feb 2025 03:17:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fbdaa5faaf2f51a48a7cdfd45cf510e60534f8b673a5ad2fd9cce416e28d2b`  
		Last Modified: Tue, 25 Feb 2025 03:20:52 GMT  
		Size: 19.0 MB (18981599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a48b918c56dfc5b9a62cadb0b4ada2c76a9601991d67f1df64e858f56e769c`  
		Last Modified: Tue, 25 Feb 2025 03:20:51 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cb11d849785f782bd3740bad49a02c0075ca488f5bdd99cbe13401b056096d`  
		Last Modified: Tue, 25 Feb 2025 03:20:51 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb83ece05aca64b488f45621248ac7e4ea48582edde5f0ee1af44a9dfd8d4a8`  
		Last Modified: Fri, 14 Mar 2025 02:20:01 GMT  
		Size: 12.7 MB (12684927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7a43aabe6eb33d42641768b5a2c8afffbf5b032fab64fd6c9378b8f58979e`  
		Last Modified: Fri, 14 Mar 2025 02:20:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f980720a79782b52b9ab76d41bf847f9117f1c82036d390e1d8d3060e1af4c`  
		Last Modified: Fri, 14 Mar 2025 02:20:01 GMT  
		Size: 11.7 MB (11655179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447a3b4544a0b34fb6ab17190fca9c18de129dd73a1f6c45e0bde3be8ea7cf99`  
		Last Modified: Fri, 14 Mar 2025 02:20:00 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc035aa10dd8299a91cf116de45d62a5be0feb9d7f3a35440b7ed9edb0c7f0a`  
		Last Modified: Fri, 14 Mar 2025 02:20:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd95bd15f4faf0e13b3f6a07ea25e41dd7bdb23ecda8944d9e84bd55dfefa35`  
		Last Modified: Fri, 14 Mar 2025 02:20:01 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b2a2054717e278eb2129091693813496ba190eb6d8f0f9340932b8c28787c`  
		Last Modified: Fri, 14 Mar 2025 22:10:36 GMT  
		Size: 2.2 MB (2196621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813066b47796c2fedfec25986c273aa39d78fe9d9b8d13ff092393928381b94a`  
		Last Modified: Fri, 14 Mar 2025 22:10:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdea63149a7bc8472a1015b5563abb9c73dbe0a0b1adc8bfc0e53400ed692b3`  
		Last Modified: Fri, 14 Mar 2025 22:10:36 GMT  
		Size: 740.8 KB (740827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac041c2bc54214a6a9418da1aae2aed9b8619b699689a02dba6986eb6b569935`  
		Last Modified: Fri, 14 Mar 2025 22:10:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d25f260677b167b5c9d102d51538911676e8e309ead6f650231865ff921b70`  
		Last Modified: Fri, 14 Mar 2025 22:10:38 GMT  
		Size: 20.1 MB (20062066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b9fcbc4cab60fe7c15ca4b556bc143258abcdddfbf668782c2e0a3d6195ab4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a4da4f553b96d5c59e774c678e659cb6140f59536a5198fd9fb1528c06b628`

```dockerfile
```

-	Layers:
	-	`sha256:19cd41e92e0bf05a6c3485cb986e3e20309af3451b082a65e17cc5a74f166fab`  
		Last Modified: Fri, 14 Mar 2025 22:10:36 GMT  
		Size: 7.0 MB (7039283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673298dbaf3db9dfd99c6ef65acad31d913c64eb11bd7109745c85027ffd5be`  
		Last Modified: Fri, 14 Mar 2025 22:10:35 GMT  
		Size: 38.2 KB (38194 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:5bbdedfebdb0d3ec5f0144abe7f0b79807cb7ce130a27a82786fdfcec549dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190558919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c76b5656257bbdf3ad06e057a12c696143acc2bdf925257832a4a9b7d4ea87`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:53:13 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26186dadc16ee051702fee42b01311971718bbb45b63562677b4bb38c2afe347`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e0d3836a33aaa295ec5d531118651620384cf70b15e3e071ef4b76e41676de`  
		Last Modified: Fri, 14 Mar 2025 00:12:40 GMT  
		Size: 92.5 MB (92521265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403272821888ed74d024eef9f3570ebbbb76a3b9b5cd399ab868d39dbb66ab66`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f4b657385355602fcf97f77270aea7b7af155c415035bb145d63bf80f2122`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 19.6 MB (19552742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ff72fe88e2adf7303428b5a60624368a82cf562ba14429a871e80c8a32e12`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3b5685384eaa61a7ba8bd7ea2d96407eefbc7ebac443fdcb95f603252606d5`  
		Last Modified: Fri, 14 Mar 2025 00:12:38 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b979cce4630cac614767d1c9dc14ca2a425a6f373a9096dec5ff13af47d296`  
		Last Modified: Fri, 14 Mar 2025 00:12:39 GMT  
		Size: 12.7 MB (12684887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4226f2694972e799b8522d311178fe1bf7c320a610c02af06496dcd0bb6037`  
		Last Modified: Fri, 14 Mar 2025 00:12:39 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a7ae5e7955bbf6f5c6c37db45bc17a5f60dd9b38b9ef3222c132fb4157e441`  
		Last Modified: Fri, 14 Mar 2025 00:12:39 GMT  
		Size: 11.8 MB (11812165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29d406df9b03884fd95a1da8a20df5dc618fb78319ce0403700fd8b6a358a1`  
		Last Modified: Fri, 14 Mar 2025 00:12:40 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42c4d939e419575cab5201968bc06f0f4a87f766d51a1b4c9b4a80e2c0405ba`  
		Last Modified: Fri, 14 Mar 2025 00:12:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9928587991c1dcf87065b81552c24206fca629cd5e3501462a9ae49264b67fbc`  
		Last Modified: Fri, 14 Mar 2025 00:12:40 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9280236c153dc432eaae557145741a67840db33da77748c304e66157b1c9e5a2`  
		Last Modified: Fri, 14 Mar 2025 02:13:16 GMT  
		Size: 2.0 MB (1998298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87593d40d85eec50b50b5846440ecbe1a0e55ab7d9bb4b90b2378b0a345e7c7c`  
		Last Modified: Fri, 14 Mar 2025 02:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93e52215901ee8405f2ca44f8d017128b47b7dc26405018ffaac3b0a81295e5`  
		Last Modified: Fri, 14 Mar 2025 02:13:16 GMT  
		Size: 740.8 KB (740827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687643fcd632e25c937af78285a0dfff79c32d82b51dd12b1929fe3e41a6d043`  
		Last Modified: Fri, 14 Mar 2025 02:13:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9780990d3a96fad7828e0cf74a3460b8195b397ab632845dc7c118d709c66055`  
		Last Modified: Fri, 14 Mar 2025 02:13:18 GMT  
		Size: 20.1 MB (20062382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f92fc6c8a4a87711884bf478bcd12965a9c9036a466836416637c41ad521771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7064943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f9b8c2b7a87618b7dbcbc6a532ec538b6409e75b0cc67fe1ceb8b69deca827`

```dockerfile
```

-	Layers:
	-	`sha256:6d200bad50dfb49e81f5e864a7d109e521b0019560a9401aa05a2bb7e9106d24`  
		Last Modified: Fri, 14 Mar 2025 02:13:16 GMT  
		Size: 7.0 MB (7027021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2227f7aea652ca4f514b9670d3fd2d4d1c098daa391b77ba1b8e93b5052b520d`  
		Last Modified: Fri, 14 Mar 2025 02:13:16 GMT  
		Size: 37.9 KB (37922 bytes)  
		MIME: application/vnd.in-toto+json
