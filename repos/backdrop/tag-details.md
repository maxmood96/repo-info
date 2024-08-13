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
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:98b0e315b37810108e966225e336773c2af1b1af7340b31beb4eb209a78cd471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:27c17ee397cb3d1495d7fdb811ae25094cf974d2dd4308fcca812c5d80952c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187474829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6690ad6e16c6713f58ce9e31d6b85bc38211c7e8f9ce88c2710f800a3af1f90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453afb71b99067855d7c37b52eb29caf3873829654e79c8f49d22536a3b5a05`  
		Last Modified: Tue, 13 Aug 2024 03:01:39 GMT  
		Size: 12.1 MB (12140203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8e682f6b26748b1df794c1457b190499fd4008903c79d21fe35df702805e9`  
		Last Modified: Tue, 13 Aug 2024 03:01:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a4688fe2529dcc9b2f423332852dada3cbfa8c85c9f68ab91fcdaa704ae00`  
		Last Modified: Tue, 13 Aug 2024 03:02:21 GMT  
		Size: 27.5 MB (27533728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2659ecc4ef1dc6b745be82f30bd217a306ec34d5a0f2e5960458e693f5efeba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074173b2aa12e335e93335a8957e7eeaf2398c7419b36c8d6315c1fec454cba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5076401f6e248e195d6827849a75832d3dd704fd5db882342122038959061db2`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa72f040dcde069f5a6f5759ed49274e6a1f8f7a6f27062ac32e339f52fc98`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 5.5 MB (5506990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cfcd1c9014a75e8fa07d526a01d81bd502219ef044409ddf5ebcbe8a2d6d0b`  
		Last Modified: Tue, 13 Aug 2024 04:01:33 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28704f038fd0fcd485fe14f45cbe855dfd437dd4c873a641e35411e567267f`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:79940aab28898f23c29fb1cf728cc2c07c7eea9f42bfdb88122e41a091f7c718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d0bb37722fd66b0b9130a3c5790e836323aa28c4dc07caa96acd52c9da7f67`

```dockerfile
```

