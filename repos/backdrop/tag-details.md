<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.23`](#backdrop123)
-	[`backdrop:1.23-apache`](#backdrop123-apache)
-	[`backdrop:1.23-fpm`](#backdrop123-fpm)
-	[`backdrop:1.23.1`](#backdrop1231)
-	[`backdrop:1.23.1-apache`](#backdrop1231-apache)
-	[`backdrop:1.23.1-fpm`](#backdrop1231-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:9bfa43ae7d9ad8e4c649e807878ac09b0d00e13e6c708b98a9295d8bd4b98e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:c1b185b1c970eaafba96b5084127ef48d2d53c0c0f830346f25044a736cccf80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172550649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c152cc2c4194a9d32a11eee167bf99e4d823324b9287d2fcc8225ce4a7976d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:01:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:27:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:27:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:37:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:37:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:37:40 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:37:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 21 Dec 2022 06:37:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 21 Dec 2022 06:37:41 GMT
EXPOSE 9000
# Wed, 21 Dec 2022 06:37:41 GMT
CMD ["php-fpm"]
# Wed, 21 Dec 2022 13:13:57 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:13:57 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:14:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:14:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:14:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:14:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05209be6c55a9a6b35e4cc9153b2d815cd9838a3b286de7fd47425c69b6512`  
		Last Modified: Wed, 21 Dec 2022 07:33:42 GMT  
		Size: 12.1 MB (12122177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94128e45b6c6c024aac8ca729c9b43ef9dbae9774fc5628fe76d9fdbe498b303`  
		Last Modified: Wed, 21 Dec 2022 07:33:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e149b2dc30e4e6c18ef77ef9d49fa120a822168f0ceed1f61d0f1b28c7d4f`  
		Last Modified: Wed, 21 Dec 2022 07:34:28 GMT  
		Size: 26.2 MB (26232687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2120d157865f86b5fb5b9b27b33c4ee020ecd430a6c4b63b83164785cd7d389`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213d22620fe9e3fd8685eb5c5114eeb02f1906fe355402d0aae9e1399322037`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173661a951b431fd591dcb9106dd0591f1f05743293aafb9f8ebabf9d381536`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8fc5a8f506ed6683947a508a5cc5e4bd5d096cf0dc38e23fd155956182719c`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 2.4 MB (2418868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078c219484db1588548fc6a04f25f80be0d7a6bd2f712635902ca250a2575b94`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 8.7 MB (8732052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b00062fbd4e71612598c9000dae3fe2504c1b8e3df388b5a1e30598b9d05c1`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:32a9739a10b0b94f211c5695415bda6075d0cbf92da093bef4ba1711d82e8146
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166442242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf67cefc45f8352f179507df29105834af71e240857695170d180ef5be3c3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:55:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:34:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:43:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:43:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:43:23 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:43:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 00:43:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 00:43:24 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 00:43:24 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:24:21 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:24:21 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:24:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:24:24 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:24:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e90c3eb2b94f907241b1f597aa010d3c868c13194711aaa59d0ce142605d1d`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 12.1 MB (12070648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d5c14f0b50e7037eccd7b541d3a6c66d11cb94ab9059ae3bf03d197b9e726`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab484ef8c694e6aa09c73cf0bf8215b1e00d2d48d3a5e58e66433302ca2a6791`  
		Last Modified: Fri, 06 Jan 2023 02:01:23 GMT  
		Size: 26.3 MB (26273553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839f659848fa8e2814fe589e3e2fb7467a52e30227b5d829cb59a2517811cda`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bf1047b15b358d729fd544bf759b3def1b85cb9135dbbcc673f495996053d5`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffac7a155630dcba3a09abb6f6355a0d1dab71775b8f04374be6922dea7a01e`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f4b70034840e738a31cb0c6f198d018aa64ba1f5e0b69e7c17aa11a786340`  
		Last Modified: Fri, 06 Jan 2023 02:25:14 GMT  
		Size: 2.4 MB (2381274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff67abe49d60f324b15062a4c31268895ef960121d5d764999745d1e691988c`  
		Last Modified: Fri, 06 Jan 2023 02:25:15 GMT  
		Size: 8.7 MB (8732036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94641a54a0a9c1f2125cfa62d07c7d83813435767c3c4475e0490e9cb704b0`  
		Last Modified: Fri, 06 Jan 2023 02:25:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.23`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.23` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.23` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.23-apache`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.23-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.23-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.23-fpm`

```console
$ docker pull backdrop@sha256:9bfa43ae7d9ad8e4c649e807878ac09b0d00e13e6c708b98a9295d8bd4b98e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.23-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:c1b185b1c970eaafba96b5084127ef48d2d53c0c0f830346f25044a736cccf80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172550649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c152cc2c4194a9d32a11eee167bf99e4d823324b9287d2fcc8225ce4a7976d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:01:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:27:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:27:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:37:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:37:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:37:40 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:37:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 21 Dec 2022 06:37:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 21 Dec 2022 06:37:41 GMT
EXPOSE 9000
# Wed, 21 Dec 2022 06:37:41 GMT
CMD ["php-fpm"]
# Wed, 21 Dec 2022 13:13:57 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:13:57 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:14:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:14:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:14:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:14:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05209be6c55a9a6b35e4cc9153b2d815cd9838a3b286de7fd47425c69b6512`  
		Last Modified: Wed, 21 Dec 2022 07:33:42 GMT  
		Size: 12.1 MB (12122177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94128e45b6c6c024aac8ca729c9b43ef9dbae9774fc5628fe76d9fdbe498b303`  
		Last Modified: Wed, 21 Dec 2022 07:33:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e149b2dc30e4e6c18ef77ef9d49fa120a822168f0ceed1f61d0f1b28c7d4f`  
		Last Modified: Wed, 21 Dec 2022 07:34:28 GMT  
		Size: 26.2 MB (26232687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2120d157865f86b5fb5b9b27b33c4ee020ecd430a6c4b63b83164785cd7d389`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213d22620fe9e3fd8685eb5c5114eeb02f1906fe355402d0aae9e1399322037`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173661a951b431fd591dcb9106dd0591f1f05743293aafb9f8ebabf9d381536`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8fc5a8f506ed6683947a508a5cc5e4bd5d096cf0dc38e23fd155956182719c`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 2.4 MB (2418868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078c219484db1588548fc6a04f25f80be0d7a6bd2f712635902ca250a2575b94`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 8.7 MB (8732052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b00062fbd4e71612598c9000dae3fe2504c1b8e3df388b5a1e30598b9d05c1`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.23-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:32a9739a10b0b94f211c5695415bda6075d0cbf92da093bef4ba1711d82e8146
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166442242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf67cefc45f8352f179507df29105834af71e240857695170d180ef5be3c3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:55:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:34:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:43:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:43:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:43:23 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:43:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 00:43:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 00:43:24 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 00:43:24 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:24:21 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:24:21 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:24:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:24:24 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:24:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e90c3eb2b94f907241b1f597aa010d3c868c13194711aaa59d0ce142605d1d`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 12.1 MB (12070648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d5c14f0b50e7037eccd7b541d3a6c66d11cb94ab9059ae3bf03d197b9e726`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab484ef8c694e6aa09c73cf0bf8215b1e00d2d48d3a5e58e66433302ca2a6791`  
		Last Modified: Fri, 06 Jan 2023 02:01:23 GMT  
		Size: 26.3 MB (26273553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839f659848fa8e2814fe589e3e2fb7467a52e30227b5d829cb59a2517811cda`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bf1047b15b358d729fd544bf759b3def1b85cb9135dbbcc673f495996053d5`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffac7a155630dcba3a09abb6f6355a0d1dab71775b8f04374be6922dea7a01e`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f4b70034840e738a31cb0c6f198d018aa64ba1f5e0b69e7c17aa11a786340`  
		Last Modified: Fri, 06 Jan 2023 02:25:14 GMT  
		Size: 2.4 MB (2381274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff67abe49d60f324b15062a4c31268895ef960121d5d764999745d1e691988c`  
		Last Modified: Fri, 06 Jan 2023 02:25:15 GMT  
		Size: 8.7 MB (8732036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94641a54a0a9c1f2125cfa62d07c7d83813435767c3c4475e0490e9cb704b0`  
		Last Modified: Fri, 06 Jan 2023 02:25:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.23.1`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.23.1` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.23.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.23.1-apache`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.23.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.23.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:1.23.1-fpm`

```console
$ docker pull backdrop@sha256:9bfa43ae7d9ad8e4c649e807878ac09b0d00e13e6c708b98a9295d8bd4b98e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1.23.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:c1b185b1c970eaafba96b5084127ef48d2d53c0c0f830346f25044a736cccf80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172550649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c152cc2c4194a9d32a11eee167bf99e4d823324b9287d2fcc8225ce4a7976d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:01:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:27:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:27:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:37:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:37:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:37:40 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:37:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 21 Dec 2022 06:37:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 21 Dec 2022 06:37:41 GMT
EXPOSE 9000
# Wed, 21 Dec 2022 06:37:41 GMT
CMD ["php-fpm"]
# Wed, 21 Dec 2022 13:13:57 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:13:57 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:14:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:14:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:14:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:14:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05209be6c55a9a6b35e4cc9153b2d815cd9838a3b286de7fd47425c69b6512`  
		Last Modified: Wed, 21 Dec 2022 07:33:42 GMT  
		Size: 12.1 MB (12122177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94128e45b6c6c024aac8ca729c9b43ef9dbae9774fc5628fe76d9fdbe498b303`  
		Last Modified: Wed, 21 Dec 2022 07:33:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e149b2dc30e4e6c18ef77ef9d49fa120a822168f0ceed1f61d0f1b28c7d4f`  
		Last Modified: Wed, 21 Dec 2022 07:34:28 GMT  
		Size: 26.2 MB (26232687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2120d157865f86b5fb5b9b27b33c4ee020ecd430a6c4b63b83164785cd7d389`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213d22620fe9e3fd8685eb5c5114eeb02f1906fe355402d0aae9e1399322037`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173661a951b431fd591dcb9106dd0591f1f05743293aafb9f8ebabf9d381536`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8fc5a8f506ed6683947a508a5cc5e4bd5d096cf0dc38e23fd155956182719c`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 2.4 MB (2418868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078c219484db1588548fc6a04f25f80be0d7a6bd2f712635902ca250a2575b94`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 8.7 MB (8732052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b00062fbd4e71612598c9000dae3fe2504c1b8e3df388b5a1e30598b9d05c1`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1.23.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:32a9739a10b0b94f211c5695415bda6075d0cbf92da093bef4ba1711d82e8146
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166442242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf67cefc45f8352f179507df29105834af71e240857695170d180ef5be3c3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:55:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:34:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:43:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:43:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:43:23 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:43:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 00:43:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 00:43:24 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 00:43:24 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:24:21 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:24:21 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:24:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:24:24 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:24:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e90c3eb2b94f907241b1f597aa010d3c868c13194711aaa59d0ce142605d1d`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 12.1 MB (12070648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d5c14f0b50e7037eccd7b541d3a6c66d11cb94ab9059ae3bf03d197b9e726`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab484ef8c694e6aa09c73cf0bf8215b1e00d2d48d3a5e58e66433302ca2a6791`  
		Last Modified: Fri, 06 Jan 2023 02:01:23 GMT  
		Size: 26.3 MB (26273553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839f659848fa8e2814fe589e3e2fb7467a52e30227b5d829cb59a2517811cda`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bf1047b15b358d729fd544bf759b3def1b85cb9135dbbcc673f495996053d5`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffac7a155630dcba3a09abb6f6355a0d1dab71775b8f04374be6922dea7a01e`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f4b70034840e738a31cb0c6f198d018aa64ba1f5e0b69e7c17aa11a786340`  
		Last Modified: Fri, 06 Jan 2023 02:25:14 GMT  
		Size: 2.4 MB (2381274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff67abe49d60f324b15062a4c31268895ef960121d5d764999745d1e691988c`  
		Last Modified: Fri, 06 Jan 2023 02:25:15 GMT  
		Size: 8.7 MB (8732036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94641a54a0a9c1f2125cfa62d07c7d83813435767c3c4475e0490e9cb704b0`  
		Last Modified: Fri, 06 Jan 2023 02:25:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:9bfa43ae7d9ad8e4c649e807878ac09b0d00e13e6c708b98a9295d8bd4b98e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:c1b185b1c970eaafba96b5084127ef48d2d53c0c0f830346f25044a736cccf80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172550649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c152cc2c4194a9d32a11eee167bf99e4d823324b9287d2fcc8225ce4a7976d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:06:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:01:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:27:35 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:27:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:27:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:37:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:37:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:37:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:37:40 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:37:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 21 Dec 2022 06:37:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 21 Dec 2022 06:37:41 GMT
EXPOSE 9000
# Wed, 21 Dec 2022 06:37:41 GMT
CMD ["php-fpm"]
# Wed, 21 Dec 2022 13:13:57 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:13:57 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:13:57 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:14:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:14:01 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:14:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:14:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f05209be6c55a9a6b35e4cc9153b2d815cd9838a3b286de7fd47425c69b6512`  
		Last Modified: Wed, 21 Dec 2022 07:33:42 GMT  
		Size: 12.1 MB (12122177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94128e45b6c6c024aac8ca729c9b43ef9dbae9774fc5628fe76d9fdbe498b303`  
		Last Modified: Wed, 21 Dec 2022 07:33:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e149b2dc30e4e6c18ef77ef9d49fa120a822168f0ceed1f61d0f1b28c7d4f`  
		Last Modified: Wed, 21 Dec 2022 07:34:28 GMT  
		Size: 26.2 MB (26232687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2120d157865f86b5fb5b9b27b33c4ee020ecd430a6c4b63b83164785cd7d389`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213d22620fe9e3fd8685eb5c5114eeb02f1906fe355402d0aae9e1399322037`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a173661a951b431fd591dcb9106dd0591f1f05743293aafb9f8ebabf9d381536`  
		Last Modified: Wed, 21 Dec 2022 07:34:24 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8fc5a8f506ed6683947a508a5cc5e4bd5d096cf0dc38e23fd155956182719c`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 2.4 MB (2418868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078c219484db1588548fc6a04f25f80be0d7a6bd2f712635902ca250a2575b94`  
		Last Modified: Wed, 21 Dec 2022 13:14:56 GMT  
		Size: 8.7 MB (8732052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b00062fbd4e71612598c9000dae3fe2504c1b8e3df388b5a1e30598b9d05c1`  
		Last Modified: Wed, 21 Dec 2022 13:14:54 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:32a9739a10b0b94f211c5695415bda6075d0cbf92da093bef4ba1711d82e8146
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166442242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ecf67cefc45f8352f179507df29105834af71e240857695170d180ef5be3c3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:55:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:33:58 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:34:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:34:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:43:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:43:23 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:43:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:43:23 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:43:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Jan 2023 00:43:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Jan 2023 00:43:24 GMT
EXPOSE 9000
# Fri, 06 Jan 2023 00:43:24 GMT
CMD ["php-fpm"]
# Fri, 06 Jan 2023 02:24:21 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:24:21 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:24:21 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:24:24 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:24:24 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:24:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:24:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e90c3eb2b94f907241b1f597aa010d3c868c13194711aaa59d0ce142605d1d`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 12.1 MB (12070648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d5c14f0b50e7037eccd7b541d3a6c66d11cb94ab9059ae3bf03d197b9e726`  
		Last Modified: Fri, 06 Jan 2023 02:00:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab484ef8c694e6aa09c73cf0bf8215b1e00d2d48d3a5e58e66433302ca2a6791`  
		Last Modified: Fri, 06 Jan 2023 02:01:23 GMT  
		Size: 26.3 MB (26273553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839f659848fa8e2814fe589e3e2fb7467a52e30227b5d829cb59a2517811cda`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bf1047b15b358d729fd544bf759b3def1b85cb9135dbbcc673f495996053d5`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffac7a155630dcba3a09abb6f6355a0d1dab71775b8f04374be6922dea7a01e`  
		Last Modified: Fri, 06 Jan 2023 02:01:19 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f4b70034840e738a31cb0c6f198d018aa64ba1f5e0b69e7c17aa11a786340`  
		Last Modified: Fri, 06 Jan 2023 02:25:14 GMT  
		Size: 2.4 MB (2381274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff67abe49d60f324b15062a4c31268895ef960121d5d764999745d1e691988c`  
		Last Modified: Fri, 06 Jan 2023 02:25:15 GMT  
		Size: 8.7 MB (8732036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a94641a54a0a9c1f2125cfa62d07c7d83813435767c3c4475e0490e9cb704b0`  
		Last Modified: Fri, 06 Jan 2023 02:25:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:97b44236c664479750b5d13c428bf0c10e2c1b854b1a22d922e81acf918bddcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:0ebf80316668b424e522340eaf46d337d4472de774ea8a4a163e55d4ae494afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176651424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda81a69e52ca1ac7d6d72f24b66d08579b9d9406e46ae89a2029fd10804208`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:06:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 05:06:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 05:06:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:06:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 05:06:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 05:10:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 05:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 05:10:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 05:10:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 05:10:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:04:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_VERSION=8.1.13
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.13.tar.xz.asc
# Wed, 21 Dec 2022 06:30:58 GMT
ENV PHP_SHA256=b15ef0ccdd6760825604b3c4e3e73558dcf87c75ef1d68ef4289d8fd261ac856
# Wed, 21 Dec 2022 06:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 21 Dec 2022 06:31:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 21 Dec 2022 06:34:19 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 21 Dec 2022 06:34:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 21 Dec 2022 06:34:20 GMT
STOPSIGNAL SIGWINCH
# Wed, 21 Dec 2022 06:34:20 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 21 Dec 2022 06:34:20 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 06:34:20 GMT
EXPOSE 80
# Wed, 21 Dec 2022 06:34:20 GMT
CMD ["apache2-foreground"]
# Wed, 21 Dec 2022 13:11:52 GMT
RUN a2enmod rewrite
# Wed, 21 Dec 2022 13:12:50 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 21 Dec 2022 13:12:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_VERSION=1.23.1
# Wed, 21 Dec 2022 13:12:50 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Wed, 21 Dec 2022 13:12:54 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 21 Dec 2022 13:12:54 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 21 Dec 2022 13:12:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 13:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460703cf6140962e339a7c3f30256a39b69e89993380fb3c15ad2b939ae0859d`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba06349db8787dc6357728498b0da33035875a4d3fa2113c40809c3ba14a2f5`  
		Last Modified: Wed, 21 Dec 2022 07:25:13 GMT  
		Size: 91.6 MB (91634656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130a4183abd1de004c2a4f7a86e4d4e2344614fbd43930c3e97830d7c26b4e7`  
		Last Modified: Wed, 21 Dec 2022 07:24:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd60536a08336b41945e7667d501c28c5ea1616423e0ad8dbeb58c6d2013fcaa`  
		Last Modified: Wed, 21 Dec 2022 07:25:40 GMT  
		Size: 19.2 MB (19244681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e54498bf197269e593073f1b94750016135dcba55424358c496c8741ce09d7`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9812d18c874fda64d6dafda204537681dbdbf44229ad4b0249f1bbb33e51ca50`  
		Last Modified: Wed, 21 Dec 2022 07:25:37 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1e11976b9c817fcdb047b4242f20551304afa5eb5de5002baaa6c9ecf8fa61`  
		Last Modified: Wed, 21 Dec 2022 07:34:11 GMT  
		Size: 12.1 MB (12144141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3d3351223cc51fc04c28bd3ee254c50dc1aa8b53fe2271157312bf6059332e`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62a76c7aab9f504821a67d731d00bfdab03d3de79c10cf2ab42d77365d59c8a`  
		Last Modified: Wed, 21 Dec 2022 07:34:10 GMT  
		Size: 11.0 MB (11047777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0818d51635f50597957fbc8da56054685fb7bbf22872448b0d394224b390cc24`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ce21c25df23473fbf6b254fc5b78b4409033f698834c45ff0e10b44402c58a`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3046ba549193d326f7414704423b8f1dd72aa9cfa44cfeecc224edc71ddf443`  
		Last Modified: Wed, 21 Dec 2022 07:34:08 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb88bd91b1c05b72e8f4a107f8ea713e5e826d9309005448ea47d894f84623e8`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3144fb6149a37eff0b2a3ad9c74075f2132cf1954c8f70ded5ce5ab5792e1655`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 2.4 MB (2444339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c8d18bf56aab23c74634d82905fc330fa99250f268a36e8b26bcaf82709ba`  
		Last Modified: Wed, 21 Dec 2022 13:14:27 GMT  
		Size: 8.7 MB (8732051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32416d0f41ecbdc2aa6ba3bba079b74ab3f11b4953e2bb4a7f52c23414f43c5d`  
		Last Modified: Wed, 21 Dec 2022 13:14:25 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:92913783b5fb24ae5156576bf156d341ff76d5f57c504e8dbe569eb84c1ca29c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170488451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d99e37146284d0046cb246f3e2f0c954fd240b3a2e5c3ebcd7fe126ac18249d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:06:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 21 Dec 2022 06:06:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 21 Dec 2022 06:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:06:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 21 Dec 2022 06:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 21 Dec 2022 06:09:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 21 Dec 2022 06:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 21 Dec 2022 06:09:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 21 Dec 2022 06:09:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 21 Dec 2022 06:09:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 21 Dec 2022 06:58:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_VERSION=8.1.14
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.14.tar.xz.asc
# Fri, 06 Jan 2023 00:37:06 GMT
ENV PHP_SHA256=e16e47a872d58685913ac848ce92ec49f42c1828110c98c65fb6265a08724a1a
# Fri, 06 Jan 2023 00:37:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Jan 2023 00:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Jan 2023 00:40:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Jan 2023 00:40:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Jan 2023 00:40:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 06 Jan 2023 00:40:13 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 06 Jan 2023 00:40:13 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 00:40:13 GMT
EXPOSE 80
# Fri, 06 Jan 2023 00:40:13 GMT
CMD ["apache2-foreground"]
# Fri, 06 Jan 2023 02:22:36 GMT
RUN a2enmod rewrite
# Fri, 06 Jan 2023 02:23:26 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 06 Jan 2023 02:23:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_VERSION=1.23.1
# Fri, 06 Jan 2023 02:23:26 GMT
ENV BACKDROP_MD5=75ab7eba27b61773dd3296ba0ab8a27b
# Fri, 06 Jan 2023 02:23:29 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 06 Jan 2023 02:23:29 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 06 Jan 2023 02:23:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jan 2023 02:23:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ed9670c1d43fe031d8dbdf1245e91ddcc8a7b9ebef601b6fbc74b965f0aaa`  
		Last Modified: Wed, 21 Dec 2022 08:06:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f716ee879c83e623ce98be3a2d7e20cc2f76201d414323bf4df4115191b97`  
		Last Modified: Wed, 21 Dec 2022 08:06:14 GMT  
		Size: 86.9 MB (86926576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce55625aa2b47393d76205f33f38efd485c611b282d0f06efa824b515e3006dd`  
		Last Modified: Wed, 21 Dec 2022 08:06:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec000a9f339ae26b6d2b7e4d0e0b8999a704635cb0492acabdcb39386b87a65`  
		Last Modified: Wed, 21 Dec 2022 08:06:40 GMT  
		Size: 19.2 MB (19166186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ebad50c90d4b14cd5063ea1ac2e84011c82d77ef362e18c22072c9f8aff34e`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae770a57a4d6d026941fda54c54aaf2c10e4bf1807348a3a25859aacd1b1b4a`  
		Last Modified: Wed, 21 Dec 2022 08:06:38 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c291ce88696e50a2c8be58368fda243845776eaa8510fcd892306f7f1d008740`  
		Last Modified: Fri, 06 Jan 2023 02:01:05 GMT  
		Size: 12.1 MB (12092812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2faa21fcc5c3c180afcfb4da30674b2664c903944c571d92ad27545b7b5fb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a46d5bca88e7ddeb0b7dd9875499f24bd4e6ef2fd759199bf9e5e2ea36729ee`  
		Last Modified: Fri, 06 Jan 2023 02:01:04 GMT  
		Size: 11.1 MB (11112922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74012f233148d7e9620205bfbc1148b073f2b3609eceb71034b63473636e77bb`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2c3fdc1c9ac719d0be8abeecc66487a521598663cdbeb0a0282f7800960827`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95aa49c9ca9e765f5bd11b8ff311814295608b12412195950fbc6fe9627d93`  
		Last Modified: Fri, 06 Jan 2023 02:01:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d1a2306c999b6c613a0c4b334ad5048082e635e7f86cb0391ff0a508c77b91`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b09399f0be9a1aefa401dfcdd6de4a293431f66577b019ba8b0caf9d2e6cb9`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 2.4 MB (2406314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cee0a5553e97c137a9c4c712f73ef4797b70f6ce9e2a583e3ab9f2b668c49b3`  
		Last Modified: Fri, 06 Jan 2023 02:24:48 GMT  
		Size: 8.7 MB (8732028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f47cbfcd40d6f7f7884b66ec274a2da9b4cc0fe5307581340a5073925589`  
		Last Modified: Fri, 06 Jan 2023 02:24:46 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
