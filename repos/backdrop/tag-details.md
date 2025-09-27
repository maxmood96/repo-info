<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.32`](#backdrop132)
-	[`backdrop:1.32-apache`](#backdrop132-apache)
-	[`backdrop:1.32-fpm`](#backdrop132-fpm)
-	[`backdrop:1.32.0`](#backdrop1320)
-	[`backdrop:1.32.0-apache`](#backdrop1320-apache)
-	[`backdrop:1.32.0-fpm`](#backdrop1320-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:42bb5356f2a5e3e99671dbf26746d5973ee7d3463d96babbf4eee292e1fe8271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1a8bd53a0c338e0844c6de2dbbd109db63d0ec62d45a69fcf10fecff5d5c4745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187956823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79fadad200b82c7e36b7bb9bdcea02a496205dcd5df1507e56b775364408707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5e7d2873ac957ef8cc59bcd6e31b535bd2801ea28a57e1501fdb8e58608c0`  
		Last Modified: Fri, 26 Sep 2025 21:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530aba786a02493324c7bc13bbcc1d1b1776e13b788802de0f1138da76fab0a4`  
		Last Modified: Fri, 26 Sep 2025 22:04:02 GMT  
		Size: 117.8 MB (117837019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3dffb7375d5c97058fb9c6c174b866bb57b13d8adce558c635bc4336a1a80`  
		Last Modified: Fri, 26 Sep 2025 21:40:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4815698f9e98e7d9b6cfeace1b58613b4df10562ba060821fb41443e1456459a`  
		Last Modified: Fri, 26 Sep 2025 21:46:57 GMT  
		Size: 12.7 MB (12727871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2babd2be764aa9c678edabf01261f1aa9899da5719fbc043830131b0061abd90`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9df7fddf02497347a9f081a5f44c63a9dfb8d6392a676afaf0b855ad464e25`  
		Last Modified: Fri, 26 Sep 2025 21:46:55 GMT  
		Size: 11.9 MB (11895462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8160e058e1ee65c9fa76e5fa84cd155f115308d955e45a8a016f62cd9ca6359`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7dbe2646978e215150c5707cb961bcd5300666a9fd0f45416a4331e263d09`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efcffe8984f21b198b9ba5918027184e6ce17c5bc8bae3664548363d621e8c`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec825c9f0ff8f3343933c13ffed18f498f8764cfae490438360dbd336a58bd7`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be70345e7818cf75febc4e111df3f2522fc120253abeea5ce5900856ba568d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 6.5 MB (6538096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6eaf900e6271959c6ef8c907e8324ca83ba90acd1e39ae5fe0164634d7cea2`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 9.2 MB (9170788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21125b6c4e5bb98ae8304cb03b7c7ed0fb4856d152850c17d87a0853d1e3935a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:e3349e6cb869a97435e40eab5bd55c5d2d9f71a9353a7a9a192f98e6a615ce4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20b9ef52806095b2a55ea2093b67acaa71a7e2933a79b2c1a21b6b5e2368ad`

```dockerfile
```

-	Layers:
	-	`sha256:fa06c51abaeb8c29451eaf90a75d7e0a53617dcb011bc47fda67ca42d3bd9844`  
		Last Modified: Sat, 27 Sep 2025 00:26:38 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381e9c0613710b4e411f54d54e98b3445af81553a8c1611283f10653782419a3`  
		Last Modified: Sat, 27 Sep 2025 00:26:39 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:53c4ef749aabe16770bc76295e1f3f7af800c960324173ac12f1326c68675266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181290621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77e6c664bdfba3089b76de28a202bfbf2c7e6a97bc5c097c57e90eb09b9dc79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb32568030279142c9af20da9ddab677bbecf14b8421c6f4ec2027128223aa`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7679eb08550e9f5937b85b2f2cd67f42f0a5caf25643ec01362952734323bae`  
		Last Modified: Fri, 26 Sep 2025 21:58:05 GMT  
		Size: 110.2 MB (110162841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075cf11816fa955bbd8b58daebc6a9cd4213819c8be2df90d9cbb63323c6860`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe1d9145869060a4b5fb52b48fc76dbe36e6d6203af7cdd530586b96c43668c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 12.7 MB (12727375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbb8249730786a0fa81ae5a5eff0148303efb9f7cef8322380887ac4768817e`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcc4e9daf143e0a51a03e480be22cd957d552ef3bf2d4404361978f9a3275e`  
		Last Modified: Fri, 26 Sep 2025 21:48:13 GMT  
		Size: 11.9 MB (11921480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4068253cba836105e44c3548c88ad52d71e111b0c4809b6a75d3efa78863ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317f9d0c1e9f99232fdeae49d740b59fc14dc7b09ade58f72207a099f2d51ab`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5177935b97c2e97c5679a7b31c913aa1e71e666dfcdd305f4732e4cac6b4f`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e5875b252712faaa70aa7149e17a8a7a7ffac6cb348cc21e4eb6568e6239c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdad946ce2366f48cc5bde302880b96ae7f717e522563f9687633d2d7ad50c3`  
		Last Modified: Fri, 26 Sep 2025 22:00:21 GMT  
		Size: 7.2 MB (7157411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4a870539c4a1d6a2ece560e947386b405b3cc17591b00eec27cb8c160de5c8`  
		Last Modified: Fri, 26 Sep 2025 22:00:23 GMT  
		Size: 9.2 MB (9170795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1777d899633a5efc1a18df0079fe09f1843a1214246afad7c6ac83ec9f11a913`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:3095be463eb6d67485ea6343fde4de610c0156ad5b697c51a85e27705c2a0a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b79bb202a0ddeb5f464f949dac6f70b627fdc212f2c6f23aed6b8716dbbb490`

```dockerfile
```

-	Layers:
	-	`sha256:590fff32f0193aca9d230b9e87689bd95750c727962afac5ab15757b9453f9f1`  
		Last Modified: Sat, 27 Sep 2025 00:26:44 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a62deec33dd8983d1e15d3d757e8af31cbb9562d98bfd40cc340b870e7b283`  
		Last Modified: Sat, 27 Sep 2025 00:26:45 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32-apache`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32-fpm`

```console
$ docker pull backdrop@sha256:42bb5356f2a5e3e99671dbf26746d5973ee7d3463d96babbf4eee292e1fe8271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1a8bd53a0c338e0844c6de2dbbd109db63d0ec62d45a69fcf10fecff5d5c4745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187956823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79fadad200b82c7e36b7bb9bdcea02a496205dcd5df1507e56b775364408707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5e7d2873ac957ef8cc59bcd6e31b535bd2801ea28a57e1501fdb8e58608c0`  
		Last Modified: Fri, 26 Sep 2025 21:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530aba786a02493324c7bc13bbcc1d1b1776e13b788802de0f1138da76fab0a4`  
		Last Modified: Fri, 26 Sep 2025 22:04:02 GMT  
		Size: 117.8 MB (117837019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3dffb7375d5c97058fb9c6c174b866bb57b13d8adce558c635bc4336a1a80`  
		Last Modified: Fri, 26 Sep 2025 21:40:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4815698f9e98e7d9b6cfeace1b58613b4df10562ba060821fb41443e1456459a`  
		Last Modified: Fri, 26 Sep 2025 21:46:57 GMT  
		Size: 12.7 MB (12727871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2babd2be764aa9c678edabf01261f1aa9899da5719fbc043830131b0061abd90`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9df7fddf02497347a9f081a5f44c63a9dfb8d6392a676afaf0b855ad464e25`  
		Last Modified: Fri, 26 Sep 2025 21:46:55 GMT  
		Size: 11.9 MB (11895462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8160e058e1ee65c9fa76e5fa84cd155f115308d955e45a8a016f62cd9ca6359`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7dbe2646978e215150c5707cb961bcd5300666a9fd0f45416a4331e263d09`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efcffe8984f21b198b9ba5918027184e6ce17c5bc8bae3664548363d621e8c`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec825c9f0ff8f3343933c13ffed18f498f8764cfae490438360dbd336a58bd7`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be70345e7818cf75febc4e111df3f2522fc120253abeea5ce5900856ba568d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 6.5 MB (6538096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6eaf900e6271959c6ef8c907e8324ca83ba90acd1e39ae5fe0164634d7cea2`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 9.2 MB (9170788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21125b6c4e5bb98ae8304cb03b7c7ed0fb4856d152850c17d87a0853d1e3935a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:e3349e6cb869a97435e40eab5bd55c5d2d9f71a9353a7a9a192f98e6a615ce4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20b9ef52806095b2a55ea2093b67acaa71a7e2933a79b2c1a21b6b5e2368ad`

```dockerfile
```

-	Layers:
	-	`sha256:fa06c51abaeb8c29451eaf90a75d7e0a53617dcb011bc47fda67ca42d3bd9844`  
		Last Modified: Sat, 27 Sep 2025 00:26:38 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381e9c0613710b4e411f54d54e98b3445af81553a8c1611283f10653782419a3`  
		Last Modified: Sat, 27 Sep 2025 00:26:39 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:53c4ef749aabe16770bc76295e1f3f7af800c960324173ac12f1326c68675266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181290621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77e6c664bdfba3089b76de28a202bfbf2c7e6a97bc5c097c57e90eb09b9dc79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb32568030279142c9af20da9ddab677bbecf14b8421c6f4ec2027128223aa`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7679eb08550e9f5937b85b2f2cd67f42f0a5caf25643ec01362952734323bae`  
		Last Modified: Fri, 26 Sep 2025 21:58:05 GMT  
		Size: 110.2 MB (110162841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075cf11816fa955bbd8b58daebc6a9cd4213819c8be2df90d9cbb63323c6860`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe1d9145869060a4b5fb52b48fc76dbe36e6d6203af7cdd530586b96c43668c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 12.7 MB (12727375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbb8249730786a0fa81ae5a5eff0148303efb9f7cef8322380887ac4768817e`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcc4e9daf143e0a51a03e480be22cd957d552ef3bf2d4404361978f9a3275e`  
		Last Modified: Fri, 26 Sep 2025 21:48:13 GMT  
		Size: 11.9 MB (11921480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4068253cba836105e44c3548c88ad52d71e111b0c4809b6a75d3efa78863ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317f9d0c1e9f99232fdeae49d740b59fc14dc7b09ade58f72207a099f2d51ab`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5177935b97c2e97c5679a7b31c913aa1e71e666dfcdd305f4732e4cac6b4f`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e5875b252712faaa70aa7149e17a8a7a7ffac6cb348cc21e4eb6568e6239c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdad946ce2366f48cc5bde302880b96ae7f717e522563f9687633d2d7ad50c3`  
		Last Modified: Fri, 26 Sep 2025 22:00:21 GMT  
		Size: 7.2 MB (7157411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4a870539c4a1d6a2ece560e947386b405b3cc17591b00eec27cb8c160de5c8`  
		Last Modified: Fri, 26 Sep 2025 22:00:23 GMT  
		Size: 9.2 MB (9170795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1777d899633a5efc1a18df0079fe09f1843a1214246afad7c6ac83ec9f11a913`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:3095be463eb6d67485ea6343fde4de610c0156ad5b697c51a85e27705c2a0a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b79bb202a0ddeb5f464f949dac6f70b627fdc212f2c6f23aed6b8716dbbb490`

```dockerfile
```

-	Layers:
	-	`sha256:590fff32f0193aca9d230b9e87689bd95750c727962afac5ab15757b9453f9f1`  
		Last Modified: Sat, 27 Sep 2025 00:26:44 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a62deec33dd8983d1e15d3d757e8af31cbb9562d98bfd40cc340b870e7b283`  
		Last Modified: Sat, 27 Sep 2025 00:26:45 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.0`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.0` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.0` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.0-apache`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.0-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.0-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.0-fpm`

```console
$ docker pull backdrop@sha256:42bb5356f2a5e3e99671dbf26746d5973ee7d3463d96babbf4eee292e1fe8271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.0-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1a8bd53a0c338e0844c6de2dbbd109db63d0ec62d45a69fcf10fecff5d5c4745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187956823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79fadad200b82c7e36b7bb9bdcea02a496205dcd5df1507e56b775364408707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5e7d2873ac957ef8cc59bcd6e31b535bd2801ea28a57e1501fdb8e58608c0`  
		Last Modified: Fri, 26 Sep 2025 21:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530aba786a02493324c7bc13bbcc1d1b1776e13b788802de0f1138da76fab0a4`  
		Last Modified: Fri, 26 Sep 2025 22:04:02 GMT  
		Size: 117.8 MB (117837019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3dffb7375d5c97058fb9c6c174b866bb57b13d8adce558c635bc4336a1a80`  
		Last Modified: Fri, 26 Sep 2025 21:40:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4815698f9e98e7d9b6cfeace1b58613b4df10562ba060821fb41443e1456459a`  
		Last Modified: Fri, 26 Sep 2025 21:46:57 GMT  
		Size: 12.7 MB (12727871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2babd2be764aa9c678edabf01261f1aa9899da5719fbc043830131b0061abd90`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9df7fddf02497347a9f081a5f44c63a9dfb8d6392a676afaf0b855ad464e25`  
		Last Modified: Fri, 26 Sep 2025 21:46:55 GMT  
		Size: 11.9 MB (11895462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8160e058e1ee65c9fa76e5fa84cd155f115308d955e45a8a016f62cd9ca6359`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7dbe2646978e215150c5707cb961bcd5300666a9fd0f45416a4331e263d09`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efcffe8984f21b198b9ba5918027184e6ce17c5bc8bae3664548363d621e8c`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec825c9f0ff8f3343933c13ffed18f498f8764cfae490438360dbd336a58bd7`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be70345e7818cf75febc4e111df3f2522fc120253abeea5ce5900856ba568d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 6.5 MB (6538096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6eaf900e6271959c6ef8c907e8324ca83ba90acd1e39ae5fe0164634d7cea2`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 9.2 MB (9170788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21125b6c4e5bb98ae8304cb03b7c7ed0fb4856d152850c17d87a0853d1e3935a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:e3349e6cb869a97435e40eab5bd55c5d2d9f71a9353a7a9a192f98e6a615ce4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20b9ef52806095b2a55ea2093b67acaa71a7e2933a79b2c1a21b6b5e2368ad`

```dockerfile
```

-	Layers:
	-	`sha256:fa06c51abaeb8c29451eaf90a75d7e0a53617dcb011bc47fda67ca42d3bd9844`  
		Last Modified: Sat, 27 Sep 2025 00:26:38 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381e9c0613710b4e411f54d54e98b3445af81553a8c1611283f10653782419a3`  
		Last Modified: Sat, 27 Sep 2025 00:26:39 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.0-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:53c4ef749aabe16770bc76295e1f3f7af800c960324173ac12f1326c68675266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181290621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77e6c664bdfba3089b76de28a202bfbf2c7e6a97bc5c097c57e90eb09b9dc79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb32568030279142c9af20da9ddab677bbecf14b8421c6f4ec2027128223aa`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7679eb08550e9f5937b85b2f2cd67f42f0a5caf25643ec01362952734323bae`  
		Last Modified: Fri, 26 Sep 2025 21:58:05 GMT  
		Size: 110.2 MB (110162841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075cf11816fa955bbd8b58daebc6a9cd4213819c8be2df90d9cbb63323c6860`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe1d9145869060a4b5fb52b48fc76dbe36e6d6203af7cdd530586b96c43668c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 12.7 MB (12727375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbb8249730786a0fa81ae5a5eff0148303efb9f7cef8322380887ac4768817e`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcc4e9daf143e0a51a03e480be22cd957d552ef3bf2d4404361978f9a3275e`  
		Last Modified: Fri, 26 Sep 2025 21:48:13 GMT  
		Size: 11.9 MB (11921480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4068253cba836105e44c3548c88ad52d71e111b0c4809b6a75d3efa78863ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317f9d0c1e9f99232fdeae49d740b59fc14dc7b09ade58f72207a099f2d51ab`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5177935b97c2e97c5679a7b31c913aa1e71e666dfcdd305f4732e4cac6b4f`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e5875b252712faaa70aa7149e17a8a7a7ffac6cb348cc21e4eb6568e6239c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdad946ce2366f48cc5bde302880b96ae7f717e522563f9687633d2d7ad50c3`  
		Last Modified: Fri, 26 Sep 2025 22:00:21 GMT  
		Size: 7.2 MB (7157411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4a870539c4a1d6a2ece560e947386b405b3cc17591b00eec27cb8c160de5c8`  
		Last Modified: Fri, 26 Sep 2025 22:00:23 GMT  
		Size: 9.2 MB (9170795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1777d899633a5efc1a18df0079fe09f1843a1214246afad7c6ac83ec9f11a913`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.0-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:3095be463eb6d67485ea6343fde4de610c0156ad5b697c51a85e27705c2a0a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b79bb202a0ddeb5f464f949dac6f70b627fdc212f2c6f23aed6b8716dbbb490`

```dockerfile
```

-	Layers:
	-	`sha256:590fff32f0193aca9d230b9e87689bd95750c727962afac5ab15757b9453f9f1`  
		Last Modified: Sat, 27 Sep 2025 00:26:44 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a62deec33dd8983d1e15d3d757e8af31cbb9562d98bfd40cc340b870e7b283`  
		Last Modified: Sat, 27 Sep 2025 00:26:45 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:42bb5356f2a5e3e99671dbf26746d5973ee7d3463d96babbf4eee292e1fe8271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:1a8bd53a0c338e0844c6de2dbbd109db63d0ec62d45a69fcf10fecff5d5c4745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187956823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79fadad200b82c7e36b7bb9bdcea02a496205dcd5df1507e56b775364408707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a5e7d2873ac957ef8cc59bcd6e31b535bd2801ea28a57e1501fdb8e58608c0`  
		Last Modified: Fri, 26 Sep 2025 21:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530aba786a02493324c7bc13bbcc1d1b1776e13b788802de0f1138da76fab0a4`  
		Last Modified: Fri, 26 Sep 2025 22:04:02 GMT  
		Size: 117.8 MB (117837019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3dffb7375d5c97058fb9c6c174b866bb57b13d8adce558c635bc4336a1a80`  
		Last Modified: Fri, 26 Sep 2025 21:40:58 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4815698f9e98e7d9b6cfeace1b58613b4df10562ba060821fb41443e1456459a`  
		Last Modified: Fri, 26 Sep 2025 21:46:57 GMT  
		Size: 12.7 MB (12727871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2babd2be764aa9c678edabf01261f1aa9899da5719fbc043830131b0061abd90`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9df7fddf02497347a9f081a5f44c63a9dfb8d6392a676afaf0b855ad464e25`  
		Last Modified: Fri, 26 Sep 2025 21:46:55 GMT  
		Size: 11.9 MB (11895462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8160e058e1ee65c9fa76e5fa84cd155f115308d955e45a8a016f62cd9ca6359`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7dbe2646978e215150c5707cb961bcd5300666a9fd0f45416a4331e263d09`  
		Last Modified: Fri, 26 Sep 2025 21:46:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efcffe8984f21b198b9ba5918027184e6ce17c5bc8bae3664548363d621e8c`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec825c9f0ff8f3343933c13ffed18f498f8764cfae490438360dbd336a58bd7`  
		Last Modified: Fri, 26 Sep 2025 21:46:56 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11be70345e7818cf75febc4e111df3f2522fc120253abeea5ce5900856ba568d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 6.5 MB (6538096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6eaf900e6271959c6ef8c907e8324ca83ba90acd1e39ae5fe0164634d7cea2`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 9.2 MB (9170788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21125b6c4e5bb98ae8304cb03b7c7ed0fb4856d152850c17d87a0853d1e3935a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:e3349e6cb869a97435e40eab5bd55c5d2d9f71a9353a7a9a192f98e6a615ce4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20b9ef52806095b2a55ea2093b67acaa71a7e2933a79b2c1a21b6b5e2368ad`

```dockerfile
```

-	Layers:
	-	`sha256:fa06c51abaeb8c29451eaf90a75d7e0a53617dcb011bc47fda67ca42d3bd9844`  
		Last Modified: Sat, 27 Sep 2025 00:26:38 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381e9c0613710b4e411f54d54e98b3445af81553a8c1611283f10653782419a3`  
		Last Modified: Sat, 27 Sep 2025 00:26:39 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:53c4ef749aabe16770bc76295e1f3f7af800c960324173ac12f1326c68675266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181290621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77e6c664bdfba3089b76de28a202bfbf2c7e6a97bc5c097c57e90eb09b9dc79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb32568030279142c9af20da9ddab677bbecf14b8421c6f4ec2027128223aa`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7679eb08550e9f5937b85b2f2cd67f42f0a5caf25643ec01362952734323bae`  
		Last Modified: Fri, 26 Sep 2025 21:58:05 GMT  
		Size: 110.2 MB (110162841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075cf11816fa955bbd8b58daebc6a9cd4213819c8be2df90d9cbb63323c6860`  
		Last Modified: Fri, 26 Sep 2025 21:40:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe1d9145869060a4b5fb52b48fc76dbe36e6d6203af7cdd530586b96c43668c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 12.7 MB (12727375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbb8249730786a0fa81ae5a5eff0148303efb9f7cef8322380887ac4768817e`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcc4e9daf143e0a51a03e480be22cd957d552ef3bf2d4404361978f9a3275e`  
		Last Modified: Fri, 26 Sep 2025 21:48:13 GMT  
		Size: 11.9 MB (11921480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4068253cba836105e44c3548c88ad52d71e111b0c4809b6a75d3efa78863ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317f9d0c1e9f99232fdeae49d740b59fc14dc7b09ade58f72207a099f2d51ab`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5177935b97c2e97c5679a7b31c913aa1e71e666dfcdd305f4732e4cac6b4f`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e5875b252712faaa70aa7149e17a8a7a7ffac6cb348cc21e4eb6568e6239c`  
		Last Modified: Fri, 26 Sep 2025 21:48:11 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdad946ce2366f48cc5bde302880b96ae7f717e522563f9687633d2d7ad50c3`  
		Last Modified: Fri, 26 Sep 2025 22:00:21 GMT  
		Size: 7.2 MB (7157411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4a870539c4a1d6a2ece560e947386b405b3cc17591b00eec27cb8c160de5c8`  
		Last Modified: Fri, 26 Sep 2025 22:00:23 GMT  
		Size: 9.2 MB (9170795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1777d899633a5efc1a18df0079fe09f1843a1214246afad7c6ac83ec9f11a913`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:3095be463eb6d67485ea6343fde4de610c0156ad5b697c51a85e27705c2a0a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b79bb202a0ddeb5f464f949dac6f70b627fdc212f2c6f23aed6b8716dbbb490`

```dockerfile
```

-	Layers:
	-	`sha256:590fff32f0193aca9d230b9e87689bd95750c727962afac5ab15757b9453f9f1`  
		Last Modified: Sat, 27 Sep 2025 00:26:44 GMT  
		Size: 7.0 MB (7035037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a62deec33dd8983d1e15d3d757e8af31cbb9562d98bfd40cc340b870e7b283`  
		Last Modified: Sat, 27 Sep 2025 00:26:45 GMT  
		Size: 22.5 KB (22473 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:def2a6bf149932de5b8a0cc52fb3db8f93d889f431df52249f88e15a4cf1ddb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:532161df685d070b5497110bdfaad1f33bbc7bf2f5b6579799a4c24fd8420cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192006664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05718dddf3440d405b79c4b71967ae7ec61d2d638a2fd26a200e6671f17fa770`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb236c67515ff7c62600eaa8b639fb51476d77fdeadfcc7e6f37e66de95580d9`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722e18c03054f6e48efce287c546123b84ddfa13514ba42c7945d30a0628a41`  
		Last Modified: Fri, 26 Sep 2025 21:40:20 GMT  
		Size: 117.8 MB (117836715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c847656b0a3735ce83bee31afe5560fb8dfd2a085144a0772281c102ffddcf`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff3e6be43afc59ce5b18f3617bcfc1162f9998119e226d33633535455a62b78`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 4.2 MB (4224081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e74b229e787d3a512ea93b244da83f57ad14519d5e8b595ff772a00f14182`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68233c8e0a8e2933c748ceba7e20e754a81a1061a39e8fc2b0e0b005a1086f30`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234e98dd4206de417e6e4c95a91c80277f6a39711a2fd8cc3ee55fd30f5c5308`  
		Last Modified: Fri, 26 Sep 2025 21:47:10 GMT  
		Size: 12.7 MB (12746815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9d9a4bb8d788e5277e0c30342b2dc6f69793e629e55e45a97a9023ae806a4c`  
		Last Modified: Fri, 26 Sep 2025 21:47:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9580d4c648cb50f5402f40201dfe10d182202b3744847b8ad09a924efb59825d`  
		Last Modified: Fri, 26 Sep 2025 21:47:00 GMT  
		Size: 11.7 MB (11710256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47febb661cba385ab9aa50270db0e47ba45e864417b8dfb3673138d081f38274`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91857c9950c7de98d8bddb556e56146d1d7623cf319673816fac2bc70b34316`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca35e8ff91fbd6e7d22d834b7cc47fffb8e9e869bc8de1e2239f0f22f751a7b`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4272a886973666e84779dc8a65707b99934d2db135f81302a42a6af8c2b30d`  
		Last Modified: Fri, 26 Sep 2025 21:46:59 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40687002df9caae662d9adaf80e93d7712fce7451270c870ef1c83c9adf651d3`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101a822d5dc9862ce298d344ac67629ccec96a98cbdcc7754af95657fa87a0bb`  
		Last Modified: Fri, 26 Sep 2025 22:06:18 GMT  
		Size: 6.5 MB (6537449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f915dc894d4852487eb7f714077d8e1f3498f5f4fabe1252898d5e57df516a`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac993eed723791014d3b31100b85878add7f08855a4f0903a3dc406743b6e68d`  
		Last Modified: Fri, 26 Sep 2025 22:06:17 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:77039a47051c86efcd974bf66f1d41b170154a2989185ee8088e4cea02228c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa10722e7f9c8705c0ef91dafc43365312b49819a6c80f840957124e187bb1a7`

```dockerfile
```

-	Layers:
	-	`sha256:26943283cc9c52298a2f1b19bc58ad107e8b3f91e2f5adcd43aa9e9eb01a84fa`  
		Last Modified: Sat, 27 Sep 2025 00:26:26 GMT  
		Size: 7.5 MB (7461276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbb7e1c3a915f3b0147653b56761e1ebf66829e6b0255138fb2b41016ab3c9b`  
		Last Modified: Sat, 27 Sep 2025 00:26:27 GMT  
		Size: 30.6 KB (30601 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:03380986d225b2bb6643f7c22ba5983a2abb42c64e3f0b48cd7eb19592539db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185414613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61bdeaebe5499fabd30882f4245c60ac9cef42852862fc0074eba07c661dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 18 Sep 2025 23:57:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Sep 2025 23:57:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_VERSION=8.3.26
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 18 Sep 2025 23:57:15 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Sep 2025 23:57:15 GMT
STOPSIGNAL SIGWINCH
# Thu, 18 Sep 2025 23:57:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
# Thu, 18 Sep 2025 23:57:15 GMT
RUN a2enmod rewrite # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
WORKDIR /var/www/html
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_VERSION=1.32.0
# Thu, 18 Sep 2025 23:57:15 GMT
ENV BACKDROP_MD5=dd1b43ba169fb750c64cc2da035b4ceb
# Thu, 18 Sep 2025 23:57:15 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 23:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 23:57:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe286e4391ff579cb76e6eb9e4c8373a0a47bd6c381d9098cc7f411515669a`  
		Last Modified: Fri, 26 Sep 2025 21:40:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c05ec9d96ed1f2e2ec0402d8491d10ca191e0d77f983d94b3b5f21114d3eb2`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 110.2 MB (110162791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88df4e02be715671ea678a06925e734e09b9b7a4ac2a0e1f8d4f0bad3737ee5`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a6a89650c0bb80084fb5c2c57871f0e1c361fd65db330bb5fe7de026d4df`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab26c1a2e31ef81430345efa3966ffed1676151c1d9dc6c9a6ddeb1adf7e6c`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8bc8cddb5d6d0afee07b94683f89b32447fde6a7ea475feeade240b4d69c7`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f3a898a28a3208366b15bec7a7b6baabfe178d9c7e2d5184f0199c487fe09`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 12.7 MB (12746447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f956e70f11466c51962c639a5d0b4fac9575403cd5c5ec3550cfbf8db8b63`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212dc59de538ffeeb3dbc00650a8edc7cbc1e77f38b80dbd5ec91737b28c4ef`  
		Last Modified: Fri, 26 Sep 2025 21:48:21 GMT  
		Size: 11.7 MB (11731783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef914bb683300152680f90deb04d1325ebc81d708d3aa21b288d461a25754d1f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80da7d9f4e62b53d7a30fbfe9b47b44aa47d4cd7f4d03a52db858050e80ec6f`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad109460fcc2d12f06ed8b71fd35b31b14c8abac56f07e6fa4038c995b5a44`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6f011ca460e16e3f56a43bbd23527cae796b6c409c1aa5a435f5ee669894ae`  
		Last Modified: Fri, 26 Sep 2025 21:48:20 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96171111538cc9b566676168dd4332f097389eb12d4f839ba4c0a752d3da6a2`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 305.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16896830d824ce7a67bae5d4761ccb51a92eebb5c78f324cae605397c000f46a`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 7.2 MB (7157015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd56a18c5812d85626996f5a70f40d45b2b7faca5c2c3c943971ec325423637`  
		Last Modified: Fri, 26 Sep 2025 22:00:20 GMT  
		Size: 9.2 MB (9170811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2680a9f7720b65b2b87cb1477428ea76c74ba2cf3a8ec5ebef391dbffa4e94`  
		Last Modified: Fri, 26 Sep 2025 22:00:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:8cd58ddc5611bde4c450eb1012cdfa868c953b463c1dc6bc2067d39aa725f806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7994be9c24b298364122830769d4c187ad5741d3ffe507b0846b7f2d7711faa`

```dockerfile
```

-	Layers:
	-	`sha256:bbab50d2607c3256bc32603d059b075da75b02f445035263e273f918653266aa`  
		Last Modified: Sat, 27 Sep 2025 00:26:32 GMT  
		Size: 7.6 MB (7558656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffdc67481fed44e4cf58b2ea3d47fa9de0c16db0f3307c62252c532768640a`  
		Last Modified: Sat, 27 Sep 2025 00:26:33 GMT  
		Size: 30.8 KB (30783 bytes)  
		MIME: application/vnd.in-toto+json