-	Layers:
	-	`sha256:ecd6a5e8c4b7f3aaec1be6ed16415aecf83b7848f71fcb9d650888f099568592`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 6.4 MB (6416804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cf40236bd9bd32f56d2199aeaf06daa3a6111b4fb89644084b937b5cc8b3a6`  
		Last Modified: Tue, 13 Aug 2024 04:01:31 GMT  
		Size: 20.8 KB (20848 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e08ce7968fbb3abb3f1186946df415313c8c94682f2fc7c0e6c33b0c26611b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181253364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e998700ef1a94c0149ec489658e32e95e5a1e46adf16c25532f2ae1fe6ff47e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfebf66cc50866c1598f478e798c74ec5fc6ba224a6090416ac10afc0e3d963`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 12.1 MB (12139927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e8606882b93475626d555528701120155428ea3faa7d6fc5807746bbd77e7`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dae67f0268f37fc082f95b9fd7691fcfc707abd0b1aacb16f984c015873be`  
		Last Modified: Tue, 23 Jul 2024 08:00:17 GMT  
		Size: 27.5 MB (27480017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f658dc980d7c6ea5804e7aa0f4b123b1078addedcee411867094839cbda7f`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d965414a6a7620df03220c6316ddc8c78bc2960c8e5ebddd76478182b5e85a5`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651c016ca4d3023f1a86cc97e00ecbef93bf114ac664421cdc1d1dd28223a77`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00380050ce8fca415555f73298169e71b3d3ed04f8874b02957313c1ee5749b`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 5.5 MB (5526724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d91033b32f2f7eb20753209e9b525bbedcb3bdfc5a84a77329b1ef147d2699`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638efbace47688e117bfed1437ebb55042a6e877360bdba4db9c5022ebaa93a2`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:fa3dd22f4ece87cad39ac10f65f7c70e61ca80ec6e2d3dbd213be7fd41871e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b7345dbd5c05f5f6147d91944444de7747c0dcdb106c1fed56290929ac1e4`

```dockerfile
```

-	Layers:
	-	`sha256:db0efa13f236828533c84129ba2b222e92d88c76c1a5824b78f5cbec6c1f5f10`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 6.4 MB (6445252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638bd43a7a0d5160d9a210393f8a8a024f054e86a1594cc91cbdf53adcf91405`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26-apache`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26-fpm`

```console
$ docker pull backdrop@sha256:98b0e315b37810108e966225e336773c2af1b1af7340b31beb4eb209a78cd471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:27c17ee397cb3d1495d7fdb811ae25094cf974d2dd4308fcca812c5d80952c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187474829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6690ad6e16c6713f58ce9e31d6b85bc38211c7e8f9ce88c2710f800a3af1f90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453afb71b99067855d7c37b52eb29caf3873829654e79c8f49d22536a3b5a05`  
		Last Modified: Tue, 13 Aug 2024 03:01:39 GMT  
		Size: 12.1 MB (12140203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8e682f6b26748b1df794c1457b190499fd4008903c79d21fe35df702805e9`  
		Last Modified: Tue, 13 Aug 2024 03:01:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a4688fe2529dcc9b2f423332852dada3cbfa8c85c9f68ab91fcdaa704ae00`  
		Last Modified: Tue, 13 Aug 2024 03:02:21 GMT  
		Size: 27.5 MB (27533728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2659ecc4ef1dc6b745be82f30bd217a306ec34d5a0f2e5960458e693f5efeba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074173b2aa12e335e93335a8957e7eeaf2398c7419b36c8d6315c1fec454cba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5076401f6e248e195d6827849a75832d3dd704fd5db882342122038959061db2`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa72f040dcde069f5a6f5759ed49274e6a1f8f7a6f27062ac32e339f52fc98`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 5.5 MB (5506990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cfcd1c9014a75e8fa07d526a01d81bd502219ef044409ddf5ebcbe8a2d6d0b`  
		Last Modified: Tue, 13 Aug 2024 04:01:33 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28704f038fd0fcd485fe14f45cbe855dfd437dd4c873a641e35411e567267f`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:79940aab28898f23c29fb1cf728cc2c07c7eea9f42bfdb88122e41a091f7c718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d0bb37722fd66b0b9130a3c5790e836323aa28c4dc07caa96acd52c9da7f67`

```dockerfile
```

-	Layers:
	-	`sha256:ecd6a5e8c4b7f3aaec1be6ed16415aecf83b7848f71fcb9d650888f099568592`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 6.4 MB (6416804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cf40236bd9bd32f56d2199aeaf06daa3a6111b4fb89644084b937b5cc8b3a6`  
		Last Modified: Tue, 13 Aug 2024 04:01:31 GMT  
		Size: 20.8 KB (20848 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e08ce7968fbb3abb3f1186946df415313c8c94682f2fc7c0e6c33b0c26611b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181253364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e998700ef1a94c0149ec489658e32e95e5a1e46adf16c25532f2ae1fe6ff47e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfebf66cc50866c1598f478e798c74ec5fc6ba224a6090416ac10afc0e3d963`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 12.1 MB (12139927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e8606882b93475626d555528701120155428ea3faa7d6fc5807746bbd77e7`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dae67f0268f37fc082f95b9fd7691fcfc707abd0b1aacb16f984c015873be`  
		Last Modified: Tue, 23 Jul 2024 08:00:17 GMT  
		Size: 27.5 MB (27480017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f658dc980d7c6ea5804e7aa0f4b123b1078addedcee411867094839cbda7f`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d965414a6a7620df03220c6316ddc8c78bc2960c8e5ebddd76478182b5e85a5`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651c016ca4d3023f1a86cc97e00ecbef93bf114ac664421cdc1d1dd28223a77`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00380050ce8fca415555f73298169e71b3d3ed04f8874b02957313c1ee5749b`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 5.5 MB (5526724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d91033b32f2f7eb20753209e9b525bbedcb3bdfc5a84a77329b1ef147d2699`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638efbace47688e117bfed1437ebb55042a6e877360bdba4db9c5022ebaa93a2`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:fa3dd22f4ece87cad39ac10f65f7c70e61ca80ec6e2d3dbd213be7fd41871e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b7345dbd5c05f5f6147d91944444de7747c0dcdb106c1fed56290929ac1e4`

```dockerfile
```

-	Layers:
	-	`sha256:db0efa13f236828533c84129ba2b222e92d88c76c1a5824b78f5cbec6c1f5f10`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 6.4 MB (6445252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638bd43a7a0d5160d9a210393f8a8a024f054e86a1594cc91cbdf53adcf91405`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1-apache`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.26.1-fpm`

```console
$ docker pull backdrop@sha256:98b0e315b37810108e966225e336773c2af1b1af7340b31beb4eb209a78cd471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.26.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:27c17ee397cb3d1495d7fdb811ae25094cf974d2dd4308fcca812c5d80952c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187474829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6690ad6e16c6713f58ce9e31d6b85bc38211c7e8f9ce88c2710f800a3af1f90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453afb71b99067855d7c37b52eb29caf3873829654e79c8f49d22536a3b5a05`  
		Last Modified: Tue, 13 Aug 2024 03:01:39 GMT  
		Size: 12.1 MB (12140203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8e682f6b26748b1df794c1457b190499fd4008903c79d21fe35df702805e9`  
		Last Modified: Tue, 13 Aug 2024 03:01:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a4688fe2529dcc9b2f423332852dada3cbfa8c85c9f68ab91fcdaa704ae00`  
		Last Modified: Tue, 13 Aug 2024 03:02:21 GMT  
		Size: 27.5 MB (27533728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2659ecc4ef1dc6b745be82f30bd217a306ec34d5a0f2e5960458e693f5efeba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074173b2aa12e335e93335a8957e7eeaf2398c7419b36c8d6315c1fec454cba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5076401f6e248e195d6827849a75832d3dd704fd5db882342122038959061db2`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa72f040dcde069f5a6f5759ed49274e6a1f8f7a6f27062ac32e339f52fc98`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 5.5 MB (5506990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cfcd1c9014a75e8fa07d526a01d81bd502219ef044409ddf5ebcbe8a2d6d0b`  
		Last Modified: Tue, 13 Aug 2024 04:01:33 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28704f038fd0fcd485fe14f45cbe855dfd437dd4c873a641e35411e567267f`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:79940aab28898f23c29fb1cf728cc2c07c7eea9f42bfdb88122e41a091f7c718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d0bb37722fd66b0b9130a3c5790e836323aa28c4dc07caa96acd52c9da7f67`

```dockerfile
```

-	Layers:
	-	`sha256:ecd6a5e8c4b7f3aaec1be6ed16415aecf83b7848f71fcb9d650888f099568592`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 6.4 MB (6416804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cf40236bd9bd32f56d2199aeaf06daa3a6111b4fb89644084b937b5cc8b3a6`  
		Last Modified: Tue, 13 Aug 2024 04:01:31 GMT  
		Size: 20.8 KB (20848 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.26.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e08ce7968fbb3abb3f1186946df415313c8c94682f2fc7c0e6c33b0c26611b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181253364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e998700ef1a94c0149ec489658e32e95e5a1e46adf16c25532f2ae1fe6ff47e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfebf66cc50866c1598f478e798c74ec5fc6ba224a6090416ac10afc0e3d963`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 12.1 MB (12139927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e8606882b93475626d555528701120155428ea3faa7d6fc5807746bbd77e7`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dae67f0268f37fc082f95b9fd7691fcfc707abd0b1aacb16f984c015873be`  
		Last Modified: Tue, 23 Jul 2024 08:00:17 GMT  
		Size: 27.5 MB (27480017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f658dc980d7c6ea5804e7aa0f4b123b1078addedcee411867094839cbda7f`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d965414a6a7620df03220c6316ddc8c78bc2960c8e5ebddd76478182b5e85a5`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651c016ca4d3023f1a86cc97e00ecbef93bf114ac664421cdc1d1dd28223a77`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00380050ce8fca415555f73298169e71b3d3ed04f8874b02957313c1ee5749b`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 5.5 MB (5526724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d91033b32f2f7eb20753209e9b525bbedcb3bdfc5a84a77329b1ef147d2699`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638efbace47688e117bfed1437ebb55042a6e877360bdba4db9c5022ebaa93a2`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.26.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:fa3dd22f4ece87cad39ac10f65f7c70e61ca80ec6e2d3dbd213be7fd41871e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b7345dbd5c05f5f6147d91944444de7747c0dcdb106c1fed56290929ac1e4`

```dockerfile
```

-	Layers:
	-	`sha256:db0efa13f236828533c84129ba2b222e92d88c76c1a5824b78f5cbec6c1f5f10`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 6.4 MB (6445252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638bd43a7a0d5160d9a210393f8a8a024f054e86a1594cc91cbdf53adcf91405`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:98b0e315b37810108e966225e336773c2af1b1af7340b31beb4eb209a78cd471
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:27c17ee397cb3d1495d7fdb811ae25094cf974d2dd4308fcca812c5d80952c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187474829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6690ad6e16c6713f58ce9e31d6b85bc38211c7e8f9ce88c2710f800a3af1f90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453afb71b99067855d7c37b52eb29caf3873829654e79c8f49d22536a3b5a05`  
		Last Modified: Tue, 13 Aug 2024 03:01:39 GMT  
		Size: 12.1 MB (12140203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8e682f6b26748b1df794c1457b190499fd4008903c79d21fe35df702805e9`  
		Last Modified: Tue, 13 Aug 2024 03:01:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a4688fe2529dcc9b2f423332852dada3cbfa8c85c9f68ab91fcdaa704ae00`  
		Last Modified: Tue, 13 Aug 2024 03:02:21 GMT  
		Size: 27.5 MB (27533728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2659ecc4ef1dc6b745be82f30bd217a306ec34d5a0f2e5960458e693f5efeba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074173b2aa12e335e93335a8957e7eeaf2398c7419b36c8d6315c1fec454cba9`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5076401f6e248e195d6827849a75832d3dd704fd5db882342122038959061db2`  
		Last Modified: Tue, 13 Aug 2024 03:02:17 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa72f040dcde069f5a6f5759ed49274e6a1f8f7a6f27062ac32e339f52fc98`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 5.5 MB (5506990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cfcd1c9014a75e8fa07d526a01d81bd502219ef044409ddf5ebcbe8a2d6d0b`  
		Last Modified: Tue, 13 Aug 2024 04:01:33 GMT  
		Size: 8.8 MB (8805180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28704f038fd0fcd485fe14f45cbe855dfd437dd4c873a641e35411e567267f`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:79940aab28898f23c29fb1cf728cc2c07c7eea9f42bfdb88122e41a091f7c718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d0bb37722fd66b0b9130a3c5790e836323aa28c4dc07caa96acd52c9da7f67`

```dockerfile
```

-	Layers:
	-	`sha256:ecd6a5e8c4b7f3aaec1be6ed16415aecf83b7848f71fcb9d650888f099568592`  
		Last Modified: Tue, 13 Aug 2024 04:01:32 GMT  
		Size: 6.4 MB (6416804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cf40236bd9bd32f56d2199aeaf06daa3a6111b4fb89644084b937b5cc8b3a6`  
		Last Modified: Tue, 13 Aug 2024 04:01:31 GMT  
		Size: 20.8 KB (20848 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:e08ce7968fbb3abb3f1186946df415313c8c94682f2fc7c0e6c33b0c26611b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181253364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e998700ef1a94c0149ec489658e32e95e5a1e46adf16c25532f2ae1fe6ff47e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 9000
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfebf66cc50866c1598f478e798c74ec5fc6ba224a6090416ac10afc0e3d963`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 12.1 MB (12139927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e8606882b93475626d555528701120155428ea3faa7d6fc5807746bbd77e7`  
		Last Modified: Tue, 23 Jul 2024 07:59:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dae67f0268f37fc082f95b9fd7691fcfc707abd0b1aacb16f984c015873be`  
		Last Modified: Tue, 23 Jul 2024 08:00:17 GMT  
		Size: 27.5 MB (27480017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f658dc980d7c6ea5804e7aa0f4b123b1078addedcee411867094839cbda7f`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d965414a6a7620df03220c6316ddc8c78bc2960c8e5ebddd76478182b5e85a5`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651c016ca4d3023f1a86cc97e00ecbef93bf114ac664421cdc1d1dd28223a77`  
		Last Modified: Tue, 23 Jul 2024 08:00:14 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00380050ce8fca415555f73298169e71b3d3ed04f8874b02957313c1ee5749b`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 5.5 MB (5526724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d91033b32f2f7eb20753209e9b525bbedcb3bdfc5a84a77329b1ef147d2699`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638efbace47688e117bfed1437ebb55042a6e877360bdba4db9c5022ebaa93a2`  
		Last Modified: Tue, 23 Jul 2024 11:13:11 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:fa3dd22f4ece87cad39ac10f65f7c70e61ca80ec6e2d3dbd213be7fd41871e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7b7345dbd5c05f5f6147d91944444de7747c0dcdb106c1fed56290929ac1e4`

```dockerfile
```

-	Layers:
	-	`sha256:db0efa13f236828533c84129ba2b222e92d88c76c1a5824b78f5cbec6c1f5f10`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 6.4 MB (6445252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638bd43a7a0d5160d9a210393f8a8a024f054e86a1594cc91cbdf53adcf91405`  
		Last Modified: Tue, 23 Jul 2024 11:13:09 GMT  
		Size: 21.1 KB (21142 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:648655bcd223c686c0d53e4a5f61be4507c96de33996005a28a95ca087401a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:65f1103d27cbfdeab122ec37ea13dd4456655c6bc2ed9fff19c4fb00556d75cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e54434e12481d630c6e587c160e8645a057af62cca30f04078a2883f5baac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe65c9579cf319330d41574ba2da6432b17c0704a30f367e69a18f8fb521d08`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fb9bdf2456ca44f41273902e3ffd4c8913ba2c9e48754e4802b8646b2d6cf8`  
		Last Modified: Tue, 13 Aug 2024 02:54:11 GMT  
		Size: 104.3 MB (104349003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029db5f1c17f8a732ffd7afbeccfbaaf44323a683087527c8d2414213ab53f32`  
		Last Modified: Tue, 13 Aug 2024 02:53:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fd66af37d30f608a646fe71d0c1e709e0549a5d4d3fb008993ec89ebfe57b`  
		Last Modified: Tue, 13 Aug 2024 02:54:33 GMT  
		Size: 20.3 MB (20327979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de55dbd5d2208f77cf2fe2643914f9f219753016786a9cea73fb344ac0f892b7`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b6e8540b906f4440e44686742488990c25449285e6138059d60f268556b965`  
		Last Modified: Tue, 13 Aug 2024 02:54:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b088dc790fe0f6c346b16b5f80d6ec93cc1e71cddbe6b51b7a5f1b7f4e67fc`  
		Last Modified: Tue, 13 Aug 2024 03:02:05 GMT  
		Size: 12.2 MB (12159416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25779f1055863b9fd30f308fd727e0c0e650c6cf713e812f1c8364fb95506bc0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781cb0f10758969e239f7fdb573e608e3d85b9d3e029518d976c112e63c3840`  
		Last Modified: Tue, 13 Aug 2024 03:02:04 GMT  
		Size: 11.2 MB (11155845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555397bcfab647ff44d94f832c3e0588943255bb25637402d04edc379f6bde0`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e4ceed4d60375c67c596077465c4925f4acad6b042aaab7ba824c7d1e5989`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbed0b95816864f8a261190688aa2ae587c5bdbbc812f7208221707d22bc77b`  
		Last Modified: Tue, 13 Aug 2024 03:02:02 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e30d2c9502bd6c1fdea608710506ecaf11bb9fd295e7e06a82e622fbef12f`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d530ec10014af85296e384eee01c10d1b6f3373917eb360e5a97548bd8812cf`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 5.5 MB (5501759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7869fb1262a6fcaaa983d5c5101915f4d1ceb1e87d54d483c01f3e87fc380ba`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 8.8 MB (8805154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d83d8844d5dfd735fe9c43fbe677df5464d4aaf42273c0fc5bf21bbaea4ec2d`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:de600ad0ec61aae818059c024e8466872a580fe15cf298ada2f359bbea7fe046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213cb5289f363788224ee734a0b86bd34a20d89e6fa1369be4d87e6b23fe5368`

```dockerfile
```

-	Layers:
	-	`sha256:c333742e027300148857def78c6482151ed162c8adaf5bc5e81232b82cc10b4e`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 6.9 MB (6926280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c79de848488f459792550ec90afe0a303b722f83b59be80c14dc18a515c213`  
		Last Modified: Tue, 13 Aug 2024 04:01:36 GMT  
		Size: 28.9 KB (28949 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a03c903e82a06e83624ea263c2a2f88df64f194ed07de1ab432a7279a4b6315b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185259817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e34e809df7665c405ccb0c44e2d49e07b487ceb919a4eae28c663838a323daa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 14 Oct 2023 00:46:03 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 14 Oct 2023 00:46:03 GMT
CMD ["bash"]
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 14 Oct 2023 00:46:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Sat, 14 Oct 2023 00:46:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Sat, 14 Oct 2023 00:46:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 14 Oct 2023 00:46:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_VERSION=8.1.29
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Sat, 14 Oct 2023 00:46:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 14 Oct 2023 00:46:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 14 Oct 2023 00:46:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 14 Oct 2023 00:46:03 GMT
STOPSIGNAL SIGWINCH
# Sat, 14 Oct 2023 00:46:03 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 14 Oct 2023 00:46:03 GMT
WORKDIR /var/www/html
# Sat, 14 Oct 2023 00:46:03 GMT
EXPOSE 80
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
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc24c12812b24708888b440f67cf39295111ce0406b3816522533957cfca6a5`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80056e3fbbff475fe84dde2da2642e8ed70b430cb97f6aa613d49ef6c635624`  
		Last Modified: Tue, 23 Jul 2024 07:48:07 GMT  
		Size: 98.1 MB (98131446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09a265e9595e55f8a9e0c1f1e8b47c3dfa5c5ef02b83f68606ccaca026601a`  
		Last Modified: Tue, 23 Jul 2024 07:47:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bee02aac93aa565658f5f0df1cfbc9d3bd396876bd1c96e47ba2aa0529bd33`  
		Last Modified: Tue, 23 Jul 2024 07:48:30 GMT  
		Size: 20.3 MB (20324783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df0b4d6b36f10ef6560f6dec888e4c9a33aaf22dd49ab5406dc4bf2b4a41ff2`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee99f2fe1d2c0500eea615b9137c7284a47b9e6bac9f34a412dab37f39b6d7`  
		Last Modified: Tue, 23 Jul 2024 07:48:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aa511cf3ab2c98eab26613ed0359f79b351b7d2fb884dc1b928b2133feb403`  
		Last Modified: Tue, 23 Jul 2024 07:59:57 GMT  
		Size: 12.2 MB (12159036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269536d152165187d565a0eadd714bce34ae92c27c1215fcb2e19c2efd21ad01`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9729c5375183ecc71e8ba24f125937fe85f92664a52515ee535f538c03cf44f4`  
		Last Modified: Tue, 23 Jul 2024 07:59:56 GMT  
		Size: 11.2 MB (11154586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daee4feb0a2602a28bad589927be4bfe565070df6a2281568becde4fb4bf022`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751bac29936487c5c4625fca68a93e4f1bd32f28395aaeb36381dbebe8eaec5f`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77525f8b166eb792f5de4c1fe7082d10f5ea1735a93b72ead3df97d86c09125d`  
		Last Modified: Tue, 23 Jul 2024 07:59:55 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be397d309c8a336fc937ac3301aa9f1c0eabe90ac87a2828de2ec28b8274352`  
		Last Modified: Tue, 23 Jul 2024 11:11:46 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce44306e951d8ae1af2c1a9f4c8323c25f1b233446f50f35e70c89831328a158`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 5.5 MB (5521473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a42ca8fddc1f70209c809ef1e9104c758f3b1820d65e5b1aeb3409d7300d3`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 8.8 MB (8805178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08159f37174fa841546f5948cc275530afd32adabef0258ecdf7771d9f973b66`  
		Last Modified: Tue, 23 Jul 2024 11:11:47 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:6d0e1799d585182361e55c8e0d0ca13b1f0efd238f85848504d1438c38ad587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298c3e1fbdc755f15375846b4fa3d228a706ee70aacbd0b1f52e60af82c4b534`

```dockerfile
```

-	Layers:
	-	`sha256:4f4f6a2a77aaea52694ef533aa903ed7877f0cc976e79a689f2c63eccee0595c`  
		Last Modified: Tue, 23 Jul 2024 11:11:43 GMT  
		Size: 7.0 MB (6954792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fd1146ecc3b42a45d23308ee40bdfdb8b64ee8247a83c79cf5f718c584fc1`  
		Last Modified: Tue, 23 Jul 2024 11:11:42 GMT  
		Size: 29.3 KB (29293 bytes)  
		MIME: application/vnd.in-toto+json
