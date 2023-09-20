## `backdrop:latest`

```console
$ docker pull backdrop@sha256:7ebc0020b0dee0e18a3753fd2150fde4201eba37d618e763e4299fb8212e749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:84c84c539c476827afe1d5833fd902a4ee45d8ab05471dbe3beab8d34d484764
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191589797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69312bb954e6fa1e10f1eea03ea163545600182efc33ef93918ad9f48e1baf1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:51 GMT
ADD file:3a8cd4de7f163d93718670f4db1de49045f5e04af3a8aa27d81c0f14647db707 in / 
# Thu, 07 Sep 2023 00:20:51 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:24:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 05:24:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 05:25:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:25:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 05:25:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 05:29:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 07 Sep 2023 05:29:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 07 Sep 2023 05:29:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 07 Sep 2023 05:29:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 07 Sep 2023 05:29:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 07 Sep 2023 05:29:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 05:29:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 05:29:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 06:26:57 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 07 Sep 2023 06:26:57 GMT
ENV PHP_VERSION=8.1.23
# Thu, 07 Sep 2023 06:26:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.23.tar.xz.asc
# Thu, 07 Sep 2023 06:26:57 GMT
ENV PHP_SHA256=fc48422fa7e75bb45916fc192a9f9728cb38bb2b5858572c51ea15825326360c
# Thu, 07 Sep 2023 06:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 06:27:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 06:30:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 06:30:42 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 07 Sep 2023 06:30:43 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 06:30:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 06:30:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 07 Sep 2023 06:30:43 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 07 Sep 2023 06:30:43 GMT
WORKDIR /var/www/html
# Thu, 07 Sep 2023 06:30:43 GMT
EXPOSE 80
# Thu, 07 Sep 2023 06:30:43 GMT
CMD ["apache2-foreground"]
# Fri, 08 Sep 2023 00:45:44 GMT
RUN a2enmod rewrite
# Fri, 08 Sep 2023 00:46:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 08 Sep 2023 00:46:44 GMT
WORKDIR /var/www/html
# Fri, 08 Sep 2023 00:46:44 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 08 Sep 2023 00:46:44 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 08 Sep 2023 00:46:47 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Fri, 08 Sep 2023 00:46:47 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 08 Sep 2023 00:46:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Sep 2023 00:46:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:360eba32fa65016e0d558c6af176db31a202e9a6071666f9b629cb8ba6ccedf0`  
		Last Modified: Thu, 07 Sep 2023 00:25:22 GMT  
		Size: 29.1 MB (29124494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19de89a948b7f6b9323b6a1527cc16893b5319ba6fefe8eba853b1002afe2f29`  
		Last Modified: Thu, 07 Sep 2023 07:20:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0f9df298ac76ec4aecebc6c4666ff37300aa5efabc8d8860c4eb751629d3ec`  
		Last Modified: Thu, 07 Sep 2023 07:20:22 GMT  
		Size: 104.3 MB (104340593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda134203c51146200f3d4b782ced86835ba92893570b87e2f94b9f67f3a24c4`  
		Last Modified: Thu, 07 Sep 2023 07:20:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299efc6dd925e06536530937f01a53b2553bdc1a075c4e7fa7b5d610c62df087`  
		Last Modified: Thu, 07 Sep 2023 07:20:51 GMT  
		Size: 20.3 MB (20303144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2655c36e1966597a46a212169994013342d109f5324dbf91c5c1f50ccea1ac8`  
		Last Modified: Thu, 07 Sep 2023 07:20:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b90a10a720965e2d61c5d6405d267b5c3ddd22ab024d10450f3e74c48fdd4`  
		Last Modified: Thu, 07 Sep 2023 07:20:49 GMT  
		Size: 514.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b386acbe21686e3979f6f65a0ac212366d1c901d750ef2f81da8b859fc092cc1`  
		Last Modified: Thu, 07 Sep 2023 07:27:05 GMT  
		Size: 12.2 MB (12204235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2afb7b4a56cc15814a7ec2e49cfe28d289bf382e2abe96a390409d0186cc33c`  
		Last Modified: Thu, 07 Sep 2023 07:27:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f551875fe1b2080a9a56f5bb260c08e98db5c97be7c878a72251ea1ff7fda82d`  
		Last Modified: Thu, 07 Sep 2023 07:27:04 GMT  
		Size: 11.1 MB (11145944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f326d1caca3dd364adae6c29da38226de1ecbb3763ee825ea2a858f0751d84de`  
		Last Modified: Thu, 07 Sep 2023 07:27:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cf3ad195aa2f8deca7783da385b298966c07c6b16338ec6d176dd355afa728`  
		Last Modified: Thu, 07 Sep 2023 07:27:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8221fa0366e06c019e0bec191eefc40bf4f61190890579058b4fdb7d3e3d2085`  
		Last Modified: Thu, 07 Sep 2023 07:27:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cecd1bfcf374b1b2e0ef06c9afc219c219d284ab8416c901791405aa396873`  
		Last Modified: Fri, 08 Sep 2023 00:48:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f012351546fce8e264b2ee5f5f706ba4e177fc3c05e7c61feeb7fd483d44dba1`  
		Last Modified: Fri, 08 Sep 2023 00:48:15 GMT  
		Size: 5.7 MB (5698829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ca39e7ef8983b9fab9342e4b585ce96aa0c10038310ae4165a232bb75255b`  
		Last Modified: Fri, 08 Sep 2023 00:48:16 GMT  
		Size: 8.8 MB (8765723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6c0318670efd037db73a9cc476532edeb2346c98d719b8f07aaf25acd353f5`  
		Last Modified: Fri, 08 Sep 2023 00:48:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a5fb7d0b440b13f121bf6ef46af28b3ae1f2c82751de48b4f17d6e19e933875c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185405829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f068911a7784245ef627d20b824d681835f59628e015a188d946acef1cb802a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:13 GMT
ADD file:ec1a6e0aedd76c8fdc8544775f8b553f58950e9435f5cfe919f39374e222cfbb in / 
# Wed, 20 Sep 2023 02:44:14 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 02:52:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 20 Sep 2023 02:52:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Sep 2023 02:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 02:53:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Sep 2023 02:53:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 20 Sep 2023 02:57:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Sep 2023 02:57:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Sep 2023 02:57:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 20 Sep 2023 02:57:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 20 Sep 2023 02:57:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 20 Sep 2023 02:57:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 02:57:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Sep 2023 02:57:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Sep 2023 04:16:09 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 20 Sep 2023 05:16:29 GMT
ENV PHP_VERSION=8.1.23
# Wed, 20 Sep 2023 05:16:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.23.tar.xz.asc
# Wed, 20 Sep 2023 05:16:29 GMT
ENV PHP_SHA256=fc48422fa7e75bb45916fc192a9f9728cb38bb2b5858572c51ea15825326360c
# Wed, 20 Sep 2023 05:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 20 Sep 2023 05:16:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 20 Sep 2023 05:19:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 20 Sep 2023 05:19:56 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 20 Sep 2023 05:19:57 GMT
RUN docker-php-ext-enable sodium
# Wed, 20 Sep 2023 05:19:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Sep 2023 05:19:57 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Sep 2023 05:19:57 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 20 Sep 2023 05:19:57 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 05:19:57 GMT
EXPOSE 80
# Wed, 20 Sep 2023 05:19:57 GMT
CMD ["apache2-foreground"]
# Wed, 20 Sep 2023 18:22:00 GMT
RUN a2enmod rewrite
# Wed, 20 Sep 2023 18:22:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Wed, 20 Sep 2023 18:22:53 GMT
WORKDIR /var/www/html
# Wed, 20 Sep 2023 18:22:53 GMT
ENV BACKDROP_VERSION=1.25.1
# Wed, 20 Sep 2023 18:22:53 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Wed, 20 Sep 2023 18:22:56 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites
# Wed, 20 Sep 2023 18:22:56 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Wed, 20 Sep 2023 18:22:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Sep 2023 18:22:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e886f0f47ef56fcadb6ecaf2116056bbdb273e0afe07ed034498b198d386c04e`  
		Last Modified: Wed, 20 Sep 2023 02:47:36 GMT  
		Size: 29.2 MB (29157221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4b1c5363061d299f9340dcbc40e3a72f489e7d4bc4f11a42044267bc480634`  
		Last Modified: Wed, 20 Sep 2023 05:59:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6c7adc7b3830328e51b6e68419760d8036c87394c9a09fead73478f67f58bb`  
		Last Modified: Wed, 20 Sep 2023 05:59:42 GMT  
		Size: 98.1 MB (98111498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7e7400ce12c1eeba03b34d6a220b7fc38cc011c52134d3ae19cd0e78dc2bd8`  
		Last Modified: Wed, 20 Sep 2023 05:59:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59572f84f3fa9dcf6ef27894127f256922909b98960561e2dedb8b1d7816fe0f`  
		Last Modified: Wed, 20 Sep 2023 06:00:20 GMT  
		Size: 20.3 MB (20304488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bc70b64a40a408c9f63882bffe6b850efbbe5f4421c4e4345e5c4b6034434a`  
		Last Modified: Wed, 20 Sep 2023 06:00:17 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f189cf2b806d7ec6e02590c55abf84a6fd6293eb915144796d46edf3fddb2ac6`  
		Last Modified: Wed, 20 Sep 2023 06:00:17 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd7f80a566c7df6baeb19773ee997fee63a64ffec43852b5aa3bd5725b22417`  
		Last Modified: Wed, 20 Sep 2023 06:13:26 GMT  
		Size: 12.2 MB (12203837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089393cfb0e504ca74074bbdbf48ed38b82398d09a6e6e05d08f58edc0c7ca5f`  
		Last Modified: Wed, 20 Sep 2023 06:13:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bddfb77c65db4af413f49cea0c6c409478ffd1cb400f54a270edf74158b84a0`  
		Last Modified: Wed, 20 Sep 2023 06:13:24 GMT  
		Size: 11.1 MB (11142006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baed59b11d617d05513166318756f1fc04e1f4ff776ee6dc18170aa24b78cd74`  
		Last Modified: Wed, 20 Sep 2023 06:13:23 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1565697279a0f784a4f172d6ea00e5f66fd8d25f0899ef3bfc03b9ea12842af6`  
		Last Modified: Wed, 20 Sep 2023 06:13:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116cfb7065e1382b9b96bf70f2778c915ae434bb72ced8250b9ff05d831ec9da`  
		Last Modified: Wed, 20 Sep 2023 06:13:23 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac5529eae3ce836a9775f6247dc21ef539cd58386235a90d1bf70ce13dab048`  
		Last Modified: Wed, 20 Sep 2023 18:24:15 GMT  
		Size: 311.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1c8f86ac0bea7e2534960ccdbac2013dc45cb376244a609bcf38cdaec2bb915`  
		Last Modified: Wed, 20 Sep 2023 18:24:16 GMT  
		Size: 5.7 MB (5714218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5583f7313680afa1411c012b9fe340417c2db95fec50dae4e0b94ccad99232b`  
		Last Modified: Wed, 20 Sep 2023 18:24:17 GMT  
		Size: 8.8 MB (8765742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdc87d504418f4fb25c5a94c8620841f402d3a02744cee3ab9deb479414cb4c`  
		Last Modified: Wed, 20 Sep 2023 18:24:15 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
