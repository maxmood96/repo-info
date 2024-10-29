<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.26`](#backdrop126)
-	[`backdrop:1.26-apache`](#backdrop126-apache)
-	[`backdrop:1.26-fpm`](#backdrop126-fpm)
-	[`backdrop:1.26.1`](#backdrop1261)
-	[`backdrop:1.26.1-apache`](#backdrop1261-apache)
-	[`backdrop:1.26.1-fpm`](#backdrop1261-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:dad1adb3777a59b9bb6b702558c843819995193234dd02bd743b4a1fc1d4a031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:fe21513ca45ee683e2a94c4f4d09f8a1d5739bf12f655aee4f7e032842cea503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187088790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997826a2d17a1967c4c0cd1371f66f9df1c94389986f17d44a05edd028f447a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c488b6fcdeb51ea6d25f932c69c9c123be5506b80c5dcc989457387219b1af`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 104.3 MB (104344946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9d324bbc20219cb5e7504cc3b152cc771d888a99dd4a2d4accf698c19800e3`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c6928b4367860d227b0bae016fef9e96e4196051bf3d73ab3c24186823a4d`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 12.0 MB (11960157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fe0adc031982a6320a7659ca4495bf56b20556e77bb9ef2ed4f3d9887f8a7`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853772b7f9aed4c7f8e6dcc6ca2b261ac5e1101ab2e67f6e44a6d69bed45b8b0`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 27.3 MB (27329500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4a74b332a56a4c4a4fa933a18052ed2f87d79d3d9040c7d933585c7d70ace`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3649173c8c9c7aff2c1fda122643c2809fd4876db0365ef76c1e6fe575d643e4`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23dc8862ff72a2617589043ec4e4c53d34f7b800d753edc50decaec29463487`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74332ee57c59583e688d42d8c420a0ab0157efe1cc39eb4b95aebb94cca775f8`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 5.5 MB (5509214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a23b72a2c359d2921faa8a7b4a71f8bc357234a2380c4b86e3c6107fe45c36`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a7b321e6ece4992590cb3af88cbb757364ceacdf8e6a9e2454db38db1d7c64`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:db12238218948944a8cd628fc726961e7bc51dbe862da8cd38dd7e792bccefe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b364376f03082825fd59e9e7dbc30d56e10473d8b3c225b78c742017098416`

```dockerfile
```

-	Layers:
	-	`sha256:8fe2b2144703bb9f3a4058e11084af7dc886bacb32c480aff960ece9104ae681`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 6.4 MB (6440022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4812bcd877bc5246241fd7f96f48017e5a5110b44d8d08dc3d32c812bd5b5f`  
		Last Modified: Mon, 28 Oct 2024 23:06:04 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:034073b22320b16adf77b84b560b4a3e12ae6f2b73d4ddd71c799624811f935a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180869132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939109163b6a2021ee9fb5ff4aaf258073bf4b0768c56cbec5724152c20783c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e173c4e2420d4b5e9e3f7d6151dae56295e5764e18fa4243b2da8de4e5c69359`  
		Last Modified: Tue, 29 Oct 2024 00:54:10 GMT  
		Size: 12.0 MB (11960009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0214ebcf7fcf3a8ace0f1133e677cc390b69bf72bf339ff83bef007929e85`  
		Last Modified: Tue, 29 Oct 2024 00:54:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08bd95ab39238643d14a4e3812b26c2b0cb65c1d78557c1cabb4f6f17731eee`  
		Last Modified: Tue, 29 Oct 2024 01:02:04 GMT  
		Size: 27.3 MB (27275531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d64ecabcb23e0060c37a184c243d092a8fc4f46e4cb9c2552cd22930d6c5015`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa027a11cde5991ce68c3a2e12d5c715ad6a4fa8bd62d2d68693885f774eb8`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83029b6d89993a5036522ffe6d53caa816a702f5dbb98106aeb0381c145c914d`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf60cb291b4326d41481cfd4c942c01fee32bade0f5589474eb4563867eb96d`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 5.5 MB (5528500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb0238fb0023f36af8818ef9cc043542e8342d412cb7380ebd32fdaec05753`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42781e331e6d12fe3c78782ce4cad32c5c180068b12f3f3a201281350c63cbee`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:7b7d102ddea12fb7290b805e49532b1fe1885ea8271bebad980e65ffae63f07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ac83cb8b6c25b8339aa966b218d8740e0398f025621ce6496316b72486728e`

```dockerfile
```

-	Layers:
	-	`sha256:5feda9cda11fce4da8b86dc2952fa1cf8b9609572b75c9a2d301c5ea030d22c1`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 6.5 MB (6468470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384436f95039c903089854e117f3817da1cce2197a6a87283b96eca3b56d00e0`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 21.7 KB (21714 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26-apache`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26-fpm`

```console
$ docker pull backdrop@sha256:dad1adb3777a59b9bb6b702558c843819995193234dd02bd743b4a1fc1d4a031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:fe21513ca45ee683e2a94c4f4d09f8a1d5739bf12f655aee4f7e032842cea503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187088790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997826a2d17a1967c4c0cd1371f66f9df1c94389986f17d44a05edd028f447a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c488b6fcdeb51ea6d25f932c69c9c123be5506b80c5dcc989457387219b1af`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 104.3 MB (104344946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9d324bbc20219cb5e7504cc3b152cc771d888a99dd4a2d4accf698c19800e3`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c6928b4367860d227b0bae016fef9e96e4196051bf3d73ab3c24186823a4d`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 12.0 MB (11960157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fe0adc031982a6320a7659ca4495bf56b20556e77bb9ef2ed4f3d9887f8a7`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853772b7f9aed4c7f8e6dcc6ca2b261ac5e1101ab2e67f6e44a6d69bed45b8b0`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 27.3 MB (27329500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4a74b332a56a4c4a4fa933a18052ed2f87d79d3d9040c7d933585c7d70ace`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3649173c8c9c7aff2c1fda122643c2809fd4876db0365ef76c1e6fe575d643e4`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23dc8862ff72a2617589043ec4e4c53d34f7b800d753edc50decaec29463487`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74332ee57c59583e688d42d8c420a0ab0157efe1cc39eb4b95aebb94cca775f8`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 5.5 MB (5509214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a23b72a2c359d2921faa8a7b4a71f8bc357234a2380c4b86e3c6107fe45c36`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a7b321e6ece4992590cb3af88cbb757364ceacdf8e6a9e2454db38db1d7c64`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:db12238218948944a8cd628fc726961e7bc51dbe862da8cd38dd7e792bccefe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b364376f03082825fd59e9e7dbc30d56e10473d8b3c225b78c742017098416`

```dockerfile
```

-	Layers:
	-	`sha256:8fe2b2144703bb9f3a4058e11084af7dc886bacb32c480aff960ece9104ae681`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 6.4 MB (6440022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4812bcd877bc5246241fd7f96f48017e5a5110b44d8d08dc3d32c812bd5b5f`  
		Last Modified: Mon, 28 Oct 2024 23:06:04 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:034073b22320b16adf77b84b560b4a3e12ae6f2b73d4ddd71c799624811f935a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180869132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939109163b6a2021ee9fb5ff4aaf258073bf4b0768c56cbec5724152c20783c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e173c4e2420d4b5e9e3f7d6151dae56295e5764e18fa4243b2da8de4e5c69359`  
		Last Modified: Tue, 29 Oct 2024 00:54:10 GMT  
		Size: 12.0 MB (11960009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0214ebcf7fcf3a8ace0f1133e677cc390b69bf72bf339ff83bef007929e85`  
		Last Modified: Tue, 29 Oct 2024 00:54:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08bd95ab39238643d14a4e3812b26c2b0cb65c1d78557c1cabb4f6f17731eee`  
		Last Modified: Tue, 29 Oct 2024 01:02:04 GMT  
		Size: 27.3 MB (27275531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d64ecabcb23e0060c37a184c243d092a8fc4f46e4cb9c2552cd22930d6c5015`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa027a11cde5991ce68c3a2e12d5c715ad6a4fa8bd62d2d68693885f774eb8`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83029b6d89993a5036522ffe6d53caa816a702f5dbb98106aeb0381c145c914d`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf60cb291b4326d41481cfd4c942c01fee32bade0f5589474eb4563867eb96d`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 5.5 MB (5528500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb0238fb0023f36af8818ef9cc043542e8342d412cb7380ebd32fdaec05753`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42781e331e6d12fe3c78782ce4cad32c5c180068b12f3f3a201281350c63cbee`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:7b7d102ddea12fb7290b805e49532b1fe1885ea8271bebad980e65ffae63f07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ac83cb8b6c25b8339aa966b218d8740e0398f025621ce6496316b72486728e`

```dockerfile
```

-	Layers:
	-	`sha256:5feda9cda11fce4da8b86dc2952fa1cf8b9609572b75c9a2d301c5ea030d22c1`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 6.5 MB (6468470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384436f95039c903089854e117f3817da1cce2197a6a87283b96eca3b56d00e0`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 21.7 KB (21714 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1-apache`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1-fpm`

```console
$ docker pull backdrop@sha256:dad1adb3777a59b9bb6b702558c843819995193234dd02bd743b4a1fc1d4a031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:fe21513ca45ee683e2a94c4f4d09f8a1d5739bf12f655aee4f7e032842cea503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187088790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997826a2d17a1967c4c0cd1371f66f9df1c94389986f17d44a05edd028f447a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c488b6fcdeb51ea6d25f932c69c9c123be5506b80c5dcc989457387219b1af`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 104.3 MB (104344946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9d324bbc20219cb5e7504cc3b152cc771d888a99dd4a2d4accf698c19800e3`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c6928b4367860d227b0bae016fef9e96e4196051bf3d73ab3c24186823a4d`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 12.0 MB (11960157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fe0adc031982a6320a7659ca4495bf56b20556e77bb9ef2ed4f3d9887f8a7`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853772b7f9aed4c7f8e6dcc6ca2b261ac5e1101ab2e67f6e44a6d69bed45b8b0`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 27.3 MB (27329500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4a74b332a56a4c4a4fa933a18052ed2f87d79d3d9040c7d933585c7d70ace`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3649173c8c9c7aff2c1fda122643c2809fd4876db0365ef76c1e6fe575d643e4`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23dc8862ff72a2617589043ec4e4c53d34f7b800d753edc50decaec29463487`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74332ee57c59583e688d42d8c420a0ab0157efe1cc39eb4b95aebb94cca775f8`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 5.5 MB (5509214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a23b72a2c359d2921faa8a7b4a71f8bc357234a2380c4b86e3c6107fe45c36`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a7b321e6ece4992590cb3af88cbb757364ceacdf8e6a9e2454db38db1d7c64`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:db12238218948944a8cd628fc726961e7bc51dbe862da8cd38dd7e792bccefe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b364376f03082825fd59e9e7dbc30d56e10473d8b3c225b78c742017098416`

```dockerfile
```

-	Layers:
	-	`sha256:8fe2b2144703bb9f3a4058e11084af7dc886bacb32c480aff960ece9104ae681`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 6.4 MB (6440022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4812bcd877bc5246241fd7f96f48017e5a5110b44d8d08dc3d32c812bd5b5f`  
		Last Modified: Mon, 28 Oct 2024 23:06:04 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:034073b22320b16adf77b84b560b4a3e12ae6f2b73d4ddd71c799624811f935a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180869132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939109163b6a2021ee9fb5ff4aaf258073bf4b0768c56cbec5724152c20783c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e173c4e2420d4b5e9e3f7d6151dae56295e5764e18fa4243b2da8de4e5c69359`  
		Last Modified: Tue, 29 Oct 2024 00:54:10 GMT  
		Size: 12.0 MB (11960009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0214ebcf7fcf3a8ace0f1133e677cc390b69bf72bf339ff83bef007929e85`  
		Last Modified: Tue, 29 Oct 2024 00:54:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08bd95ab39238643d14a4e3812b26c2b0cb65c1d78557c1cabb4f6f17731eee`  
		Last Modified: Tue, 29 Oct 2024 01:02:04 GMT  
		Size: 27.3 MB (27275531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d64ecabcb23e0060c37a184c243d092a8fc4f46e4cb9c2552cd22930d6c5015`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa027a11cde5991ce68c3a2e12d5c715ad6a4fa8bd62d2d68693885f774eb8`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83029b6d89993a5036522ffe6d53caa816a702f5dbb98106aeb0381c145c914d`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf60cb291b4326d41481cfd4c942c01fee32bade0f5589474eb4563867eb96d`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 5.5 MB (5528500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb0238fb0023f36af8818ef9cc043542e8342d412cb7380ebd32fdaec05753`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42781e331e6d12fe3c78782ce4cad32c5c180068b12f3f3a201281350c63cbee`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:7b7d102ddea12fb7290b805e49532b1fe1885ea8271bebad980e65ffae63f07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ac83cb8b6c25b8339aa966b218d8740e0398f025621ce6496316b72486728e`

```dockerfile
```

-	Layers:
	-	`sha256:5feda9cda11fce4da8b86dc2952fa1cf8b9609572b75c9a2d301c5ea030d22c1`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 6.5 MB (6468470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384436f95039c903089854e117f3817da1cce2197a6a87283b96eca3b56d00e0`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 21.7 KB (21714 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:dad1adb3777a59b9bb6b702558c843819995193234dd02bd743b4a1fc1d4a031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:fe21513ca45ee683e2a94c4f4d09f8a1d5739bf12f655aee4f7e032842cea503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187088790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997826a2d17a1967c4c0cd1371f66f9df1c94389986f17d44a05edd028f447a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c488b6fcdeb51ea6d25f932c69c9c123be5506b80c5dcc989457387219b1af`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 104.3 MB (104344946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9d324bbc20219cb5e7504cc3b152cc771d888a99dd4a2d4accf698c19800e3`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c6928b4367860d227b0bae016fef9e96e4196051bf3d73ab3c24186823a4d`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 12.0 MB (11960157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fe0adc031982a6320a7659ca4495bf56b20556e77bb9ef2ed4f3d9887f8a7`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853772b7f9aed4c7f8e6dcc6ca2b261ac5e1101ab2e67f6e44a6d69bed45b8b0`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 27.3 MB (27329500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4a74b332a56a4c4a4fa933a18052ed2f87d79d3d9040c7d933585c7d70ace`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3649173c8c9c7aff2c1fda122643c2809fd4876db0365ef76c1e6fe575d643e4`  
		Last Modified: Mon, 28 Oct 2024 22:12:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23dc8862ff72a2617589043ec4e4c53d34f7b800d753edc50decaec29463487`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74332ee57c59583e688d42d8c420a0ab0157efe1cc39eb4b95aebb94cca775f8`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 5.5 MB (5509214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a23b72a2c359d2921faa8a7b4a71f8bc357234a2380c4b86e3c6107fe45c36`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a7b321e6ece4992590cb3af88cbb757364ceacdf8e6a9e2454db38db1d7c64`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:db12238218948944a8cd628fc726961e7bc51dbe862da8cd38dd7e792bccefe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b364376f03082825fd59e9e7dbc30d56e10473d8b3c225b78c742017098416`

```dockerfile
```

-	Layers:
	-	`sha256:8fe2b2144703bb9f3a4058e11084af7dc886bacb32c480aff960ece9104ae681`  
		Last Modified: Mon, 28 Oct 2024 23:06:05 GMT  
		Size: 6.4 MB (6440022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4812bcd877bc5246241fd7f96f48017e5a5110b44d8d08dc3d32c812bd5b5f`  
		Last Modified: Mon, 28 Oct 2024 23:06:04 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:034073b22320b16adf77b84b560b4a3e12ae6f2b73d4ddd71c799624811f935a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180869132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939109163b6a2021ee9fb5ff4aaf258073bf4b0768c56cbec5724152c20783c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e173c4e2420d4b5e9e3f7d6151dae56295e5764e18fa4243b2da8de4e5c69359`  
		Last Modified: Tue, 29 Oct 2024 00:54:10 GMT  
		Size: 12.0 MB (11960009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0214ebcf7fcf3a8ace0f1133e677cc390b69bf72bf339ff83bef007929e85`  
		Last Modified: Tue, 29 Oct 2024 00:54:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08bd95ab39238643d14a4e3812b26c2b0cb65c1d78557c1cabb4f6f17731eee`  
		Last Modified: Tue, 29 Oct 2024 01:02:04 GMT  
		Size: 27.3 MB (27275531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d64ecabcb23e0060c37a184c243d092a8fc4f46e4cb9c2552cd22930d6c5015`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa027a11cde5991ce68c3a2e12d5c715ad6a4fa8bd62d2d68693885f774eb8`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83029b6d89993a5036522ffe6d53caa816a702f5dbb98106aeb0381c145c914d`  
		Last Modified: Tue, 29 Oct 2024 01:02:03 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf60cb291b4326d41481cfd4c942c01fee32bade0f5589474eb4563867eb96d`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 5.5 MB (5528500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb0238fb0023f36af8818ef9cc043542e8342d412cb7380ebd32fdaec05753`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42781e331e6d12fe3c78782ce4cad32c5c180068b12f3f3a201281350c63cbee`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:7b7d102ddea12fb7290b805e49532b1fe1885ea8271bebad980e65ffae63f07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ac83cb8b6c25b8339aa966b218d8740e0398f025621ce6496316b72486728e`

```dockerfile
```

-	Layers:
	-	`sha256:5feda9cda11fce4da8b86dc2952fa1cf8b9609572b75c9a2d301c5ea030d22c1`  
		Last Modified: Tue, 29 Oct 2024 02:35:55 GMT  
		Size: 6.5 MB (6468470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384436f95039c903089854e117f3817da1cce2197a6a87283b96eca3b56d00e0`  
		Last Modified: Tue, 29 Oct 2024 02:35:54 GMT  
		Size: 21.7 KB (21714 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:90881e3294191f6ff052db42863f48658ac7831636ba193ab5d8da355ca493e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:1302efce4a7a33bc878cc15dee796874d88a6e01b6af8eaa89cddf3e100e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191046125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee2717290271b29be5b1ac4fe1658e458bfd059c30f1cd1102eadfd9e31c234`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ede2d39f271145f7b9813008687cde7e4d2e1c86b1357d74098980d2023c05`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2195a9d0263f2358843ca62296f7873c93a0a27c94aee522a12d2d51f6bf7`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 5.5 MB (5505644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10a8e1c8a84fe0f547bb40b406fcb5e4b86d25186360b2d7f2d415bec2656`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5036110c1f36ef030b373b6bab0e3b485b00c6c020a2ee5e4227b3554d3d1`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:c97c9a1b0d72f5cee8880a3d9c3fa4d107817dd50fb225f955c71e06a042c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c91ee3d785021dd90c0093593cdd49f415ca8f294a0704df16cebaddf26ce5d`

```dockerfile
```

-	Layers:
	-	`sha256:5baba57d1a3b2a775390ec089d0e3f2e95ed5ecd6c3f299c321932f27f52a20e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 7.0 MB (6951230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0c4f036743264e8685e5fb90d19397398af1aa04c5c318a5d2f18a4f5a003e`  
		Last Modified: Mon, 28 Oct 2024 23:06:09 GMT  
		Size: 29.6 KB (29646 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:47b423e230d813f2b3a1f114f792863013a39c948127c412dcf961dc96c94856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184875836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4ad28794c4942c50be5a9afbace5c3ef56df330a0e1d1f9049802688ba818f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.30
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE map[80/tcp:{}]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2enmod rewrite # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_VERSION=1.26.1
# Sat, 14 Oct 2023 00:46:03 GMT
ENV BACKDROP_MD5=0a6fad09190b1f8da266f586955454a2
# Sat, 14 Oct 2023 00:46:03 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448c4d117fc72154603747364c05d3b5d9f0f99e482b90e922c0435edd26573`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aeb5ae9fa59831b6d3341e5cecd682e0b5936e51727a6500e3bb3ecfac3baf`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 5.5 MB (5524789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a39d6c6f0948abb78395a5af374a94d8de7e4f038e466dbb59133a621dd3d`  
		Last Modified: Tue, 29 Oct 2024 02:34:32 GMT  
		Size: 8.8 MB (8805171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf5866e45f283a9ab74b46acddde25cfa31d6d16922889d782344754d3cf2f`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e24435724737a7561e337dd036c32948cd616b8ce993753bbaf54fa37e271f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44802f017dd6c80d6022477d69a1de736990e184615029b4aeff56f82e874a`

```dockerfile
```

-	Layers:
	-	`sha256:37410aecbe44d83b4fe10544174fb3680746a494c43f60ad21443d7454726633`  
		Last Modified: Tue, 29 Oct 2024 02:34:31 GMT  
		Size: 7.0 MB (6979742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae7b6b716ad4d21137c2aefbdae235fbb228822533f535d3d0d0fa9d316be965`  
		Last Modified: Tue, 29 Oct 2024 02:34:30 GMT  
		Size: 29.9 KB (29859 bytes)  
		MIME: application/vnd.in-toto+json
