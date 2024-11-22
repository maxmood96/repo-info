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
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:11ff2928b8e53a3f0b2ff726fa547679f861713de309a82cdddf8e5f01125b68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:ab28210e9cc52938de21a1446a1988b797f345bb8e54006d5554b516d9fef067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187159069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869fd2770c7b865d724e1ddfd1cd480498e7ed3b3ed3eae9b8eebd02cb9cbfb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12f5d87b9b8ca8369c048b6d6dea58af1f7bf8884a24ed79e35cabbbee8155`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825f50d7a1a4522908da2815cb916fdd6b5cd723dc36b88e233bc0a38f3b070d`  
		Last Modified: Thu, 21 Nov 2024 18:06:19 GMT  
		Size: 104.3 MB (104345693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438190412cd50a5c6ec242b7cac877dd2e2f6345d97dd329b152360782a6b82e`  
		Last Modified: Thu, 21 Nov 2024 18:06:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34bc06f43aaa90dce463d5f76cc69d53f261fb5bb78a0baebe6d475954c865`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 12.0 MB (12026541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d155b57310c6da2c2fc1b52ad39de2ce7cf90114a0dc7c447c9f3080e03c979`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8fd7ece228d0a7797c432cf69bfff89346f045ec45d28d4f062f49841ae212`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 27.3 MB (27330430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885bfec8575f5522f00a5ad153958c756c3562b738691b6ec4193464b7551069`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa61f2b534f49bbb2e85fc931f5f3902dd2e29ed873142722d5cffa8a2831365`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8faa87b752576bf2bb671ec8bc6f750e101713a8ceec23742994ec207d052aa`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5153181ed05e0b6e6b4044e02893ddd16414ffaeef87c2d24d39b6793a8a93`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 5.5 MB (5509720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee683f7602e5297d9093b4eee5a0a70a9a863f10d13c9119141c3703c3b23075`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 8.8 MB (8805158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:b0a2980ebbea8679a3df5dcfbfa54239909293af370862515f2e3bb8c2febe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e159f72556db1839e9129f62dfcf63210465925238a6e7280cc0ecb1b6c35b`

```dockerfile
```

-	Layers:
	-	`sha256:81f5286d746e46c4203a16c6f75fb59e12299f7e30dba5914872772e4f559649`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 6.4 MB (6440058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64e5bd0483e8f7f7f15402f43f278ec69556a900506c6c16a1cc79959c571c5`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e1dab8708f2b15d94a24633c3e95900ee0145b8014407689417dfbe2575bdcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180871841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3901c6796782d49c2416571d560f8bbde143ef0a50075148a4236069b26d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d9393dd9f2b8766c406f2a152f0875c76450eb8ab9a5565e1ec45a2c5689b`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 12.0 MB (11960029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4ae78985ca094a26b126937640b174722c0b8175825aae8822e4f4a1b5515a`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76025589d680f9a8fc617f33224737d1675536d8fbf452f0038c23c69b33fc6`  
		Last Modified: Tue, 12 Nov 2024 08:23:38 GMT  
		Size: 27.3 MB (27275461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fada07c03a4a3f8faf9d04033dc785abe51d1723b49aefeedb3125199ac78d2`  
		Last Modified: Tue, 12 Nov 2024 08:23:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a23b570d24db731441c5ccc694e34c6e25497b59504f59a0dbc4087d97c55`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21cc76254af2bae7ffcd509c78fe4589ef8573ec9be57389f9e7f8a941e4bd`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a24bf52bfd2ca0d69efa123187d49a959311301f3522b8d73f9bf38adc6e03`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 5.5 MB (5529598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcb2c5b826483840499322d61c7af2f9d07387a44a677049fb992aef5ad2954`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6007c0747b11841d218301433d3bc032837b1d42d8da092df480f731915755a5`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecf9459e689449c555c0537315a5abbad76bd6f0289d4ed76caf92c70c861803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3849fe4cfa7d94e11392ba60423f8cb2f35db0550a9e7a3bdbf377967c8d26e`

```dockerfile
```

-	Layers:
	-	`sha256:e57e7f62f054386a7cc6c6fd7f99dab8ff6f9f576bb490efa7390331b537c785`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 6.5 MB (6468506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8cad831c9fd8594d2c4dccf409366a3b0461ce413d49b85ce3568c86ba3be`  
		Last Modified: Wed, 13 Nov 2024 02:41:09 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26-apache`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26-fpm`

```console
$ docker pull backdrop@sha256:11ff2928b8e53a3f0b2ff726fa547679f861713de309a82cdddf8e5f01125b68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:ab28210e9cc52938de21a1446a1988b797f345bb8e54006d5554b516d9fef067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187159069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869fd2770c7b865d724e1ddfd1cd480498e7ed3b3ed3eae9b8eebd02cb9cbfb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12f5d87b9b8ca8369c048b6d6dea58af1f7bf8884a24ed79e35cabbbee8155`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825f50d7a1a4522908da2815cb916fdd6b5cd723dc36b88e233bc0a38f3b070d`  
		Last Modified: Thu, 21 Nov 2024 18:06:19 GMT  
		Size: 104.3 MB (104345693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438190412cd50a5c6ec242b7cac877dd2e2f6345d97dd329b152360782a6b82e`  
		Last Modified: Thu, 21 Nov 2024 18:06:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34bc06f43aaa90dce463d5f76cc69d53f261fb5bb78a0baebe6d475954c865`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 12.0 MB (12026541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d155b57310c6da2c2fc1b52ad39de2ce7cf90114a0dc7c447c9f3080e03c979`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8fd7ece228d0a7797c432cf69bfff89346f045ec45d28d4f062f49841ae212`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 27.3 MB (27330430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885bfec8575f5522f00a5ad153958c756c3562b738691b6ec4193464b7551069`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa61f2b534f49bbb2e85fc931f5f3902dd2e29ed873142722d5cffa8a2831365`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8faa87b752576bf2bb671ec8bc6f750e101713a8ceec23742994ec207d052aa`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5153181ed05e0b6e6b4044e02893ddd16414ffaeef87c2d24d39b6793a8a93`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 5.5 MB (5509720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee683f7602e5297d9093b4eee5a0a70a9a863f10d13c9119141c3703c3b23075`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 8.8 MB (8805158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:b0a2980ebbea8679a3df5dcfbfa54239909293af370862515f2e3bb8c2febe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e159f72556db1839e9129f62dfcf63210465925238a6e7280cc0ecb1b6c35b`

```dockerfile
```

-	Layers:
	-	`sha256:81f5286d746e46c4203a16c6f75fb59e12299f7e30dba5914872772e4f559649`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 6.4 MB (6440058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64e5bd0483e8f7f7f15402f43f278ec69556a900506c6c16a1cc79959c571c5`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e1dab8708f2b15d94a24633c3e95900ee0145b8014407689417dfbe2575bdcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180871841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3901c6796782d49c2416571d560f8bbde143ef0a50075148a4236069b26d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d9393dd9f2b8766c406f2a152f0875c76450eb8ab9a5565e1ec45a2c5689b`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 12.0 MB (11960029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4ae78985ca094a26b126937640b174722c0b8175825aae8822e4f4a1b5515a`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76025589d680f9a8fc617f33224737d1675536d8fbf452f0038c23c69b33fc6`  
		Last Modified: Tue, 12 Nov 2024 08:23:38 GMT  
		Size: 27.3 MB (27275461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fada07c03a4a3f8faf9d04033dc785abe51d1723b49aefeedb3125199ac78d2`  
		Last Modified: Tue, 12 Nov 2024 08:23:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a23b570d24db731441c5ccc694e34c6e25497b59504f59a0dbc4087d97c55`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21cc76254af2bae7ffcd509c78fe4589ef8573ec9be57389f9e7f8a941e4bd`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a24bf52bfd2ca0d69efa123187d49a959311301f3522b8d73f9bf38adc6e03`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 5.5 MB (5529598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcb2c5b826483840499322d61c7af2f9d07387a44a677049fb992aef5ad2954`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6007c0747b11841d218301433d3bc032837b1d42d8da092df480f731915755a5`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecf9459e689449c555c0537315a5abbad76bd6f0289d4ed76caf92c70c861803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3849fe4cfa7d94e11392ba60423f8cb2f35db0550a9e7a3bdbf377967c8d26e`

```dockerfile
```

-	Layers:
	-	`sha256:e57e7f62f054386a7cc6c6fd7f99dab8ff6f9f576bb490efa7390331b537c785`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 6.5 MB (6468506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8cad831c9fd8594d2c4dccf409366a3b0461ce413d49b85ce3568c86ba3be`  
		Last Modified: Wed, 13 Nov 2024 02:41:09 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1-apache`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1-fpm`

```console
$ docker pull backdrop@sha256:11ff2928b8e53a3f0b2ff726fa547679f861713de309a82cdddf8e5f01125b68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:ab28210e9cc52938de21a1446a1988b797f345bb8e54006d5554b516d9fef067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187159069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869fd2770c7b865d724e1ddfd1cd480498e7ed3b3ed3eae9b8eebd02cb9cbfb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12f5d87b9b8ca8369c048b6d6dea58af1f7bf8884a24ed79e35cabbbee8155`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825f50d7a1a4522908da2815cb916fdd6b5cd723dc36b88e233bc0a38f3b070d`  
		Last Modified: Thu, 21 Nov 2024 18:06:19 GMT  
		Size: 104.3 MB (104345693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438190412cd50a5c6ec242b7cac877dd2e2f6345d97dd329b152360782a6b82e`  
		Last Modified: Thu, 21 Nov 2024 18:06:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34bc06f43aaa90dce463d5f76cc69d53f261fb5bb78a0baebe6d475954c865`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 12.0 MB (12026541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d155b57310c6da2c2fc1b52ad39de2ce7cf90114a0dc7c447c9f3080e03c979`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8fd7ece228d0a7797c432cf69bfff89346f045ec45d28d4f062f49841ae212`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 27.3 MB (27330430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885bfec8575f5522f00a5ad153958c756c3562b738691b6ec4193464b7551069`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa61f2b534f49bbb2e85fc931f5f3902dd2e29ed873142722d5cffa8a2831365`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8faa87b752576bf2bb671ec8bc6f750e101713a8ceec23742994ec207d052aa`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5153181ed05e0b6e6b4044e02893ddd16414ffaeef87c2d24d39b6793a8a93`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 5.5 MB (5509720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee683f7602e5297d9093b4eee5a0a70a9a863f10d13c9119141c3703c3b23075`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 8.8 MB (8805158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:b0a2980ebbea8679a3df5dcfbfa54239909293af370862515f2e3bb8c2febe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e159f72556db1839e9129f62dfcf63210465925238a6e7280cc0ecb1b6c35b`

```dockerfile
```

-	Layers:
	-	`sha256:81f5286d746e46c4203a16c6f75fb59e12299f7e30dba5914872772e4f559649`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 6.4 MB (6440058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64e5bd0483e8f7f7f15402f43f278ec69556a900506c6c16a1cc79959c571c5`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e1dab8708f2b15d94a24633c3e95900ee0145b8014407689417dfbe2575bdcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180871841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3901c6796782d49c2416571d560f8bbde143ef0a50075148a4236069b26d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d9393dd9f2b8766c406f2a152f0875c76450eb8ab9a5565e1ec45a2c5689b`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 12.0 MB (11960029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4ae78985ca094a26b126937640b174722c0b8175825aae8822e4f4a1b5515a`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76025589d680f9a8fc617f33224737d1675536d8fbf452f0038c23c69b33fc6`  
		Last Modified: Tue, 12 Nov 2024 08:23:38 GMT  
		Size: 27.3 MB (27275461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fada07c03a4a3f8faf9d04033dc785abe51d1723b49aefeedb3125199ac78d2`  
		Last Modified: Tue, 12 Nov 2024 08:23:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a23b570d24db731441c5ccc694e34c6e25497b59504f59a0dbc4087d97c55`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21cc76254af2bae7ffcd509c78fe4589ef8573ec9be57389f9e7f8a941e4bd`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a24bf52bfd2ca0d69efa123187d49a959311301f3522b8d73f9bf38adc6e03`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 5.5 MB (5529598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcb2c5b826483840499322d61c7af2f9d07387a44a677049fb992aef5ad2954`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6007c0747b11841d218301433d3bc032837b1d42d8da092df480f731915755a5`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecf9459e689449c555c0537315a5abbad76bd6f0289d4ed76caf92c70c861803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3849fe4cfa7d94e11392ba60423f8cb2f35db0550a9e7a3bdbf377967c8d26e`

```dockerfile
```

-	Layers:
	-	`sha256:e57e7f62f054386a7cc6c6fd7f99dab8ff6f9f576bb490efa7390331b537c785`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 6.5 MB (6468506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8cad831c9fd8594d2c4dccf409366a3b0461ce413d49b85ce3568c86ba3be`  
		Last Modified: Wed, 13 Nov 2024 02:41:09 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:11ff2928b8e53a3f0b2ff726fa547679f861713de309a82cdddf8e5f01125b68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:ab28210e9cc52938de21a1446a1988b797f345bb8e54006d5554b516d9fef067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.2 MB (187159069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869fd2770c7b865d724e1ddfd1cd480498e7ed3b3ed3eae9b8eebd02cb9cbfb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12f5d87b9b8ca8369c048b6d6dea58af1f7bf8884a24ed79e35cabbbee8155`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825f50d7a1a4522908da2815cb916fdd6b5cd723dc36b88e233bc0a38f3b070d`  
		Last Modified: Thu, 21 Nov 2024 18:06:19 GMT  
		Size: 104.3 MB (104345693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438190412cd50a5c6ec242b7cac877dd2e2f6345d97dd329b152360782a6b82e`  
		Last Modified: Thu, 21 Nov 2024 18:06:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f34bc06f43aaa90dce463d5f76cc69d53f261fb5bb78a0baebe6d475954c865`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 12.0 MB (12026541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d155b57310c6da2c2fc1b52ad39de2ce7cf90114a0dc7c447c9f3080e03c979`  
		Last Modified: Thu, 21 Nov 2024 18:06:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8fd7ece228d0a7797c432cf69bfff89346f045ec45d28d4f062f49841ae212`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 27.3 MB (27330430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885bfec8575f5522f00a5ad153958c756c3562b738691b6ec4193464b7551069`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa61f2b534f49bbb2e85fc931f5f3902dd2e29ed873142722d5cffa8a2831365`  
		Last Modified: Thu, 21 Nov 2024 18:06:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8faa87b752576bf2bb671ec8bc6f750e101713a8ceec23742994ec207d052aa`  
		Last Modified: Thu, 21 Nov 2024 18:06:18 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5153181ed05e0b6e6b4044e02893ddd16414ffaeef87c2d24d39b6793a8a93`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 5.5 MB (5509720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee683f7602e5297d9093b4eee5a0a70a9a863f10d13c9119141c3703c3b23075`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 8.8 MB (8805158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:b0a2980ebbea8679a3df5dcfbfa54239909293af370862515f2e3bb8c2febe4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e159f72556db1839e9129f62dfcf63210465925238a6e7280cc0ecb1b6c35b`

```dockerfile
```

-	Layers:
	-	`sha256:81f5286d746e46c4203a16c6f75fb59e12299f7e30dba5914872772e4f559649`  
		Last Modified: Thu, 21 Nov 2024 18:11:13 GMT  
		Size: 6.4 MB (6440058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64e5bd0483e8f7f7f15402f43f278ec69556a900506c6c16a1cc79959c571c5`  
		Last Modified: Thu, 21 Nov 2024 18:11:12 GMT  
		Size: 21.6 KB (21570 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e1dab8708f2b15d94a24633c3e95900ee0145b8014407689417dfbe2575bdcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180871841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3901c6796782d49c2416571d560f8bbde143ef0a50075148a4236069b26d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d9393dd9f2b8766c406f2a152f0875c76450eb8ab9a5565e1ec45a2c5689b`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 12.0 MB (11960029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4ae78985ca094a26b126937640b174722c0b8175825aae8822e4f4a1b5515a`  
		Last Modified: Tue, 12 Nov 2024 08:15:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76025589d680f9a8fc617f33224737d1675536d8fbf452f0038c23c69b33fc6`  
		Last Modified: Tue, 12 Nov 2024 08:23:38 GMT  
		Size: 27.3 MB (27275461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fada07c03a4a3f8faf9d04033dc785abe51d1723b49aefeedb3125199ac78d2`  
		Last Modified: Tue, 12 Nov 2024 08:23:36 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884a23b570d24db731441c5ccc694e34c6e25497b59504f59a0dbc4087d97c55`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a21cc76254af2bae7ffcd509c78fe4589ef8573ec9be57389f9e7f8a941e4bd`  
		Last Modified: Tue, 12 Nov 2024 08:23:37 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a24bf52bfd2ca0d69efa123187d49a959311301f3522b8d73f9bf38adc6e03`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 5.5 MB (5529598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcb2c5b826483840499322d61c7af2f9d07387a44a677049fb992aef5ad2954`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6007c0747b11841d218301433d3bc032837b1d42d8da092df480f731915755a5`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecf9459e689449c555c0537315a5abbad76bd6f0289d4ed76caf92c70c861803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6490190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3849fe4cfa7d94e11392ba60423f8cb2f35db0550a9e7a3bdbf377967c8d26e`

```dockerfile
```

-	Layers:
	-	`sha256:e57e7f62f054386a7cc6c6fd7f99dab8ff6f9f576bb490efa7390331b537c785`  
		Last Modified: Wed, 13 Nov 2024 02:41:10 GMT  
		Size: 6.5 MB (6468506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b8cad831c9fd8594d2c4dccf409366a3b0461ce413d49b85ce3568c86ba3be`  
		Last Modified: Wed, 13 Nov 2024 02:41:09 GMT  
		Size: 21.7 KB (21684 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:e5f2f9e05a2e29c60ed74e7f1255b7d0da97844d6cf0ab07a561304b43239f65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:12c954096bd94d58a19f0c9234d303f0463b914796d9b77db91855018d908b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191117403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74920f5d237a813d4fb7a360d8a4cdab227573857a86b9488150c37432d046f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
ENV PHP_VERSION=8.1.31
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78785830491e249d9f5bd83049a666d903b4761f00b09584b3ada0a9dec9d1d`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681124892d7f5eb9a2a24707c0caca43919b651d721ed73b54fe7917f74ffd4f`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 104.3 MB (104345530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26211806203d3f972191e9c4c7accb1a5d466395a3dbca2c4302c7bacf32830`  
		Last Modified: Thu, 21 Nov 2024 18:05:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea8e8574cb05c08117c3bb798a09f301ac3324209d6c5defda4c06d733ed9f`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 20.1 MB (20123767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda45c4e5244e9d74d13c03cb3d7e3fd110661ad49300ba8b0796fdb6972c42`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845b5e1070e4e0bbbe681ddff6380991d2cc05127444475e040e135f2a46482`  
		Last Modified: Thu, 21 Nov 2024 18:05:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d4b1a1d98e8575e3999a85a64003ecb1836f6076dfe1ceaf18c900ec8f0e10`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 12.0 MB (12045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cee8824ddea0fcab7e855f2874c5b5349920e1c8d5adac49057dc85387e1058`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c19edffe89caa79df220f557c2fe68963d3fdfa9a0d2006be2bfb7f77e897c0`  
		Last Modified: Thu, 21 Nov 2024 18:05:57 GMT  
		Size: 11.2 MB (11156747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1fa1e107e87c5da1e6b7593f6a077704b207c59e0b4e07480f8b5e1e1bef23`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0192d951aef3f36109ba1b1c5ec84c4fc1fa97e118727c127c41a69023780d2`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f1fa76ace1cf408cb6d2680dd39cb0cfb6d0ac3c121d8fbda0700b9e6408f7`  
		Last Modified: Thu, 21 Nov 2024 18:05:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611431cfd9b7e42a703f3dcd98c36c85cf542ca6554514311d28ee170c1612a`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9385d639a4f261dfb6706c225fd84e09e72c2f0f21284c1763b81e54ffda8530`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 5.5 MB (5506160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e50bac47c0a2366e37e9bbfec3c2d9e3c3c9f1b90c154ceb9700372a22872`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 8.8 MB (8805155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb9f5d4199b33a797ca3fe86530208f90222d3ce8f53c1786fcd29d6cc2c8c`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:42ba5c8ce961a44a20f11f6dffa358a9cf49b584cab88d92d7f63e31b5a5e0cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfe87964c938f1a5140eec3e295c101a4431cae745a1087118cec0296f64efc`

```dockerfile
```

-	Layers:
	-	`sha256:d2f3d97baa08552c79ce7bbdbc64ff97f10ee9e12bce8490777ee1f980a53cf7`  
		Last Modified: Thu, 21 Nov 2024 18:11:11 GMT  
		Size: 7.0 MB (6951302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42fe2529e39f9f01bbca6765ec95097e549d145fd2293b45a4ca4d90d0d4c76a`  
		Last Modified: Thu, 21 Nov 2024 18:11:10 GMT  
		Size: 29.6 KB (29647 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:855d3a00f5c666e0ba1816e2c5e3cf9d1def3ce81125fb85fae5c6cd6f0dc526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184879091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081f1d10ddec085a79732cecce2bb98bc9291c66783214088985e842008831ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9756e7bfc559baf6454131f81839efb97d80f167664be5b4272ac469b5960`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e27785ead77c6cc3a0473bbe35b537db4b7a71bc35c6289f88af2c9ee06119`  
		Last Modified: Tue, 12 Nov 2024 03:32:19 GMT  
		Size: 98.1 MB (98130714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a00cfa6daf2de029a0f81a774bb1018582dc28b1eb0b8bb09c1d7672fb91ce`  
		Last Modified: Tue, 12 Nov 2024 03:32:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35e1d28ad7ebbff66a1fdc4d24ada4c30b131fd323f6cbea4b7fb07bc8d706`  
		Last Modified: Tue, 12 Nov 2024 03:36:02 GMT  
		Size: 20.1 MB (20120907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410639cb967ec54ee760206ed58c1613b50690b91d753ac3ebf143807443f069`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9efafdf219d3eb366948d2078a5f7f1d4ff893121d52b94c89678ccbee36ac`  
		Last Modified: Tue, 12 Nov 2024 03:36:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bab2b47a418040b3840a1bafcfea2f14f9752f49aa2ea6b90974b32ebf2ca`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 12.0 MB (11978802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc778d53608f1875cff56001c235f7a531018d16c1c5b9eabbf1045edaf4bb1`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067793269ed8f18b52705036a589901218319c15e56dab38bd93f8418ba922d8`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 11.2 MB (11153004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d7059b64fcd5314c5606911c22679791f1e4b3ba533d2c82967a21ebac1b9f`  
		Last Modified: Tue, 12 Nov 2024 08:19:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b49f87fa8a33c58bb71bd42eea361299ba660da11b7bae42e39e2ea423491e`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244f81f99ec0f9ed41ad84510f56429b7287f313a6c809b9afc360f0a3bf89b`  
		Last Modified: Tue, 12 Nov 2024 08:19:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d58a0b4cc33e0f8fc24517a57fa92f22b25718b92aff472ead1418306b0507`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71100770710da5e74f1eb845c3a89a2690a44fd54f8463925e81b0b797f6a799`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 5.5 MB (5526351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f634ec6c610d5da15b855138d272e4c800c408773048a9be7bcdac4bb560db6f`  
		Last Modified: Wed, 13 Nov 2024 02:39:48 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf76e4a888e0e1c437979f45f6a4410049ebb0c76b563cfb7fea042b1f22c4`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:62ce9d3745b81e0fbb65269638edbe63e042f0000839d4c075d89da4b1a055a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4866bccb8ad021f4d99a67afc79be0af2a1a5aad17acba6b27c58dbf1bfb1ca1`

```dockerfile
```

-	Layers:
	-	`sha256:d22353b44f4417827e8bba6be4946a5a2f3ec01db7a27851135f0baef31e0a64`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 7.0 MB (6979814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37b9f5d58f853f080778bcf1c82741e40714ccb24f01ee2db94e978812cf949`  
		Last Modified: Wed, 13 Nov 2024 02:39:47 GMT  
		Size: 29.8 KB (29823 bytes)  
		MIME: application/vnd.in-toto+json
