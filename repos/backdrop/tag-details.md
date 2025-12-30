<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `backdrop`

-	[`backdrop:1`](#backdrop1)
-	[`backdrop:1-apache`](#backdrop1-apache)
-	[`backdrop:1-fpm`](#backdrop1-fpm)
-	[`backdrop:1.32`](#backdrop132)
-	[`backdrop:1.32-apache`](#backdrop132-apache)
-	[`backdrop:1.32-fpm`](#backdrop132-fpm)
-	[`backdrop:1.32.1`](#backdrop1321)
-	[`backdrop:1.32.1-apache`](#backdrop1321-apache)
-	[`backdrop:1.32.1-fpm`](#backdrop1321-fpm)
-	[`backdrop:apache`](#backdropapache)
-	[`backdrop:fpm`](#backdropfpm)
-	[`backdrop:latest`](#backdroplatest)

## `backdrop:1`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-apache`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:93b7018fbbb7d5ea1e2bd17cf7acc9914a28d24456cac1bf60710ee48de6e031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0e13c9731944cbd186f5401680da9662598e1ccf914594dac852a73c66633319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187988685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec1f9e0cd93ee7e6390e3fa01e33f1a281a0a8ffcea56e19efd444c211a85ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:23 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:30:24 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:30:24 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:30:24 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:22:40 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:40 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:42 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202811c68f67e44bebb8cbcab5368426f755e61daafc226e0a11505731a32610`  
		Last Modified: Mon, 29 Dec 2025 23:30:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24273ba12d1af0810d7820c7c75ca2b3fe832cb221b71e49e6c26c8138dc23e0`  
		Last Modified: Mon, 29 Dec 2025 23:31:02 GMT  
		Size: 117.8 MB (117838542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d35c8551543daa57c82c78738cce70808d7814d181a064fb5a6e35cfae3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c35ab5e15ef59f75876f694971c7463b29b5439f72fd75d99b7bf75bdbb20`  
		Last Modified: Mon, 29 Dec 2025 23:30:56 GMT  
		Size: 12.7 MB (12749880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ca494a431dd2878f8739fdb5e76c388a0722b00a6391cb5e36e301ff30df2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287427e4d8f82a4a368376d90e27813a59b8f1f04f20fc9e3f94f8a5ac5b8d92`  
		Last Modified: Mon, 29 Dec 2025 23:30:54 GMT  
		Size: 11.9 MB (11897962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ad282648acf930cde22d3abf9cc4ab8aa1e17235fbf4c93b10b667c9e302b`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f29fae1d861375d38b732c702d2361e1fac4c61e26c709a55bf974f14d12d2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc2f98800abb9ff3433c4cb8758f3e376655b54cddcfa08febd96507f60ca1d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2222a5f3710ed1173899dad10c5c5b165fed76153a242c880e607e4cf592940d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db916cf354f888e2139bcc7e394859d51259606abf54cdced9e8b7fd769720`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 6.5 MB (6540680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d0079d9ee1cbb23a6ea8c3a133f364e41e1213c27c0fdbf28a79d24f19d83`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48aae085f39e8700bb89143b4759ba500ebf147e53ab1322b041e889dd7d59`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ed8427937a976b6eef1976eda440b36cca30a14246c37ee286320aa342027ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e670f4a754c71645bee36b16f8b15ce9c1d167ea9f8c4d501323c6840aa89538`

```dockerfile
```

-	Layers:
	-	`sha256:25a6f8f1ede86f1f5a4cdead3d28c98987bef1cc49664d1df38ef38d69f068a6`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 6.9 MB (6937893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ecbe0485448e3dc7955742708de6b65403579b4835e5af3766874e07faff48`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:27fb526277bd8ad5353841506080ec0882beeae5b70b90d2c246d0d7ad202589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181320187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf4c5f39ee4dd5398eec982a829861995e4fbeaddb6b12f7b6e149b56eddd61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:28:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:32:01 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:32:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:32:02 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:32:02 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:32:02 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:25:33 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:25:33 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:25:35 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:25:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6f857c375092a498e45aa7e4eafede989661dab3df985f8991a4ec8708f4f7`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50be2b43a73faa2ac649448727767a1a8b893c5944a0cf84ead770caba14a28`  
		Last Modified: Mon, 29 Dec 2025 23:32:42 GMT  
		Size: 110.2 MB (110162775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f2ce11fa03a0aa05db30d42e8f83ec994ed53ee47288f65308f077c2fe83f`  
		Last Modified: Mon, 29 Dec 2025 23:31:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec25fe35ec5081a533a586a0699c25483e293b81af559d48fb2c2c73a949ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 12.7 MB (12749425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b600cf4286483f95b3815be58c0d61c02de463ba0dd5fec5cd4ceaa97cf53d`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6e73ddc39ef42a8ecb65f58e8a3f6051336f63897f8c53643e0f6a93d9025`  
		Last Modified: Mon, 29 Dec 2025 23:32:33 GMT  
		Size: 11.9 MB (11925365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad922c5b18ddb1921f9a712389844117402404cc8efe4f58479a3f5648aadbbe`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7c886390f32ea4216e380e105aa4d795302d8b140ee5844f12bb66f360273`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d2c724f5ee7fb7b30c30d2c4da72ff114d29ede9253b9a361d558d85255`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1b42487df6bb0a9e4fe65b9428ce018a5441e4ed3b17b898bef965e59396ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0cb734be4028746665b25f78a4ff521d5ec110545039d977832bb7e5307a41`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 7.2 MB (7158900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ab3a3f4e38d479342f956db63c7af0ca0850858458f9487897ac910994e82a`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b3d37560d20bdcbb9fd064128157fb90bbfe40c39d56e8f87531d1c06e1b49`  
		Last Modified: Tue, 30 Dec 2025 01:25:53 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecd38b27dbc195440c178e101c9e39b78002cb47c7f61d123d612b67cc2ae803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5afedb886798760f15092c9cc78e78f1a49dcd9c9c649dcaae3f07675c9d79`

```dockerfile
```

-	Layers:
	-	`sha256:439b223c17dfe559f8822654bd551070551a7726a44a462347400989eea0865e`  
		Last Modified: Tue, 30 Dec 2025 04:26:57 GMT  
		Size: 7.0 MB (7035209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f5443575dafa6baaa8bf7d17cee8c11e72fc2a8eda427009406e517c89c8ea`  
		Last Modified: Tue, 30 Dec 2025 04:26:58 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32-apache`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32-fpm`

```console
$ docker pull backdrop@sha256:93b7018fbbb7d5ea1e2bd17cf7acc9914a28d24456cac1bf60710ee48de6e031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0e13c9731944cbd186f5401680da9662598e1ccf914594dac852a73c66633319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187988685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec1f9e0cd93ee7e6390e3fa01e33f1a281a0a8ffcea56e19efd444c211a85ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:23 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:30:24 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:30:24 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:30:24 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:22:40 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:40 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:42 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202811c68f67e44bebb8cbcab5368426f755e61daafc226e0a11505731a32610`  
		Last Modified: Mon, 29 Dec 2025 23:30:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24273ba12d1af0810d7820c7c75ca2b3fe832cb221b71e49e6c26c8138dc23e0`  
		Last Modified: Mon, 29 Dec 2025 23:31:02 GMT  
		Size: 117.8 MB (117838542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d35c8551543daa57c82c78738cce70808d7814d181a064fb5a6e35cfae3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c35ab5e15ef59f75876f694971c7463b29b5439f72fd75d99b7bf75bdbb20`  
		Last Modified: Mon, 29 Dec 2025 23:30:56 GMT  
		Size: 12.7 MB (12749880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ca494a431dd2878f8739fdb5e76c388a0722b00a6391cb5e36e301ff30df2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287427e4d8f82a4a368376d90e27813a59b8f1f04f20fc9e3f94f8a5ac5b8d92`  
		Last Modified: Mon, 29 Dec 2025 23:30:54 GMT  
		Size: 11.9 MB (11897962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ad282648acf930cde22d3abf9cc4ab8aa1e17235fbf4c93b10b667c9e302b`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f29fae1d861375d38b732c702d2361e1fac4c61e26c709a55bf974f14d12d2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc2f98800abb9ff3433c4cb8758f3e376655b54cddcfa08febd96507f60ca1d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2222a5f3710ed1173899dad10c5c5b165fed76153a242c880e607e4cf592940d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db916cf354f888e2139bcc7e394859d51259606abf54cdced9e8b7fd769720`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 6.5 MB (6540680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d0079d9ee1cbb23a6ea8c3a133f364e41e1213c27c0fdbf28a79d24f19d83`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48aae085f39e8700bb89143b4759ba500ebf147e53ab1322b041e889dd7d59`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ed8427937a976b6eef1976eda440b36cca30a14246c37ee286320aa342027ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e670f4a754c71645bee36b16f8b15ce9c1d167ea9f8c4d501323c6840aa89538`

```dockerfile
```

-	Layers:
	-	`sha256:25a6f8f1ede86f1f5a4cdead3d28c98987bef1cc49664d1df38ef38d69f068a6`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 6.9 MB (6937893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ecbe0485448e3dc7955742708de6b65403579b4835e5af3766874e07faff48`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:27fb526277bd8ad5353841506080ec0882beeae5b70b90d2c246d0d7ad202589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181320187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf4c5f39ee4dd5398eec982a829861995e4fbeaddb6b12f7b6e149b56eddd61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:28:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:32:01 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:32:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:32:02 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:32:02 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:32:02 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:25:33 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:25:33 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:25:35 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:25:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6f857c375092a498e45aa7e4eafede989661dab3df985f8991a4ec8708f4f7`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50be2b43a73faa2ac649448727767a1a8b893c5944a0cf84ead770caba14a28`  
		Last Modified: Mon, 29 Dec 2025 23:32:42 GMT  
		Size: 110.2 MB (110162775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f2ce11fa03a0aa05db30d42e8f83ec994ed53ee47288f65308f077c2fe83f`  
		Last Modified: Mon, 29 Dec 2025 23:31:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec25fe35ec5081a533a586a0699c25483e293b81af559d48fb2c2c73a949ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 12.7 MB (12749425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b600cf4286483f95b3815be58c0d61c02de463ba0dd5fec5cd4ceaa97cf53d`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6e73ddc39ef42a8ecb65f58e8a3f6051336f63897f8c53643e0f6a93d9025`  
		Last Modified: Mon, 29 Dec 2025 23:32:33 GMT  
		Size: 11.9 MB (11925365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad922c5b18ddb1921f9a712389844117402404cc8efe4f58479a3f5648aadbbe`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7c886390f32ea4216e380e105aa4d795302d8b140ee5844f12bb66f360273`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d2c724f5ee7fb7b30c30d2c4da72ff114d29ede9253b9a361d558d85255`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1b42487df6bb0a9e4fe65b9428ce018a5441e4ed3b17b898bef965e59396ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0cb734be4028746665b25f78a4ff521d5ec110545039d977832bb7e5307a41`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 7.2 MB (7158900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ab3a3f4e38d479342f956db63c7af0ca0850858458f9487897ac910994e82a`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b3d37560d20bdcbb9fd064128157fb90bbfe40c39d56e8f87531d1c06e1b49`  
		Last Modified: Tue, 30 Dec 2025 01:25:53 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecd38b27dbc195440c178e101c9e39b78002cb47c7f61d123d612b67cc2ae803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5afedb886798760f15092c9cc78e78f1a49dcd9c9c649dcaae3f07675c9d79`

```dockerfile
```

-	Layers:
	-	`sha256:439b223c17dfe559f8822654bd551070551a7726a44a462347400989eea0865e`  
		Last Modified: Tue, 30 Dec 2025 04:26:57 GMT  
		Size: 7.0 MB (7035209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f5443575dafa6baaa8bf7d17cee8c11e72fc2a8eda427009406e517c89c8ea`  
		Last Modified: Tue, 30 Dec 2025 04:26:58 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.1`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.1` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.1` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.1` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.1-apache`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.1-apache` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.1-apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.1-apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:1.32.1-fpm`

```console
$ docker pull backdrop@sha256:93b7018fbbb7d5ea1e2bd17cf7acc9914a28d24456cac1bf60710ee48de6e031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1.32.1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0e13c9731944cbd186f5401680da9662598e1ccf914594dac852a73c66633319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187988685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec1f9e0cd93ee7e6390e3fa01e33f1a281a0a8ffcea56e19efd444c211a85ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:23 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:30:24 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:30:24 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:30:24 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:22:40 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:40 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:42 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202811c68f67e44bebb8cbcab5368426f755e61daafc226e0a11505731a32610`  
		Last Modified: Mon, 29 Dec 2025 23:30:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24273ba12d1af0810d7820c7c75ca2b3fe832cb221b71e49e6c26c8138dc23e0`  
		Last Modified: Mon, 29 Dec 2025 23:31:02 GMT  
		Size: 117.8 MB (117838542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d35c8551543daa57c82c78738cce70808d7814d181a064fb5a6e35cfae3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c35ab5e15ef59f75876f694971c7463b29b5439f72fd75d99b7bf75bdbb20`  
		Last Modified: Mon, 29 Dec 2025 23:30:56 GMT  
		Size: 12.7 MB (12749880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ca494a431dd2878f8739fdb5e76c388a0722b00a6391cb5e36e301ff30df2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287427e4d8f82a4a368376d90e27813a59b8f1f04f20fc9e3f94f8a5ac5b8d92`  
		Last Modified: Mon, 29 Dec 2025 23:30:54 GMT  
		Size: 11.9 MB (11897962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ad282648acf930cde22d3abf9cc4ab8aa1e17235fbf4c93b10b667c9e302b`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f29fae1d861375d38b732c702d2361e1fac4c61e26c709a55bf974f14d12d2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc2f98800abb9ff3433c4cb8758f3e376655b54cddcfa08febd96507f60ca1d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2222a5f3710ed1173899dad10c5c5b165fed76153a242c880e607e4cf592940d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db916cf354f888e2139bcc7e394859d51259606abf54cdced9e8b7fd769720`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 6.5 MB (6540680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d0079d9ee1cbb23a6ea8c3a133f364e41e1213c27c0fdbf28a79d24f19d83`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48aae085f39e8700bb89143b4759ba500ebf147e53ab1322b041e889dd7d59`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ed8427937a976b6eef1976eda440b36cca30a14246c37ee286320aa342027ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e670f4a754c71645bee36b16f8b15ce9c1d167ea9f8c4d501323c6840aa89538`

```dockerfile
```

-	Layers:
	-	`sha256:25a6f8f1ede86f1f5a4cdead3d28c98987bef1cc49664d1df38ef38d69f068a6`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 6.9 MB (6937893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ecbe0485448e3dc7955742708de6b65403579b4835e5af3766874e07faff48`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1.32.1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:27fb526277bd8ad5353841506080ec0882beeae5b70b90d2c246d0d7ad202589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181320187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf4c5f39ee4dd5398eec982a829861995e4fbeaddb6b12f7b6e149b56eddd61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:28:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:32:01 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:32:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:32:02 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:32:02 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:32:02 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:25:33 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:25:33 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:25:35 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:25:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6f857c375092a498e45aa7e4eafede989661dab3df985f8991a4ec8708f4f7`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50be2b43a73faa2ac649448727767a1a8b893c5944a0cf84ead770caba14a28`  
		Last Modified: Mon, 29 Dec 2025 23:32:42 GMT  
		Size: 110.2 MB (110162775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f2ce11fa03a0aa05db30d42e8f83ec994ed53ee47288f65308f077c2fe83f`  
		Last Modified: Mon, 29 Dec 2025 23:31:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec25fe35ec5081a533a586a0699c25483e293b81af559d48fb2c2c73a949ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 12.7 MB (12749425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b600cf4286483f95b3815be58c0d61c02de463ba0dd5fec5cd4ceaa97cf53d`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6e73ddc39ef42a8ecb65f58e8a3f6051336f63897f8c53643e0f6a93d9025`  
		Last Modified: Mon, 29 Dec 2025 23:32:33 GMT  
		Size: 11.9 MB (11925365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad922c5b18ddb1921f9a712389844117402404cc8efe4f58479a3f5648aadbbe`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7c886390f32ea4216e380e105aa4d795302d8b140ee5844f12bb66f360273`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d2c724f5ee7fb7b30c30d2c4da72ff114d29ede9253b9a361d558d85255`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1b42487df6bb0a9e4fe65b9428ce018a5441e4ed3b17b898bef965e59396ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0cb734be4028746665b25f78a4ff521d5ec110545039d977832bb7e5307a41`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 7.2 MB (7158900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ab3a3f4e38d479342f956db63c7af0ca0850858458f9487897ac910994e82a`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b3d37560d20bdcbb9fd064128157fb90bbfe40c39d56e8f87531d1c06e1b49`  
		Last Modified: Tue, 30 Dec 2025 01:25:53 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1.32.1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecd38b27dbc195440c178e101c9e39b78002cb47c7f61d123d612b67cc2ae803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5afedb886798760f15092c9cc78e78f1a49dcd9c9c649dcaae3f07675c9d79`

```dockerfile
```

-	Layers:
	-	`sha256:439b223c17dfe559f8822654bd551070551a7726a44a462347400989eea0865e`  
		Last Modified: Tue, 30 Dec 2025 04:26:57 GMT  
		Size: 7.0 MB (7035209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f5443575dafa6baaa8bf7d17cee8c11e72fc2a8eda427009406e517c89c8ea`  
		Last Modified: Tue, 30 Dec 2025 04:26:58 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:apache`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:apache` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:apache` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:apache` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:93b7018fbbb7d5ea1e2bd17cf7acc9914a28d24456cac1bf60710ee48de6e031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0e13c9731944cbd186f5401680da9662598e1ccf914594dac852a73c66633319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187988685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec1f9e0cd93ee7e6390e3fa01e33f1a281a0a8ffcea56e19efd444c211a85ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:23 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:30:24 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:30:24 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:30:24 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:22:40 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:40 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:42 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:42 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202811c68f67e44bebb8cbcab5368426f755e61daafc226e0a11505731a32610`  
		Last Modified: Mon, 29 Dec 2025 23:30:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24273ba12d1af0810d7820c7c75ca2b3fe832cb221b71e49e6c26c8138dc23e0`  
		Last Modified: Mon, 29 Dec 2025 23:31:02 GMT  
		Size: 117.8 MB (117838542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d35c8551543daa57c82c78738cce70808d7814d181a064fb5a6e35cfae3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c35ab5e15ef59f75876f694971c7463b29b5439f72fd75d99b7bf75bdbb20`  
		Last Modified: Mon, 29 Dec 2025 23:30:56 GMT  
		Size: 12.7 MB (12749880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ca494a431dd2878f8739fdb5e76c388a0722b00a6391cb5e36e301ff30df2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287427e4d8f82a4a368376d90e27813a59b8f1f04f20fc9e3f94f8a5ac5b8d92`  
		Last Modified: Mon, 29 Dec 2025 23:30:54 GMT  
		Size: 11.9 MB (11897962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ad282648acf930cde22d3abf9cc4ab8aa1e17235fbf4c93b10b667c9e302b`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f29fae1d861375d38b732c702d2361e1fac4c61e26c709a55bf974f14d12d2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc2f98800abb9ff3433c4cb8758f3e376655b54cddcfa08febd96507f60ca1d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2222a5f3710ed1173899dad10c5c5b165fed76153a242c880e607e4cf592940d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61db916cf354f888e2139bcc7e394859d51259606abf54cdced9e8b7fd769720`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 6.5 MB (6540680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41d0079d9ee1cbb23a6ea8c3a133f364e41e1213c27c0fdbf28a79d24f19d83`  
		Last Modified: Tue, 30 Dec 2025 01:22:59 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48aae085f39e8700bb89143b4759ba500ebf147e53ab1322b041e889dd7d59`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ed8427937a976b6eef1976eda440b36cca30a14246c37ee286320aa342027ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e670f4a754c71645bee36b16f8b15ce9c1d167ea9f8c4d501323c6840aa89538`

```dockerfile
```

-	Layers:
	-	`sha256:25a6f8f1ede86f1f5a4cdead3d28c98987bef1cc49664d1df38ef38d69f068a6`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 6.9 MB (6937893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ecbe0485448e3dc7955742708de6b65403579b4835e5af3766874e07faff48`  
		Last Modified: Tue, 30 Dec 2025 04:26:51 GMT  
		Size: 22.3 KB (22311 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:27fb526277bd8ad5353841506080ec0882beeae5b70b90d2c246d0d7ad202589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181320187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf4c5f39ee4dd5398eec982a829861995e4fbeaddb6b12f7b6e149b56eddd61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:28:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:32:01 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:32:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:32:02 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:32:02 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:32:02 GMT
CMD ["php-fpm"]
# Tue, 30 Dec 2025 01:25:33 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:25:33 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:25:35 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:25:35 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:25:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6f857c375092a498e45aa7e4eafede989661dab3df985f8991a4ec8708f4f7`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50be2b43a73faa2ac649448727767a1a8b893c5944a0cf84ead770caba14a28`  
		Last Modified: Mon, 29 Dec 2025 23:32:42 GMT  
		Size: 110.2 MB (110162775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f2ce11fa03a0aa05db30d42e8f83ec994ed53ee47288f65308f077c2fe83f`  
		Last Modified: Mon, 29 Dec 2025 23:31:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec25fe35ec5081a533a586a0699c25483e293b81af559d48fb2c2c73a949ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 12.7 MB (12749425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b600cf4286483f95b3815be58c0d61c02de463ba0dd5fec5cd4ceaa97cf53d`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6e73ddc39ef42a8ecb65f58e8a3f6051336f63897f8c53643e0f6a93d9025`  
		Last Modified: Mon, 29 Dec 2025 23:32:33 GMT  
		Size: 11.9 MB (11925365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad922c5b18ddb1921f9a712389844117402404cc8efe4f58479a3f5648aadbbe`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7c886390f32ea4216e380e105aa4d795302d8b140ee5844f12bb66f360273`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d2c724f5ee7fb7b30c30d2c4da72ff114d29ede9253b9a361d558d85255`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1b42487df6bb0a9e4fe65b9428ce018a5441e4ed3b17b898bef965e59396ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0cb734be4028746665b25f78a4ff521d5ec110545039d977832bb7e5307a41`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 7.2 MB (7158900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ab3a3f4e38d479342f956db63c7af0ca0850858458f9487897ac910994e82a`  
		Last Modified: Tue, 30 Dec 2025 01:25:54 GMT  
		Size: 9.2 MB (9171003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b3d37560d20bdcbb9fd064128157fb90bbfe40c39d56e8f87531d1c06e1b49`  
		Last Modified: Tue, 30 Dec 2025 01:25:53 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ecd38b27dbc195440c178e101c9e39b78002cb47c7f61d123d612b67cc2ae803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5afedb886798760f15092c9cc78e78f1a49dcd9c9c649dcaae3f07675c9d79`

```dockerfile
```

-	Layers:
	-	`sha256:439b223c17dfe559f8822654bd551070551a7726a44a462347400989eea0865e`  
		Last Modified: Tue, 30 Dec 2025 04:26:57 GMT  
		Size: 7.0 MB (7035209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f5443575dafa6baaa8bf7d17cee8c11e72fc2a8eda427009406e517c89c8ea`  
		Last Modified: Tue, 30 Dec 2025 04:26:58 GMT  
		Size: 22.4 KB (22430 bytes)  
		MIME: application/vnd.in-toto+json

## `backdrop:latest`

```console
$ docker pull backdrop@sha256:fbd108c4972dda0c0f7b78b7633cf95a9a5c7399f1378d79d2e26c308f30f62c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:latest` - linux; amd64

```console
$ docker pull backdrop@sha256:c58205e30945b86a12a1460b40017326c395e64ad61e87210e020e938a5f01aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192042220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd5d366645eecb401cfe54e5a641fb6178e79837d8918fa59e331aeed53a8ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:29 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:16 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:30:16 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:16 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:30:16 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:21:31 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:22:20 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:22:22 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:22:22 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:22:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:22:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47515a93ea45e878cc8ab0a17b4df23603ed521df59ef429ea76d9d969ce4c2c`  
		Last Modified: Mon, 29 Dec 2025 23:27:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111e5a75e258f688ff3b3a5d78f93045efe98ca50aa2cfa3935f71cc63d1d16`  
		Last Modified: Mon, 29 Dec 2025 23:27:09 GMT  
		Size: 117.8 MB (117838476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c344d7f71bac1aa994dc888ff0876329395f7211c6b02317224dd83e9a693bc6`  
		Last Modified: Mon, 29 Dec 2025 23:27:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99084f3266494a7e4251a1b1288fd791baac5ee5c5d1a07ce09caa4cf9955f`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 4.2 MB (4224525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45efbdfda9a10f66d5a08831569fe53b22697c033e6b4e8cbb4084ae1cf9886c`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b60e2efcf2ee842c32160f8a17fa909c3c3470fc325fada8ef9aa3daff0b65`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f273184712e3aea46a1df9831b503b783d2cd165c746374b711b410bb15468`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 12.8 MB (12768868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd80ddb7da11f1d2de701166f05a3f7fa25eae36ba3ee2ab8ca8f54202e9823`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1b57b51bd9510ed010d29c861f8b74aecb5198d41f31460b96e510bfe227d`  
		Last Modified: Mon, 29 Dec 2025 23:30:37 GMT  
		Size: 11.7 MB (11713536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b27bc2d2f055a08bf2cb4302c87df3288be2b1beca62da6df29c00a73a513`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffefb09c5065e7a6e9721e8e1c5f1af8aa9841e020f4e1a0929faf3f96cb4732`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938502cdfcaa95d41e2b3375ac076198b875eec417e4cf6f9fedb722ea35c540`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a911e04a3f68e07dac575e590f6daec31c7c81e5aedd02b2a2e07952c4df102`  
		Last Modified: Mon, 29 Dec 2025 23:30:36 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5dd6c4c4d708d3c98a4a4f53450c4fe9b681cda2f95e895ff5e7ae20e51c0e`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68ce049874ea8751731d3b0218e516a7c19349b770e1178b8ebcac26c7ed9`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 6.5 MB (6542240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6d1147315dcb31f909c5ab594a6c55d6a762a1d4770a4afffc357a62bd6af8`  
		Last Modified: Tue, 30 Dec 2025 01:22:41 GMT  
		Size: 9.2 MB (9171004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8d8bc89794f65939d095422acd34cc8ad0f62b6ed78b707984245941793ee`  
		Last Modified: Tue, 30 Dec 2025 01:22:40 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:eb13aa13033e4b13a091638f00070b50203e67063e3cbd8f53f0be658d2573c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576eb980f906ebb99faa6d2500b6707a50a7580e4edf293fe58432bd2b0cdf59`

```dockerfile
```

-	Layers:
	-	`sha256:db68075e61d06919fa2b099a5f343d1ea26794d6cd2ceae2e6d429f8490b16da`  
		Last Modified: Tue, 30 Dec 2025 04:26:36 GMT  
		Size: 7.5 MB (7461430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2139b00358316c35033f96d074ab07ef8fc9f9749c4ecd2d3806ddbca21e665d`  
		Last Modified: Tue, 30 Dec 2025 04:26:37 GMT  
		Size: 30.6 KB (30557 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:latest` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:b2fb9cbba5711b64d22c589e9de36b016faf590adf0ce7ad0d559b530911b447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185442935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e356653cd96c21080c21ee2e8ac8460e6b1d49207ecb8fa8dac496678d02f23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:23:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:23:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:23:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:57 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:31:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:31:56 GMT
STOPSIGNAL SIGWINCH
# Mon, 29 Dec 2025 23:31:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:31:56 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:31:56 GMT
EXPOSE map[80/tcp:{}]
# Mon, 29 Dec 2025 23:31:56 GMT
CMD ["apache2-foreground"]
# Tue, 30 Dec 2025 01:23:48 GMT
RUN a2enmod rewrite # buildkit
# Tue, 30 Dec 2025 01:24:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Tue, 30 Dec 2025 01:24:57 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_VERSION=1.32.1
# Tue, 30 Dec 2025 01:24:58 GMT
ENV BACKDROP_MD5=75a8854a67c2602c93db633905c08e28
# Tue, 30 Dec 2025 01:24:58 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/refs/tags/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz   && echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c -   && tar -xz --strip-components=1 -f backdrop.tar.gz   && rm backdrop.tar.gz   && chown -R www-data:www-data sites files # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 01:24:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db1bce867eb8aa657139968cd725329c9f00bf30f61dca6d0dda3eafe20ea09`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524a7c309e4ba85237b8aff8aaa1330e5d2ab11ace49759817f2902c2a015a`  
		Last Modified: Mon, 29 Dec 2025 23:27:45 GMT  
		Size: 110.2 MB (110162756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e7af17f2cbb080bd992abbd1d36484e1cd483f495e4638831f1726e0c8857d`  
		Last Modified: Mon, 29 Dec 2025 23:27:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cef929bdea7a541e0645399797bbc305f53075368833e9c9f3eb9531917c2`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 4.3 MB (4302265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add364dde4161a2045b27075b034ad689a76bd21375bb6cdaefa9bbac61b6e5b`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a52d993f79581f5b7452d9789692f14765f08bfb49542383affa0044a026cff`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca2a87d014ad8f1f2d6b3fd03850eaf2f5d15add3363be3692661f191c28eb`  
		Last Modified: Mon, 29 Dec 2025 23:32:18 GMT  
		Size: 12.8 MB (12768460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1636a6843be8fc74f96313af26afaef785e5371ad1b5814a607c448940eb72f0`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeef8fddc40280678cfe32900dc7f71f8db7720e6a2e943ce11e3f75a5417fb`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 11.7 MB (11732497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e32122f144a0407610cb1dc2c7803912e1f86ce685ad2f7b607f9c9cfe62ed`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c430a819f978ac04a6fc3a9e087dc473597f9fc62a19e2ec62ea654bf88920`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6a752357ea399420bf52c2e2aaf694ba9f6698d6d0e74a70df52cacd56099`  
		Last Modified: Mon, 29 Dec 2025 23:32:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8137781ce1cbf99bc2a06e6a0c8407f5dbf6e8a957ff0342bf87e76b4dd7718`  
		Last Modified: Mon, 29 Dec 2025 23:32:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65170970d0193092b2ce308531e732b32ab695adcc388b21da3a0739ed0f0582`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ed339fc4b6e78cc8f668eac5f61c3d78944f9f103744e31c0367cc5d6c7af7`  
		Last Modified: Tue, 30 Dec 2025 01:25:19 GMT  
		Size: 7.2 MB (7160289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cbf59a4321da54e01171158d4071a8d22c8caac275793ca7857aaddd96c5b`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 9.2 MB (9170999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e40d59cb6108148cfc25fe1bd67148eb5420321a5ff1df4b737c0b3805895ce`  
		Last Modified: Tue, 30 Dec 2025 01:25:18 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:latest` - unknown; unknown

```console
$ docker pull backdrop@sha256:d2184feba8507bb54fa96e49d81c4e3b54aec5bd79a4d186ae95713a2bbf45e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7589550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d8166757b66949f93b96d19c83b78288a766a743d47a321e67f5c7f5d10f5b`

```dockerfile
```

-	Layers:
	-	`sha256:d8eeb595880e2ec7db206ca08e2011a4ca7b35a41c972d5ce1eb8292bfe0eafa`  
		Last Modified: Tue, 30 Dec 2025 04:26:43 GMT  
		Size: 7.6 MB (7558810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a35eee997df73bf64bd7cead3467d92b888e4355e59b5e8bd9a923bf618b82c`  
		Last Modified: Tue, 30 Dec 2025 04:26:44 GMT  
		Size: 30.7 KB (30740 bytes)  
		MIME: application/vnd.in-toto+json
