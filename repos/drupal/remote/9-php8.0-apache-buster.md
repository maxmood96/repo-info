## `drupal:9-php8.0-apache-buster`

```console
$ docker pull drupal@sha256:a30ba2d67ea384c033453a69845817858f6b7b8cd9fe1113e45d888a85a6943e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:9-php8.0-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:2863ee040ee8363cdbf73adf665fa00a6148eb014d356765e27ee51a4c9d741a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169333145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28310da99f7b093db0032e4e97d6167f29c3bf5005730d797ae52288ed70a554`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 13:45:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 13:45:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 13:45:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 13:45:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 13:49:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 13:49:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 13:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 13:49:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 13:49:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 13:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 13:49:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 13:49:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 15:13:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 25 Oct 2022 15:13:06 GMT
ENV PHP_VERSION=8.0.24
# Tue, 25 Oct 2022 15:13:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Tue, 25 Oct 2022 15:13:06 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Tue, 25 Oct 2022 15:13:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 15:13:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 15:16:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 15:16:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Oct 2022 15:16:26 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 15:16:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 15:16:26 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Oct 2022 15:16:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Oct 2022 15:16:27 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 15:16:27 GMT
EXPOSE 80
# Tue, 25 Oct 2022 15:16:27 GMT
CMD ["apache2-foreground"]
# Wed, 26 Oct 2022 17:10:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 17:10:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Oct 2022 17:10:49 GMT
COPY file:885ab970f10508225fd61630bb5f5deca9a4c5f5efa71af5b20e1efa22fecb2c in /usr/local/bin/ 
# Wed, 26 Oct 2022 17:10:49 GMT
ENV DRUPAL_VERSION=9.4.8
# Wed, 26 Oct 2022 17:10:49 GMT
WORKDIR /opt/drupal
# Wed, 26 Oct 2022 17:11:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 26 Oct 2022 17:11:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad727a2a192a78bffbc3ed59e1c156238f5c5dcf05eb9112956009305515f6e`  
		Last Modified: Wed, 26 Oct 2022 15:59:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c444d7f33c77c65f0bb5e8d86acab5a52270e72cced8bcd87956fdf10c7b5b`  
		Last Modified: Wed, 26 Oct 2022 15:59:26 GMT  
		Size: 76.7 MB (76687181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318cde4e04bca787e367e88de1fa26c35b078c62d5ba9005843174551e912173`  
		Last Modified: Wed, 26 Oct 2022 15:59:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414e253b03043e5f230253e4503bb20feafe386e0998c7ff896f99df2678504b`  
		Last Modified: Wed, 26 Oct 2022 15:59:48 GMT  
		Size: 18.7 MB (18683987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30d38210a15665774eff096001e3c87f7d3c312cb9ef239d119120773b409f1`  
		Last Modified: Wed, 26 Oct 2022 15:59:45 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f16444ec43758eba857e32a23d06c47d252b1a90d700d79f9ae02a4f2f19460`  
		Last Modified: Wed, 26 Oct 2022 15:59:45 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5554a9787336526e7673346b7f1c2239bf7fe4017826adf88356d5b8aa7139b`  
		Last Modified: Wed, 26 Oct 2022 16:09:36 GMT  
		Size: 11.2 MB (11233884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffc154069d1ff6e021bcbb5f29cf8ee178b56f9934f42c2995fd9b38af0c6fd`  
		Last Modified: Wed, 26 Oct 2022 16:09:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd059bb1440c3f7c9d707ebabd6bee945f15f0faa7eab833f6364d326337aa5b`  
		Last Modified: Wed, 26 Oct 2022 16:09:35 GMT  
		Size: 10.7 MB (10735751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a126ff0cbb74ecaf8c89e03f6ab087f7bdacfb1962370f385843163a1a0946f`  
		Last Modified: Wed, 26 Oct 2022 16:09:33 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc3b165c1e1a0cf8cd7778dce5023a5f4037add974578a1395a2229338739f0`  
		Last Modified: Wed, 26 Oct 2022 16:09:33 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a539041b536b238889df833ec1ee391f6cec410399d9f3f7b937e8c7081e3139`  
		Last Modified: Wed, 26 Oct 2022 16:09:33 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083b1ae3a6ae16a9d904959db5838fe365802bbccaeddd631a4d6fcd35227841`  
		Last Modified: Wed, 26 Oct 2022 17:33:52 GMT  
		Size: 2.2 MB (2247177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621a1469354b78c007d6bc5115b1255149d21219c10b8456e13e7e7035a85672`  
		Last Modified: Wed, 26 Oct 2022 17:33:51 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff864392a5930ba9cb07a5206b438b3dbf2b97c74b480a60efb70d449f339a4c`  
		Last Modified: Wed, 26 Oct 2022 17:33:52 GMT  
		Size: 694.8 KB (694774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb52fbe60d02a0625819ce9bc5a4bf5a4f3eeed65f5350d5bf3cd66f8d3a0cf`  
		Last Modified: Wed, 26 Oct 2022 17:33:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c3c225025f1752dd1036fca30412884fe38826fb5e6c33960756837d5e84ab`  
		Last Modified: Wed, 26 Oct 2022 17:33:57 GMT  
		Size: 21.9 MB (21903520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php8.0-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:46e87827eb942606f4037f382ba1934317d73e96e601863d632db3f6fa036187
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144505289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6291da8913bfb862e80ac7d5c89a482c8d04ec6a1f8583ab92ad98eee0a736b0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:00 GMT
ADD file:d3bb9b1f86a2639e67a7615e4d07996af61820f6d866ee4f6c5c8e5396da794d in / 
# Tue, 25 Oct 2022 03:15:00 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:56:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 23:56:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 23:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 23:56:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 23:56:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 23:59:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 23:59:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 23:59:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 23:59:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 23:59:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 23:59:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 23:59:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 23:59:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 26 Oct 2022 02:16:55 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 26 Oct 2022 02:16:55 GMT
ENV PHP_VERSION=8.0.24
# Wed, 26 Oct 2022 02:16:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Wed, 26 Oct 2022 02:16:55 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Wed, 26 Oct 2022 02:17:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Oct 2022 02:17:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:19:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 26 Oct 2022 02:19:28 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:19:28 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Oct 2022 02:19:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Oct 2022 02:19:29 GMT
STOPSIGNAL SIGWINCH
# Wed, 26 Oct 2022 02:19:29 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:19:29 GMT
WORKDIR /var/www/html
# Wed, 26 Oct 2022 02:19:29 GMT
EXPOSE 80
# Wed, 26 Oct 2022 02:19:29 GMT
CMD ["apache2-foreground"]
# Wed, 26 Oct 2022 17:25:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 17:25:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Oct 2022 17:25:24 GMT
COPY file:885ab970f10508225fd61630bb5f5deca9a4c5f5efa71af5b20e1efa22fecb2c in /usr/local/bin/ 
# Wed, 26 Oct 2022 17:25:24 GMT
ENV DRUPAL_VERSION=9.4.8
# Wed, 26 Oct 2022 17:25:24 GMT
WORKDIR /opt/drupal
# Wed, 26 Oct 2022 17:25:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 26 Oct 2022 17:25:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e4ea50bd37db50088d8cad765fade1138e096b0f83b40a13e3127931b49bab77`  
		Last Modified: Tue, 25 Oct 2022 03:22:12 GMT  
		Size: 22.8 MB (22750167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c111e6902f2fe0700f40a93990002fbe09394456d6c181d707c1e31a648db8f8`  
		Last Modified: Wed, 26 Oct 2022 03:37:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d80063ba09709048835b0f2717984ff1a7d8bcb329686498b043b1178a00bb`  
		Last Modified: Wed, 26 Oct 2022 03:37:57 GMT  
		Size: 59.5 MB (59542567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88105ef7ac9e90f382068c55360862c6b601cbddff4c985e3ebabe604399933`  
		Last Modified: Wed, 26 Oct 2022 03:37:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b8bbb55a6c620d26abf87a01151efcf13269b49186e955fcd6ce05c0fdc9b8`  
		Last Modified: Wed, 26 Oct 2022 03:38:24 GMT  
		Size: 17.5 MB (17481565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b945e786d0a9e8123d5fa6f2b12eb309c1e24215430078487b5be6a805c13f`  
		Last Modified: Wed, 26 Oct 2022 03:38:20 GMT  
		Size: 437.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5304d3c01dee3cc84fe47ee91d8bb5d777d1ec75f033148afb4bbb7ca1e2d2ed`  
		Last Modified: Wed, 26 Oct 2022 03:38:20 GMT  
		Size: 486.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775bef3f4318a21e17d416855969b914c441799f40762b36246fca815e987293`  
		Last Modified: Wed, 26 Oct 2022 03:58:13 GMT  
		Size: 11.2 MB (11231955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6660d89770e40a11e33cc359c654bf4bce6c5bd05158566d360a18e5ac4f1f3d`  
		Last Modified: Wed, 26 Oct 2022 03:58:09 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fee96a4075b9924de4b49eae4a8a62eb231af0d053ef32f625d67e6084afb43`  
		Last Modified: Wed, 26 Oct 2022 03:58:11 GMT  
		Size: 9.3 MB (9261804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f947f4e578a4dfc4bc6c33631d0e06e5e8014ecab853efcc684e113dcda1712`  
		Last Modified: Wed, 26 Oct 2022 03:58:09 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca3af36ae95f41b29b1e175139e5008f8df18f576ded532593e3c9b716a8c53`  
		Last Modified: Wed, 26 Oct 2022 03:58:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82599cc77c40f4866a8d2ba452c4c56dc114ddaa2f9bc6eefc5607d9280aae15`  
		Last Modified: Wed, 26 Oct 2022 03:58:09 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087997a2de92a6f418bce164001370365a4d57e23d13f26f51c23501fe0d1493`  
		Last Modified: Wed, 26 Oct 2022 18:15:16 GMT  
		Size: 1.6 MB (1633023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfaa3f9b4017644ba182457702f76d09edb0a1268479980607f3d709ac06832`  
		Last Modified: Wed, 26 Oct 2022 18:15:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce40ed6ea8de0e07adbce8e84d092bef33bd6179c248a269a423de08bb9e6cb`  
		Last Modified: Wed, 26 Oct 2022 18:15:16 GMT  
		Size: 694.8 KB (694768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c07908a7cdb401d8df415faf6130de4112ab7b221b1669f4728aae4d747218`  
		Last Modified: Wed, 26 Oct 2022 18:15:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039862ae33972757ed5ceb8a15f7b84af51e12ebe76651b679e6ad072847c8f`  
		Last Modified: Wed, 26 Oct 2022 18:15:23 GMT  
		Size: 21.9 MB (21903534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php8.0-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:855a2e144c7e2546eeb0fd14aa5426cf25dcab295c145e14a01002383dbbcdf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160808291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b7b560fa7d80287d57725944ddc4371d244968df5a7cc2cd89c53e1f37f113`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:13 GMT
ADD file:342233874a06722375663380e7e3a04502a995dfbbc425cd1913f10e96a50dcb in / 
# Tue, 25 Oct 2022 05:46:14 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:12:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 16:12:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 16:12:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:12:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 16:12:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 16:16:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 16:16:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 16:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 16:16:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 16:16:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 16:16:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:16:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:16:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 18:38:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 25 Oct 2022 18:38:57 GMT
ENV PHP_VERSION=8.0.24
# Tue, 25 Oct 2022 18:38:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Tue, 25 Oct 2022 18:38:58 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Tue, 25 Oct 2022 18:39:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 18:39:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 18:41:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 18:41:06 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Oct 2022 18:41:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 18:41:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 18:41:07 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Oct 2022 18:41:07 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Oct 2022 18:41:07 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 18:41:07 GMT
EXPOSE 80
# Tue, 25 Oct 2022 18:41:07 GMT
CMD ["apache2-foreground"]
# Wed, 26 Oct 2022 12:15:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 12:15:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Oct 2022 12:15:57 GMT
COPY file:885ab970f10508225fd61630bb5f5deca9a4c5f5efa71af5b20e1efa22fecb2c in /usr/local/bin/ 
# Wed, 26 Oct 2022 12:15:57 GMT
ENV DRUPAL_VERSION=9.4.8
# Wed, 26 Oct 2022 12:15:57 GMT
WORKDIR /opt/drupal
# Wed, 26 Oct 2022 12:16:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 26 Oct 2022 12:16:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5f30c56efde95016859c51bdc10e665dd57dc3c8d22e7abbf384ae9722dfa19e`  
		Last Modified: Tue, 25 Oct 2022 05:49:47 GMT  
		Size: 25.9 MB (25914885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db72537674c01746e8cfe0de3e33e690ea7b2ae6fa309c2ffa58dee432a2bceb`  
		Last Modified: Tue, 25 Oct 2022 19:40:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7b984e345891e702f79e87a64afcb69f5638c39f8c4b4ab7a47ef6b684ade7`  
		Last Modified: Tue, 25 Oct 2022 19:40:27 GMT  
		Size: 70.4 MB (70363634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69589caadcdad7bc8722fad7dc9dc935cc8c3ef7d482ca924922ee280d6fb06d`  
		Last Modified: Tue, 25 Oct 2022 19:40:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f30c34bb868e79def32132e1af63dcc95297810349e2fb2ecc147924089501c`  
		Last Modified: Tue, 25 Oct 2022 19:40:48 GMT  
		Size: 18.6 MB (18583655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bd3642839a18503f373dfa482936f015eb7467f1199aca6a1631d7d37116c`  
		Last Modified: Tue, 25 Oct 2022 19:40:45 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4213b9b6d7a9cc8a47a69b38cd848e9f5c84becd2e2d88c400a5ce708932c8`  
		Last Modified: Tue, 25 Oct 2022 19:40:45 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ce0e47f151e9b2386b46647ff5b5592b12ae8a78784c59893049d6eb1d27f7`  
		Last Modified: Tue, 25 Oct 2022 19:55:36 GMT  
		Size: 11.2 MB (11232729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145ba78b97c2282e5d9b27c7cae5f3b7687c5d12c05c1b330d3c3de697ee6cc5`  
		Last Modified: Tue, 25 Oct 2022 19:55:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75420a10d6f1c787747f3ff99e5a78595ed72ac61d988201df56969d5572491`  
		Last Modified: Tue, 25 Oct 2022 19:55:34 GMT  
		Size: 10.2 MB (10208874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ae950d654f661c742b8afd9cc6242f564a838c1bda789b70e6d557840204ad`  
		Last Modified: Tue, 25 Oct 2022 19:55:33 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd8e713575baead7ce03a1a90190bdb2153064dda8a786a45ec20432dcf4158`  
		Last Modified: Tue, 25 Oct 2022 19:55:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c37b4b89a17f0839d246d7cda11f7d2e787a1900cdb6524adba9efa49e4f96e`  
		Last Modified: Tue, 25 Oct 2022 19:55:33 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23d7f0b222ff569e926078ef230c0e186e958cb36dbfd1324a8489f0321ca01`  
		Last Modified: Wed, 26 Oct 2022 12:45:40 GMT  
		Size: 1.9 MB (1900256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb33533c5f3a4a0e1a76a6afa948c7fc1ee46b70c50181391dea662e9a0ec1a`  
		Last Modified: Wed, 26 Oct 2022 12:45:39 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfed00c0c195c23942d27243b182de24b1e33565a7c9498cc94eff406a48bc2`  
		Last Modified: Wed, 26 Oct 2022 12:45:39 GMT  
		Size: 694.8 KB (694772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b826fc2bbee668781f3b7ca41f6e899d7580c1206f2d03c65d1314ce8ccd8d`  
		Last Modified: Wed, 26 Oct 2022 12:45:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05be7a451ea4935de125ccda7a431589e004a242b6d7595ed01b4e572fb0f87a`  
		Last Modified: Wed, 26 Oct 2022 12:45:43 GMT  
		Size: 21.9 MB (21903435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-php8.0-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:1e57c3404709be6078d64d1999d6759e2f3899841229847437cbdf4177a49a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174607164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196ffbd2950f9a98ee02af19e4def9c041d876fea928e1370bdb4a4635ef5477`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:02 GMT
ADD file:49981fa4bc36bce6e4fdd74b2c4429cc4faef5498c3d8fb20fb98b426bbf8c4d in / 
# Tue, 25 Oct 2022 02:23:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:56:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 25 Oct 2022 07:56:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 25 Oct 2022 07:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:56:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 07:56:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 08:00:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 25 Oct 2022 08:00:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 25 Oct 2022 08:00:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 25 Oct 2022 08:00:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 25 Oct 2022 08:00:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 25 Oct 2022 08:00:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 08:00:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 08:00:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 09:16:17 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Tue, 25 Oct 2022 09:16:18 GMT
ENV PHP_VERSION=8.0.24
# Tue, 25 Oct 2022 09:16:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.24.tar.xz.asc
# Tue, 25 Oct 2022 09:16:20 GMT
ENV PHP_SHA256=8e6a63ac9cdabe4c345b32a54b18f348d9e50a1decda217faf2d61278d22f08b
# Tue, 25 Oct 2022 09:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 25 Oct 2022 09:16:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 09:19:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 09:19:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 25 Oct 2022 09:19:09 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 09:19:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 09:19:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 25 Oct 2022 09:19:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 25 Oct 2022 09:19:13 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 09:19:14 GMT
EXPOSE 80
# Tue, 25 Oct 2022 09:19:15 GMT
CMD ["apache2-foreground"]
# Tue, 25 Oct 2022 19:17:02 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 19:17:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 25 Oct 2022 19:17:04 GMT
COPY file:885ab970f10508225fd61630bb5f5deca9a4c5f5efa71af5b20e1efa22fecb2c in /usr/local/bin/ 
# Tue, 25 Oct 2022 19:17:04 GMT
ENV DRUPAL_VERSION=9.4.8
# Tue, 25 Oct 2022 19:17:05 GMT
WORKDIR /opt/drupal
# Tue, 25 Oct 2022 19:17:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 25 Oct 2022 19:17:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:32caca2e9abac2a8ffc2b083d202d57e1970d8adc212be17451a992441fad01b`  
		Last Modified: Tue, 25 Oct 2022 02:29:19 GMT  
		Size: 27.8 MB (27799224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140e6bcf950ee2d755ce50e370b6647bc357dcbd24dd0ece7e8d7b388f84d94d`  
		Last Modified: Tue, 25 Oct 2022 09:56:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d087454ecae3a96210f9074f3beccfe18b333cf212f9946b1aa8a54c4d0c064c`  
		Last Modified: Tue, 25 Oct 2022 09:57:02 GMT  
		Size: 81.2 MB (81234271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2520a6c0f52f7418abcd797a402d8844158c345af1bc2f6a196ef56b0d9b85d6`  
		Last Modified: Tue, 25 Oct 2022 09:56:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10767ffcd61bf365893f41478142575a626be4309a58d0ff91365a013c2976b`  
		Last Modified: Tue, 25 Oct 2022 09:57:26 GMT  
		Size: 18.9 MB (18900801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e017d214c18776904c54b35b1b5803ba97d3dd0cd9ac7ebf134e7beb0235aa`  
		Last Modified: Tue, 25 Oct 2022 09:57:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353ace81a532edeb6342ba0eeb71d4a12b5f458af2c0f8af8a56d0bd2e80c050`  
		Last Modified: Tue, 25 Oct 2022 09:57:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79ce1248a972603e61c29ba372c280f79876a8c4d5a9834a1a4246dbcfe887a`  
		Last Modified: Tue, 25 Oct 2022 10:09:29 GMT  
		Size: 11.0 MB (11020416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8636a1b0f1823bfcc1ed8e10ce1f8be4a111167302887d29fdd126e3e69256b`  
		Last Modified: Tue, 25 Oct 2022 10:09:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d392ad7bce79216921c5d6c4007cf894c492933cf4cb5aa1de9e5da40a0962`  
		Last Modified: Tue, 25 Oct 2022 10:09:27 GMT  
		Size: 10.9 MB (10943053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7cdaf596bd65ea7655220e7e8da0fd01873b20fa5dc7e0718f6c3856ad3f90`  
		Last Modified: Tue, 25 Oct 2022 10:09:25 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fd7b20b366477eeaf61423ef37abe1941490779a0404c6e8b85a4d80dfaf70`  
		Last Modified: Tue, 25 Oct 2022 10:09:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d65548e26ab489026d2320add77e98ab1f7948a482b4acf16d7502d40d6c9d`  
		Last Modified: Tue, 25 Oct 2022 10:09:25 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d561b24603e6684613bcda163ac4a170a500d06bc465d49b68f4399a0a14366c`  
		Last Modified: Tue, 25 Oct 2022 19:50:26 GMT  
		Size: 2.1 MB (2102218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd228523c7d7d589a16363401a90d5b5356e06a6a3509e36ccb4828f22305202`  
		Last Modified: Tue, 25 Oct 2022 19:50:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0f2e7b75a56b3f83c8a99af06f180830b272d4b81944e9a6c2d1d935bfdce`  
		Last Modified: Tue, 25 Oct 2022 19:50:25 GMT  
		Size: 694.8 KB (694775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b1ddb8c988b13cb2e5975c9d077dbe68a4f2deb70c47c072677c604bf6e2a5`  
		Last Modified: Tue, 25 Oct 2022 19:50:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9fed1c20f652c623c13ca1c35d4a8e9cbb18f0ae3fcc39a72624dda4acbfcd`  
		Last Modified: Tue, 25 Oct 2022 19:50:30 GMT  
		Size: 21.9 MB (21906505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
