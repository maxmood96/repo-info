## `drupal:9-apache-buster`

```console
$ docker pull drupal@sha256:dabd6c2eefba165aad78419fe6ab9dbd14ba50884ebfa2fd21c3416510a4ad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `drupal:9-apache-buster` - linux; amd64

```console
$ docker pull drupal@sha256:6ae4e1df517cd2ecb755ec334f88ef8cacc651317728651644cb957c57f0bd12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171328395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb5fe99ea4b43e9a58302bf5e10596a62d62ef5f5a7f0faafafac294a3b8c49`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 12:19:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 01 Mar 2023 12:19:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Mar 2023 12:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 12:19:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Mar 2023 12:19:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 01 Mar 2023 12:22:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Mar 2023 12:22:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Mar 2023 12:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 01 Mar 2023 12:23:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 01 Mar 2023 12:23:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 01 Mar 2023 12:23:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 12:23:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 12:23:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Mar 2023 12:49:33 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 16 Mar 2023 22:26:22 GMT
ENV PHP_VERSION=8.1.17
# Thu, 16 Mar 2023 22:26:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Thu, 16 Mar 2023 22:26:23 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Thu, 16 Mar 2023 22:26:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Mar 2023 22:26:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Mar 2023 22:29:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 16 Mar 2023 22:29:39 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 16 Mar 2023 22:29:39 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Mar 2023 22:29:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Mar 2023 22:29:39 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Mar 2023 22:29:40 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 16 Mar 2023 22:29:40 GMT
WORKDIR /var/www/html
# Thu, 16 Mar 2023 22:29:40 GMT
EXPOSE 80
# Thu, 16 Mar 2023 22:29:40 GMT
CMD ["apache2-foreground"]
# Fri, 17 Mar 2023 00:34:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Mar 2023 00:34:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 21 Mar 2023 20:23:45 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Tue, 21 Mar 2023 20:25:15 GMT
ENV DRUPAL_VERSION=9.5.5
# Tue, 21 Mar 2023 20:25:15 GMT
WORKDIR /opt/drupal
# Tue, 21 Mar 2023 20:25:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 21 Mar 2023 20:25:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83b3ecc128c09ea7b53df46a0fbf2971d9dc77ac2893e52bc2784760a829c35`  
		Last Modified: Wed, 01 Mar 2023 13:30:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f0a974ccb7229aa047aa19e0fdbd29ef937f0ab2611c3d9265c383ae81b77`  
		Last Modified: Wed, 01 Mar 2023 13:30:49 GMT  
		Size: 76.7 MB (76693078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b974206414d9913df844efe41244bb1274c99d9eed1d2e818619ef9347fbc90e`  
		Last Modified: Wed, 01 Mar 2023 13:30:38 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7311be4befaaecefd363f933e93243768b5ce21b0a1c789c8470ad8482f15f`  
		Last Modified: Wed, 01 Mar 2023 13:31:16 GMT  
		Size: 18.7 MB (18685426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3b2e237166fb1c37dad149e0f5a982f11e02e4ecc09680c81acdd98cb7f9af`  
		Last Modified: Wed, 01 Mar 2023 13:31:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e023f8f4fcf29d6f222771168be5980e65a9a7928482bf7a3a82354fdd86b06a`  
		Last Modified: Wed, 01 Mar 2023 13:31:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5d03f819a4ca7c5b15466a2a8aeb4b25e36083571e39a45b6a2b238f1ba62`  
		Last Modified: Thu, 16 Mar 2023 23:12:16 GMT  
		Size: 12.2 MB (12158617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314a91d7a40f45f1dc053b3600b0cb27efb68a4412f9618c99bf80c1818a9eca`  
		Last Modified: Thu, 16 Mar 2023 23:12:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31b9bba396882df47b3edab577679acf59b9c35af640325b12c9ad1b052791b`  
		Last Modified: Thu, 16 Mar 2023 23:12:15 GMT  
		Size: 11.0 MB (11009242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e74b5ab0e0b8fd362a3ab861b6c9d18348f026f5d82d326269be0e1369dbed`  
		Last Modified: Thu, 16 Mar 2023 23:12:13 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d918b3247c340f6ccac0946d88ee5d9a5c58f275ca0ebe6067a6cf461095ff3`  
		Last Modified: Thu, 16 Mar 2023 23:12:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09cce3c63b68596b0db32061d1a239b0428b6a10ecad2721d27d1e1b039f21ef`  
		Last Modified: Thu, 16 Mar 2023 23:12:14 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd09c05277fa75a392d0b25cf4ceaa826b1279bdbdd370368d1c3eb6ccb6854`  
		Last Modified: Fri, 17 Mar 2023 00:52:20 GMT  
		Size: 2.1 MB (2089281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fa6c75ea4ac58defdcab2f0f6aa544b71c72de7fda77f78df7d1866d59e866`  
		Last Modified: Fri, 17 Mar 2023 00:52:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717d88f33d6f30136e9009390693a3e87f36e1940958369056bad0f64cc577a1`  
		Last Modified: Tue, 21 Mar 2023 20:37:10 GMT  
		Size: 697.5 KB (697532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8dddb68b34cc3a5047ee0a2f4824fa19988df1ec7059fd116362827406385bb`  
		Last Modified: Tue, 21 Mar 2023 20:39:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2217d1e6148717f228adbda0fab6303c0ce2d7ae755d475256d49059e792b638`  
		Last Modified: Tue, 21 Mar 2023 20:40:00 GMT  
		Size: 22.8 MB (22849297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b526bfa6bf31f9d46a192066fb05a6a4716fc35ae8959152ee81c7368722b37d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7a1d7d8db8090c3a8050192b03b96a65ed5399d2f90a26c3406d69366228d9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 01:20:33 GMT
ADD file:b3a5424864097d73516302c7e0a8fe9394880555c85f25a82a020ec3fc887eb8 in / 
# Thu, 23 Mar 2023 01:20:34 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 10:02:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 10:02:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 10:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 10:02:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Mar 2023 10:02:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Mar 2023 10:04:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Mar 2023 10:04:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Mar 2023 10:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Mar 2023 10:05:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Mar 2023 10:05:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Mar 2023 10:05:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 10:05:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 10:05:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Mar 2023 10:23:47 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Mar 2023 10:23:47 GMT
ENV PHP_VERSION=8.1.17
# Thu, 23 Mar 2023 10:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Thu, 23 Mar 2023 10:23:48 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Thu, 23 Mar 2023 10:23:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Mar 2023 10:23:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:26:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Mar 2023 10:26:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:26:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Mar 2023 10:26:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Mar 2023 10:26:10 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Mar 2023 10:26:10 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Mar 2023 10:26:10 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 10:26:10 GMT
EXPOSE 80
# Thu, 23 Mar 2023 10:26:10 GMT
CMD ["apache2-foreground"]
# Thu, 23 Mar 2023 17:36:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 17:36:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Mar 2023 17:36:18 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 23 Mar 2023 17:38:28 GMT
ENV DRUPAL_VERSION=9.5.5
# Thu, 23 Mar 2023 17:38:28 GMT
WORKDIR /opt/drupal
# Thu, 23 Mar 2023 17:39:03 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 23 Mar 2023 17:39:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:369fe072796976e1501c1a8d490c05b9ac47287c34c004013e0982d2dd4bb7c2`  
		Last Modified: Thu, 23 Mar 2023 01:33:32 GMT  
		Size: 22.7 MB (22748632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996895293e2c2af33f1bb50acd02b4400f04a4dcf57ddedd68e50599416caf53`  
		Last Modified: Thu, 23 Mar 2023 10:52:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb42cb3f50a59194bcc38d67ad256f4f2ea02d33a535cfc4746bfac34a85c8f8`  
		Last Modified: Thu, 23 Mar 2023 10:52:21 GMT  
		Size: 59.5 MB (59543404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf21d7202aeadab485cd99745b4decb146036e7aaac8737d3355b0e017f8564`  
		Last Modified: Thu, 23 Mar 2023 10:52:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf618cd406a3d9aa26189bf26a6dd1fa0581b028add545b12038d07b1003a0a`  
		Last Modified: Thu, 23 Mar 2023 10:52:47 GMT  
		Size: 17.5 MB (17481692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd35a73f0d26550e8a93c2d51126a0166093cbe4a1ac6f9beb5bc56336ed6711`  
		Last Modified: Thu, 23 Mar 2023 10:52:45 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07596d7b35761071bc642f77ba3061f9dff257addc2626f4c73e4f81e661212`  
		Last Modified: Thu, 23 Mar 2023 10:52:44 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e2dd8c7b838bb99d0a623fc87a9500a931f153ddb261d326668b6e9dda62cf`  
		Last Modified: Thu, 23 Mar 2023 10:55:16 GMT  
		Size: 12.2 MB (12156575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f818b6527def82d2cc8c463c7b9328c84589c9f9ea32c9061c4fa8bc3cfad`  
		Last Modified: Thu, 23 Mar 2023 10:55:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dd5e79ead55240ebd78219323a4525e420a31f21c4db9eeb69abe379cc0380`  
		Last Modified: Thu, 23 Mar 2023 10:55:16 GMT  
		Size: 9.5 MB (9506395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64458b5dba6cf40bdb30fe72f115b115482bf48eb2ddc77614809ec00179e09a`  
		Last Modified: Thu, 23 Mar 2023 10:55:14 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fcf2a4b41f968a6cb8c6d5cb10f2fc7aab20a512fa109a775452301b85de50`  
		Last Modified: Thu, 23 Mar 2023 10:55:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e70cfb21e75ab078815b7cf66f922abf5b2e9f58e60d35b3293f4e3170ac5a`  
		Last Modified: Thu, 23 Mar 2023 10:55:14 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8276298f2f3cc95719dbe245244284e70c8b7ea4ce575305cfcecb3f52ec0425`  
		Last Modified: Thu, 23 Mar 2023 17:53:38 GMT  
		Size: 1.5 MB (1481594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322cad230a5600325d86e6218c67ced390d0b7a881441d14d17658c9c89ee243`  
		Last Modified: Thu, 23 Mar 2023 17:53:37 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ddfdc1dd500329fe079a41fea0dc0a38e0a6413cc8aaddd3c619ccbed6c3a6`  
		Last Modified: Thu, 23 Mar 2023 17:53:38 GMT  
		Size: 697.5 KB (697533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c34ec136fdcc3a4255ebd4d342920046b3332131ba0b4beda4c574f8de29f9`  
		Last Modified: Thu, 23 Mar 2023 17:55:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c244eda597d2614fffa4535983f394d0ecd3c0d3050f7fb7ae4d45b1639ec2`  
		Last Modified: Thu, 23 Mar 2023 17:56:01 GMT  
		Size: 22.8 MB (22849971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:e08be7386227ecce9fc34cd7d6eec767358aae8871f2a8ac57a7841201b993cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164021376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef98f9e0b10547d4bd0e0c15c028cdab0e8894f05b91dd74dc833b548a6580f4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:23 GMT
ADD file:44e400cc6a1bc5df5a57bda478c9accf9b58950fa2fd069cc7620128fe786770 in / 
# Thu, 23 Mar 2023 00:45:23 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:24:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Mar 2023 12:24:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Mar 2023 12:25:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:25:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Mar 2023 12:25:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Mar 2023 12:28:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 23 Mar 2023 12:28:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 23 Mar 2023 12:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 23 Mar 2023 12:28:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 23 Mar 2023 12:28:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 23 Mar 2023 12:28:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 12:28:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Mar 2023 12:28:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Mar 2023 12:52:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Mar 2023 12:52:35 GMT
ENV PHP_VERSION=8.1.17
# Thu, 23 Mar 2023 12:52:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Thu, 23 Mar 2023 12:52:35 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Thu, 23 Mar 2023 12:52:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Mar 2023 12:52:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:55:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Mar 2023 12:55:33 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:55:34 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Mar 2023 12:55:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Mar 2023 12:55:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 23 Mar 2023 12:55:34 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:55:34 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:55:34 GMT
EXPOSE 80
# Thu, 23 Mar 2023 12:55:34 GMT
CMD ["apache2-foreground"]
# Thu, 23 Mar 2023 19:49:14 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 19:49:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Mar 2023 19:49:15 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Thu, 23 Mar 2023 19:51:55 GMT
ENV DRUPAL_VERSION=9.5.5
# Thu, 23 Mar 2023 19:51:55 GMT
WORKDIR /opt/drupal
# Thu, 23 Mar 2023 19:52:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 23 Mar 2023 19:52:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cfe0f778e53ce031ef449bc02975a07f2568716dea807ed2f390d352c0001972`  
		Last Modified: Thu, 23 Mar 2023 00:48:45 GMT  
		Size: 25.9 MB (25922660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d986ff4e4cf97a42b83fd9c83a28cd860ad9466daad20f215ac4148673a58052`  
		Last Modified: Thu, 23 Mar 2023 13:22:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdb88fcece1e9a98713860e0048b95dffe1a07d8480d365491a749fb1dab1ce`  
		Last Modified: Thu, 23 Mar 2023 13:22:33 GMT  
		Size: 70.4 MB (70365819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d88f9e53082155e46ba1806c06508e8e86a204eac61d69b95f1340ca74d1a`  
		Last Modified: Thu, 23 Mar 2023 13:22:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598f4fed24c0975b0ed9c475b52dc64798b18909fc45b1ff496d44c2ca203735`  
		Last Modified: Thu, 23 Mar 2023 13:22:58 GMT  
		Size: 18.6 MB (18585841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4713c9f3df8c793d45bd52f2649ca1c46c8c8f4e7f00e2366c0c69b9081e5ec`  
		Last Modified: Thu, 23 Mar 2023 13:22:56 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac5ce312fb6c8c8db4227d097a61da363efea342381b76d848703b8f428ed98`  
		Last Modified: Thu, 23 Mar 2023 13:22:56 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b963010d365ddf93c6c2c895f858d56ee4bbef09edbb6d283ca6283ea29b383`  
		Last Modified: Thu, 23 Mar 2023 13:25:28 GMT  
		Size: 12.2 MB (12157338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a54fdd2a480abeff6439a1dfc0f451b2414c1fed2d5156c2f0ea228a7c94bd6`  
		Last Modified: Thu, 23 Mar 2023 13:25:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962d4dc1a2adb6610238a50b1eb0fe43d1da47202e9019aee7665c378a2117d1`  
		Last Modified: Thu, 23 Mar 2023 13:25:27 GMT  
		Size: 11.1 MB (11080200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d90434d3166760c0c886e857af74aa3c108b740e6965779926dce40f125991`  
		Last Modified: Thu, 23 Mar 2023 13:25:25 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7155da86e0e85eb5ce39b2352a2f6a5b8426ee78ac2c1ba0977d14a5c3042f7b`  
		Last Modified: Thu, 23 Mar 2023 13:25:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adb9378a9d58c77ef6b755097bcc57b722d3bc9344e17951415bd62885c22f7`  
		Last Modified: Thu, 23 Mar 2023 13:25:25 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a441549abc0339c761b18c7858a8ac87c98b8d843c83c5ea5d0f79fcad53a60`  
		Last Modified: Thu, 23 Mar 2023 20:04:45 GMT  
		Size: 2.4 MB (2356865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e3fdeaa5633a4b5128d00670b989103c8227d18fb5f6b3a037a87e4ac6d842`  
		Last Modified: Thu, 23 Mar 2023 20:04:44 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f95de1f3b34dcaa0131aa32bb372fffc49717ff1a00d3725b8d2afbde436ca`  
		Last Modified: Thu, 23 Mar 2023 20:04:45 GMT  
		Size: 697.5 KB (697532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9c18dde3bc46ad45db0bf5e920b24c84de9c8cf2c2ee15303146b38c3a2b42`  
		Last Modified: Thu, 23 Mar 2023 20:06:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a41268f133c41ad8756debf0f852abfe1cef694e59b85da84faa0eff5e4fe1c`  
		Last Modified: Thu, 23 Mar 2023 20:06:51 GMT  
		Size: 22.8 MB (22849086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:9-apache-buster` - linux; 386

```console
$ docker pull drupal@sha256:9ba507681176708dd97ac521fa947c2330df24178a2fb120b6dad77059f41b4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.3 MB (177255462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d950676d8332b3606672c2e20a330eed735b642ecabfd123411b657243e8a7b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:35 GMT
ADD file:d90e1c78fceb91ea00c9b00cdf477b7254e3d4d37b561698e90b75c62d84320c in / 
# Wed, 01 Mar 2023 01:39:35 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 14:47:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 01 Mar 2023 14:47:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 01 Mar 2023 14:47:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 14:47:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 01 Mar 2023 14:47:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 01 Mar 2023 14:52:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 01 Mar 2023 14:52:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 01 Mar 2023 14:53:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 01 Mar 2023 14:53:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 01 Mar 2023 14:53:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 01 Mar 2023 14:53:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 14:53:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 01 Mar 2023 14:53:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 01 Mar 2023 16:15:38 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 16 Mar 2023 23:32:47 GMT
ENV PHP_VERSION=8.1.17
# Thu, 16 Mar 2023 23:32:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.17.tar.xz.asc
# Thu, 16 Mar 2023 23:32:47 GMT
ENV PHP_SHA256=b5c48f95b8e1d8624dd05fc2eab7be13277f9a203ccba97bdca5a1a0fb4a1460
# Thu, 16 Mar 2023 23:32:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Mar 2023 23:32:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Mar 2023 23:37:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 16 Mar 2023 23:37:44 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 16 Mar 2023 23:37:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Mar 2023 23:37:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Mar 2023 23:37:44 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Mar 2023 23:37:45 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 16 Mar 2023 23:37:45 GMT
WORKDIR /var/www/html
# Thu, 16 Mar 2023 23:37:45 GMT
EXPOSE 80
# Thu, 16 Mar 2023 23:37:45 GMT
CMD ["apache2-foreground"]
# Fri, 17 Mar 2023 01:21:39 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Mar 2023 01:21:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 21 Mar 2023 21:04:33 GMT
COPY file:3cfddcfffbb1a2b0544304897907e3a08247bd92e3e7f53da87a4646baf89113 in /usr/local/bin/ 
# Tue, 21 Mar 2023 21:06:09 GMT
ENV DRUPAL_VERSION=9.5.5
# Tue, 21 Mar 2023 21:06:09 GMT
WORKDIR /opt/drupal
# Tue, 21 Mar 2023 21:06:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Tue, 21 Mar 2023 21:06:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5dd0dee7d259a761fe8021e1fd6a2a9a8590880098b27d4f97cfbda4e50bc631`  
		Last Modified: Wed, 01 Mar 2023 01:45:36 GMT  
		Size: 27.8 MB (27798766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387c6bf19cab4ac9a56c078c6948c57f559d8d6a8188a9f8479f1a3ba2d7cdbd`  
		Last Modified: Wed, 01 Mar 2023 18:21:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c1ee9425978cc9dee96402d220271f287bd024f8e3f70b60b45e54626ad6d`  
		Last Modified: Wed, 01 Mar 2023 18:22:13 GMT  
		Size: 81.2 MB (81238084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a0778af02b444a917ecc9c784e60e3f0600ac5b79779d0c9c45fc5142d06e3`  
		Last Modified: Wed, 01 Mar 2023 18:21:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28022b3a19c3b0e511a813ff76da4dd9249618ded71866118b549444a54dd9d2`  
		Last Modified: Wed, 01 Mar 2023 18:22:48 GMT  
		Size: 19.1 MB (19116261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110aa2434c6ea7bd36e9a6545e39bd768d2632b85686d39f94ff6c99a3db4a9`  
		Last Modified: Wed, 01 Mar 2023 18:22:44 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90394f28f547516f93afb2b3de5e8896544b6b0d7e2cc802f3e2a5910ae99cda`  
		Last Modified: Wed, 01 Mar 2023 18:22:44 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795e27bbd0de8f0c876977b26c4157cc8d5cde21dfdd85678ab493830ee4566f`  
		Last Modified: Fri, 17 Mar 2023 00:47:17 GMT  
		Size: 12.2 MB (12157977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7bc4f98df29c8c9804431b64c45fc33838305a6c148d912622d929a65ab5c5`  
		Last Modified: Fri, 17 Mar 2023 00:47:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92886c83140c7a8eb7c5186edf56a72e13450f446ab4362cb09d1e2d315a4492`  
		Last Modified: Fri, 17 Mar 2023 00:47:16 GMT  
		Size: 11.2 MB (11233477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874d301c8a3ad287bd7299a0310cd80530813ab603037761f94a2daac934c7c1`  
		Last Modified: Fri, 17 Mar 2023 00:47:13 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8179d35c9fabd8feb62d8cb87406405191070cb235592a4f7963b127d44febb6`  
		Last Modified: Fri, 17 Mar 2023 00:47:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2901ffba5e155d19ba54a5a857fe12536282ffb363524a36ea4f0decc305878`  
		Last Modified: Fri, 17 Mar 2023 00:47:13 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0f7e801c5089ec1f1f85ed7fc017ddee748e4f89d5f8a025496cc5b5024c3`  
		Last Modified: Fri, 17 Mar 2023 01:49:21 GMT  
		Size: 2.2 MB (2158083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a84941256f2e700746e0c8ba17615699dd47e55574dac51934870a64c254eaa`  
		Last Modified: Fri, 17 Mar 2023 01:49:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7689805be81a3cdecac992775e4a29fbaa97999c82e2ad49cc4181d32736b5`  
		Last Modified: Tue, 21 Mar 2023 21:19:39 GMT  
		Size: 697.5 KB (697533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f198454903f98e62d8d0f83a08babb7f1550b3139b485e4265557ffd3e1a3f`  
		Last Modified: Tue, 21 Mar 2023 21:22:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce0434089d75264436104d442807157ffdc6e3bbb399cb2f256fe422c5ab325`  
		Last Modified: Tue, 21 Mar 2023 21:22:52 GMT  
		Size: 22.8 MB (22849233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
