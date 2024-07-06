## `drupal:rc-php8.3-apache`

```console
$ docker pull drupal@sha256:e3ccdc94ecff4b95a59757254af30bc635981c219af03819f40ed137b08f8850
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

### `drupal:rc-php8.3-apache` - linux; amd64

```console
$ docker pull drupal@sha256:04bb9d6762a21ed65a2df32c08c2aa6018250af25b9fc4fe4620bb24aef59e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199933825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6739fd5fb573c08030b762a581702b6fc1269f575acabea5132d790dc0d0c7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 22 May 2024 23:55:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.9
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 May 2024 23:55:49 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 80
# Wed, 22 May 2024 23:55:49 GMT
CMD ["apache2-foreground"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c1fd48de30b16f5766e6ac96a6fe3c0b3241c34c93fe82ddc8a8536729dd53`  
		Last Modified: Tue, 02 Jul 2024 04:36:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b3bda7c6d1ae6620633030596609872e7f2b102e3f274f02c71ee92e136cb7`  
		Last Modified: Tue, 02 Jul 2024 04:36:44 GMT  
		Size: 104.3 MB (104349018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a68eb681dd3cc5f145cf854bf049843298d6ee06c3259ddff5bf4793710a80`  
		Last Modified: Tue, 02 Jul 2024 04:36:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35406f9afc7f771a49890b78aa21515eb9a55078c04c935db2eccebfa0ee09e1`  
		Last Modified: Tue, 02 Jul 2024 04:37:07 GMT  
		Size: 20.3 MB (20328149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d29e3575095485f641778e00db76200a84450e66c56ade92952177c80038fd`  
		Last Modified: Tue, 02 Jul 2024 04:37:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497b137ced83d700feeac177251b0552c63749019adf459aeb89db255825ee2`  
		Last Modified: Tue, 02 Jul 2024 04:37:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc68bc20094cc495d322f71809c8a7fffde63607f9504aa564d72f5462d22db`  
		Last Modified: Sat, 06 Jul 2024 02:25:06 GMT  
		Size: 12.8 MB (12803302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7401f0ea96034ef4feae397a5e50fd9b3e628bda283f40eea7196b2d59e994ee`  
		Last Modified: Sat, 06 Jul 2024 02:25:04 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cccaf419fb398acfa6e4bf7de01794975045ea2c0a5a4b6bdd1df93d79ac3e2`  
		Last Modified: Sat, 06 Jul 2024 02:25:06 GMT  
		Size: 11.6 MB (11635598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86825edd5f6eb00a6f399512eabe96d9a9b394843814f5351a190921b8e271f4`  
		Last Modified: Sat, 06 Jul 2024 02:25:04 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e2c5a7b120d7f917ad7d124b46db31615d9cd0aa1ee718059c466dcf8a8062`  
		Last Modified: Sat, 06 Jul 2024 02:25:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209a72e837ef20c3521fc36bb83f81e6b9c8e545b29955293b73967c05eea745`  
		Last Modified: Sat, 06 Jul 2024 02:25:04 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142655a6e25dd84b416999ba82459fe33f536feae67c61f356430d95475e2c4`  
		Last Modified: Sat, 06 Jul 2024 05:55:32 GMT  
		Size: 2.0 MB (1998923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29019ad795b45c43cf82be82b5b27a37ce19f87b8cd35094aae2bf67d2bf894d`  
		Last Modified: Sat, 06 Jul 2024 05:55:32 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d981ce4ad5c7ed9eadf3bb7e046096e242bce6aaf797e27b4d2295ce7058ba6`  
		Last Modified: Sat, 06 Jul 2024 05:55:32 GMT  
		Size: 726.3 KB (726337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5d76e379de59c668324ecae27eec9424d3c3f83b7b760ea14f678fa6d9021a`  
		Last Modified: Sat, 06 Jul 2024 05:55:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c19946cab1ed7fe05b8e70f5e0a7c37d763d407792cfa6162841768ba5f57a`  
		Last Modified: Sat, 06 Jul 2024 05:55:33 GMT  
		Size: 19.0 MB (18960333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:4b98c04582d94b60d7b826ebff20f8ef5028f6473ed37ec30027294d2cc4a082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6823840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b19a7d36c28518f50195443ca87a95e5ac56d6e71d893535d2e5c38827dc43`

```dockerfile
```

-	Layers:
	-	`sha256:b77ffdb89f598b813a59093e04cd2611064b283469d368925f2bccd17fc5f8b4`  
		Last Modified: Sat, 06 Jul 2024 05:55:32 GMT  
		Size: 6.8 MB (6786442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c4995fa396e2fc8afdbe1b52c1cc2f45c27be386df1cb896a104b46b08bd06d`  
		Last Modified: Sat, 06 Jul 2024 05:55:31 GMT  
		Size: 37.4 KB (37398 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5d602c3a98997f330db0405721a1efd7fa497e9b770f4a7defbe2435be737d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163819769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5acc2bdee0a88167db77fa5995fccb997bd7c164b1b27f845ed9bf9680d85c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 22 May 2024 23:55:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.9
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 May 2024 23:55:49 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 80
# Wed, 22 May 2024 23:55:49 GMT
CMD ["apache2-foreground"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98f2ea35903ab22a64a0b9429586e5ebf253d8f30160f658c9a3e91506b6b4f`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed99c1553b06b60dc38f501a723427469be3c7f305f660c2d3f5c4826636db6`  
		Last Modified: Tue, 02 Jul 2024 03:57:17 GMT  
		Size: 76.2 MB (76166316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff1c809dc06de95648d78a0490826dc9afc53a05c01d001be86b39ec6903ec`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751f0125442586c37682f7ec34b710b4ab71ddc530c91fea2cf2af4901d2a1a4`  
		Last Modified: Tue, 02 Jul 2024 03:57:42 GMT  
		Size: 19.1 MB (19057874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016198828fa6032df9c10ec2e792db92c6a8b19d35a884387328ccb4cb68f19d`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b6f3e158190277e0f0f214b0dc62c26057875ebd2af19ac0a15534c73fb171`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c2454bdeb5a3d11f6e0173ed5e3e42b4a0d19c9ccb480a5fa59b2947ff4423`  
		Last Modified: Sat, 06 Jul 2024 02:44:30 GMT  
		Size: 12.8 MB (12801309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c6b50ed89d5d6e3026bd226d88ab472e8efae5ee68995f6dc7ec99dbe892c7`  
		Last Modified: Sat, 06 Jul 2024 02:44:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574a13e1c52d7e30f47ee1190d407f994269a3111c64e9e31228f50943bf9854`  
		Last Modified: Sat, 06 Jul 2024 02:44:30 GMT  
		Size: 10.0 MB (10029245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e55661b13c68889fc57056f18148ccdd218f074760d197c380afe20c6401670`  
		Last Modified: Sat, 06 Jul 2024 02:44:28 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1473431aa95ee93f46ed26607e394c8947a638894c5c3d551282d8b228416ea`  
		Last Modified: Sat, 06 Jul 2024 02:44:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd7d238b822172b6a531e7531c209e036c2ce946d1bd13826e98faf0074509e`  
		Last Modified: Sat, 06 Jul 2024 02:44:28 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936bc7d78f5b5f33546a6edda318301bab57bf794afd8f97cb1e5c342112e97d`  
		Last Modified: Sat, 06 Jul 2024 05:55:00 GMT  
		Size: 1.4 MB (1354290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdb17c3c913e4b1f88ce8bdd226ee18d055c93f816d47358af49fd5c9190fda`  
		Last Modified: Sat, 06 Jul 2024 05:54:59 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9bc0606512d8b5a4a8671fc24214c57be3ab68f2f78866b6fc4e2f3a5e15b51`  
		Last Modified: Sat, 06 Jul 2024 05:55:00 GMT  
		Size: 726.3 KB (726339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf63719541b1c46093c86faeca409501899fd74efe1745dfc46803c990615d0`  
		Last Modified: Sat, 06 Jul 2024 05:55:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b4bffd69ca0f536847809781a2b27ed5682f008ea369ee14973f4ced0d22ae`  
		Last Modified: Sat, 06 Jul 2024 05:55:01 GMT  
		Size: 19.0 MB (18960331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:d551494257bf12724d191a9620d0979ac41c0008431b9f62ccd590632b3fd630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6640159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3ffd2b1cad33331f29fb8af4c2b694d224165fc8e02a18507a6ec420d74c19`

```dockerfile
```

-	Layers:
	-	`sha256:656b7bd09cef65848206f51076d5ea88e827799c7afa1e07def17cd0f9549ad1`  
		Last Modified: Sat, 06 Jul 2024 05:55:00 GMT  
		Size: 6.6 MB (6602553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:957380c1897980f2433d188149faba2eb090e58a0a463c9d50eb6ac1ac22b125`  
		Last Modified: Sat, 06 Jul 2024 05:54:59 GMT  
		Size: 37.6 KB (37606 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:7ac05f8584198bd46d94a9b89ea8c8e46e96d9c72313993c102c35549d05abad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193995189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a90ce99ee9716517c47ac327278c24d522cde15d2e05cc601a81eb5131d08c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 22 May 2024 23:55:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.9
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 May 2024 23:55:49 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 80
# Wed, 22 May 2024 23:55:49 GMT
CMD ["apache2-foreground"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d168c82669385a88cb2d49927f5d97a9fd361459c5ba221ade1b4833b14530`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be59d5943ae49be3e4ff309c07ef79eacf2bf161b53590db30e1227422f98601`  
		Last Modified: Tue, 02 Jul 2024 03:36:42 GMT  
		Size: 98.1 MB (98131121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702846940aedcd56970bc052b4e64fa8ff21b12b0a6ba8ca8273f4e256aaedc2`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8911daeb05e620d4f86e6e1800ae61553a08eaf29667c22d5a6bdae9461cada3`  
		Last Modified: Tue, 02 Jul 2024 03:37:07 GMT  
		Size: 20.3 MB (20321495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4028ee2076616a6cf681ab5e49658e589a2d0b1918e9213d61a41938d6b4299b`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4d03e54d8a1108c589658f102c0afa22f96cd422f05ace79e1ae3b68741d06`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c808eeca45116d3cfa07373e584b8a1db8647ac22533da62fb8f8c11f6269f`  
		Last Modified: Sat, 06 Jul 2024 02:29:19 GMT  
		Size: 12.8 MB (12802988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0dcb69f3122ee943fe6f146c2365efb2a50957037d930bc751d32a66c2a42a`  
		Last Modified: Sat, 06 Jul 2024 02:29:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c91c430be8ccbd4cb9c7e6d54f97f2b2ae9c2616ef3e4f83d512554e758c7d7`  
		Last Modified: Sat, 06 Jul 2024 02:29:18 GMT  
		Size: 11.6 MB (11633654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ecfba338a83ffa80f0f512fa3c5a3528172a8122a8585f0c0d44ca7badd951`  
		Last Modified: Sat, 06 Jul 2024 02:29:17 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90200d393b43d51ac053d747aebaf909383b6d37932a51653545340766c0bc3`  
		Last Modified: Sat, 06 Jul 2024 02:29:17 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91302423466fbe7c12650537186f35d032e9d4866153289ee75cc4e2c11586a`  
		Last Modified: Sat, 06 Jul 2024 02:29:17 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b14d4f0166d2e68bf24ee2f8e39cc66bd1b724f3850fd67252cf3215587e103`  
		Last Modified: Sat, 06 Jul 2024 05:55:27 GMT  
		Size: 2.3 MB (2256807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14a5170c7fbb2661bd461d3b918153121bacc4b352c58ba4b8cab3fa967527f`  
		Last Modified: Sat, 06 Jul 2024 05:55:27 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9ef84c6803da6eb34721f2687b5f4c8e6378f24d98fb86f56836f7066f6ada`  
		Last Modified: Sat, 06 Jul 2024 05:55:27 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5d76e379de59c668324ecae27eec9424d3c3f83b7b760ea14f678fa6d9021a`  
		Last Modified: Sat, 06 Jul 2024 05:55:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39421519eca079c475ce0ae542f7b5da0d7c6b698f11a8747e04e47ec1734143`  
		Last Modified: Sat, 06 Jul 2024 05:55:29 GMT  
		Size: 19.0 MB (18960339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:ad32515bd75c6437d36099222506c4a83db7a2d5b2c20997c71c2a859d315655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6853087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a387fa094398895cb2d968fa84de1b3d6bf7b7f14d8118a8df92ad8c770ac`

```dockerfile
```

-	Layers:
	-	`sha256:272f7d000c41715e785a28e8fc0bdaeb1a4c10052386dd20d41ef90771209e0c`  
		Last Modified: Sat, 06 Jul 2024 05:55:27 GMT  
		Size: 6.8 MB (6814946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e223169a5380d75768ea2caf053529b5fb839013b54f59fbf3148983e3fe707`  
		Last Modified: Sat, 06 Jul 2024 05:55:27 GMT  
		Size: 38.1 KB (38141 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache` - linux; 386

```console
$ docker pull drupal@sha256:92709614a9b7c88c124751933ec9ae61cd1deab9d484636b7f9c95ddeb28a557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198923983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dce0fa771def6fdbd76fd82f8a92689e5606bdcec169c4448f3baed4b8b889`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 22 May 2024 23:55:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 May 2024 23:55:49 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 80
# Wed, 22 May 2024 23:55:49 GMT
CMD ["apache2-foreground"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daa048202ff5a552b6eacd27b84297ac780821f0730574f9bb61ed3a6996e20`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d876e28acd3b5f3038bdfb0fb8fe720824179dc347e25e6d745ae512376fa6`  
		Last Modified: Tue, 02 Jul 2024 05:39:40 GMT  
		Size: 101.5 MB (101516977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe24ff1fc83352bac36eafb7daa5d32e7ea2232fe6fef612107fdbd1f81e7c8`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087987d024f8b2145282ca5bfbb784c34ed054bbc454fc96a25334882be4e1fe`  
		Last Modified: Tue, 02 Jul 2024 05:40:06 GMT  
		Size: 20.8 MB (20843476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723ec10434fcdc00676902f705fe56081a8fb0a774cb1a3a00894a4be83d8bf`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f856f33b11561e423f77df5f979a60b6dd4042c3f53df3d21647a29b671248`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b85e93cf20edc3a74338b3e76862967ce00db8edc95b80b225532ff96e0a81`  
		Last Modified: Tue, 02 Jul 2024 05:43:01 GMT  
		Size: 12.8 MB (12813175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563f24447dbb940aed06e6cbd3925fc83469da6fe26a8a5278139e07a43619c5`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa92b71a357d6cb4cd2b2ff75daf50f105c5b4862295d8f23059b0889279c68`  
		Last Modified: Tue, 02 Jul 2024 05:43:01 GMT  
		Size: 11.9 MB (11862314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7237f03a3d2814de9df424c01e8bb410509d39ade80450711ccd7517e8987745`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d7609802db7bd708d6cc8af552d1cdbff6c9f77315a1c1f21f85fce58be838`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c666f6279f00f518eaa5fcd4cfd3f5cdfbbdb17dd10fd1bd12018cc756e135a2`  
		Last Modified: Tue, 02 Jul 2024 05:42:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e01bceeac965ed03efe913433bd7daf0f4c18e750d4f2d65b4ce909b46ee31`  
		Last Modified: Tue, 02 Jul 2024 07:10:05 GMT  
		Size: 2.1 MB (2051147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d544d381be9027e88645f6f94b670e4922e8b935af12c6d6252f9a700d23a2b`  
		Last Modified: Tue, 02 Jul 2024 07:10:05 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b046453008d6dd7805c660d76a18b8a6acf4bad3e323f31a7f19e94b66d495`  
		Last Modified: Tue, 02 Jul 2024 07:10:05 GMT  
		Size: 726.3 KB (726337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3bb4bbfa5d514304f0d2a29d670bd66bea1c6f4e93c2f0fed7b55d14627b1a`  
		Last Modified: Tue, 02 Jul 2024 07:10:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2c4ae87cd9f4270f0c544f9bd51bae9e25a22896ad9b261fa0de8c7eb2d57`  
		Last Modified: Tue, 02 Jul 2024 07:10:06 GMT  
		Size: 19.0 MB (18960398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:11315c6499ff3e2bcdd293f71e106c0380436e184dd4fcdb978fe416f26620ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6804510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0473e83769570f79a734dfb2fa459f8876f9e25f7c2e92b080fe4752cb598272`

```dockerfile
```

-	Layers:
	-	`sha256:8ffb3021e6a7f7509f1daecc76f90d826c6f630a186fdecd69c8c4b0fb41635d`  
		Last Modified: Tue, 02 Jul 2024 07:10:04 GMT  
		Size: 6.8 MB (6767175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c82531829aa25433da7d013657a94d4fc9a880bca1151d34cec8744b85e1b4`  
		Last Modified: Tue, 02 Jul 2024 07:10:03 GMT  
		Size: 37.3 KB (37335 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:b4126179a42d55667d8b11e928e4ebfc400e40c58bcbc13405038ec4bca1eace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204366324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaabf71e13bc1f0fc3236bb8c26774caafdfecd05a4aa1712101c4f18e4e562c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 22 May 2024 23:55:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.8
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.8.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=aea358b56186f943c2bbd350c9005b9359133d47e954cfc561385319ae5bb8d7
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 May 2024 23:55:49 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 80
# Wed, 22 May 2024 23:55:49 GMT
CMD ["apache2-foreground"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609eb2596342a8a7f536a9dbbffcfccaaadff4bcd99626d15c588274979eaf2a`  
		Last Modified: Tue, 02 Jul 2024 04:14:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9e2e6a6e6ca971bb68e9cd39a2e7d46e2bacfa5a93def5ea728e84f1553a4`  
		Last Modified: Tue, 02 Jul 2024 04:15:02 GMT  
		Size: 103.3 MB (103317721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8703185de8bbe987d67d7808f74a14a5bcb767eadd604f0096503f998496675`  
		Last Modified: Tue, 02 Jul 2024 04:14:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bfa1030b231350ace419a1b1cb2251a16babac7f828c4850f38366b1a7319a`  
		Last Modified: Tue, 02 Jul 2024 04:15:27 GMT  
		Size: 21.5 MB (21511668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ed004f3d7d188c082021564296cd592b4b41057f3e2a33679c35c3e7bb1a2c`  
		Last Modified: Tue, 02 Jul 2024 04:15:25 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacb72cfc9dd2acb981ca25b9f1f57e62d7bf82694d0a3219b604b104ba52cab`  
		Last Modified: Tue, 02 Jul 2024 04:15:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee019b9c004127f837b9d2c7226e82ce292df62dd64d3519f65887ba0e610832`  
		Last Modified: Tue, 02 Jul 2024 04:18:11 GMT  
		Size: 12.8 MB (12813507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e766d42fda63ef67eed68be47d5f50878afdd1b4e4e880845c906520ea95410`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be12d2bf092f77e4d7fbbc8801fd8d7ed07ec2660abc9c5c2ba4037e37580a7f`  
		Last Modified: Tue, 02 Jul 2024 04:18:10 GMT  
		Size: 12.1 MB (12053279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2560c21f83acf49f4b81440045271ad23b81a4d67d6cc274297d909bc8459f4`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560bba3b36fb7d576c2975e69ceff7c67a7e861bfa9aff093cd913d759d6aa32`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa870c08d564e55bdd62cc1ac5d7bcddbd0cdba2a0ff9324091b67358d77e23f`  
		Last Modified: Tue, 02 Jul 2024 04:18:08 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2974446c78d9f05693f8a09bd6b112209acac368323811f594a3ca1b1cb574f1`  
		Last Modified: Wed, 03 Jul 2024 00:54:45 GMT  
		Size: 1.9 MB (1855280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa054e5820bd681288b716575ae97b78a693cd8cd52e724cfd5b2107f8a16909`  
		Last Modified: Wed, 03 Jul 2024 00:54:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccec073deddea2fb09d8fbbb8bd9380857b271450ff2ca1abce718d8da3bbb83`  
		Last Modified: Wed, 03 Jul 2024 00:54:46 GMT  
		Size: 726.3 KB (726349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d211b65b4e3f6a5946a79941c70ee094929c35a837b14042dc31a66360c278d`  
		Last Modified: Wed, 03 Jul 2024 00:54:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b12e19fd8908f5f5536de6866922a7e5a84e21ea89fd13b49e40a36d5ab6e`  
		Last Modified: Wed, 03 Jul 2024 00:54:47 GMT  
		Size: 19.0 MB (18960338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:8457448edc708c5a66800b9a8ae7cc2fbba0ce845acd7e574b5ff003faeac0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6801258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6abae0478d3a2324f7b10d30aeabae2bdb064c2bec55c561e8b47f275b363b0`

```dockerfile
```

-	Layers:
	-	`sha256:1af420cf038ce75a8c574d8116af6c263cd774172378891b495e3f35b13878f2`  
		Last Modified: Wed, 03 Jul 2024 00:54:42 GMT  
		Size: 6.8 MB (6763771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20d8a6cb437eb6c32c9b704c341811d79bbb58e7de003e29ca83b6438eab9a2`  
		Last Modified: Wed, 03 Jul 2024 00:54:41 GMT  
		Size: 37.5 KB (37487 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-apache` - linux; s390x

```console
$ docker pull drupal@sha256:e2a6a8c26ab8c7a935859287a7fb81b4c034e89b077d60ed23b3538914bc3c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173312016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd20aac69a8367f4271ec1b941f1010d56daf4762bb69afcb78dd8ebb1f0dd1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 22 May 2024 23:55:49 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Wed, 22 May 2024 23:55:49 GMT
CMD ["bash"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 May 2024 23:55:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 22 May 2024 23:55:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:55:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_VERSION=8.3.9
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Wed, 22 May 2024 23:55:49 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 May 2024 23:55:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:55:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:55:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:55:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 May 2024 23:55:49 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:55:49 GMT
EXPOSE 80
# Wed, 22 May 2024 23:55:49 GMT
CMD ["apache2-foreground"]
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 23:55:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:55:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV DRUPAL_VERSION=11.0.0-beta1
# Wed, 22 May 2024 23:55:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:55:49 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:55:49 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:55:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9251ecd224e15bee1af8e5d8ed06b4583727d21c25571b0841308fa40637020`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de732a471a32b9581046aa3735f5891fa36c8dc024c7c7a007087dd77b0bd3a`  
		Last Modified: Tue, 02 Jul 2024 03:05:16 GMT  
		Size: 80.8 MB (80817736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f9b6de1c71adae007cab6934b2b7dfe2155be5d6b7fecfea770f4dca1aa159`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac393ffa46cdbdd309e76835caefc39b9a5f28208a5117719850422e50cd1830`  
		Last Modified: Tue, 02 Jul 2024 03:05:34 GMT  
		Size: 20.1 MB (20101995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b9ac198003d25e1ae488b290fbd759f674d87fea5692596dc85177b0ad0014`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe10d7b17a1f1937efded756698b3791c41a781a95ad1f5b3436f29993e08d6`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a1e401e22a30c1a84de6bfe943be1b58e35d48b0d56c54e70479c70dd9d13b`  
		Last Modified: Sat, 06 Jul 2024 02:06:54 GMT  
		Size: 12.8 MB (12801714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a553866d91fce15a1f97db85ebaec6bbe8c22bdade8bcfa0631c4837b9a4913`  
		Last Modified: Sat, 06 Jul 2024 02:06:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d6a1422f3d37b7843d1e54588d4600ef1d905453f91d36358f0502a00eac43`  
		Last Modified: Sat, 06 Jul 2024 02:06:53 GMT  
		Size: 10.9 MB (10855018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf17256a0f72945095ea6187b56115a646cd8d88e86147497aaa559baa3417b`  
		Last Modified: Sat, 06 Jul 2024 02:06:52 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0295ac0611c0dd5393bff26a956265696c1b403552d906752604a1024fb0c3f3`  
		Last Modified: Sat, 06 Jul 2024 02:06:52 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ced62591fae0f3c6c86a76ecda707eeacee5fcc1bb602aec49921581b3d64bb`  
		Last Modified: Sat, 06 Jul 2024 02:06:52 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c856b0b7e51227b3311fc201cc418a735a93dbbaae862fe55715963c71f83a`  
		Last Modified: Sat, 06 Jul 2024 05:54:33 GMT  
		Size: 1.6 MB (1553095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bb7bf18f94289f43bd3eea7fd51b65c381c6e0f315c6ccb60347ceb482b46f`  
		Last Modified: Sat, 06 Jul 2024 05:54:33 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6184a2ccbfc9ff3a749f45560b47c7825359f6c85a457f771658f0f16e01a8ff`  
		Last Modified: Sat, 06 Jul 2024 05:54:33 GMT  
		Size: 726.3 KB (726338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebec3aede40d007fe252b615229ea29cbbd49e9732336af96d2455d0d6ae3ec`  
		Last Modified: Sat, 06 Jul 2024 05:54:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aec3d4a11ae0ac19c0517999b8319d6c65f19243067dd06144cf99d21a9d3b`  
		Last Modified: Sat, 06 Jul 2024 05:54:34 GMT  
		Size: 19.0 MB (18960148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:7a85029ba213ad43d645a23a155041bb373483fcdd617a2f9a16f962436260c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec112e2002b6c80dc94af2ed11d15406f8025ee25fb006c32ea7e9d6adfb3a3`

```dockerfile
```

-	Layers:
	-	`sha256:da5b5a2cc257bfc3332214be6fa36f8df7f17be378bca5b7f64b8c8bc4895f7c`  
		Last Modified: Sat, 06 Jul 2024 05:54:33 GMT  
		Size: 6.6 MB (6628864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34521bfc413b58a67cfdf9c3b9489551825cbd3b49fb8d469f954491688914c2`  
		Last Modified: Sat, 06 Jul 2024 05:54:33 GMT  
		Size: 37.4 KB (37448 bytes)  
		MIME: application/vnd.in-toto+json
