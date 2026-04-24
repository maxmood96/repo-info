<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `matomo`

-	[`matomo:5`](#matomo5)
-	[`matomo:5-apache`](#matomo5-apache)
-	[`matomo:5-fpm`](#matomo5-fpm)
-	[`matomo:5-fpm-alpine`](#matomo5-fpm-alpine)
-	[`matomo:5.9`](#matomo59)
-	[`matomo:5.9-apache`](#matomo59-apache)
-	[`matomo:5.9-fpm`](#matomo59-fpm)
-	[`matomo:5.9-fpm-alpine`](#matomo59-fpm-alpine)
-	[`matomo:5.9.0`](#matomo590)
-	[`matomo:5.9.0-apache`](#matomo590-apache)
-	[`matomo:5.9.0-fpm`](#matomo590-fpm)
-	[`matomo:5.9.0-fpm-alpine`](#matomo590-fpm-alpine)
-	[`matomo:apache`](#matomoapache)
-	[`matomo:fpm`](#matomofpm)
-	[`matomo:fpm-alpine`](#matomofpm-alpine)
-	[`matomo:latest`](#matomolatest)

## `matomo:5`

```console
$ docker pull matomo@sha256:d6daf1cd148fdc8b4b896b2f5bd8fa10ba99c0fcf464fc86c00fe352f8ca5adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:5` - linux; amd64

```console
$ docker pull matomo@sha256:12c152741a75162431fe589dc58010ba84e2bec65c4ecc70143d55c4e2553737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204385414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02018cb5db2c814c3cd9fb610752f770bacf3b0380c02a5e210026b6095a0ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:24:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:56 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:52:44 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:52:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:52:55 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:52:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023baa873c0991ddaa7419301cf610d5e56ceb38356f1845ae0e94eb05dc3c9`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574faee95b5376fc2f0f3f093a9e6780a97d7eedc2da840e55380b1d36f85a89`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 117.8 MB (117843202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa6ce5874bc20b89543cd80d41f58507e071af1977b4fc38fe6a13ca83fdeb`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcafbe281a6757cd10d2aea9b90f3636b474dd2516c0980d602df86c6d4781b`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 4.2 MB (4226905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c19f6aeb84e92127e2e3d01ae0c2404b696e34500cff3e1730ca85603f24ae`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed48780967058ba90258dfa165a33a65ef90d6260c78464947bb8732c2091f`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a3c22f89f33eacca27643c304fbf4cdced1a494513ba0684cd5faf51ff50a`  
		Last Modified: Wed, 22 Apr 2026 01:28:20 GMT  
		Size: 13.9 MB (13852567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7e42314878fa75790cd20ec64c41553110fe17f16b9c26967a225173a8acf`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c72387956fde81883201db10160d5778cbc5b4846c394578385ffadd64ade`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 13.6 MB (13557477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae044dcde24485109733a3bc78f06686efea05cd32c03f0c38c68e2f825a8b00`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de552cfaae1b01c9edff1ddfa947b594abc5c5cd7e5935083ef66faf36a2e64`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a166fb5f1996a6802829599fa567e0f5051d57568f2922b032eb0402fe03cdff`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aafaa0f9a2d4557c2e9c1f953def4005d036064e46b0d8226bd8aa3047f10c`  
		Last Modified: Wed, 22 Apr 2026 01:28:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456ddb90857497cb87ca412dfc2f926ab21071759cf8fcb9a903fc7f38bc1f`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 2.7 MB (2717845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc0226b1100105f4d89cdf4bcf367da0f16e6606031f8f1c2a01494a8ef71cc`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906f8621388502a1c2fafadad71dfc4f8e6a79c0f3968c5e19ac3e3ff9914f6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 22.4 MB (22400019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eed11ba24da6d3ddc5fba318e47ac47c9eace9fba0f69c65f1ec68d9db43a04`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09df151f9988ce5a0c814ce4e9d8c3b6ba17c2f3552077dc6cd497b584327c6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:bb49764520a93d3fadb85fe316c6c91c38b0d19b7f270bf74188a81e1f457a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ffd650e6dd4076605c2b6b683b5cc5faab13fcbf9150d7b757ca61fbabb1b5`

```dockerfile
```

-	Layers:
	-	`sha256:80bec4086b4c60d81e45a4f6d2bdde09f55a31b64da8d3f8a8b0226929bebd68`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 37.5 KB (37471 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; arm variant v5

```console
$ docker pull matomo@sha256:b3f79e04d9b94de7b50b88dfdfbfa132845da9c7c6e4a96372f00c2265f912b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096adafe94dbb74320d05d940b1a9e5ec6f5eac8667ff3392a8eb6b57d13d6e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:27:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:28:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:28:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:31:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:31:37 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 03:41:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 03:41:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 03:42:05 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 03:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 03:42:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab8cd142c874a4a2116214700713c2dec92f9352b96761c33107037fb9f0d57`  
		Last Modified: Wed, 22 Apr 2026 01:31:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd9fa364a1786b392bac2e6ddd6745d7ce20e23d3d55e5dea7f9550e1299d7`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 94.9 MB (94884502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2affe866774915b1ac9a46a4e1ac18de29da227b2d5a68bcfd8c3c538e7b7d6`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80b088c9aeb209cf831aef8b763b0ec951fff041e9f33eb8457a075d2631ccb`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 4.1 MB (4089308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d32ed0510893abbd91f5e84dca0a9241e463b74e591f0100df6bb9c725623`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c8c0d10e5b9e10c1dd295649dd23ec4b53c92bca9182c071138a5e19d42d9`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a080db7c5dc718990269dc0f1f41e1ff18d27fefe892e5d28132340c72c9`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 13.8 MB (13849980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1c211cec5c80e05741841fad4f75d84ce5ae2e3f18171df44c774b5de93330`  
		Last Modified: Wed, 22 Apr 2026 01:31:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729daea6a9d1fe569b7a314fda12a22849a3e8fca3f0f6258dfe0b5d8222098d`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 12.2 MB (12206143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378076dd33dadd4c5e3699bb5f0d22530b9631762f33e38ace0f9ced22b890ed`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2380879c990070fe22833595bddb7e02c9b0ee05c886afd7343a6a0f1eff2a`  
		Last Modified: Wed, 22 Apr 2026 01:32:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff707614457b67b0eb77d55973fc3d28054243f45091bf9d0997d370f60df5d4`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5655cb2fd9ecf9b2f590ce94143aaf2a2b527fbe2489f5b3780216e7ae9c24`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d7df617229c5cc1a9a119d1a416cc5a5ca4690a3c1f5b28eac6de4189d1020`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 2.5 MB (2540941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d80a4659a3571e68d354a2656794a7e7d82c6666ee8425b2d70e39489f2daa`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76978f69025491f93184f38ba37d08d7cb833167a5867ab287ba88542f00f547`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 22.4 MB (22397964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7764c5d0265720d63f293ae158d0e6d6b9d2ed1f8910051b1cdc7570adcd7d5a`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f8c981c39ae50f561ff131ba6812c46579b2eb0d1a7a9c731f9d5e4393c726`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:f99d9eb764a1c4bfab790795df645bba9b3938d285255f316807dafee16d4168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332b81849e2103dd20bc7855d23d32a991eafa638521b6b03e7ddfe0fe94964`

```dockerfile
```

-	Layers:
	-	`sha256:e48f117027110118d1c39af8234e7fbd20682416aed9f39c73e1a3690b46eef5`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; arm variant v7

```console
$ docker pull matomo@sha256:704ea7b9198d0ea68b00d8502802cf9d8bdf423cba5ad6c46382d1a9ad4b5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166515903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dfa22ddd64577d28b1e403be4579b1a089eda6ccfe933ac6c43d305499cc32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:29:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:29:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:29:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:29:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:32:53 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:32:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:32:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:32:53 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:00:33 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:00:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:00:45 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:00:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:00:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5106b06fd3c072093bded94807949d02b5d151d8aa469eeb46a006453a7965c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355c944c4093dc300ebcdafb3bda8a6c9ec4d565280f4214da78dcb5c72d8e8`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 86.2 MB (86247520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a3ee64c140bf6e6df68932390ad89442245fc71e2957dffcd5fd91b5d25c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8490fa290792bd4ae1508b2e69453cf84b93a093779bd2af997a7ac80f5e85`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 3.8 MB (3757190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a76912f0330b5a8e70a8fe111b069c3d44062696c997577bb47dd4a4b8b525`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ef1f39e2cbd10d3c21fd5b455d521b8f52edac13cb84361830d0401e056cac`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efef0f29c620f3102b1cb37a57abdb740e18afa37345163f546b45b7e315db3`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 13.9 MB (13850104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178f3b58b928248d5313cea7c2af0b1191a4134e5a2ea89dcefbeee3867e9558`  
		Last Modified: Wed, 22 Apr 2026 01:33:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701abf00c86fb9ba5d35d547ea7424a7005a7054ac5a6a99ac57e7f7b0bfa52`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 11.6 MB (11617459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1893df0361b2d097c967eb96fb1a8ed66537461ffa47cfaacbd00525053417`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9137d5f6e1867a22561c5d4852fe69d4d5871d641401476fa35959cefd60b9`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344333c00c42b7386ac635f2edc6f7eea53ca2fa38185bcfb85c9c47cfccd2f0`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d097e3f5dc408f7a2ec0f1811eeef125ae55df101558b0b59f1472f8ccfaa7`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd7af921602983bbb84f849980faeae03206451c48016c267efac138fb85d2e`  
		Last Modified: Wed, 22 Apr 2026 04:00:53 GMT  
		Size: 2.4 MB (2423407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd46eaa7f0b8afc693ebc9ac147abaa96e690a6a2fcda89c5adeed6b99dd674`  
		Last Modified: Wed, 22 Apr 2026 04:00:59 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192108aa8a7e7c0156e5d9c86e0ff96c4653ac3d439d341f16057d7e7ee8d02`  
		Last Modified: Wed, 22 Apr 2026 04:01:00 GMT  
		Size: 22.4 MB (22398176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaa66c3db7078e11ce7a6b35effa084a27f2cd317004b643e0d8f5db9d6d83a`  
		Last Modified: Wed, 22 Apr 2026 04:00:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0b8da69cc5561177aed4321e855591775749dcd99c365d47d899fdf5b59370`  
		Last Modified: Wed, 22 Apr 2026 04:00:57 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:2c46c268c61a1ecd5dee08fd6d61ba7cbfd21f3b433de455979424cb92e71042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96950acdfa31d5d16bc845cf7ce279205260039bfb15d82725e61367e7d3fd48`

```dockerfile
```

-	Layers:
	-	`sha256:ffe614280a9b04b1c586f7c9faeb6c8b6c9372de7ad4b4e512fac579471a7ef2`  
		Last Modified: Wed, 22 Apr 2026 04:00:52 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:ab2dcb212c07347abe77449f11cad81b22120cf0dc07e197d68270ade1dba465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196769775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14945bc3708b1df92ba2b2f5fbc29866180f097e40b3ae2491f7aa51b25089a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:15:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:24:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:46 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:46 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 02:41:00 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 02:41:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 02:41:11 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 02:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:41:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e7361c4edf16eb4272307ea2ee57447cf2ec134af0f0326596d3c94a90d7c`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391fd317e2422a2b998a5b8f46476782dda67b0195c064eccf5d895e482ad1b`  
		Last Modified: Wed, 22 Apr 2026 01:19:38 GMT  
		Size: 110.2 MB (110165312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18568485fa5a6e44bf015471b704446b95da6eba7e85f8f6cac1dc351aba16c5`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc61f4154b4e36f9f3303c2b5d7cc39748b46c166e3b463351a9e8cd220f168`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 4.3 MB (4305491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc86735d128f1fbd8106cc32d6afae7a900147daa337150c4739d4f1da4346a`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5795b9e26f314196881b133a91769e53e2828131d098f8db7d9a800b3e89e`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502f96df57cbf4d7939c397fd68491b3e4dc7ff372c63a924fa619428d5ce55`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.9 MB (13852179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c671d94ce0c6c5a51de7fc69370d23707fb0718409f951b587be6798c77cdb`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325d25ee42064c543212ea6c19bbac76a85d4adc1cf6dfcd77fcbd4fe2382b1`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.2 MB (13206146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b47d3caf75cacc27de055e12f70c9488af4a77ec463a8a8803aea30d969715`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab2816bd1e826aae48479663d523550acd969be5b93285569dd982e03a671af`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0f0dbec67a1da7c28e365dadc3da7041014b5b9baf54c270e51e230514fa8`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e7217b1331d5942ccaacf9df0f007a688d6cc47181ba879aa1f856ac11fcc`  
		Last Modified: Wed, 22 Apr 2026 01:27:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa4922aa898ed8d63dca36bc92280eb42fe3d79eb890ddbb2259d0d6f5e41c`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 2.7 MB (2689943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f80fc04bf2842b7907c34cc355b9fbf3a8bf4c940f016885d0c1ac2289bea5`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c238b3cab631145cb2c7fd748f13647a154c52bd26f015e00814d91d30229bf`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 22.4 MB (22399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933121251f2ea8358e789aba4823d58ed5e7d70fccfab2b7639e3a1c51299521`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f08ca589b4bae468116a8f6db8123fa341908d69ef11acf6ae82b48772355a`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:863bad92be9713ba8bcb7beb234be02780085f33286f8e8084008465d3d017e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a11b51a0968c2cf96156db8040090822cc3639a9958977f3d751d1729e91825`

```dockerfile
```

-	Layers:
	-	`sha256:1416c764e4d00d79fc909cbe75de1ee64470178596ed648380f6ea85b2359296`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 37.7 KB (37654 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; 386

```console
$ docker pull matomo@sha256:1c1309fcf70db7d5aada1313f718e3e18653afdc5ff156e0a617eaf48a950ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204710405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1045868eb2c98cf46a416f775849eb27fb25286f9b71a40d65c7023392d62074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:34 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:25:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:25:34 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 05:10:32 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 05:10:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 05:10:43 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 05:10:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:10:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ad892368f928cf2c1259fdac7b49dec39b5e0100dc38505086d1f04fb0223`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a854b9375cf76c04d007410d1b4f9960253c91e039f3fcb12bd3c7da649d1`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 116.1 MB (116144340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b221c038be8eef2d78c984f7ad0d2dc0453d8cdf3bfc51ad75822776b02c5`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea166db99c0aa8459ec40867c9181d68e865592724270ab960b87a59316cef`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 4.5 MB (4458361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ff3928a5ae8b1b558eef86bacf78c1a2d3acee46fe57fbd521c584e8e925`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4831e8917f639e8f5338c7edb49dc14aa2d40befe0ab2492f12791411ce60c42`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ba05e513a80b82c62a1f5983b0933fbd3dfee5e689cea629457ebedbb230`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 13.9 MB (13851522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab312dab66ebf333df3271b5f453521908be468732a06d8501f0c05010dcbb`  
		Last Modified: Wed, 22 Apr 2026 01:25:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a251efd274db5d34c0539ddf36b203537156fff65d0dd99d6206eb755da`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 13.9 MB (13858390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c38f71c21793b514dafb1af49df5345e3a36057bd995386b1721dad70ae5c1`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e3ac463e003ef2a90ed29684c1fec4adb899f721d8ca37df7bdc97f93e810`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abb31896c1032bcf7ef68bd4c309fec9e010b234c4f1ce7bf73c77d7e652cc4`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2e5cc369f5d824ad4e235d2ad3a85a02ecec99498753828309af3d8497942d`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe74de20b0aed283f8dfacadd066c1b866e7e713365c92add76f3eb93a3142f`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 2.7 MB (2695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f70249788be758fa0c374f2201e7ddd74a626cec88d83d55f7f3dbc5336329`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecb4969fd8c7e45f3b01fe4f7674cdf2a81ddcbab2fcd06f95732737d687a0`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 22.4 MB (22399199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6baa5a4e1ac6e37fe0663c2a16a7460de7d4da7e2d9ca774be8bf8f24ab90e`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4d6c98ecf0f190733724883fa2dcfd119ddf57870ea4a110d054bb067bd05`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:07afcb4a3f8ef2f649b1062a2d05b6c9edd68ca33220ab0afe16dd6c1159a6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305e68ddb09754704bb1eedd924f9f348dc2105efd8751945e851f3cd7c15b50`

```dockerfile
```

-	Layers:
	-	`sha256:76a872aab9742b54def28f8f9f09f139870219db07eafec324889e38707ff6a9`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 37.4 KB (37416 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; ppc64le

```console
$ docker pull matomo@sha256:558b509b6c438846c89e60d7ffddafa641cd764bec4f6cfd5f0afeba31d71466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201268007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b0a0f46052ab0d0d7faa5e005cd429839904c722c8e11194972de9c7108608`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:55:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:55:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:24:29 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 02:24:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:30 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:24:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 02:24:30 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 10:55:21 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 10:55:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 10:55:44 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 10:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 10:55:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab63631568fe36922db06d590c893408dd270fd36872c90416de60627387ddce`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 4.9 MB (4881692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438bcf1abed6360e9adac08f804567924b049146c3294914aa102a3f7c41821`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e295926cdc5af3d791955667e4175ebedf05ec97080bd65bd6d11dabf8992`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286ae5221aff2ed1a4a8a4baf4172ad032a7bc332f63f890612205f59604724d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 13.9 MB (13851763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67505e93e2a17315b3576e01845784735fd7612b2eba5ee18fb5e1825fc5a4ec`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c411040503656e63e555235609eca014c8a578020fd6fde25775feb51770f`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 14.0 MB (13956005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d038fd0dacac84a920cc05f508ee5bb0e0c9d08d1a72f3d96e5f75fe524595`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce972e1f08c44df934bf2f5a50d413fa96defc3a3e5af20f6031c30f82275300`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c414f8be1c63ac3c42a432d3030e7c783159d103fd4e5ea6b8df58e8ddfab0d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be4ec9fb48b51715a67384041424d5e3e0e3468e2d9182dc45ad510e144a87`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e884c3d1fa913f34c366a6fc98547d1ecb5b9a27bb1240460902988fc3b0e011`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 3.0 MB (2974034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e2227d7fb70d54ba4b77dcde32ed88eaa5c3f8f8dfbf1cd1ae8b0b99ad878`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dbd12cbf47f04953f09756fbf5445ccad7f5ef3bd747b030e6665e3a5338b8`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 22.4 MB (22399966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8bf5242f2944c1380e67fdc6dc45d28378163497c60bb8cd85b2e5b755313`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19871154c75f6f17ec259370a7742b4dccce1bb26d6fd0c5c1c80710563430`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:d9af1012a7106008ad18566e1e554936ff4d4f022d85bdcfa51a76b580738c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97b8ae50ab4be24e976ede726bf8780e1f869f862f8280567dd5fb333468e07`

```dockerfile
```

-	Layers:
	-	`sha256:c3509d9b911e4d1b3ec37730332352101ca474bd7ff9f59709e048ba9e1376f7`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; riscv64

```console
$ docker pull matomo@sha256:1b1374d4bf1624ec39522f6940af9e6b78bfd5f869278ffeb9e6c4bf0b4cb928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233788266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a814b40196d1c72ad00aafed53c670ab9aae9c4d1c996b9814241f18e6086`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 11:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 11:52:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 11:52:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 16:36:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 16:36:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 17:30:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 17:30:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 17:30:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:53 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 17:30:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 17:30:53 GMT
CMD ["apache2-foreground"]
# Sun, 12 Apr 2026 13:02:30 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sun, 12 Apr 2026 13:02:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
ENV MATOMO_VERSION=5.8.0
# Sun, 12 Apr 2026 13:03:52 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 13:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 12 Apr 2026 13:03:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1748d653b8c3ed98b870438732aa56def2ef4f267a38a228a8d4e1a775744da`  
		Last Modified: Tue, 07 Apr 2026 12:53:25 GMT  
		Size: 4.0 MB (4031244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79c952e0710b8d660c2b70f3e9f2716a16833b628e3b2dd090af31c1cf7438`  
		Last Modified: Tue, 07 Apr 2026 12:53:24 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe6480453dd1cec4db695c1e657272ce31a8c86abec42383da6aa9846d7dc4`  
		Last Modified: Tue, 07 Apr 2026 12:53:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dacce83cf82615cd1d4a6c1a86cea6e40883d3a42ad8656c9b8763530155814`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 13.9 MB (13866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3323b96cffff08af8f445b80f611ebe68799371d01077775a0c3f4567380bd`  
		Last Modified: Fri, 10 Apr 2026 17:34:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e4e9e187467f7ffbcfe1cdf4d10ee90f6ee36da3b522274275365cc718ee0`  
		Last Modified: Fri, 10 Apr 2026 17:34:06 GMT  
		Size: 16.0 MB (16013910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb761f6a2a209495608bb857bb80d3d0d0aa4de2fb075e52945a24da89addada`  
		Last Modified: Fri, 10 Apr 2026 17:34:01 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ced9f37602f905311a1e2a29a005c079a57757cdbf7e7fb075022b1a0f660b`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494a5659332e0f15ed2f4d61e062b27c51744e0fa85863035bb125c624a2ad0`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6cee257162c3d59f0cd7d2be13c20ecd7f6bf71c712eecacc44cc33a5fec83`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c54731eefd24f5be8c3be0e167304e36cc69b70462507d80ccee20c97285125`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 2.6 MB (2614022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93170443e6c9159fcbd88f4c341eeeea304875579d3f0a96e2d394517a45ab0c`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72489f0fe05b81788af39c9e702ce18d653102a5f9d70840781a6456c6da216f`  
		Last Modified: Sun, 12 Apr 2026 13:05:15 GMT  
		Size: 22.4 MB (22400287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29582f6aa97de83cc2e3b1070f8e16811e430db99830c4548ff4151cef5d682e`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae08e7812254f8597aa1f47af714fb516cac8f33972c277e72c29956b6ef64`  
		Last Modified: Sun, 12 Apr 2026 13:05:12 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:044fd16450e94817d1f1ebc47d8b8d9709562399d3f06bd84151c253155e6ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8cbd64c659d77d407cb66fe3189531945fc5fe28c9849fa3a4e57c61cada0`

```dockerfile
```

-	Layers:
	-	`sha256:791843956f9e2428ebb0d78e1b2c97d5ddb76f0011b84c41f30227973e1d00db`  
		Last Modified: Sun, 12 Apr 2026 13:05:10 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5` - linux; s390x

```console
$ docker pull matomo@sha256:6cf85e049fc320cd8aec35cc44d082d802da2c38536f6bbdd501de2103e81c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179059874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995327f35af3666a70c2b8f73cbabc6e04075ad4e578d7161973c87c00ca4aa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:39 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:37:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:37:39 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:41:27 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:41:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:41:38 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:41:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ece9a9560b771b29f91d1b2fa69377a7a6998382890ab15dc4a92ce806048b`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ccbb849cf7d524fb26003a40a6f2ddbd73713723d4bf57178fec331c8472df`  
		Last Modified: Wed, 22 Apr 2026 01:27:55 GMT  
		Size: 92.6 MB (92573082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdb404da573a86ead75a2c55d7c0f8bd69a0480a6e1e9d1e17b114c37703861`  
		Last Modified: Wed, 22 Apr 2026 01:27:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7964dc0539da49b7d15124dd7f7170a7706b36795438d37e1b510fef67d922`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 4.3 MB (4329303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d928c48d6c321d2eeb66c3c389766cf9ae0d3b52927919a0fb9928aa3790f1`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cc4503afd2ec97db21c3221acd45b9429c93ad112050f26555547d7899269`  
		Last Modified: Wed, 22 Apr 2026 01:27:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ccf2ac717c82b15002dd84ef1d42b8130bd9336b5ee96c48db314d863c1a`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 13.9 MB (13850951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d18571a8b1fd3a48f17e0ed57746721b5633a3d9d6fa17bea75e647e5dadb2`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af7cd74da0af1e5075282c2cb414e4d83acaeeb6bd637c46acbf94b5414eaa`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 13.3 MB (13311877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d5c986b0140b3c1c0aadeb97c7c15b48faacd44db4831ea9d0d2fffab85e97`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd187c896be49dc43ba8e03a8e69c5e53fe53aec2711d75d512f702105a9e6`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1dcabe41bbe8315743a1f135c7e213230ec4c4802210eac62355753a21234`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f3b59bcfa40537a6d7da3db395965ad05e8bb13ba9c58d1bd555b7be4cdcd0`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12d807e0e3c374569c0b1e1b7e34053e827157eb1bdaf0a8d4352ed9566c33`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 2.7 MB (2748316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bcd04f47c821ef46e5f55b5e15f7b9ab6e8255eda8e16a77b1c0651c988eb0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3591996980aec43931f2cfd37dc3c0d7757b9e8252e4c9da2ac3ee6f7ac5da`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 22.4 MB (22398820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93afd3e6d8bb757c222e5ddb8be065f77013e9147fd82999457b98952f458bd0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d977a5ee6fe1cdfefa7fd25d7e089a23e5adc1380e201464878e0cc3358b254`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5` - unknown; unknown

```console
$ docker pull matomo@sha256:35e05b0967102445629beffe14fdb57e770914fa2607f0247303bcb44928be5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aee6ace1d2419bac32bedf90aece37b63bb8077a84f38e86eea3c24580010b`

```dockerfile
```

-	Layers:
	-	`sha256:bf0616b74b590e9ac3532d9d0e1826d70f42f64c7bdf51345482ea2dabca15b7`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 37.5 KB (37466 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:5-apache`

```console
$ docker pull matomo@sha256:d6daf1cd148fdc8b4b896b2f5bd8fa10ba99c0fcf464fc86c00fe352f8ca5adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:5-apache` - linux; amd64

```console
$ docker pull matomo@sha256:12c152741a75162431fe589dc58010ba84e2bec65c4ecc70143d55c4e2553737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204385414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02018cb5db2c814c3cd9fb610752f770bacf3b0380c02a5e210026b6095a0ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:24:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:56 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:52:44 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:52:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:52:55 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:52:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023baa873c0991ddaa7419301cf610d5e56ceb38356f1845ae0e94eb05dc3c9`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574faee95b5376fc2f0f3f093a9e6780a97d7eedc2da840e55380b1d36f85a89`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 117.8 MB (117843202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa6ce5874bc20b89543cd80d41f58507e071af1977b4fc38fe6a13ca83fdeb`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcafbe281a6757cd10d2aea9b90f3636b474dd2516c0980d602df86c6d4781b`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 4.2 MB (4226905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c19f6aeb84e92127e2e3d01ae0c2404b696e34500cff3e1730ca85603f24ae`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed48780967058ba90258dfa165a33a65ef90d6260c78464947bb8732c2091f`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a3c22f89f33eacca27643c304fbf4cdced1a494513ba0684cd5faf51ff50a`  
		Last Modified: Wed, 22 Apr 2026 01:28:20 GMT  
		Size: 13.9 MB (13852567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7e42314878fa75790cd20ec64c41553110fe17f16b9c26967a225173a8acf`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c72387956fde81883201db10160d5778cbc5b4846c394578385ffadd64ade`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 13.6 MB (13557477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae044dcde24485109733a3bc78f06686efea05cd32c03f0c38c68e2f825a8b00`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de552cfaae1b01c9edff1ddfa947b594abc5c5cd7e5935083ef66faf36a2e64`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a166fb5f1996a6802829599fa567e0f5051d57568f2922b032eb0402fe03cdff`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aafaa0f9a2d4557c2e9c1f953def4005d036064e46b0d8226bd8aa3047f10c`  
		Last Modified: Wed, 22 Apr 2026 01:28:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456ddb90857497cb87ca412dfc2f926ab21071759cf8fcb9a903fc7f38bc1f`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 2.7 MB (2717845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc0226b1100105f4d89cdf4bcf367da0f16e6606031f8f1c2a01494a8ef71cc`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906f8621388502a1c2fafadad71dfc4f8e6a79c0f3968c5e19ac3e3ff9914f6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 22.4 MB (22400019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eed11ba24da6d3ddc5fba318e47ac47c9eace9fba0f69c65f1ec68d9db43a04`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09df151f9988ce5a0c814ce4e9d8c3b6ba17c2f3552077dc6cd497b584327c6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:bb49764520a93d3fadb85fe316c6c91c38b0d19b7f270bf74188a81e1f457a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ffd650e6dd4076605c2b6b683b5cc5faab13fcbf9150d7b757ca61fbabb1b5`

```dockerfile
```

-	Layers:
	-	`sha256:80bec4086b4c60d81e45a4f6d2bdde09f55a31b64da8d3f8a8b0226929bebd68`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 37.5 KB (37471 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm variant v5

```console
$ docker pull matomo@sha256:b3f79e04d9b94de7b50b88dfdfbfa132845da9c7c6e4a96372f00c2265f912b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096adafe94dbb74320d05d940b1a9e5ec6f5eac8667ff3392a8eb6b57d13d6e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:27:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:28:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:28:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:31:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:31:37 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 03:41:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 03:41:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 03:42:05 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 03:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 03:42:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab8cd142c874a4a2116214700713c2dec92f9352b96761c33107037fb9f0d57`  
		Last Modified: Wed, 22 Apr 2026 01:31:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd9fa364a1786b392bac2e6ddd6745d7ce20e23d3d55e5dea7f9550e1299d7`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 94.9 MB (94884502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2affe866774915b1ac9a46a4e1ac18de29da227b2d5a68bcfd8c3c538e7b7d6`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80b088c9aeb209cf831aef8b763b0ec951fff041e9f33eb8457a075d2631ccb`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 4.1 MB (4089308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d32ed0510893abbd91f5e84dca0a9241e463b74e591f0100df6bb9c725623`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c8c0d10e5b9e10c1dd295649dd23ec4b53c92bca9182c071138a5e19d42d9`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a080db7c5dc718990269dc0f1f41e1ff18d27fefe892e5d28132340c72c9`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 13.8 MB (13849980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1c211cec5c80e05741841fad4f75d84ce5ae2e3f18171df44c774b5de93330`  
		Last Modified: Wed, 22 Apr 2026 01:31:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729daea6a9d1fe569b7a314fda12a22849a3e8fca3f0f6258dfe0b5d8222098d`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 12.2 MB (12206143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378076dd33dadd4c5e3699bb5f0d22530b9631762f33e38ace0f9ced22b890ed`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2380879c990070fe22833595bddb7e02c9b0ee05c886afd7343a6a0f1eff2a`  
		Last Modified: Wed, 22 Apr 2026 01:32:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff707614457b67b0eb77d55973fc3d28054243f45091bf9d0997d370f60df5d4`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5655cb2fd9ecf9b2f590ce94143aaf2a2b527fbe2489f5b3780216e7ae9c24`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d7df617229c5cc1a9a119d1a416cc5a5ca4690a3c1f5b28eac6de4189d1020`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 2.5 MB (2540941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d80a4659a3571e68d354a2656794a7e7d82c6666ee8425b2d70e39489f2daa`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76978f69025491f93184f38ba37d08d7cb833167a5867ab287ba88542f00f547`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 22.4 MB (22397964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7764c5d0265720d63f293ae158d0e6d6b9d2ed1f8910051b1cdc7570adcd7d5a`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f8c981c39ae50f561ff131ba6812c46579b2eb0d1a7a9c731f9d5e4393c726`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:f99d9eb764a1c4bfab790795df645bba9b3938d285255f316807dafee16d4168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332b81849e2103dd20bc7855d23d32a991eafa638521b6b03e7ddfe0fe94964`

```dockerfile
```

-	Layers:
	-	`sha256:e48f117027110118d1c39af8234e7fbd20682416aed9f39c73e1a3690b46eef5`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm variant v7

```console
$ docker pull matomo@sha256:704ea7b9198d0ea68b00d8502802cf9d8bdf423cba5ad6c46382d1a9ad4b5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166515903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dfa22ddd64577d28b1e403be4579b1a089eda6ccfe933ac6c43d305499cc32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:29:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:29:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:29:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:29:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:32:53 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:32:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:32:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:32:53 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:00:33 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:00:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:00:45 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:00:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:00:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5106b06fd3c072093bded94807949d02b5d151d8aa469eeb46a006453a7965c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355c944c4093dc300ebcdafb3bda8a6c9ec4d565280f4214da78dcb5c72d8e8`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 86.2 MB (86247520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a3ee64c140bf6e6df68932390ad89442245fc71e2957dffcd5fd91b5d25c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8490fa290792bd4ae1508b2e69453cf84b93a093779bd2af997a7ac80f5e85`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 3.8 MB (3757190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a76912f0330b5a8e70a8fe111b069c3d44062696c997577bb47dd4a4b8b525`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ef1f39e2cbd10d3c21fd5b455d521b8f52edac13cb84361830d0401e056cac`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efef0f29c620f3102b1cb37a57abdb740e18afa37345163f546b45b7e315db3`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 13.9 MB (13850104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178f3b58b928248d5313cea7c2af0b1191a4134e5a2ea89dcefbeee3867e9558`  
		Last Modified: Wed, 22 Apr 2026 01:33:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701abf00c86fb9ba5d35d547ea7424a7005a7054ac5a6a99ac57e7f7b0bfa52`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 11.6 MB (11617459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1893df0361b2d097c967eb96fb1a8ed66537461ffa47cfaacbd00525053417`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9137d5f6e1867a22561c5d4852fe69d4d5871d641401476fa35959cefd60b9`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344333c00c42b7386ac635f2edc6f7eea53ca2fa38185bcfb85c9c47cfccd2f0`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d097e3f5dc408f7a2ec0f1811eeef125ae55df101558b0b59f1472f8ccfaa7`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd7af921602983bbb84f849980faeae03206451c48016c267efac138fb85d2e`  
		Last Modified: Wed, 22 Apr 2026 04:00:53 GMT  
		Size: 2.4 MB (2423407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd46eaa7f0b8afc693ebc9ac147abaa96e690a6a2fcda89c5adeed6b99dd674`  
		Last Modified: Wed, 22 Apr 2026 04:00:59 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192108aa8a7e7c0156e5d9c86e0ff96c4653ac3d439d341f16057d7e7ee8d02`  
		Last Modified: Wed, 22 Apr 2026 04:01:00 GMT  
		Size: 22.4 MB (22398176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaa66c3db7078e11ce7a6b35effa084a27f2cd317004b643e0d8f5db9d6d83a`  
		Last Modified: Wed, 22 Apr 2026 04:00:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0b8da69cc5561177aed4321e855591775749dcd99c365d47d899fdf5b59370`  
		Last Modified: Wed, 22 Apr 2026 04:00:57 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:2c46c268c61a1ecd5dee08fd6d61ba7cbfd21f3b433de455979424cb92e71042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96950acdfa31d5d16bc845cf7ce279205260039bfb15d82725e61367e7d3fd48`

```dockerfile
```

-	Layers:
	-	`sha256:ffe614280a9b04b1c586f7c9faeb6c8b6c9372de7ad4b4e512fac579471a7ef2`  
		Last Modified: Wed, 22 Apr 2026 04:00:52 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:ab2dcb212c07347abe77449f11cad81b22120cf0dc07e197d68270ade1dba465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196769775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14945bc3708b1df92ba2b2f5fbc29866180f097e40b3ae2491f7aa51b25089a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:15:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:24:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:46 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:46 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 02:41:00 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 02:41:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 02:41:11 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 02:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:41:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e7361c4edf16eb4272307ea2ee57447cf2ec134af0f0326596d3c94a90d7c`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391fd317e2422a2b998a5b8f46476782dda67b0195c064eccf5d895e482ad1b`  
		Last Modified: Wed, 22 Apr 2026 01:19:38 GMT  
		Size: 110.2 MB (110165312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18568485fa5a6e44bf015471b704446b95da6eba7e85f8f6cac1dc351aba16c5`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc61f4154b4e36f9f3303c2b5d7cc39748b46c166e3b463351a9e8cd220f168`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 4.3 MB (4305491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc86735d128f1fbd8106cc32d6afae7a900147daa337150c4739d4f1da4346a`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5795b9e26f314196881b133a91769e53e2828131d098f8db7d9a800b3e89e`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502f96df57cbf4d7939c397fd68491b3e4dc7ff372c63a924fa619428d5ce55`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.9 MB (13852179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c671d94ce0c6c5a51de7fc69370d23707fb0718409f951b587be6798c77cdb`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325d25ee42064c543212ea6c19bbac76a85d4adc1cf6dfcd77fcbd4fe2382b1`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.2 MB (13206146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b47d3caf75cacc27de055e12f70c9488af4a77ec463a8a8803aea30d969715`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab2816bd1e826aae48479663d523550acd969be5b93285569dd982e03a671af`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0f0dbec67a1da7c28e365dadc3da7041014b5b9baf54c270e51e230514fa8`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e7217b1331d5942ccaacf9df0f007a688d6cc47181ba879aa1f856ac11fcc`  
		Last Modified: Wed, 22 Apr 2026 01:27:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa4922aa898ed8d63dca36bc92280eb42fe3d79eb890ddbb2259d0d6f5e41c`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 2.7 MB (2689943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f80fc04bf2842b7907c34cc355b9fbf3a8bf4c940f016885d0c1ac2289bea5`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c238b3cab631145cb2c7fd748f13647a154c52bd26f015e00814d91d30229bf`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 22.4 MB (22399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933121251f2ea8358e789aba4823d58ed5e7d70fccfab2b7639e3a1c51299521`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f08ca589b4bae468116a8f6db8123fa341908d69ef11acf6ae82b48772355a`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:863bad92be9713ba8bcb7beb234be02780085f33286f8e8084008465d3d017e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a11b51a0968c2cf96156db8040090822cc3639a9958977f3d751d1729e91825`

```dockerfile
```

-	Layers:
	-	`sha256:1416c764e4d00d79fc909cbe75de1ee64470178596ed648380f6ea85b2359296`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 37.7 KB (37654 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; 386

```console
$ docker pull matomo@sha256:1c1309fcf70db7d5aada1313f718e3e18653afdc5ff156e0a617eaf48a950ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204710405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1045868eb2c98cf46a416f775849eb27fb25286f9b71a40d65c7023392d62074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:34 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:25:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:25:34 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 05:10:32 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 05:10:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 05:10:43 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 05:10:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:10:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ad892368f928cf2c1259fdac7b49dec39b5e0100dc38505086d1f04fb0223`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a854b9375cf76c04d007410d1b4f9960253c91e039f3fcb12bd3c7da649d1`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 116.1 MB (116144340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b221c038be8eef2d78c984f7ad0d2dc0453d8cdf3bfc51ad75822776b02c5`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea166db99c0aa8459ec40867c9181d68e865592724270ab960b87a59316cef`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 4.5 MB (4458361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ff3928a5ae8b1b558eef86bacf78c1a2d3acee46fe57fbd521c584e8e925`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4831e8917f639e8f5338c7edb49dc14aa2d40befe0ab2492f12791411ce60c42`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ba05e513a80b82c62a1f5983b0933fbd3dfee5e689cea629457ebedbb230`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 13.9 MB (13851522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab312dab66ebf333df3271b5f453521908be468732a06d8501f0c05010dcbb`  
		Last Modified: Wed, 22 Apr 2026 01:25:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a251efd274db5d34c0539ddf36b203537156fff65d0dd99d6206eb755da`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 13.9 MB (13858390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c38f71c21793b514dafb1af49df5345e3a36057bd995386b1721dad70ae5c1`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e3ac463e003ef2a90ed29684c1fec4adb899f721d8ca37df7bdc97f93e810`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abb31896c1032bcf7ef68bd4c309fec9e010b234c4f1ce7bf73c77d7e652cc4`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2e5cc369f5d824ad4e235d2ad3a85a02ecec99498753828309af3d8497942d`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe74de20b0aed283f8dfacadd066c1b866e7e713365c92add76f3eb93a3142f`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 2.7 MB (2695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f70249788be758fa0c374f2201e7ddd74a626cec88d83d55f7f3dbc5336329`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecb4969fd8c7e45f3b01fe4f7674cdf2a81ddcbab2fcd06f95732737d687a0`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 22.4 MB (22399199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6baa5a4e1ac6e37fe0663c2a16a7460de7d4da7e2d9ca774be8bf8f24ab90e`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4d6c98ecf0f190733724883fa2dcfd119ddf57870ea4a110d054bb067bd05`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:07afcb4a3f8ef2f649b1062a2d05b6c9edd68ca33220ab0afe16dd6c1159a6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305e68ddb09754704bb1eedd924f9f348dc2105efd8751945e851f3cd7c15b50`

```dockerfile
```

-	Layers:
	-	`sha256:76a872aab9742b54def28f8f9f09f139870219db07eafec324889e38707ff6a9`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 37.4 KB (37416 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; ppc64le

```console
$ docker pull matomo@sha256:558b509b6c438846c89e60d7ffddafa641cd764bec4f6cfd5f0afeba31d71466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201268007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b0a0f46052ab0d0d7faa5e005cd429839904c722c8e11194972de9c7108608`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:55:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:55:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:24:29 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 02:24:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:30 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:24:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 02:24:30 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 10:55:21 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 10:55:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 10:55:44 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 10:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 10:55:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab63631568fe36922db06d590c893408dd270fd36872c90416de60627387ddce`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 4.9 MB (4881692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438bcf1abed6360e9adac08f804567924b049146c3294914aa102a3f7c41821`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e295926cdc5af3d791955667e4175ebedf05ec97080bd65bd6d11dabf8992`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286ae5221aff2ed1a4a8a4baf4172ad032a7bc332f63f890612205f59604724d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 13.9 MB (13851763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67505e93e2a17315b3576e01845784735fd7612b2eba5ee18fb5e1825fc5a4ec`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c411040503656e63e555235609eca014c8a578020fd6fde25775feb51770f`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 14.0 MB (13956005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d038fd0dacac84a920cc05f508ee5bb0e0c9d08d1a72f3d96e5f75fe524595`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce972e1f08c44df934bf2f5a50d413fa96defc3a3e5af20f6031c30f82275300`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c414f8be1c63ac3c42a432d3030e7c783159d103fd4e5ea6b8df58e8ddfab0d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be4ec9fb48b51715a67384041424d5e3e0e3468e2d9182dc45ad510e144a87`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e884c3d1fa913f34c366a6fc98547d1ecb5b9a27bb1240460902988fc3b0e011`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 3.0 MB (2974034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e2227d7fb70d54ba4b77dcde32ed88eaa5c3f8f8dfbf1cd1ae8b0b99ad878`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dbd12cbf47f04953f09756fbf5445ccad7f5ef3bd747b030e6665e3a5338b8`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 22.4 MB (22399966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8bf5242f2944c1380e67fdc6dc45d28378163497c60bb8cd85b2e5b755313`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19871154c75f6f17ec259370a7742b4dccce1bb26d6fd0c5c1c80710563430`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:d9af1012a7106008ad18566e1e554936ff4d4f022d85bdcfa51a76b580738c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97b8ae50ab4be24e976ede726bf8780e1f869f862f8280567dd5fb333468e07`

```dockerfile
```

-	Layers:
	-	`sha256:c3509d9b911e4d1b3ec37730332352101ca474bd7ff9f59709e048ba9e1376f7`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; riscv64

```console
$ docker pull matomo@sha256:1b1374d4bf1624ec39522f6940af9e6b78bfd5f869278ffeb9e6c4bf0b4cb928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233788266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a814b40196d1c72ad00aafed53c670ab9aae9c4d1c996b9814241f18e6086`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 11:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 11:52:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 11:52:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 16:36:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 16:36:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 17:30:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 17:30:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 17:30:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:53 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 17:30:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 17:30:53 GMT
CMD ["apache2-foreground"]
# Sun, 12 Apr 2026 13:02:30 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sun, 12 Apr 2026 13:02:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
ENV MATOMO_VERSION=5.8.0
# Sun, 12 Apr 2026 13:03:52 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 13:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 12 Apr 2026 13:03:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1748d653b8c3ed98b870438732aa56def2ef4f267a38a228a8d4e1a775744da`  
		Last Modified: Tue, 07 Apr 2026 12:53:25 GMT  
		Size: 4.0 MB (4031244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79c952e0710b8d660c2b70f3e9f2716a16833b628e3b2dd090af31c1cf7438`  
		Last Modified: Tue, 07 Apr 2026 12:53:24 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe6480453dd1cec4db695c1e657272ce31a8c86abec42383da6aa9846d7dc4`  
		Last Modified: Tue, 07 Apr 2026 12:53:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dacce83cf82615cd1d4a6c1a86cea6e40883d3a42ad8656c9b8763530155814`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 13.9 MB (13866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3323b96cffff08af8f445b80f611ebe68799371d01077775a0c3f4567380bd`  
		Last Modified: Fri, 10 Apr 2026 17:34:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e4e9e187467f7ffbcfe1cdf4d10ee90f6ee36da3b522274275365cc718ee0`  
		Last Modified: Fri, 10 Apr 2026 17:34:06 GMT  
		Size: 16.0 MB (16013910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb761f6a2a209495608bb857bb80d3d0d0aa4de2fb075e52945a24da89addada`  
		Last Modified: Fri, 10 Apr 2026 17:34:01 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ced9f37602f905311a1e2a29a005c079a57757cdbf7e7fb075022b1a0f660b`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494a5659332e0f15ed2f4d61e062b27c51744e0fa85863035bb125c624a2ad0`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6cee257162c3d59f0cd7d2be13c20ecd7f6bf71c712eecacc44cc33a5fec83`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c54731eefd24f5be8c3be0e167304e36cc69b70462507d80ccee20c97285125`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 2.6 MB (2614022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93170443e6c9159fcbd88f4c341eeeea304875579d3f0a96e2d394517a45ab0c`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72489f0fe05b81788af39c9e702ce18d653102a5f9d70840781a6456c6da216f`  
		Last Modified: Sun, 12 Apr 2026 13:05:15 GMT  
		Size: 22.4 MB (22400287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29582f6aa97de83cc2e3b1070f8e16811e430db99830c4548ff4151cef5d682e`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae08e7812254f8597aa1f47af714fb516cac8f33972c277e72c29956b6ef64`  
		Last Modified: Sun, 12 Apr 2026 13:05:12 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:044fd16450e94817d1f1ebc47d8b8d9709562399d3f06bd84151c253155e6ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8cbd64c659d77d407cb66fe3189531945fc5fe28c9849fa3a4e57c61cada0`

```dockerfile
```

-	Layers:
	-	`sha256:791843956f9e2428ebb0d78e1b2c97d5ddb76f0011b84c41f30227973e1d00db`  
		Last Modified: Sun, 12 Apr 2026 13:05:10 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-apache` - linux; s390x

```console
$ docker pull matomo@sha256:6cf85e049fc320cd8aec35cc44d082d802da2c38536f6bbdd501de2103e81c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179059874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995327f35af3666a70c2b8f73cbabc6e04075ad4e578d7161973c87c00ca4aa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:39 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:37:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:37:39 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:41:27 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:41:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:41:38 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:41:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ece9a9560b771b29f91d1b2fa69377a7a6998382890ab15dc4a92ce806048b`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ccbb849cf7d524fb26003a40a6f2ddbd73713723d4bf57178fec331c8472df`  
		Last Modified: Wed, 22 Apr 2026 01:27:55 GMT  
		Size: 92.6 MB (92573082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdb404da573a86ead75a2c55d7c0f8bd69a0480a6e1e9d1e17b114c37703861`  
		Last Modified: Wed, 22 Apr 2026 01:27:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7964dc0539da49b7d15124dd7f7170a7706b36795438d37e1b510fef67d922`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 4.3 MB (4329303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d928c48d6c321d2eeb66c3c389766cf9ae0d3b52927919a0fb9928aa3790f1`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cc4503afd2ec97db21c3221acd45b9429c93ad112050f26555547d7899269`  
		Last Modified: Wed, 22 Apr 2026 01:27:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ccf2ac717c82b15002dd84ef1d42b8130bd9336b5ee96c48db314d863c1a`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 13.9 MB (13850951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d18571a8b1fd3a48f17e0ed57746721b5633a3d9d6fa17bea75e647e5dadb2`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af7cd74da0af1e5075282c2cb414e4d83acaeeb6bd637c46acbf94b5414eaa`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 13.3 MB (13311877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d5c986b0140b3c1c0aadeb97c7c15b48faacd44db4831ea9d0d2fffab85e97`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd187c896be49dc43ba8e03a8e69c5e53fe53aec2711d75d512f702105a9e6`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1dcabe41bbe8315743a1f135c7e213230ec4c4802210eac62355753a21234`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f3b59bcfa40537a6d7da3db395965ad05e8bb13ba9c58d1bd555b7be4cdcd0`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12d807e0e3c374569c0b1e1b7e34053e827157eb1bdaf0a8d4352ed9566c33`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 2.7 MB (2748316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bcd04f47c821ef46e5f55b5e15f7b9ab6e8255eda8e16a77b1c0651c988eb0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3591996980aec43931f2cfd37dc3c0d7757b9e8252e4c9da2ac3ee6f7ac5da`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 22.4 MB (22398820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93afd3e6d8bb757c222e5ddb8be065f77013e9147fd82999457b98952f458bd0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d977a5ee6fe1cdfefa7fd25d7e089a23e5adc1380e201464878e0cc3358b254`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-apache` - unknown; unknown

```console
$ docker pull matomo@sha256:35e05b0967102445629beffe14fdb57e770914fa2607f0247303bcb44928be5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aee6ace1d2419bac32bedf90aece37b63bb8077a84f38e86eea3c24580010b`

```dockerfile
```

-	Layers:
	-	`sha256:bf0616b74b590e9ac3532d9d0e1826d70f42f64c7bdf51345482ea2dabca15b7`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 37.5 KB (37466 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:5-fpm`

```console
$ docker pull matomo@sha256:12cca10b57291eeece1b5379e1de7d79a64cd004e721086e23cd74a694cd59ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:5-fpm` - linux; amd64

```console
$ docker pull matomo@sha256:710598e9b5782d7decbbd2b3fc03d429db93489c7272c5457b3b4100f77bd2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200234403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c685b4d923afe384af898efc7b268f9f42ca2b8cc63cee09bb7b4034a4bb5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:28:05 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:28:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:28:05 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:28:05 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:52:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:52:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:52:49 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:52:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:58 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:52:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:52:58 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:52:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:52:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3e427b1d425dd16f39094572ce5dafba4053375f058521058ffe66a8a08c4b`  
		Last Modified: Wed, 22 Apr 2026 01:25:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32fe875c9f9eace2d0f6384ad31d970a8b3af511137e1e8cfc4a3185ccbbc97`  
		Last Modified: Wed, 22 Apr 2026 01:25:30 GMT  
		Size: 117.8 MB (117842644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f934793218e2ce567e18037b6afc9ffbf4e872ce44616bf5d481a5a71cb94ae`  
		Last Modified: Wed, 22 Apr 2026 01:25:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342f4bf50b5034c0f35a87263038654cda7c935ef0277f1c079f515bb4f1f857`  
		Last Modified: Wed, 22 Apr 2026 01:28:16 GMT  
		Size: 13.8 MB (13833818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b3fbcca5d92b01137fc6843512c1474da5212e74888f649c95d50d0f45d8d`  
		Last Modified: Wed, 22 Apr 2026 01:28:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2dd358023fed96e25674a1e5b934d1e3b38a953aaae3d98d31c2774b955a29`  
		Last Modified: Wed, 22 Apr 2026 01:28:15 GMT  
		Size: 13.7 MB (13691364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17da2e8e93dfcebc9ccd0eca5464f06206a170793b4504b77a3febaa3f38716`  
		Last Modified: Wed, 22 Apr 2026 01:28:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e7ed16b284ade9be62b85d67e85b32539006905c05c01c4a3f969ef224ecf`  
		Last Modified: Wed, 22 Apr 2026 01:28:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7122489bbe4d0e843fe308e2a9505ce7149dc3958344f46c0b6acc3d12e056f`  
		Last Modified: Wed, 22 Apr 2026 01:28:16 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a55794049acce36f6ae1a2c2d46d53e84eefada5b0192556bf8c12540bc8cc8`  
		Last Modified: Wed, 22 Apr 2026 01:28:17 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656f0b430fde31ec31f389f29673dd9f4006ae14a0833c32a421f15c1dfe0815`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 2.7 MB (2694911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3248f4a587728bc1b02068f9ac6f9d6354fca35d1737138a6f5e18f6ddd417`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30e27799776718db3672fec967e75dd4f043b9d922b7f45ac8f48e388249897`  
		Last Modified: Wed, 22 Apr 2026 04:53:06 GMT  
		Size: 22.4 MB (22376818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b4b956f172489676a03278be713601c3449126e08c7ef46329bf7a1b679958`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838019e911cce957e670f00152dba0c1957e61bebfaf5fd7d1914edd684f9f25`  
		Last Modified: Wed, 22 Apr 2026 04:53:06 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:ca0a8db5345d7b2dc61be7e21f155dbd36e5d06566e70e21a47d02af766013b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f81feab3ef575dbca3e084f5b7658208ba6851570459bc3e455630461816f99`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c47479e919f704dc152a29ea6fc5257a1fbea1ed57206b4635115e106c052`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 33.2 KB (33247 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; arm variant v5

```console
$ docker pull matomo@sha256:bc735a61c96bed63c6da03c6e1e6ba4af467998e0ed521cd93b8644860c2e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173814214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf32aece57f5e841f58ad8adee9a7cb2195add1e9cdfb49ee1c8988c253cc97d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:20:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:20:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:14 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:31:14 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:31:14 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 03:41:51 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 03:41:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:41:52 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:41:52 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 03:42:08 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:42:08 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 03:42:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 03:42:08 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 03:42:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 03:42:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceb84c9f466573920de66d24a34f2c68c19bcf0a1b2c264f34c332471c69fb9`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d33534dd8e573ebb0c8014512c21ee46f5bdb0a9a8bed6d2c2c4a536a5c0601`  
		Last Modified: Wed, 22 Apr 2026 01:24:12 GMT  
		Size: 94.9 MB (94884496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d956e9df4e4f3f00f9b8089a0a62668d9ac506d5116beec87459b0a803584220`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c7a86002d0cf82ec530b94e216fd8f013d7010b9c6dfda5ca8def8d13207e`  
		Last Modified: Wed, 22 Apr 2026 01:31:24 GMT  
		Size: 13.8 MB (13831363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e6e39bf4d8c54d24a63940c3934a18b6a289beda740be95a30dced7a41f0a`  
		Last Modified: Wed, 22 Apr 2026 01:31:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae7ca7c7642e9c4e422bae51701bcec334d5cc8bf1c8d1a71d87c350006383`  
		Last Modified: Wed, 22 Apr 2026 01:31:25 GMT  
		Size: 12.2 MB (12242217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97bb8469d1f54dc7168ce6fcf9f91193a064dd380736b62ffeb332eb015a7f`  
		Last Modified: Wed, 22 Apr 2026 01:31:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2467f5b8fe9db39a57179044bc6b28c10a10de883418437d9a9ae12bbfecbf4d`  
		Last Modified: Wed, 22 Apr 2026 01:31:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef2d69f9cfb30f9818c1b6933bf04057906707a7b4a229f002d70d7e766b326`  
		Last Modified: Wed, 22 Apr 2026 01:31:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0092956d054a82c6c158d383c7c03cdb07936473a1c53cefcffaeccb843e62`  
		Last Modified: Wed, 22 Apr 2026 01:31:26 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138e335c64da8e1fb0dd5c0e6d16577e4a3b261c8de218218e498153c44118cc`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 2.5 MB (2518332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752163400c54dd6cb3282313983bf2d39e4d3e2a17a1c1172fd1014ba59ed17c`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501fd7e5e435094c6e9c12cd751ff4736eeb4cc45fa4b35de8086d37178522c`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 22.4 MB (22374943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32efa751fe756435801240ad9a66fa82ba55aa851e627e18456e9bc1df9c957`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5adfa7b73930f455eba3b122867f1e9919d182c94badba206821594a885e89`  
		Last Modified: Wed, 22 Apr 2026 03:42:16 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:c8663fd98695dd6f3990b4479313a67d3a9ae92296309c557c70d6879f83ed2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57991c3f863e7503041e69d52cb8b993b531d9e976b1d347814fb4ad14a7dbda`

```dockerfile
```

-	Layers:
	-	`sha256:2844cfbfa4edde2cd056cbb74d8ad5f0a438c4a8b52c4711c07994f0f3ca7a39`  
		Last Modified: Wed, 22 Apr 2026 03:42:14 GMT  
		Size: 33.3 KB (33348 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; arm variant v7

```console
$ docker pull matomo@sha256:35f7cc08b2f483d437498549400b3f405a27f60b4597d11724d06d0c2695b8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162663283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffe871bd97e2752c20a1e4b69b59e8b607c5468f1550d6dc5a65a2bc4f6c24a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:31:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:31:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:33:38 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:33:39 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:33:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:33:39 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:33:39 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:00:40 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:00:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:00:40 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:00:54 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:54 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:00:54 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:00:54 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:00:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55902cd11f5cee73e37dd6b7274ad068d6ab77feb8165d071674df0ccf38417`  
		Last Modified: Wed, 22 Apr 2026 01:26:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0b5ea04af6bac36d38da15e40540ff669cfc9d5141d6bcab3317138fc62e3f`  
		Last Modified: Wed, 22 Apr 2026 01:27:02 GMT  
		Size: 86.2 MB (86248228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25364998dea0b06b29b1751f14ff8ba40896bb1fc689649eec92f9c35da15d3`  
		Last Modified: Wed, 22 Apr 2026 01:26:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53652e91bb75567649cbe37e0295b5f321f34db9e9bd71defbde7045ea5b2ef`  
		Last Modified: Wed, 22 Apr 2026 01:33:49 GMT  
		Size: 13.8 MB (13831498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bd347c00b03d789171cd29fdb3ff73232e46767edad9fa67ad3cbdeb0c12`  
		Last Modified: Wed, 22 Apr 2026 01:33:49 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ec168117e0ec7749daab8645c027b86821d2770688ce0c8f989a6dcbb0fd5`  
		Last Modified: Wed, 22 Apr 2026 01:33:49 GMT  
		Size: 11.6 MB (11578134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e67a910b1bc5a88ffabfca6de789363c93c9197fe665cdfa48ddd5061ffb918`  
		Last Modified: Wed, 22 Apr 2026 01:33:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867543f872b7d68cc584e2bccfc9326f139460fb0abbfe0b5088450a1bff8e09`  
		Last Modified: Wed, 22 Apr 2026 01:33:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f9d8517c2f282b742135496a0b92c3233029e6943e96c6d3c16cf28f7e6935`  
		Last Modified: Wed, 22 Apr 2026 01:33:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6ce405333963fdc520e92d36f4d5bb377e38403cfcabaa518f073f5212a153`  
		Last Modified: Wed, 22 Apr 2026 01:33:50 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92224881ecbdd8d334354f500189752c1c3f88a11559131b192a4462f574ad8d`  
		Last Modified: Wed, 22 Apr 2026 04:01:04 GMT  
		Size: 2.4 MB (2400825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea02161be504b52e539efc900c7358b3028631c2762498779cf56b20bcc8c5b3`  
		Last Modified: Wed, 22 Apr 2026 04:01:06 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312dad7da0e41b7f3e862b95f65972ba4edf051e8ae52d755abd8a2a67510bb`  
		Last Modified: Wed, 22 Apr 2026 04:01:23 GMT  
		Size: 22.4 MB (22375083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1062e0bde1d15312ab54ebdc046e4d7614833837f09b0ffc042edfd949e1224`  
		Last Modified: Wed, 22 Apr 2026 04:01:27 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe99439af59ee10b75ecb05810ad1219ba8b05c6194bcd6691b58f2595727f`  
		Last Modified: Wed, 22 Apr 2026 04:01:28 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:59907d6c34327f3fac9bbccc4aa379bc144f5a257aca082fddf5d358b5ba4655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acf3c9b7f340ccd3cacc45bc0bfcc60b31773fa2806709f476229413968c82a`

```dockerfile
```

-	Layers:
	-	`sha256:077d79428eb9e0f2a19de16b58851cc959f6c26040d9364b95cb8cae9cf2eb9f`  
		Last Modified: Wed, 22 Apr 2026 04:01:04 GMT  
		Size: 33.3 KB (33348 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:93a9138c384e4766c0f748eacafbf632f8aed00184b7e5ea8efd242c817dbf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192547517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c092be200738af47f6a3664ce85d7ae94019353f9e48501b3b7061942f23c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:25:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:25:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:28:52 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:28:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:28:52 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:28:52 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 02:41:05 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 02:41:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:41:05 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 02:41:14 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:14 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 02:41:14 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:41:14 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 02:41:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:41:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf58408576af2949270f11d85790f89b2b7f90001101ca6a168af36b90ec241`  
		Last Modified: Wed, 22 Apr 2026 01:29:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df2ee54d67d8da4777af2387c44849e36a7079172ac5d98d34d05857d9811d`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 110.2 MB (110164886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be478d67298ff292bb2ac64cb4620e7a85bd9fdb97f4560ebfa7c52abcfda9c`  
		Last Modified: Wed, 22 Apr 2026 01:29:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f6ab9342fc1c138b193bfecfcfba6e6a2bcb986e1f808905cab9613a10565a`  
		Last Modified: Wed, 22 Apr 2026 01:29:13 GMT  
		Size: 13.8 MB (13833355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88fc6d051913dbea29e6527c934049337911e3918aced0cf00cc2901674d04e`  
		Last Modified: Wed, 22 Apr 2026 01:29:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c4b9b85deed42586236b7e0713b199505777171a5d84e72fe121c9cf965cf`  
		Last Modified: Wed, 22 Apr 2026 01:29:14 GMT  
		Size: 13.3 MB (13347436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7870b2dffe2752d9dd4369c99dfdb604c5866e584fb6f7a059518a6ffd639`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f4a215ef981c4758dd3a96fa6fe44f201ddde1ef4fdbaeec265180fb88247`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa24fc68f67212fcace70385af136b353aed829577a69f85e4f4bc94fbd6d397`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfab259c828b009e3663f691e187f018707b736687e11fc8762b82688916a64`  
		Last Modified: Wed, 22 Apr 2026 01:29:16 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b113e63d84bf51765b53a67eb577d3d7436715da1bee70eac3a8dafa34e1d91f`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 2.7 MB (2667030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aca8a952c0d444057893da765e743fc86341090970417f3c51681517834005`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280f9645fe5177875bb655252b4ccb988b8df7147fbb67104bf3672b5784a58a`  
		Last Modified: Wed, 22 Apr 2026 02:41:22 GMT  
		Size: 22.4 MB (22376529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac4412f8e8868c46a46a4c50173cc3a35753e5b74a3ba6c0aa121e820fc683`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b254226281f0a3967a19acd3bcafe60c94cb8f014b31f50e0ae92fa3ad28d2`  
		Last Modified: Wed, 22 Apr 2026 02:41:22 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:880dfe07e9d57fa9c74614df7484751dc1bc7e119a4cb300184eeb7a5774f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1542439493a639d4937252c4a5fcd2d91f5e60093507fc4b638fd1806eff2d6d`

```dockerfile
```

-	Layers:
	-	`sha256:803dfdf7f694a724ef09d54b5a9c47e68d30cb1a6d3390c3845fc3ec4ad83196`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 33.4 KB (33382 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; 386

```console
$ docker pull matomo@sha256:6cd72f57168134dc856dfb50f985473c9df9c9230056bf11538465b9027d9937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200318576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ef79765cf196a28e3b4e3ebbc62dd1abeb4f24f8355f5ff690fbe37747b5b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:18:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:18:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:18:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:01 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:25:01 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:25:01 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 05:10:41 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 05:10:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:10:41 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 05:10:53 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:53 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 05:10:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:10:53 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 05:10:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:10:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8563d86caa1b64b3c5a8f33ed6ea2513154a20313e9cc080e11259de2a9e0ea4`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce65dbe4c3b52070c1a4481a910d3917a82aaec9b107415b798388785ce7c2de`  
		Last Modified: Wed, 22 Apr 2026 01:21:55 GMT  
		Size: 116.1 MB (116144400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64874dcfcd41d63e88c04482c6ebbe34a9b64d9026562f74bc7fd128d4ab503d`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7843bdfd3e5bef86fb4a2db1cbd7684da9701341b71092f7553a4833a19536`  
		Last Modified: Wed, 22 Apr 2026 01:25:12 GMT  
		Size: 13.8 MB (13832785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f45043fb34da86612cfee1ec3bb75a574799a2b0017c8b95d25bf16aeffc0b`  
		Last Modified: Wed, 22 Apr 2026 01:25:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54667adee37dac9923958a56f911728a8970570b1f31425b5ca5413d454320a9`  
		Last Modified: Wed, 22 Apr 2026 01:25:12 GMT  
		Size: 14.0 MB (13982222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9575ffc62cd44336c2017d3988602129522f90e7ca1eca4d6b0523aae083745`  
		Last Modified: Wed, 22 Apr 2026 01:25:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ad35c8ef467d6b726752ae72175016c0e9d101f18f3487871de94e08a52cf9`  
		Last Modified: Wed, 22 Apr 2026 01:25:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d84ad638d9198e79a6a03d866a0d835af8d1a28da961e44f7975bd67905a22b`  
		Last Modified: Wed, 22 Apr 2026 01:25:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658b4d5df669458f134b0ec1768f5e9d318a5871e21c79500d75162dfc95b503`  
		Last Modified: Wed, 22 Apr 2026 01:25:14 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582a0dced91d8d9a94d400b52f1f4ebb14ecb1b84552be7a9cc0b06c410d7e24`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 2.7 MB (2672048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c4d1c2351646088f2f8d751deaa69cb4c71b25d174736de139f45cddbc791a`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6e93e192aa5455a940cb277e2b72f856c76b65faeddef95dfd1c901502ad87`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 22.4 MB (22376123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5477b881c2462f05da0c5839f438ca55d1db4042f069ef5e85893230d696`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe04bc85078a24980577892bdb2156de6744f67b6f8b509fd97af4aaa924b3a`  
		Last Modified: Wed, 22 Apr 2026 05:11:01 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:a2e860183a215e5d92a208478957ca2f557d08cf787b0d1eea85ddf5528233c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a620106732531c56dfda4765383ab1065582be32c60755815df6050352d99903`

```dockerfile
```

-	Layers:
	-	`sha256:540f104f6445164c8e63d57d2e454789cdd02d23e89ad8c7f606a1443e8fe7b6`  
		Last Modified: Wed, 22 Apr 2026 05:10:59 GMT  
		Size: 33.2 KB (33212 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; ppc64le

```console
$ docker pull matomo@sha256:2272d049c167970b58114120c97e04ac95243b0ac4d4709985f501c921288a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196589128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8660a06ec7a51d3b4d79c2ebfb775636687459a7e5cbfc5f05f15bdb9eddec3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:54:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:29:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:29:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:29:00 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:29:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 02:29:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 02:29:01 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 02:29:01 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 10:58:10 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 10:58:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:58:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 10:58:11 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 10:58:33 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:58:33 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 10:58:34 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 10:58:34 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 10:58:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 10:58:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b5847d95feef86743cbd49c633eb60f2ff5fe302e71093f49fbd2320e1d58`  
		Last Modified: Wed, 22 Apr 2026 02:24:03 GMT  
		Size: 13.8 MB (13833103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b8e5fda2efc50218998dd81d724b6628613051cf19a1910551da522c682a78`  
		Last Modified: Wed, 22 Apr 2026 02:24:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982b00cc68c3293e74b57069ebee18bfb120fd36d88dbfebbf2b9a65911fa379`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 14.2 MB (14216593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c4a379ef2f399d72ca01f374eaa921c02a69167826bb2c3e0829d8906fac45`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e895ecc092a768d556e7735d4ad08f7b02d9251191e053d07a267350128f47`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3916d2e474ef6e91c9eebef2373811cf9ef128ca7891f0cdb6e790747598f41`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f1fed36adf60cc812d5d5ac75e5173f419b3ee00d8175c70fe1248910c1870`  
		Last Modified: Wed, 22 Apr 2026 02:29:22 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244a2ad125d492fe8f68320f86813741af59f922cbd19ac74a42191a61493e9`  
		Last Modified: Wed, 22 Apr 2026 10:58:47 GMT  
		Size: 3.0 MB (2950748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e1d38fb371a11279ead74d150bcc58fac098ae7db0cbf38fea7098ecbf3325`  
		Last Modified: Wed, 22 Apr 2026 10:58:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2b55ea9e92b219dd33654b8fa5613df6529783053395015869d5b04349294`  
		Last Modified: Wed, 22 Apr 2026 10:58:47 GMT  
		Size: 22.4 MB (22376692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c866d0e345fb64e1b9f03fd52d93306619c265245058a1bd262d8768e02b0`  
		Last Modified: Wed, 22 Apr 2026 10:58:46 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c0e2d7ff69124209de8849ce1ccd0e8618f566551107a6fec927adc1e4ca34`  
		Last Modified: Wed, 22 Apr 2026 10:58:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:74aa06715616364d79051eedbf9462a7711558a23ec56feb8a76581ba62cf670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66792397d53c1908cb44188f94433a16391e9ae7b18a161b32146349a953ee9f`

```dockerfile
```

-	Layers:
	-	`sha256:55c7332afff313e603a3d1bcf6b01bc25c1dad58ec2e743c2a5a244c81660bcd`  
		Last Modified: Wed, 22 Apr 2026 10:58:46 GMT  
		Size: 33.3 KB (33296 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; riscv64

```console
$ docker pull matomo@sha256:504f2c73659274722e9f667c69c87d8a14c741503b5908f0df88b33aecab39b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229873784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5a51a4832edd12ad746268e4810d53d872950442c60d6fbf552e82d64d3ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 10:47:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 15:38:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 15:38:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 18:28:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 18:28:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 18:28:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 18:28:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 18:28:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 18:28:22 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 18:28:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 18:28:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 18:28:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 18:28:23 GMT
CMD ["php-fpm"]
# Sun, 12 Apr 2026 13:17:10 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sun, 12 Apr 2026 13:17:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:17:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 13:17:10 GMT
ENV MATOMO_VERSION=5.8.0
# Sun, 12 Apr 2026 13:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:18:33 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Sun, 12 Apr 2026 13:18:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 12 Apr 2026 13:18:33 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 13:18:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 12 Apr 2026 13:18:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773a2a196a80b508d441421fafe9f9f2b0687fe4d6110d2eef7685df3c398534`  
		Last Modified: Fri, 10 Apr 2026 16:34:41 GMT  
		Size: 13.8 MB (13847821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c66f4a1e9830c2bd547f6ca1e7d6b7bc3890378e6e846822db9ce8b636016`  
		Last Modified: Fri, 10 Apr 2026 16:34:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec49cf72012e3dbfcdf19461fac9bf43e6dcfaaa4da30b1530d748ccdf898eb2`  
		Last Modified: Fri, 10 Apr 2026 18:31:23 GMT  
		Size: 16.2 MB (16188977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c2d283ba34d67ffc81547f065b648e98c2206a8fb5e3169d48df92b2807f46`  
		Last Modified: Fri, 10 Apr 2026 18:31:20 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a5cd3a99b08449087aceea0a1b678e590e563979ed733b09f33e8f84eef84`  
		Last Modified: Fri, 10 Apr 2026 18:31:20 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f307b71a024f957a1e073f50d366fe9e9c7f1720112a04b1d5c90a790582d4`  
		Last Modified: Fri, 10 Apr 2026 18:31:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2ad55814a4f1eb12dee4f88c8e63ff806bcfb57804b4b32b007ddc607fa61`  
		Last Modified: Fri, 10 Apr 2026 18:31:22 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb0bf8c414152e8b464008ed0d044a4f3b108d8da4ebb99587312044dc46bc7`  
		Last Modified: Sun, 12 Apr 2026 13:19:51 GMT  
		Size: 2.6 MB (2590769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee34030f3b64b2b898502de6175d8e66be8ec177857b7364a7a07c1942cd5c3`  
		Last Modified: Sun, 12 Apr 2026 13:19:50 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8069510d0fbefe136426e097f0e918a824b46cfc3cd8b9f2c21388ab2dfc59`  
		Last Modified: Sun, 12 Apr 2026 13:19:54 GMT  
		Size: 22.4 MB (22376758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc66dacc90ab2af8a18d581367caea0c142823a8d9a4ae38b5158ffe984a417b`  
		Last Modified: Sun, 12 Apr 2026 13:19:50 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22255be07b517bac69a6e8929520f6b238a66ad8483eae51d0f8f53940f1827`  
		Last Modified: Sun, 12 Apr 2026 13:19:51 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:7a0fee42aef504131a9af146743489743ab72ad8ff64cd16b2051beeb1226226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fe6d5e964aff0bb9de72a8a304ffa76e9dab2bbe4afda31816f9b1a9fb6b43`

```dockerfile
```

-	Layers:
	-	`sha256:5e114abf31929431b1e11182ae38cc27b1419e6e1bb42f9f47f2dd78dc7cc7b4`  
		Last Modified: Sun, 12 Apr 2026 13:19:49 GMT  
		Size: 33.3 KB (33296 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; s390x

```console
$ docker pull matomo@sha256:fdb7a8c553a3bcec9370b68fc3e921d7eb324c289414a9db062aea35a15d3969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174823600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddfcbe7a129e8312ea22bcb3f049fde87d1ab8158dfc59afad1e211d1862f13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:33:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:37:56 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:37:56 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:41:47 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:41:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:41:47 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:41:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:58 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:41:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:41:58 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:41:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:41:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757f702e0a9ae41a0668944dbb4c245387fe46a7b86e9158d6238a0a7a2e8d3b`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4485b6f62a7b6c400504342749f4784b13250b4a4923fa17548e35ec69126`  
		Last Modified: Wed, 22 Apr 2026 01:26:48 GMT  
		Size: 92.6 MB (92572845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521371e2b81d32dcc512c19954776e0f6ba6f3e6d3ab464b138a9d29e2737a4`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895072f1915069db96de1e6cd2775cfc97d31d00723b0b58b689f76a62b114b4`  
		Last Modified: Wed, 22 Apr 2026 01:37:07 GMT  
		Size: 13.8 MB (13832213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e06742a171f68cde5770d70c17567b9188ea34dedcf5227404e9cec8cb39c`  
		Last Modified: Wed, 22 Apr 2026 01:37:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618e083a88d6c35da869cebae5f113b9d04739889d9759e66ea3a3ac03dbfd44`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 13.5 MB (13462525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1f567e1ecc28a79a4def138b98f18610cdf8cbc4c52e98b56481eaae456cec`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bc44b21c26e70bb61141c8e8efce2d9f0f970663295792c1e4aee3edd1056b`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3b2142ea31f473941f8b36e1138fb495ed25f97b049103d4bb8307d58dd432`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02955ca59e915e77d99e4d867b1d53eabb24d3af4353fb49005525fc7de8a345`  
		Last Modified: Wed, 22 Apr 2026 01:38:15 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5724c2aa0fdc2900032153f14dac2022d56635de1dae751ab643b55baec1366`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 2.7 MB (2725455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf960f67b40800005e95b318e3eeb609c4087091a12b34d7a8a6eb293a5f23a`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87699047e6d8b2d3b9d950fe583d407a20d59d56c4fa4cd138edecd085fbf5a2`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 22.4 MB (22375590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f2d8de858a4c4cbe613043364f7769968d21ab526bfd7ea1dfa367e8ab2f8`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ef3f67459ea00f232576b036cb8350926e3e14fd70267673b60891c3f22293`  
		Last Modified: Wed, 22 Apr 2026 04:42:10 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:138516e39207d526251e66847d67b8d791985960062b10337dd8878f1eaac691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863d1496ae174a7130582b30322b91afde58ca0f565b4ee4415587ba04bc044`

```dockerfile
```

-	Layers:
	-	`sha256:5ee4dacdcb3405a3757d64b5d29b8b18b8be9f7ba74afe46dec2188df9501152`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:5-fpm-alpine`

```console
$ docker pull matomo@sha256:ec311e446452a864e627f50a6b318a43b2f78d0b354302e5e66fac0fac74af66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:5-fpm-alpine` - linux; amd64

```console
$ docker pull matomo@sha256:72b62e5007021941fb18fad0092abdf162db8235c4a80f087a9267b6253c57df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61540623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0cabaf43e5695e72598809dfbe5c8a6bbfe74b9b14bff6f7f8dbdaba53df18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:27 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:21:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:21:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:21:27 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:40:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:40:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:40:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:40:12 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:40:17 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:40:17 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:40:17 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:17 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:40:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ef6327a484adad40c70cc6260e6c05b6496a95d7f17bc657f1608ef1d98c65`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 3.6 MB (3587421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34a3b26ad831d1b88e28205d0697d293a6b9bd48bba6c0618d2a962f6b7ab5`  
		Last Modified: Wed, 15 Apr 2026 20:21:17 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd24741e080b2f5812c84cec27dcacc6faa6834e57a410d0498f39e3f589d63e`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae9fc1b3d2fd71e5fe569524101eda391f21af0725aee92bb039cd3e3e2ec9`  
		Last Modified: Wed, 15 Apr 2026 20:21:35 GMT  
		Size: 13.7 MB (13709881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cfb46d077b27f03899c4f08b5ebd738a21e79448dda30c53e084e4d1ee1b0`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6b4452123be6c2fb9a132b567d46df619e884ca6553bb2e96c5073a44ac072`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 15.2 MB (15201457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5ec8e36b924dcf98696ef1cf37b7f68a7521e815288899c6939d7bcddb5012`  
		Last Modified: Wed, 15 Apr 2026 20:21:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbd3ef9745bc4e4b2d2170cdc2beda14f18aba440b3973124628fe77aeb08b0`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 23.4 KB (23403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80181fe3ced17e0662a1f6639130ad39f9d44b208813f75cb2e77e3597e4da87`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 23.4 KB (23414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9440a7ee03ff048797e0bc98dadb4bca879b081ddaf7f005cad80dbb7c779`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d4b1b4dbe81b9fe09ec6ec1761a13158d3d145cbf72cc0877c504ff9d9cd7`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 2.8 MB (2831499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbea798e96b34fabcf879b361adf2af38240de2f967cd83b69304814b1b694e`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47a9a5f11dcce9aab63cd78b9ddcf6b3ebacfa4a2433efb10eca5376a22c48e`  
		Last Modified: Wed, 15 Apr 2026 21:40:24 GMT  
		Size: 22.3 MB (22284502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce0484c5dfcfc4b17ba7e7b613af52b345be0a44b3361b35d2667f4c6edb3ca`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb7146fed469c7aa1859ad6adde3c2b4651fecf80853f198e35c37d2f5f34e`  
		Last Modified: Wed, 15 Apr 2026 21:40:24 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:ba8dcc95c947eaa034fdda8e7b2b3cd7453242fc3866f9d4f9f8805d78ec36f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3038f594426ec8336580b4aaa8d4980b35e97b46a0a9b8aee6de9b1320711e7`

```dockerfile
```

-	Layers:
	-	`sha256:c21e15fb76d20c33ee35709095ce1aea37a8f34a7d2668b4e17a62c0af8110c6`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 31.5 KB (31504 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull matomo@sha256:b38857024c83a976168e465415879c08785c837559c196d8de9ee5ceb2527428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59532340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8230318ab3cf0aa8b5baac55eb35a00d09d5f958e63871a6edcf5d561348c081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:21:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:21:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:21:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:21:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:21:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:24:56 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:24:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:24:56 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:24:56 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:26:21 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:26:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:26:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:26:21 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:26:27 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:26:27 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:26:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:26:27 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:26:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:26:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a7c0fd01aa85d53a5cc462735eb1cd908410a74091bb824d85314c572a2e98`  
		Last Modified: Wed, 15 Apr 2026 20:25:02 GMT  
		Size: 3.5 MB (3543068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0990a4f4213cfb6f619b810861edf0e55ff77432a3a9995933d5e5e0f25b962`  
		Last Modified: Wed, 15 Apr 2026 20:25:01 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c4bf762147116095a30f26ea107900f28361d1ed6bcae3c7312e6e16503d86`  
		Last Modified: Wed, 15 Apr 2026 20:25:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611c551c89d0a52d0c1fc742df48242b4822774aeb29969a04de89b831b84d2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:02 GMT  
		Size: 13.7 MB (13709885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ade602d1f9497bdb9f1408e2550053a861b3b97d3825ec1db2a3d0455503`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56588352628b072b8435ef48b6525542156117d05dc3638e928af0056385309`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 13.7 MB (13674677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268fbbb176b6d34f57da556ff71567e0c3b3c8a511e1cf4ed34733eaba6187ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e012c1772b42d6b1fba0c2455214494ec06551fd4a67e2fcef1658f848615`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc79448a1b097592a03822eba5c5d849e0e0adbd86a3409607fbc6466cf075`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e05eec180821df7fd20ebc57b940908cae6bb1d78f21f26ea0f3ff23119e46`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b4b62928d31fc023fe056b60c75906405dc312d724f2d47a6bd4498dcaff3`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 2.7 MB (2686952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2c55b51319db330e583fc26fa9c77527aa6075f531f51dd01d668039179dd3`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ad977afb62e4095af9c745fee6f6d05a85151118b8f48dcc8bb784984afb2`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 22.3 MB (22284594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec77782c804a00e8db37bd0ba12f04377223228bf59f6a25ef615e020d5f3f0`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2179c12fd7a900f1c8042cf4b706ca6414dd3c7b71719524bef2721377a53eb`  
		Last Modified: Wed, 15 Apr 2026 21:26:35 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:6e22bc5b50f784a0aa793edc6260acc0d4a3877c05f60395cb027490264508f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68dbf4995f06f7d183c25729167ac29de1950690d609f88e58fef5b771bd816`

```dockerfile
```

-	Layers:
	-	`sha256:4f0a3c077e84e19c591f72e07f35d0294eda015a1a10af99866974dae2460959`  
		Last Modified: Wed, 15 Apr 2026 21:26:33 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull matomo@sha256:db6e31bc9e56c7124d54f5138b60dc7d5293a05db2bd10f8b239393f0961ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58136619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02bb9d74ed40d1ca91e6155aa232c1266ddfbb733000a67eb8b39f3fedc9093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:21:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:21:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:21:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:21:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:24:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:36:58 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:36:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:36:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:36:58 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:37:03 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:37:03 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:37:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:37:03 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:37:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:37:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b303a0989ba45e4f7b30cb9937c77a13a6d2c7ecd4eb8917f1512079f9f97`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 3.3 MB (3343367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfb6dec2dbf14603e2027ed5b971b0cded429fa6c207d9d90b199acc9cb3f9f`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae7b5f922f713096ada0c57083da1371a86516392d3d545429f9e6f086cfc1`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd82f5c870f06ad0977d75bfd5f221698844492f83e81d648b6df4d92191d57`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 13.7 MB (13709890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319ee333590a57384eec8d838e3097a7bbbaf98511fa5f754866f9c060f4ee53`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6db70784fe0b64129cd81fcc768162b61cfcfc6046390d05cccaf7bc7b34a4`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 12.9 MB (12905191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2b25dcc6fc43cce4d7cb7527e44400765b559a9be6f70a9f0b870f5431a16`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc4e71b3774288941b5f1bfc7d26b51a56816bc620b4dc0adda2a995fe29d10`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5dbac3789d20b6f7fdf3f3626bf3319aed3094a4b8438530220ba321dbfbf`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 23.2 KB (23225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c39b81bd3ed013ae106fd28f7de2a7f5a334afda4037ae7ad637f3deab270`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30741ef8f428a294b3752c060c636de14f63c81af6838a2d87d652a5d761135c`  
		Last Modified: Wed, 15 Apr 2026 21:37:10 GMT  
		Size: 2.5 MB (2549152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cff83a4640159a1c39a4e122eadce7420f7c4b0a3cc60c02b368d6fba4ce686`  
		Last Modified: Wed, 15 Apr 2026 21:37:10 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85b2a3988d4dbb4905615749cc0e1ee60cd6c15ab8fce8bd83368d30a949bf`  
		Last Modified: Wed, 15 Apr 2026 21:37:11 GMT  
		Size: 22.3 MB (22284595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092227d820bd4efd03c085ffef1c200994de3d55222b5dad7ec30bc80b4513bd`  
		Last Modified: Wed, 15 Apr 2026 21:37:10 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e6f3346bc4998e779a11a623f40d3bafbcc6735024f682d9727810a2e4e59a`  
		Last Modified: Wed, 15 Apr 2026 21:37:11 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:a27373a579bf1332be9ac9a1e4d3c2602c83d6258c6e8a0b68e9557622b78a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762df55010d7192b5e92dab8aca42e93d29c649709d66ea0d2f20dbe9a1c517a`

```dockerfile
```

-	Layers:
	-	`sha256:2ee57c82275e330a6db543385c928244d0cdcd18d2c572132b4786db1f7b2417`  
		Last Modified: Wed, 15 Apr 2026 21:37:09 GMT  
		Size: 31.6 KB (31610 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:14f7d4262342893add2bada263de60f5c98d205fd01d834e1a3714e2923f37c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf2c472c92fe16d966e3422b8025ebd56708fc944e132d6ef1fdd077845a405`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:16:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:52 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:19:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:19:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:19:52 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:19:52 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:52:11 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:52:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:52:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:52:11 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:52:17 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:52:18 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:52:18 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:52:18 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:52:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:52:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f88c471740fcb5875464e516549da32c6c706f6987bc05fbbb6fd513a5802d`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 3.6 MB (3596129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eab76c94334ac507bd24480ab30256763b2b3d9cbee2101f931af7891065`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e2ccbab69dff79d74edc28fd92dc771024392d7f27df7019a0996222edb8f`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b53c8276cf1764bdbc2a8cc4bd82d17c9abcec1caa79e755d4bb8f6cd08689`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 13.7 MB (13709885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c9424747f4f86a2634299b5c26a2827b3fee39c8784a2cffe3db0dcccfbf2`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a7eb2230420c7fcbaa60c52674a748d09f2ceec7a1d09bb2384d3e9e4dfb9`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 14.7 MB (14702729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f864aebee5b8c62db6cc183f3cd9b7cda0fec6d388db0af242bb2496252e6b`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de20756a108dd2bb386335748415a405d248e1ab311f95e986cf3b417ed4163`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84abee5e477c51afcf6df1e875a6d0c7b98a1ceed1df6f1b371d717edad39b06`  
		Last Modified: Wed, 15 Apr 2026 20:20:01 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce22a0940badf7da9b32f48d60afebdc96dc96c225a972f67e8092b3457344e6`  
		Last Modified: Wed, 15 Apr 2026 20:20:01 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9bb764d756634d173bc061c2687846671bab4bd6160912282837e5796249aa`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 2.8 MB (2836752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b9405104ba2e4253333c12827eb1fd88d41702d848ebb4ab872a93f53616cc`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0187d8ba993d4f71202c944c0cc26a0bc6175d0d0d9a5e95d8915788a5f256`  
		Last Modified: Wed, 15 Apr 2026 21:52:25 GMT  
		Size: 22.3 MB (22284595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1b33ffe95c13f6ae24da99909f33c6e8b52b9da34561f028fc79035f1b30b5`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139ff0cd3e24d4773e1d0ae622aaa12ffb918780190141d0b527a67e174d886f`  
		Last Modified: Wed, 15 Apr 2026 21:52:25 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:cbcecf2d401ad25baca20f95b77a54169f126e78cecc67fea7936f2f5e4c4ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4deaaa4428ed1a094857259aee37a53fe2d9ef4b7ba3e1b83a53888d20d7eb`

```dockerfile
```

-	Layers:
	-	`sha256:9c012696aaac20769638f74632f1ae4e6b13a76b4f27a6706581769ae3574634`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 31.6 KB (31638 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; 386

```console
$ docker pull matomo@sha256:43a47187b21146af2ff0fabf2fb213f0644517eba079cde205a01356a5f747ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61714302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2da1ab54f59400b6588b37da5aa4e8836b685406adfe73457c3bc73ea16d4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 22:21:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 22:21:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 22:21:20 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 22:21:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 22:21:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 22:24:54 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 22:24:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 22:24:54 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 22:24:54 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 23:18:34 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 23:18:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 23:18:39 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 23:18:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 23:18:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:18:39 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c62319c64ecbc8864f653b3190fe2930cd0d7d729dd495e4f110d82beb5a8cf`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 3.6 MB (3625741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b237d5e55c87544bf498ed4aa2213ff7f3202b6e8ac11c0feb4eef6dc60561b`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce09e8975bb1abc7c27969ab796d05155e31bf9607dbc4d8d6b9869d6f42f2`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba374fe7ae564b24b876c0e37c0e24ae10295833b103ec997c6f4d51b33a2618`  
		Last Modified: Wed, 15 Apr 2026 22:25:02 GMT  
		Size: 13.7 MB (13709870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1068ef912fbd9b5cd23278793990a073d89428d5fffb6721e01c234f10214b9a`  
		Last Modified: Wed, 15 Apr 2026 22:25:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e808d6508c20e9c7b0fb968a894ef6f3a08518435e4e95508d14a683736b4`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 15.5 MB (15507087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e4133cfa5665ce34eef08043c23f2f0dba6eef44cfdd177b97398f5bba9523`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536bae25de12f93460507a4870f8205b06a2eef459609bb23b73e1bd928c055`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 23.4 KB (23399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada671ef1cb78b082bc30975712e67aa71c719e0155289b05390c82eeca47ee7`  
		Last Modified: Wed, 15 Apr 2026 22:25:04 GMT  
		Size: 23.4 KB (23417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1be0d762f8603f63ac3e25a8914ead38c4303e1cdf95c608adcbae90b5d06`  
		Last Modified: Wed, 15 Apr 2026 22:25:04 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db0ff674de354f9976f4cb4de71124f3d857265205fc44e12f9299de000d7b7`  
		Last Modified: Wed, 15 Apr 2026 23:18:46 GMT  
		Size: 2.8 MB (2835001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcd35b688436da9ddfb97263dc980ed1181f789206ee83e21624e9d32d741d`  
		Last Modified: Wed, 15 Apr 2026 23:18:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1eff2cde0cd64891546c2c0520a6e0e85baef86ace82ccbc1b93af20549984`  
		Last Modified: Wed, 15 Apr 2026 23:18:46 GMT  
		Size: 22.3 MB (22284481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcffa4a67e26c61cab98382350dcc6cfb6832986d90ff9b17b3d16d9fdfd4144`  
		Last Modified: Wed, 15 Apr 2026 23:18:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845e3234a7a6d16502c5dab54f4b301207d30fcc5cb5d8498f332d1603a28631`  
		Last Modified: Wed, 15 Apr 2026 23:18:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:067e8865347eaa0811d1d4d7a31ebb5b6e5d92441ef65fbab1ac2a371d11e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9425a3a80fcd0478859560c46b989e3fda02d500ceb18edaf8d33bd99323187`

```dockerfile
```

-	Layers:
	-	`sha256:b66b4afe30159998ad9a7a5da61f7c1ef93afaefc461e3afe3f5dbf95d840f59`  
		Last Modified: Wed, 15 Apr 2026 23:18:45 GMT  
		Size: 31.5 KB (31468 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; ppc64le

```console
$ docker pull matomo@sha256:3e617269a39433d9749e62793320d365c0c92b2c484aad1843febb2775cb2805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62442317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76506ba2465bd3366303eb15bed3b917c7edf2910b082b54d720ae23b3e987fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:26:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:27:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:37:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:37:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:37:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:38:00 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:38:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:38:00 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:38:00 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2026 01:19:34 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 16 Apr 2026 01:19:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 16 Apr 2026 01:19:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 01:19:35 GMT
ENV MATOMO_VERSION=5.8.0
# Thu, 16 Apr 2026 01:19:45 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 16 Apr 2026 01:19:46 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 16 Apr 2026 01:19:47 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Apr 2026 01:19:47 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 01:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2026 01:19:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0370fd1370a54392f3444f77669b0c6655267b3ae193cf4de50a9871836636e7`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 13.7 MB (13709879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5dbe897696d0b00e89cb8cca0978c45cfac755af8488d2743b4d1d0e8349b9`  
		Last Modified: Wed, 15 Apr 2026 20:32:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed748167a4ba110e55bf836859404ed0d07c8012c0a38120a6a71eb553916df`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 15.7 MB (15732363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e837ab2c17d3b0ba367d2b928038674b2b671b658d5d1a8d2c7c6887717a6b7`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281189f4b70a3abcf43f4fbb010b7a91d30476a4f755d51d6b0dca53f4c4c6ba`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0d3b6b2ac74c55e87998f3778dd5acb7b98b2ad5d5cda294b7423d2989ac16`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 23.3 KB (23253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f01cc8a62ac057a37f08692e3d3ca7a19a514bc8c37ba1f784049e37952d7f6`  
		Last Modified: Wed, 15 Apr 2026 20:38:18 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7972d182997daa1a63f9c8de270a132f3ad0996cbd9de17bde03407f51bf9f4`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 3.1 MB (3056093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3598cc0908f0c2d5cda65c7f1af0b4ad6e183703917fa8562d330bb4339360b9`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b5090403ade59177504bd26bfa58fab9976a7b0b3c39985d0dee964e051c65`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 22.3 MB (22284602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dddfd69364781e3e6c2eb3ee4be29f10236bbdff770bc351a2ade1ec2f9744`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71581fb99af588d7be69dfb6b528305486bcc448c5dff1b7dfd1a24d9cb2f4b2`  
		Last Modified: Thu, 16 Apr 2026 01:20:00 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:b22dfa92ab3bf45360b491181f79ac3dffa7980ede5c046fc6606b1bde28259e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d33f537552d2a51ed36e452a5f490541088fca77afe2edaad81cee667289fde`

```dockerfile
```

-	Layers:
	-	`sha256:f612ac6c8fd2eebb37620715b21d375af7bbf9a96996e2a33b1fc2a9ec56139a`  
		Last Modified: Thu, 16 Apr 2026 01:19:58 GMT  
		Size: 31.6 KB (31552 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; riscv64

```console
$ docker pull matomo@sha256:2c069dd59077c23dada2943fd180fdb220741765e0309749f1f4a56acfb01b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60726324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414a4b5c2a6ca7bad2c9f6f70dc5c83f7fad0054d249cb153fac079ec4d00fdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.4.20
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 16 Apr 2026 03:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 16 Apr 2026 03:22:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 05:19:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Apr 2026 05:19:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 05:19:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 16 Apr 2026 05:19:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Apr 2026 05:19:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2026 05:19:44 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2026 05:19:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Apr 2026 05:19:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Apr 2026 05:19:44 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Apr 2026 05:19:44 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 23:45:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 17 Apr 2026 23:45:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 23:45:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 23:45:12 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 17 Apr 2026 23:45:33 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 17 Apr 2026 23:45:34 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 17 Apr 2026 23:45:34 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:45:34 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2026 23:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:45:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4fa4e03a41893883792ee4048e5be20691de7211e35a2a172723216fa8a57`  
		Last Modified: Thu, 16 Apr 2026 04:21:29 GMT  
		Size: 13.7 MB (13709907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476302825d394ab9e227dbc6c9b962133bd1e7955ae20467d45109b6fcf1a7b1`  
		Last Modified: Thu, 16 Apr 2026 04:21:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e6b11a11df7b142f2f72f47441134f2dea9f81752b8af4643ad157bd4f7ea1`  
		Last Modified: Thu, 16 Apr 2026 05:20:38 GMT  
		Size: 14.5 MB (14463523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccddcff8df9f124f53d7f0c3cd362f4e501eb585260cb68aab0946a400e49c17`  
		Last Modified: Thu, 16 Apr 2026 05:20:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51b4405f9696a0061622be43058dd51c509ce8944908208539350d5bd6d897`  
		Last Modified: Thu, 16 Apr 2026 05:20:36 GMT  
		Size: 23.2 KB (23243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19640a83bf529fc44644d01cb849e5881a0806e197267c01ed234cb601e01408`  
		Last Modified: Thu, 16 Apr 2026 05:20:36 GMT  
		Size: 23.3 KB (23261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfc73f78721d63719063106d8bd4e69aba98677503906be7d7cdd6efb9bff6d`  
		Last Modified: Thu, 16 Apr 2026 05:20:37 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704a80fd9694762a35e270d5af27a0e15b8bbf8ce5442ea905dba125b467e9b`  
		Last Modified: Fri, 17 Apr 2026 23:46:24 GMT  
		Size: 2.9 MB (2885009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e91f22ef73e9672dd6e3d354cf638f83d5e981d0644d7992f7fe585f8e374c`  
		Last Modified: Fri, 17 Apr 2026 23:46:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271545d130736b98973b78e7bddbffb4c4016cd94ac97a425f53c5e4ade7c87d`  
		Last Modified: Fri, 17 Apr 2026 23:46:27 GMT  
		Size: 22.3 MB (22284594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f99afed4bf18ec3d58580cca07e99f3244481bf8d1b9ee7bbf75adf3660d4e9`  
		Last Modified: Fri, 17 Apr 2026 23:46:24 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcf84f38dfbdd62eacc4a267517d922199233d0590caf10ee7f11729d45155e`  
		Last Modified: Fri, 17 Apr 2026 23:46:25 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:7eef629f5e1f63665fbffcb666fac13c8a0518a886e5799f58f444f1883430f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a56b89da63d22b82b2d0ec949962013d9efec4e60cbb4b258fcc79a3622dbd`

```dockerfile
```

-	Layers:
	-	`sha256:27a8a5a8b5719b232e3a6b417f3ffa634b8a05fd20985828786fe77d3eda4ba9`  
		Last Modified: Fri, 17 Apr 2026 23:46:23 GMT  
		Size: 31.6 KB (31552 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm-alpine` - linux; s390x

```console
$ docker pull matomo@sha256:eec14288bb38131ad4473c4744adaa7e35424f4e32e7ee9c2023373d1779d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61426824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f083be08b99fc30e20322187562d43cc16b78e82377d7040dcfc1570daedf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:26:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:26:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:26:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:26:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:26:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:26:29 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:26:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:26:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:26:30 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:26:30 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2026 00:16:24 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 16 Apr 2026 00:16:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 16 Apr 2026 00:16:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 00:16:24 GMT
ENV MATOMO_VERSION=5.8.0
# Thu, 16 Apr 2026 00:16:29 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 16 Apr 2026 00:16:29 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 16 Apr 2026 00:16:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Apr 2026 00:16:29 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 00:16:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2026 00:16:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816b342f273c114d9278090832c6b271fa133343c6cc14c8db27aad0433c7e9d`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 3.8 MB (3786986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40fd55f34e09a431ffb1541581fb4b2fad1c949d00d3718c054f6a585dedbbe`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93e9efb3f33cff64fedaa7b934bccba27be41ab8437362ef089937721401080`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adefa755b1cbede3245ba350573476b4438d2c3a375101c6553fcde8df5d943`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 13.7 MB (13709892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4adca3f5704531af4fde0978117a15a124923c7e965172a5d0bb1d9fd326e`  
		Last Modified: Wed, 15 Apr 2026 20:23:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0defdbf2ba8615afbca8a0d1bfb648f2dbbd17603fe56d07c6ee5f8d4d0d2b`  
		Last Modified: Wed, 15 Apr 2026 20:26:56 GMT  
		Size: 14.9 MB (14946590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f0d2a9c2acc44acc378d8d7aa59111cf8221ffd69d95d7a6999955f35fe09d`  
		Last Modified: Wed, 15 Apr 2026 20:26:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689498889cc21894baf940c5494c0f97d27acf8dd2b3ca587252825dda967ee4`  
		Last Modified: Wed, 15 Apr 2026 20:26:54 GMT  
		Size: 23.2 KB (23234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694ba63a331296afb74fd3621407ce230372e05b0b2381d225713d7b781af44`  
		Last Modified: Wed, 15 Apr 2026 20:26:54 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6618c20be4f399ddeebdf0c1a60c3656feb24e5eb57fbe81a52c49b0d9259a5e`  
		Last Modified: Wed, 15 Apr 2026 20:26:55 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384704e8316816dd8feb34fbcbde504aa62cd06f07fb8e3118ec81479ee60340`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 2.9 MB (2910838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd055c2e270cd72a6b80e51a049d94d07e8ccbf0c8d7c8799bbf82bc5fcb2493`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47e22974fddaa636533bdde7be656b253afd709938a7e246280ca3a0945b26d`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 22.3 MB (22284623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78c27e0c6ef68a3a02f85083cbe7fbd3b4038c0adb9a8764cead2a154bb6b2d`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f22f96a49d7f79f45350eab1c6b79be94c2917c72e43eb4fb429098a81a19b`  
		Last Modified: Thu, 16 Apr 2026 00:16:41 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:cb4cc1cd3723cb8978bd1ebc2ea5fcdf17634b13d3c06aab25845c4cf160821b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d61d0da716c7d14c4f2cc5bdc9f39500166ce93321a10b81db8f6444d0c378`

```dockerfile
```

-	Layers:
	-	`sha256:34e6fbb66b9cd18d1835e7c49a4ba9077d41ba53c197e6726d28b2f7b50c7902`  
		Last Modified: Thu, 16 Apr 2026 00:16:39 GMT  
		Size: 31.5 KB (31504 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:5.9`

**does not exist** (yet?)

## `matomo:5.9-apache`

**does not exist** (yet?)

## `matomo:5.9-fpm`

**does not exist** (yet?)

## `matomo:5.9-fpm-alpine`

**does not exist** (yet?)

## `matomo:5.9.0`

**does not exist** (yet?)

## `matomo:5.9.0-apache`

**does not exist** (yet?)

## `matomo:5.9.0-fpm`

**does not exist** (yet?)

## `matomo:5.9.0-fpm-alpine`

**does not exist** (yet?)

## `matomo:apache`

```console
$ docker pull matomo@sha256:d6daf1cd148fdc8b4b896b2f5bd8fa10ba99c0fcf464fc86c00fe352f8ca5adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:apache` - linux; amd64

```console
$ docker pull matomo@sha256:12c152741a75162431fe589dc58010ba84e2bec65c4ecc70143d55c4e2553737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204385414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02018cb5db2c814c3cd9fb610752f770bacf3b0380c02a5e210026b6095a0ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:24:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:56 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:52:44 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:52:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:52:55 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:52:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023baa873c0991ddaa7419301cf610d5e56ceb38356f1845ae0e94eb05dc3c9`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574faee95b5376fc2f0f3f093a9e6780a97d7eedc2da840e55380b1d36f85a89`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 117.8 MB (117843202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa6ce5874bc20b89543cd80d41f58507e071af1977b4fc38fe6a13ca83fdeb`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcafbe281a6757cd10d2aea9b90f3636b474dd2516c0980d602df86c6d4781b`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 4.2 MB (4226905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c19f6aeb84e92127e2e3d01ae0c2404b696e34500cff3e1730ca85603f24ae`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed48780967058ba90258dfa165a33a65ef90d6260c78464947bb8732c2091f`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a3c22f89f33eacca27643c304fbf4cdced1a494513ba0684cd5faf51ff50a`  
		Last Modified: Wed, 22 Apr 2026 01:28:20 GMT  
		Size: 13.9 MB (13852567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7e42314878fa75790cd20ec64c41553110fe17f16b9c26967a225173a8acf`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c72387956fde81883201db10160d5778cbc5b4846c394578385ffadd64ade`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 13.6 MB (13557477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae044dcde24485109733a3bc78f06686efea05cd32c03f0c38c68e2f825a8b00`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de552cfaae1b01c9edff1ddfa947b594abc5c5cd7e5935083ef66faf36a2e64`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a166fb5f1996a6802829599fa567e0f5051d57568f2922b032eb0402fe03cdff`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aafaa0f9a2d4557c2e9c1f953def4005d036064e46b0d8226bd8aa3047f10c`  
		Last Modified: Wed, 22 Apr 2026 01:28:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456ddb90857497cb87ca412dfc2f926ab21071759cf8fcb9a903fc7f38bc1f`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 2.7 MB (2717845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc0226b1100105f4d89cdf4bcf367da0f16e6606031f8f1c2a01494a8ef71cc`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906f8621388502a1c2fafadad71dfc4f8e6a79c0f3968c5e19ac3e3ff9914f6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 22.4 MB (22400019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eed11ba24da6d3ddc5fba318e47ac47c9eace9fba0f69c65f1ec68d9db43a04`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09df151f9988ce5a0c814ce4e9d8c3b6ba17c2f3552077dc6cd497b584327c6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:bb49764520a93d3fadb85fe316c6c91c38b0d19b7f270bf74188a81e1f457a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ffd650e6dd4076605c2b6b683b5cc5faab13fcbf9150d7b757ca61fbabb1b5`

```dockerfile
```

-	Layers:
	-	`sha256:80bec4086b4c60d81e45a4f6d2bdde09f55a31b64da8d3f8a8b0226929bebd68`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 37.5 KB (37471 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; arm variant v5

```console
$ docker pull matomo@sha256:b3f79e04d9b94de7b50b88dfdfbfa132845da9c7c6e4a96372f00c2265f912b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096adafe94dbb74320d05d940b1a9e5ec6f5eac8667ff3392a8eb6b57d13d6e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:27:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:28:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:28:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:31:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:31:37 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 03:41:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 03:41:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 03:42:05 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 03:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 03:42:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab8cd142c874a4a2116214700713c2dec92f9352b96761c33107037fb9f0d57`  
		Last Modified: Wed, 22 Apr 2026 01:31:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd9fa364a1786b392bac2e6ddd6745d7ce20e23d3d55e5dea7f9550e1299d7`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 94.9 MB (94884502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2affe866774915b1ac9a46a4e1ac18de29da227b2d5a68bcfd8c3c538e7b7d6`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80b088c9aeb209cf831aef8b763b0ec951fff041e9f33eb8457a075d2631ccb`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 4.1 MB (4089308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d32ed0510893abbd91f5e84dca0a9241e463b74e591f0100df6bb9c725623`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c8c0d10e5b9e10c1dd295649dd23ec4b53c92bca9182c071138a5e19d42d9`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a080db7c5dc718990269dc0f1f41e1ff18d27fefe892e5d28132340c72c9`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 13.8 MB (13849980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1c211cec5c80e05741841fad4f75d84ce5ae2e3f18171df44c774b5de93330`  
		Last Modified: Wed, 22 Apr 2026 01:31:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729daea6a9d1fe569b7a314fda12a22849a3e8fca3f0f6258dfe0b5d8222098d`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 12.2 MB (12206143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378076dd33dadd4c5e3699bb5f0d22530b9631762f33e38ace0f9ced22b890ed`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2380879c990070fe22833595bddb7e02c9b0ee05c886afd7343a6a0f1eff2a`  
		Last Modified: Wed, 22 Apr 2026 01:32:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff707614457b67b0eb77d55973fc3d28054243f45091bf9d0997d370f60df5d4`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5655cb2fd9ecf9b2f590ce94143aaf2a2b527fbe2489f5b3780216e7ae9c24`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d7df617229c5cc1a9a119d1a416cc5a5ca4690a3c1f5b28eac6de4189d1020`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 2.5 MB (2540941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d80a4659a3571e68d354a2656794a7e7d82c6666ee8425b2d70e39489f2daa`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76978f69025491f93184f38ba37d08d7cb833167a5867ab287ba88542f00f547`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 22.4 MB (22397964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7764c5d0265720d63f293ae158d0e6d6b9d2ed1f8910051b1cdc7570adcd7d5a`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f8c981c39ae50f561ff131ba6812c46579b2eb0d1a7a9c731f9d5e4393c726`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:f99d9eb764a1c4bfab790795df645bba9b3938d285255f316807dafee16d4168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332b81849e2103dd20bc7855d23d32a991eafa638521b6b03e7ddfe0fe94964`

```dockerfile
```

-	Layers:
	-	`sha256:e48f117027110118d1c39af8234e7fbd20682416aed9f39c73e1a3690b46eef5`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; arm variant v7

```console
$ docker pull matomo@sha256:704ea7b9198d0ea68b00d8502802cf9d8bdf423cba5ad6c46382d1a9ad4b5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166515903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dfa22ddd64577d28b1e403be4579b1a089eda6ccfe933ac6c43d305499cc32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:29:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:29:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:29:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:29:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:32:53 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:32:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:32:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:32:53 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:00:33 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:00:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:00:45 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:00:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:00:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5106b06fd3c072093bded94807949d02b5d151d8aa469eeb46a006453a7965c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355c944c4093dc300ebcdafb3bda8a6c9ec4d565280f4214da78dcb5c72d8e8`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 86.2 MB (86247520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a3ee64c140bf6e6df68932390ad89442245fc71e2957dffcd5fd91b5d25c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8490fa290792bd4ae1508b2e69453cf84b93a093779bd2af997a7ac80f5e85`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 3.8 MB (3757190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a76912f0330b5a8e70a8fe111b069c3d44062696c997577bb47dd4a4b8b525`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ef1f39e2cbd10d3c21fd5b455d521b8f52edac13cb84361830d0401e056cac`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efef0f29c620f3102b1cb37a57abdb740e18afa37345163f546b45b7e315db3`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 13.9 MB (13850104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178f3b58b928248d5313cea7c2af0b1191a4134e5a2ea89dcefbeee3867e9558`  
		Last Modified: Wed, 22 Apr 2026 01:33:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701abf00c86fb9ba5d35d547ea7424a7005a7054ac5a6a99ac57e7f7b0bfa52`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 11.6 MB (11617459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1893df0361b2d097c967eb96fb1a8ed66537461ffa47cfaacbd00525053417`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9137d5f6e1867a22561c5d4852fe69d4d5871d641401476fa35959cefd60b9`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344333c00c42b7386ac635f2edc6f7eea53ca2fa38185bcfb85c9c47cfccd2f0`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d097e3f5dc408f7a2ec0f1811eeef125ae55df101558b0b59f1472f8ccfaa7`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd7af921602983bbb84f849980faeae03206451c48016c267efac138fb85d2e`  
		Last Modified: Wed, 22 Apr 2026 04:00:53 GMT  
		Size: 2.4 MB (2423407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd46eaa7f0b8afc693ebc9ac147abaa96e690a6a2fcda89c5adeed6b99dd674`  
		Last Modified: Wed, 22 Apr 2026 04:00:59 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192108aa8a7e7c0156e5d9c86e0ff96c4653ac3d439d341f16057d7e7ee8d02`  
		Last Modified: Wed, 22 Apr 2026 04:01:00 GMT  
		Size: 22.4 MB (22398176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaa66c3db7078e11ce7a6b35effa084a27f2cd317004b643e0d8f5db9d6d83a`  
		Last Modified: Wed, 22 Apr 2026 04:00:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0b8da69cc5561177aed4321e855591775749dcd99c365d47d899fdf5b59370`  
		Last Modified: Wed, 22 Apr 2026 04:00:57 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:2c46c268c61a1ecd5dee08fd6d61ba7cbfd21f3b433de455979424cb92e71042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96950acdfa31d5d16bc845cf7ce279205260039bfb15d82725e61367e7d3fd48`

```dockerfile
```

-	Layers:
	-	`sha256:ffe614280a9b04b1c586f7c9faeb6c8b6c9372de7ad4b4e512fac579471a7ef2`  
		Last Modified: Wed, 22 Apr 2026 04:00:52 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:ab2dcb212c07347abe77449f11cad81b22120cf0dc07e197d68270ade1dba465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196769775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14945bc3708b1df92ba2b2f5fbc29866180f097e40b3ae2491f7aa51b25089a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:15:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:24:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:46 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:46 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 02:41:00 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 02:41:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 02:41:11 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 02:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:41:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e7361c4edf16eb4272307ea2ee57447cf2ec134af0f0326596d3c94a90d7c`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391fd317e2422a2b998a5b8f46476782dda67b0195c064eccf5d895e482ad1b`  
		Last Modified: Wed, 22 Apr 2026 01:19:38 GMT  
		Size: 110.2 MB (110165312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18568485fa5a6e44bf015471b704446b95da6eba7e85f8f6cac1dc351aba16c5`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc61f4154b4e36f9f3303c2b5d7cc39748b46c166e3b463351a9e8cd220f168`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 4.3 MB (4305491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc86735d128f1fbd8106cc32d6afae7a900147daa337150c4739d4f1da4346a`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5795b9e26f314196881b133a91769e53e2828131d098f8db7d9a800b3e89e`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502f96df57cbf4d7939c397fd68491b3e4dc7ff372c63a924fa619428d5ce55`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.9 MB (13852179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c671d94ce0c6c5a51de7fc69370d23707fb0718409f951b587be6798c77cdb`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325d25ee42064c543212ea6c19bbac76a85d4adc1cf6dfcd77fcbd4fe2382b1`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.2 MB (13206146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b47d3caf75cacc27de055e12f70c9488af4a77ec463a8a8803aea30d969715`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab2816bd1e826aae48479663d523550acd969be5b93285569dd982e03a671af`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0f0dbec67a1da7c28e365dadc3da7041014b5b9baf54c270e51e230514fa8`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e7217b1331d5942ccaacf9df0f007a688d6cc47181ba879aa1f856ac11fcc`  
		Last Modified: Wed, 22 Apr 2026 01:27:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa4922aa898ed8d63dca36bc92280eb42fe3d79eb890ddbb2259d0d6f5e41c`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 2.7 MB (2689943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f80fc04bf2842b7907c34cc355b9fbf3a8bf4c940f016885d0c1ac2289bea5`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c238b3cab631145cb2c7fd748f13647a154c52bd26f015e00814d91d30229bf`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 22.4 MB (22399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933121251f2ea8358e789aba4823d58ed5e7d70fccfab2b7639e3a1c51299521`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f08ca589b4bae468116a8f6db8123fa341908d69ef11acf6ae82b48772355a`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:863bad92be9713ba8bcb7beb234be02780085f33286f8e8084008465d3d017e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a11b51a0968c2cf96156db8040090822cc3639a9958977f3d751d1729e91825`

```dockerfile
```

-	Layers:
	-	`sha256:1416c764e4d00d79fc909cbe75de1ee64470178596ed648380f6ea85b2359296`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 37.7 KB (37654 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; 386

```console
$ docker pull matomo@sha256:1c1309fcf70db7d5aada1313f718e3e18653afdc5ff156e0a617eaf48a950ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204710405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1045868eb2c98cf46a416f775849eb27fb25286f9b71a40d65c7023392d62074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:34 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:25:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:25:34 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 05:10:32 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 05:10:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 05:10:43 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 05:10:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:10:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ad892368f928cf2c1259fdac7b49dec39b5e0100dc38505086d1f04fb0223`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a854b9375cf76c04d007410d1b4f9960253c91e039f3fcb12bd3c7da649d1`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 116.1 MB (116144340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b221c038be8eef2d78c984f7ad0d2dc0453d8cdf3bfc51ad75822776b02c5`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea166db99c0aa8459ec40867c9181d68e865592724270ab960b87a59316cef`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 4.5 MB (4458361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ff3928a5ae8b1b558eef86bacf78c1a2d3acee46fe57fbd521c584e8e925`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4831e8917f639e8f5338c7edb49dc14aa2d40befe0ab2492f12791411ce60c42`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ba05e513a80b82c62a1f5983b0933fbd3dfee5e689cea629457ebedbb230`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 13.9 MB (13851522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab312dab66ebf333df3271b5f453521908be468732a06d8501f0c05010dcbb`  
		Last Modified: Wed, 22 Apr 2026 01:25:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a251efd274db5d34c0539ddf36b203537156fff65d0dd99d6206eb755da`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 13.9 MB (13858390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c38f71c21793b514dafb1af49df5345e3a36057bd995386b1721dad70ae5c1`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e3ac463e003ef2a90ed29684c1fec4adb899f721d8ca37df7bdc97f93e810`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abb31896c1032bcf7ef68bd4c309fec9e010b234c4f1ce7bf73c77d7e652cc4`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2e5cc369f5d824ad4e235d2ad3a85a02ecec99498753828309af3d8497942d`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe74de20b0aed283f8dfacadd066c1b866e7e713365c92add76f3eb93a3142f`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 2.7 MB (2695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f70249788be758fa0c374f2201e7ddd74a626cec88d83d55f7f3dbc5336329`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecb4969fd8c7e45f3b01fe4f7674cdf2a81ddcbab2fcd06f95732737d687a0`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 22.4 MB (22399199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6baa5a4e1ac6e37fe0663c2a16a7460de7d4da7e2d9ca774be8bf8f24ab90e`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4d6c98ecf0f190733724883fa2dcfd119ddf57870ea4a110d054bb067bd05`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:07afcb4a3f8ef2f649b1062a2d05b6c9edd68ca33220ab0afe16dd6c1159a6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305e68ddb09754704bb1eedd924f9f348dc2105efd8751945e851f3cd7c15b50`

```dockerfile
```

-	Layers:
	-	`sha256:76a872aab9742b54def28f8f9f09f139870219db07eafec324889e38707ff6a9`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 37.4 KB (37416 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; ppc64le

```console
$ docker pull matomo@sha256:558b509b6c438846c89e60d7ffddafa641cd764bec4f6cfd5f0afeba31d71466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201268007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b0a0f46052ab0d0d7faa5e005cd429839904c722c8e11194972de9c7108608`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:55:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:55:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:24:29 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 02:24:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:30 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:24:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 02:24:30 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 10:55:21 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 10:55:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 10:55:44 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 10:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 10:55:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab63631568fe36922db06d590c893408dd270fd36872c90416de60627387ddce`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 4.9 MB (4881692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438bcf1abed6360e9adac08f804567924b049146c3294914aa102a3f7c41821`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e295926cdc5af3d791955667e4175ebedf05ec97080bd65bd6d11dabf8992`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286ae5221aff2ed1a4a8a4baf4172ad032a7bc332f63f890612205f59604724d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 13.9 MB (13851763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67505e93e2a17315b3576e01845784735fd7612b2eba5ee18fb5e1825fc5a4ec`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c411040503656e63e555235609eca014c8a578020fd6fde25775feb51770f`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 14.0 MB (13956005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d038fd0dacac84a920cc05f508ee5bb0e0c9d08d1a72f3d96e5f75fe524595`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce972e1f08c44df934bf2f5a50d413fa96defc3a3e5af20f6031c30f82275300`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c414f8be1c63ac3c42a432d3030e7c783159d103fd4e5ea6b8df58e8ddfab0d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be4ec9fb48b51715a67384041424d5e3e0e3468e2d9182dc45ad510e144a87`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e884c3d1fa913f34c366a6fc98547d1ecb5b9a27bb1240460902988fc3b0e011`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 3.0 MB (2974034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e2227d7fb70d54ba4b77dcde32ed88eaa5c3f8f8dfbf1cd1ae8b0b99ad878`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dbd12cbf47f04953f09756fbf5445ccad7f5ef3bd747b030e6665e3a5338b8`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 22.4 MB (22399966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8bf5242f2944c1380e67fdc6dc45d28378163497c60bb8cd85b2e5b755313`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19871154c75f6f17ec259370a7742b4dccce1bb26d6fd0c5c1c80710563430`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:d9af1012a7106008ad18566e1e554936ff4d4f022d85bdcfa51a76b580738c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97b8ae50ab4be24e976ede726bf8780e1f869f862f8280567dd5fb333468e07`

```dockerfile
```

-	Layers:
	-	`sha256:c3509d9b911e4d1b3ec37730332352101ca474bd7ff9f59709e048ba9e1376f7`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; riscv64

```console
$ docker pull matomo@sha256:1b1374d4bf1624ec39522f6940af9e6b78bfd5f869278ffeb9e6c4bf0b4cb928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233788266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a814b40196d1c72ad00aafed53c670ab9aae9c4d1c996b9814241f18e6086`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 11:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 11:52:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 11:52:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 16:36:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 16:36:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 17:30:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 17:30:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 17:30:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:53 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 17:30:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 17:30:53 GMT
CMD ["apache2-foreground"]
# Sun, 12 Apr 2026 13:02:30 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sun, 12 Apr 2026 13:02:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
ENV MATOMO_VERSION=5.8.0
# Sun, 12 Apr 2026 13:03:52 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 13:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 12 Apr 2026 13:03:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1748d653b8c3ed98b870438732aa56def2ef4f267a38a228a8d4e1a775744da`  
		Last Modified: Tue, 07 Apr 2026 12:53:25 GMT  
		Size: 4.0 MB (4031244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79c952e0710b8d660c2b70f3e9f2716a16833b628e3b2dd090af31c1cf7438`  
		Last Modified: Tue, 07 Apr 2026 12:53:24 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe6480453dd1cec4db695c1e657272ce31a8c86abec42383da6aa9846d7dc4`  
		Last Modified: Tue, 07 Apr 2026 12:53:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dacce83cf82615cd1d4a6c1a86cea6e40883d3a42ad8656c9b8763530155814`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 13.9 MB (13866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3323b96cffff08af8f445b80f611ebe68799371d01077775a0c3f4567380bd`  
		Last Modified: Fri, 10 Apr 2026 17:34:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e4e9e187467f7ffbcfe1cdf4d10ee90f6ee36da3b522274275365cc718ee0`  
		Last Modified: Fri, 10 Apr 2026 17:34:06 GMT  
		Size: 16.0 MB (16013910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb761f6a2a209495608bb857bb80d3d0d0aa4de2fb075e52945a24da89addada`  
		Last Modified: Fri, 10 Apr 2026 17:34:01 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ced9f37602f905311a1e2a29a005c079a57757cdbf7e7fb075022b1a0f660b`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494a5659332e0f15ed2f4d61e062b27c51744e0fa85863035bb125c624a2ad0`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6cee257162c3d59f0cd7d2be13c20ecd7f6bf71c712eecacc44cc33a5fec83`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c54731eefd24f5be8c3be0e167304e36cc69b70462507d80ccee20c97285125`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 2.6 MB (2614022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93170443e6c9159fcbd88f4c341eeeea304875579d3f0a96e2d394517a45ab0c`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72489f0fe05b81788af39c9e702ce18d653102a5f9d70840781a6456c6da216f`  
		Last Modified: Sun, 12 Apr 2026 13:05:15 GMT  
		Size: 22.4 MB (22400287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29582f6aa97de83cc2e3b1070f8e16811e430db99830c4548ff4151cef5d682e`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae08e7812254f8597aa1f47af714fb516cac8f33972c277e72c29956b6ef64`  
		Last Modified: Sun, 12 Apr 2026 13:05:12 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:044fd16450e94817d1f1ebc47d8b8d9709562399d3f06bd84151c253155e6ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8cbd64c659d77d407cb66fe3189531945fc5fe28c9849fa3a4e57c61cada0`

```dockerfile
```

-	Layers:
	-	`sha256:791843956f9e2428ebb0d78e1b2c97d5ddb76f0011b84c41f30227973e1d00db`  
		Last Modified: Sun, 12 Apr 2026 13:05:10 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:apache` - linux; s390x

```console
$ docker pull matomo@sha256:6cf85e049fc320cd8aec35cc44d082d802da2c38536f6bbdd501de2103e81c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179059874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995327f35af3666a70c2b8f73cbabc6e04075ad4e578d7161973c87c00ca4aa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:39 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:37:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:37:39 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:41:27 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:41:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:41:38 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:41:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ece9a9560b771b29f91d1b2fa69377a7a6998382890ab15dc4a92ce806048b`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ccbb849cf7d524fb26003a40a6f2ddbd73713723d4bf57178fec331c8472df`  
		Last Modified: Wed, 22 Apr 2026 01:27:55 GMT  
		Size: 92.6 MB (92573082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdb404da573a86ead75a2c55d7c0f8bd69a0480a6e1e9d1e17b114c37703861`  
		Last Modified: Wed, 22 Apr 2026 01:27:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7964dc0539da49b7d15124dd7f7170a7706b36795438d37e1b510fef67d922`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 4.3 MB (4329303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d928c48d6c321d2eeb66c3c389766cf9ae0d3b52927919a0fb9928aa3790f1`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cc4503afd2ec97db21c3221acd45b9429c93ad112050f26555547d7899269`  
		Last Modified: Wed, 22 Apr 2026 01:27:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ccf2ac717c82b15002dd84ef1d42b8130bd9336b5ee96c48db314d863c1a`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 13.9 MB (13850951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d18571a8b1fd3a48f17e0ed57746721b5633a3d9d6fa17bea75e647e5dadb2`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af7cd74da0af1e5075282c2cb414e4d83acaeeb6bd637c46acbf94b5414eaa`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 13.3 MB (13311877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d5c986b0140b3c1c0aadeb97c7c15b48faacd44db4831ea9d0d2fffab85e97`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd187c896be49dc43ba8e03a8e69c5e53fe53aec2711d75d512f702105a9e6`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1dcabe41bbe8315743a1f135c7e213230ec4c4802210eac62355753a21234`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f3b59bcfa40537a6d7da3db395965ad05e8bb13ba9c58d1bd555b7be4cdcd0`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12d807e0e3c374569c0b1e1b7e34053e827157eb1bdaf0a8d4352ed9566c33`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 2.7 MB (2748316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bcd04f47c821ef46e5f55b5e15f7b9ab6e8255eda8e16a77b1c0651c988eb0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3591996980aec43931f2cfd37dc3c0d7757b9e8252e4c9da2ac3ee6f7ac5da`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 22.4 MB (22398820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93afd3e6d8bb757c222e5ddb8be065f77013e9147fd82999457b98952f458bd0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d977a5ee6fe1cdfefa7fd25d7e089a23e5adc1380e201464878e0cc3358b254`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:apache` - unknown; unknown

```console
$ docker pull matomo@sha256:35e05b0967102445629beffe14fdb57e770914fa2607f0247303bcb44928be5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aee6ace1d2419bac32bedf90aece37b63bb8077a84f38e86eea3c24580010b`

```dockerfile
```

-	Layers:
	-	`sha256:bf0616b74b590e9ac3532d9d0e1826d70f42f64c7bdf51345482ea2dabca15b7`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 37.5 KB (37466 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:fpm`

```console
$ docker pull matomo@sha256:12cca10b57291eeece1b5379e1de7d79a64cd004e721086e23cd74a694cd59ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:fpm` - linux; amd64

```console
$ docker pull matomo@sha256:710598e9b5782d7decbbd2b3fc03d429db93489c7272c5457b3b4100f77bd2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200234403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c685b4d923afe384af898efc7b268f9f42ca2b8cc63cee09bb7b4034a4bb5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:30 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:28:05 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:28:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:28:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:28:05 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:28:05 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:52:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:52:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:52:49 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:52:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:58 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:52:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:52:58 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:52:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:52:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3e427b1d425dd16f39094572ce5dafba4053375f058521058ffe66a8a08c4b`  
		Last Modified: Wed, 22 Apr 2026 01:25:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32fe875c9f9eace2d0f6384ad31d970a8b3af511137e1e8cfc4a3185ccbbc97`  
		Last Modified: Wed, 22 Apr 2026 01:25:30 GMT  
		Size: 117.8 MB (117842644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f934793218e2ce567e18037b6afc9ffbf4e872ce44616bf5d481a5a71cb94ae`  
		Last Modified: Wed, 22 Apr 2026 01:25:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342f4bf50b5034c0f35a87263038654cda7c935ef0277f1c079f515bb4f1f857`  
		Last Modified: Wed, 22 Apr 2026 01:28:16 GMT  
		Size: 13.8 MB (13833818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b3fbcca5d92b01137fc6843512c1474da5212e74888f649c95d50d0f45d8d`  
		Last Modified: Wed, 22 Apr 2026 01:28:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2dd358023fed96e25674a1e5b934d1e3b38a953aaae3d98d31c2774b955a29`  
		Last Modified: Wed, 22 Apr 2026 01:28:15 GMT  
		Size: 13.7 MB (13691364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17da2e8e93dfcebc9ccd0eca5464f06206a170793b4504b77a3febaa3f38716`  
		Last Modified: Wed, 22 Apr 2026 01:28:15 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e7ed16b284ade9be62b85d67e85b32539006905c05c01c4a3f969ef224ecf`  
		Last Modified: Wed, 22 Apr 2026 01:28:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7122489bbe4d0e843fe308e2a9505ce7149dc3958344f46c0b6acc3d12e056f`  
		Last Modified: Wed, 22 Apr 2026 01:28:16 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a55794049acce36f6ae1a2c2d46d53e84eefada5b0192556bf8c12540bc8cc8`  
		Last Modified: Wed, 22 Apr 2026 01:28:17 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656f0b430fde31ec31f389f29673dd9f4006ae14a0833c32a421f15c1dfe0815`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 2.7 MB (2694911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3248f4a587728bc1b02068f9ac6f9d6354fca35d1737138a6f5e18f6ddd417`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30e27799776718db3672fec967e75dd4f043b9d922b7f45ac8f48e388249897`  
		Last Modified: Wed, 22 Apr 2026 04:53:06 GMT  
		Size: 22.4 MB (22376818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b4b956f172489676a03278be713601c3449126e08c7ef46329bf7a1b679958`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838019e911cce957e670f00152dba0c1957e61bebfaf5fd7d1914edd684f9f25`  
		Last Modified: Wed, 22 Apr 2026 04:53:06 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:ca0a8db5345d7b2dc61be7e21f155dbd36e5d06566e70e21a47d02af766013b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f81feab3ef575dbca3e084f5b7658208ba6851570459bc3e455630461816f99`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c47479e919f704dc152a29ea6fc5257a1fbea1ed57206b4635115e106c052`  
		Last Modified: Wed, 22 Apr 2026 04:53:05 GMT  
		Size: 33.2 KB (33247 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm variant v5

```console
$ docker pull matomo@sha256:bc735a61c96bed63c6da03c6e1e6ba4af467998e0ed521cd93b8644860c2e514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173814214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf32aece57f5e841f58ad8adee9a7cb2195add1e9cdfb49ee1c8988c253cc97d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:20:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:20:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:14 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:31:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:31:14 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:31:14 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 03:41:51 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 03:41:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:41:52 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:41:52 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 03:42:08 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:42:08 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 03:42:08 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 03:42:08 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 03:42:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 03:42:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceb84c9f466573920de66d24a34f2c68c19bcf0a1b2c264f34c332471c69fb9`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d33534dd8e573ebb0c8014512c21ee46f5bdb0a9a8bed6d2c2c4a536a5c0601`  
		Last Modified: Wed, 22 Apr 2026 01:24:12 GMT  
		Size: 94.9 MB (94884496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d956e9df4e4f3f00f9b8089a0a62668d9ac506d5116beec87459b0a803584220`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c7a86002d0cf82ec530b94e216fd8f013d7010b9c6dfda5ca8def8d13207e`  
		Last Modified: Wed, 22 Apr 2026 01:31:24 GMT  
		Size: 13.8 MB (13831363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e6e39bf4d8c54d24a63940c3934a18b6a289beda740be95a30dced7a41f0a`  
		Last Modified: Wed, 22 Apr 2026 01:31:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae7ca7c7642e9c4e422bae51701bcec334d5cc8bf1c8d1a71d87c350006383`  
		Last Modified: Wed, 22 Apr 2026 01:31:25 GMT  
		Size: 12.2 MB (12242217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97bb8469d1f54dc7168ce6fcf9f91193a064dd380736b62ffeb332eb015a7f`  
		Last Modified: Wed, 22 Apr 2026 01:31:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2467f5b8fe9db39a57179044bc6b28c10a10de883418437d9a9ae12bbfecbf4d`  
		Last Modified: Wed, 22 Apr 2026 01:31:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef2d69f9cfb30f9818c1b6933bf04057906707a7b4a229f002d70d7e766b326`  
		Last Modified: Wed, 22 Apr 2026 01:31:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0092956d054a82c6c158d383c7c03cdb07936473a1c53cefcffaeccb843e62`  
		Last Modified: Wed, 22 Apr 2026 01:31:26 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138e335c64da8e1fb0dd5c0e6d16577e4a3b261c8de218218e498153c44118cc`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 2.5 MB (2518332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752163400c54dd6cb3282313983bf2d39e4d3e2a17a1c1172fd1014ba59ed17c`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501fd7e5e435094c6e9c12cd751ff4736eeb4cc45fa4b35de8086d37178522c`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 22.4 MB (22374943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32efa751fe756435801240ad9a66fa82ba55aa851e627e18456e9bc1df9c957`  
		Last Modified: Wed, 22 Apr 2026 03:42:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5adfa7b73930f455eba3b122867f1e9919d182c94badba206821594a885e89`  
		Last Modified: Wed, 22 Apr 2026 03:42:16 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:c8663fd98695dd6f3990b4479313a67d3a9ae92296309c557c70d6879f83ed2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57991c3f863e7503041e69d52cb8b993b531d9e976b1d347814fb4ad14a7dbda`

```dockerfile
```

-	Layers:
	-	`sha256:2844cfbfa4edde2cd056cbb74d8ad5f0a438c4a8b52c4711c07994f0f3ca7a39`  
		Last Modified: Wed, 22 Apr 2026 03:42:14 GMT  
		Size: 33.3 KB (33348 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm variant v7

```console
$ docker pull matomo@sha256:35f7cc08b2f483d437498549400b3f405a27f60b4597d11724d06d0c2695b8be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162663283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffe871bd97e2752c20a1e4b69b59e8b607c5468f1550d6dc5a65a2bc4f6c24a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:31:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:31:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:33:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:33:38 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:33:39 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:33:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:33:39 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:33:39 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:00:40 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:00:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:00:40 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:00:54 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:54 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:00:54 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:00:54 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:00:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:00:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55902cd11f5cee73e37dd6b7274ad068d6ab77feb8165d071674df0ccf38417`  
		Last Modified: Wed, 22 Apr 2026 01:26:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0b5ea04af6bac36d38da15e40540ff669cfc9d5141d6bcab3317138fc62e3f`  
		Last Modified: Wed, 22 Apr 2026 01:27:02 GMT  
		Size: 86.2 MB (86248228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25364998dea0b06b29b1751f14ff8ba40896bb1fc689649eec92f9c35da15d3`  
		Last Modified: Wed, 22 Apr 2026 01:26:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53652e91bb75567649cbe37e0295b5f321f34db9e9bd71defbde7045ea5b2ef`  
		Last Modified: Wed, 22 Apr 2026 01:33:49 GMT  
		Size: 13.8 MB (13831498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bd347c00b03d789171cd29fdb3ff73232e46767edad9fa67ad3cbdeb0c12`  
		Last Modified: Wed, 22 Apr 2026 01:33:49 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7ec168117e0ec7749daab8645c027b86821d2770688ce0c8f989a6dcbb0fd5`  
		Last Modified: Wed, 22 Apr 2026 01:33:49 GMT  
		Size: 11.6 MB (11578134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e67a910b1bc5a88ffabfca6de789363c93c9197fe665cdfa48ddd5061ffb918`  
		Last Modified: Wed, 22 Apr 2026 01:33:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867543f872b7d68cc584e2bccfc9326f139460fb0abbfe0b5088450a1bff8e09`  
		Last Modified: Wed, 22 Apr 2026 01:33:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f9d8517c2f282b742135496a0b92c3233029e6943e96c6d3c16cf28f7e6935`  
		Last Modified: Wed, 22 Apr 2026 01:33:50 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6ce405333963fdc520e92d36f4d5bb377e38403cfcabaa518f073f5212a153`  
		Last Modified: Wed, 22 Apr 2026 01:33:50 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92224881ecbdd8d334354f500189752c1c3f88a11559131b192a4462f574ad8d`  
		Last Modified: Wed, 22 Apr 2026 04:01:04 GMT  
		Size: 2.4 MB (2400825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea02161be504b52e539efc900c7358b3028631c2762498779cf56b20bcc8c5b3`  
		Last Modified: Wed, 22 Apr 2026 04:01:06 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312dad7da0e41b7f3e862b95f65972ba4edf051e8ae52d755abd8a2a67510bb`  
		Last Modified: Wed, 22 Apr 2026 04:01:23 GMT  
		Size: 22.4 MB (22375083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1062e0bde1d15312ab54ebdc046e4d7614833837f09b0ffc042edfd949e1224`  
		Last Modified: Wed, 22 Apr 2026 04:01:27 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe99439af59ee10b75ecb05810ad1219ba8b05c6194bcd6691b58f2595727f`  
		Last Modified: Wed, 22 Apr 2026 04:01:28 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:59907d6c34327f3fac9bbccc4aa379bc144f5a257aca082fddf5d358b5ba4655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acf3c9b7f340ccd3cacc45bc0bfcc60b31773fa2806709f476229413968c82a`

```dockerfile
```

-	Layers:
	-	`sha256:077d79428eb9e0f2a19de16b58851cc959f6c26040d9364b95cb8cae9cf2eb9f`  
		Last Modified: Wed, 22 Apr 2026 04:01:04 GMT  
		Size: 33.3 KB (33348 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:93a9138c384e4766c0f748eacafbf632f8aed00184b7e5ea8efd242c817dbf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192547517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511c092be200738af47f6a3664ce85d7ae94019353f9e48501b3b7061942f23c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:25:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:25:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:40 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:28:52 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:28:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:28:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:28:52 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:28:52 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 02:41:05 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 02:41:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:05 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:41:05 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 02:41:14 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:14 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 02:41:14 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:41:14 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 02:41:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:41:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf58408576af2949270f11d85790f89b2b7f90001101ca6a168af36b90ec241`  
		Last Modified: Wed, 22 Apr 2026 01:29:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73df2ee54d67d8da4777af2387c44849e36a7079172ac5d98d34d05857d9811d`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 110.2 MB (110164886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be478d67298ff292bb2ac64cb4620e7a85bd9fdb97f4560ebfa7c52abcfda9c`  
		Last Modified: Wed, 22 Apr 2026 01:29:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f6ab9342fc1c138b193bfecfcfba6e6a2bcb986e1f808905cab9613a10565a`  
		Last Modified: Wed, 22 Apr 2026 01:29:13 GMT  
		Size: 13.8 MB (13833355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88fc6d051913dbea29e6527c934049337911e3918aced0cf00cc2901674d04e`  
		Last Modified: Wed, 22 Apr 2026 01:29:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c4b9b85deed42586236b7e0713b199505777171a5d84e72fe121c9cf965cf`  
		Last Modified: Wed, 22 Apr 2026 01:29:14 GMT  
		Size: 13.3 MB (13347436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7870b2dffe2752d9dd4369c99dfdb604c5866e584fb6f7a059518a6ffd639`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f4a215ef981c4758dd3a96fa6fe44f201ddde1ef4fdbaeec265180fb88247`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa24fc68f67212fcace70385af136b353aed829577a69f85e4f4bc94fbd6d397`  
		Last Modified: Wed, 22 Apr 2026 01:29:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfab259c828b009e3663f691e187f018707b736687e11fc8762b82688916a64`  
		Last Modified: Wed, 22 Apr 2026 01:29:16 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b113e63d84bf51765b53a67eb577d3d7436715da1bee70eac3a8dafa34e1d91f`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 2.7 MB (2667030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55aca8a952c0d444057893da765e743fc86341090970417f3c51681517834005`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280f9645fe5177875bb655252b4ccb988b8df7147fbb67104bf3672b5784a58a`  
		Last Modified: Wed, 22 Apr 2026 02:41:22 GMT  
		Size: 22.4 MB (22376529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac4412f8e8868c46a46a4c50173cc3a35753e5b74a3ba6c0aa121e820fc683`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b254226281f0a3967a19acd3bcafe60c94cb8f014b31f50e0ae92fa3ad28d2`  
		Last Modified: Wed, 22 Apr 2026 02:41:22 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:880dfe07e9d57fa9c74614df7484751dc1bc7e119a4cb300184eeb7a5774f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1542439493a639d4937252c4a5fcd2d91f5e60093507fc4b638fd1806eff2d6d`

```dockerfile
```

-	Layers:
	-	`sha256:803dfdf7f694a724ef09d54b5a9c47e68d30cb1a6d3390c3845fc3ec4ad83196`  
		Last Modified: Wed, 22 Apr 2026 02:41:21 GMT  
		Size: 33.4 KB (33382 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; 386

```console
$ docker pull matomo@sha256:6cd72f57168134dc856dfb50f985473c9df9c9230056bf11538465b9027d9937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200318576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ef79765cf196a28e3b4e3ebbc62dd1abeb4f24f8355f5ff690fbe37747b5b9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:18:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:18:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:18:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:18:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:01 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:25:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:25:01 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:25:01 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 05:10:41 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 05:10:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:10:41 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 05:10:53 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:53 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 05:10:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:10:53 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 05:10:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:10:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8563d86caa1b64b3c5a8f33ed6ea2513154a20313e9cc080e11259de2a9e0ea4`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce65dbe4c3b52070c1a4481a910d3917a82aaec9b107415b798388785ce7c2de`  
		Last Modified: Wed, 22 Apr 2026 01:21:55 GMT  
		Size: 116.1 MB (116144400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64874dcfcd41d63e88c04482c6ebbe34a9b64d9026562f74bc7fd128d4ab503d`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7843bdfd3e5bef86fb4a2db1cbd7684da9701341b71092f7553a4833a19536`  
		Last Modified: Wed, 22 Apr 2026 01:25:12 GMT  
		Size: 13.8 MB (13832785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f45043fb34da86612cfee1ec3bb75a574799a2b0017c8b95d25bf16aeffc0b`  
		Last Modified: Wed, 22 Apr 2026 01:25:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54667adee37dac9923958a56f911728a8970570b1f31425b5ca5413d454320a9`  
		Last Modified: Wed, 22 Apr 2026 01:25:12 GMT  
		Size: 14.0 MB (13982222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9575ffc62cd44336c2017d3988602129522f90e7ca1eca4d6b0523aae083745`  
		Last Modified: Wed, 22 Apr 2026 01:25:12 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ad35c8ef467d6b726752ae72175016c0e9d101f18f3487871de94e08a52cf9`  
		Last Modified: Wed, 22 Apr 2026 01:25:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d84ad638d9198e79a6a03d866a0d835af8d1a28da961e44f7975bd67905a22b`  
		Last Modified: Wed, 22 Apr 2026 01:25:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658b4d5df669458f134b0ec1768f5e9d318a5871e21c79500d75162dfc95b503`  
		Last Modified: Wed, 22 Apr 2026 01:25:14 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582a0dced91d8d9a94d400b52f1f4ebb14ecb1b84552be7a9cc0b06c410d7e24`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 2.7 MB (2672048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c4d1c2351646088f2f8d751deaa69cb4c71b25d174736de139f45cddbc791a`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6e93e192aa5455a940cb277e2b72f856c76b65faeddef95dfd1c901502ad87`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 22.4 MB (22376123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5477b881c2462f05da0c5839f438ca55d1db4042f069ef5e85893230d696`  
		Last Modified: Wed, 22 Apr 2026 05:11:00 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe04bc85078a24980577892bdb2156de6744f67b6f8b509fd97af4aaa924b3a`  
		Last Modified: Wed, 22 Apr 2026 05:11:01 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:a2e860183a215e5d92a208478957ca2f557d08cf787b0d1eea85ddf5528233c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a620106732531c56dfda4765383ab1065582be32c60755815df6050352d99903`

```dockerfile
```

-	Layers:
	-	`sha256:540f104f6445164c8e63d57d2e454789cdd02d23e89ad8c7f606a1443e8fe7b6`  
		Last Modified: Wed, 22 Apr 2026 05:10:59 GMT  
		Size: 33.2 KB (33212 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; ppc64le

```console
$ docker pull matomo@sha256:2272d049c167970b58114120c97e04ac95243b0ac4d4709985f501c921288a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196589128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8660a06ec7a51d3b4d79c2ebfb775636687459a7e5cbfc5f05f15bdb9eddec3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:54:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:29:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:29:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:29:00 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:29:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 02:29:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 02:29:01 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 02:29:01 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 10:58:10 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 10:58:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:58:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 10:58:11 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 10:58:33 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:58:33 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 10:58:34 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 10:58:34 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 10:58:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 10:58:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b5847d95feef86743cbd49c633eb60f2ff5fe302e71093f49fbd2320e1d58`  
		Last Modified: Wed, 22 Apr 2026 02:24:03 GMT  
		Size: 13.8 MB (13833103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b8e5fda2efc50218998dd81d724b6628613051cf19a1910551da522c682a78`  
		Last Modified: Wed, 22 Apr 2026 02:24:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982b00cc68c3293e74b57069ebee18bfb120fd36d88dbfebbf2b9a65911fa379`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 14.2 MB (14216593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c4a379ef2f399d72ca01f374eaa921c02a69167826bb2c3e0829d8906fac45`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e895ecc092a768d556e7735d4ad08f7b02d9251191e053d07a267350128f47`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3916d2e474ef6e91c9eebef2373811cf9ef128ca7891f0cdb6e790747598f41`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f1fed36adf60cc812d5d5ac75e5173f419b3ee00d8175c70fe1248910c1870`  
		Last Modified: Wed, 22 Apr 2026 02:29:22 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244a2ad125d492fe8f68320f86813741af59f922cbd19ac74a42191a61493e9`  
		Last Modified: Wed, 22 Apr 2026 10:58:47 GMT  
		Size: 3.0 MB (2950748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e1d38fb371a11279ead74d150bcc58fac098ae7db0cbf38fea7098ecbf3325`  
		Last Modified: Wed, 22 Apr 2026 10:58:46 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2b55ea9e92b219dd33654b8fa5613df6529783053395015869d5b04349294`  
		Last Modified: Wed, 22 Apr 2026 10:58:47 GMT  
		Size: 22.4 MB (22376692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92c866d0e345fb64e1b9f03fd52d93306619c265245058a1bd262d8768e02b0`  
		Last Modified: Wed, 22 Apr 2026 10:58:46 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c0e2d7ff69124209de8849ce1ccd0e8618f566551107a6fec927adc1e4ca34`  
		Last Modified: Wed, 22 Apr 2026 10:58:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:74aa06715616364d79051eedbf9462a7711558a23ec56feb8a76581ba62cf670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66792397d53c1908cb44188f94433a16391e9ae7b18a161b32146349a953ee9f`

```dockerfile
```

-	Layers:
	-	`sha256:55c7332afff313e603a3d1bcf6b01bc25c1dad58ec2e743c2a5a244c81660bcd`  
		Last Modified: Wed, 22 Apr 2026 10:58:46 GMT  
		Size: 33.3 KB (33296 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; riscv64

```console
$ docker pull matomo@sha256:504f2c73659274722e9f667c69c87d8a14c741503b5908f0df88b33aecab39b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229873784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df5a51a4832edd12ad746268e4810d53d872950442c60d6fbf552e82d64d3ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 10:47:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 15:38:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 15:38:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 18:28:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 18:28:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 18:28:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 18:28:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 18:28:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 18:28:22 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 18:28:23 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 18:28:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 18:28:23 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 18:28:23 GMT
CMD ["php-fpm"]
# Sun, 12 Apr 2026 13:17:10 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sun, 12 Apr 2026 13:17:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:17:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 13:17:10 GMT
ENV MATOMO_VERSION=5.8.0
# Sun, 12 Apr 2026 13:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:18:33 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Sun, 12 Apr 2026 13:18:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 12 Apr 2026 13:18:33 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 13:18:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 12 Apr 2026 13:18:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773a2a196a80b508d441421fafe9f9f2b0687fe4d6110d2eef7685df3c398534`  
		Last Modified: Fri, 10 Apr 2026 16:34:41 GMT  
		Size: 13.8 MB (13847821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c66f4a1e9830c2bd547f6ca1e7d6b7bc3890378e6e846822db9ce8b636016`  
		Last Modified: Fri, 10 Apr 2026 16:34:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec49cf72012e3dbfcdf19461fac9bf43e6dcfaaa4da30b1530d748ccdf898eb2`  
		Last Modified: Fri, 10 Apr 2026 18:31:23 GMT  
		Size: 16.2 MB (16188977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c2d283ba34d67ffc81547f065b648e98c2206a8fb5e3169d48df92b2807f46`  
		Last Modified: Fri, 10 Apr 2026 18:31:20 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9a5cd3a99b08449087aceea0a1b678e590e563979ed733b09f33e8f84eef84`  
		Last Modified: Fri, 10 Apr 2026 18:31:20 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f307b71a024f957a1e073f50d366fe9e9c7f1720112a04b1d5c90a790582d4`  
		Last Modified: Fri, 10 Apr 2026 18:31:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2ad55814a4f1eb12dee4f88c8e63ff806bcfb57804b4b32b007ddc607fa61`  
		Last Modified: Fri, 10 Apr 2026 18:31:22 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb0bf8c414152e8b464008ed0d044a4f3b108d8da4ebb99587312044dc46bc7`  
		Last Modified: Sun, 12 Apr 2026 13:19:51 GMT  
		Size: 2.6 MB (2590769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee34030f3b64b2b898502de6175d8e66be8ec177857b7364a7a07c1942cd5c3`  
		Last Modified: Sun, 12 Apr 2026 13:19:50 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8069510d0fbefe136426e097f0e918a824b46cfc3cd8b9f2c21388ab2dfc59`  
		Last Modified: Sun, 12 Apr 2026 13:19:54 GMT  
		Size: 22.4 MB (22376758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc66dacc90ab2af8a18d581367caea0c142823a8d9a4ae38b5158ffe984a417b`  
		Last Modified: Sun, 12 Apr 2026 13:19:50 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22255be07b517bac69a6e8929520f6b238a66ad8483eae51d0f8f53940f1827`  
		Last Modified: Sun, 12 Apr 2026 13:19:51 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:7a0fee42aef504131a9af146743489743ab72ad8ff64cd16b2051beeb1226226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fe6d5e964aff0bb9de72a8a304ffa76e9dab2bbe4afda31816f9b1a9fb6b43`

```dockerfile
```

-	Layers:
	-	`sha256:5e114abf31929431b1e11182ae38cc27b1419e6e1bb42f9f47f2dd78dc7cc7b4`  
		Last Modified: Sun, 12 Apr 2026 13:19:49 GMT  
		Size: 33.3 KB (33296 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; s390x

```console
$ docker pull matomo@sha256:fdb7a8c553a3bcec9370b68fc3e921d7eb324c289414a9db062aea35a15d3969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174823600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddfcbe7a129e8312ea22bcb3f049fde87d1ab8158dfc59afad1e211d1862f13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:33:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:37:56 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:37:56 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:41:47 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:41:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:41:47 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:41:58 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:58 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:41:58 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:41:58 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:41:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:41:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757f702e0a9ae41a0668944dbb4c245387fe46a7b86e9158d6238a0a7a2e8d3b`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4485b6f62a7b6c400504342749f4784b13250b4a4923fa17548e35ec69126`  
		Last Modified: Wed, 22 Apr 2026 01:26:48 GMT  
		Size: 92.6 MB (92572845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521371e2b81d32dcc512c19954776e0f6ba6f3e6d3ab464b138a9d29e2737a4`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895072f1915069db96de1e6cd2775cfc97d31d00723b0b58b689f76a62b114b4`  
		Last Modified: Wed, 22 Apr 2026 01:37:07 GMT  
		Size: 13.8 MB (13832213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e06742a171f68cde5770d70c17567b9188ea34dedcf5227404e9cec8cb39c`  
		Last Modified: Wed, 22 Apr 2026 01:37:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618e083a88d6c35da869cebae5f113b9d04739889d9759e66ea3a3ac03dbfd44`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 13.5 MB (13462525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1f567e1ecc28a79a4def138b98f18610cdf8cbc4c52e98b56481eaae456cec`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bc44b21c26e70bb61141c8e8efce2d9f0f970663295792c1e4aee3edd1056b`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3b2142ea31f473941f8b36e1138fb495ed25f97b049103d4bb8307d58dd432`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02955ca59e915e77d99e4d867b1d53eabb24d3af4353fb49005525fc7de8a345`  
		Last Modified: Wed, 22 Apr 2026 01:38:15 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5724c2aa0fdc2900032153f14dac2022d56635de1dae751ab643b55baec1366`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 2.7 MB (2725455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf960f67b40800005e95b318e3eeb609c4087091a12b34d7a8a6eb293a5f23a`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87699047e6d8b2d3b9d950fe583d407a20d59d56c4fa4cd138edecd085fbf5a2`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 22.4 MB (22375590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f2d8de858a4c4cbe613043364f7769968d21ab526bfd7ea1dfa367e8ab2f8`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ef3f67459ea00f232576b036cb8350926e3e14fd70267673b60891c3f22293`  
		Last Modified: Wed, 22 Apr 2026 04:42:10 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:138516e39207d526251e66847d67b8d791985960062b10337dd8878f1eaac691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863d1496ae174a7130582b30322b91afde58ca0f565b4ee4415587ba04bc044`

```dockerfile
```

-	Layers:
	-	`sha256:5ee4dacdcb3405a3757d64b5d29b8b18b8be9f7ba74afe46dec2188df9501152`  
		Last Modified: Wed, 22 Apr 2026 04:42:09 GMT  
		Size: 33.2 KB (33241 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:fpm-alpine`

```console
$ docker pull matomo@sha256:ec311e446452a864e627f50a6b318a43b2f78d0b354302e5e66fac0fac74af66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:fpm-alpine` - linux; amd64

```console
$ docker pull matomo@sha256:72b62e5007021941fb18fad0092abdf162db8235c4a80f087a9267b6253c57df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61540623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0cabaf43e5695e72598809dfbe5c8a6bbfe74b9b14bff6f7f8dbdaba53df18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:18:07 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:27 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:21:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:21:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:21:27 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:21:27 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:40:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:40:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:40:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:40:12 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:40:17 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:40:17 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:40:17 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:40:17 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:40:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ef6327a484adad40c70cc6260e6c05b6496a95d7f17bc657f1608ef1d98c65`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 3.6 MB (3587421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34a3b26ad831d1b88e28205d0697d293a6b9bd48bba6c0618d2a962f6b7ab5`  
		Last Modified: Wed, 15 Apr 2026 20:21:17 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd24741e080b2f5812c84cec27dcacc6faa6834e57a410d0498f39e3f589d63e`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae9fc1b3d2fd71e5fe569524101eda391f21af0725aee92bb039cd3e3e2ec9`  
		Last Modified: Wed, 15 Apr 2026 20:21:35 GMT  
		Size: 13.7 MB (13709881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cfb46d077b27f03899c4f08b5ebd738a21e79448dda30c53e084e4d1ee1b0`  
		Last Modified: Wed, 15 Apr 2026 20:21:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6b4452123be6c2fb9a132b567d46df619e884ca6553bb2e96c5073a44ac072`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 15.2 MB (15201457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5ec8e36b924dcf98696ef1cf37b7f68a7521e815288899c6939d7bcddb5012`  
		Last Modified: Wed, 15 Apr 2026 20:21:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbd3ef9745bc4e4b2d2170cdc2beda14f18aba440b3973124628fe77aeb08b0`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 23.4 KB (23403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80181fe3ced17e0662a1f6639130ad39f9d44b208813f75cb2e77e3597e4da87`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 23.4 KB (23414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9440a7ee03ff048797e0bc98dadb4bca879b081ddaf7f005cad80dbb7c779`  
		Last Modified: Wed, 15 Apr 2026 20:21:36 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d4b1b4dbe81b9fe09ec6ec1761a13158d3d145cbf72cc0877c504ff9d9cd7`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 2.8 MB (2831499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbea798e96b34fabcf879b361adf2af38240de2f967cd83b69304814b1b694e`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47a9a5f11dcce9aab63cd78b9ddcf6b3ebacfa4a2433efb10eca5376a22c48e`  
		Last Modified: Wed, 15 Apr 2026 21:40:24 GMT  
		Size: 22.3 MB (22284502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce0484c5dfcfc4b17ba7e7b613af52b345be0a44b3361b35d2667f4c6edb3ca`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb7146fed469c7aa1859ad6adde3c2b4651fecf80853f198e35c37d2f5f34e`  
		Last Modified: Wed, 15 Apr 2026 21:40:24 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:ba8dcc95c947eaa034fdda8e7b2b3cd7453242fc3866f9d4f9f8805d78ec36f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3038f594426ec8336580b4aaa8d4980b35e97b46a0a9b8aee6de9b1320711e7`

```dockerfile
```

-	Layers:
	-	`sha256:c21e15fb76d20c33ee35709095ce1aea37a8f34a7d2668b4e17a62c0af8110c6`  
		Last Modified: Wed, 15 Apr 2026 21:40:23 GMT  
		Size: 31.5 KB (31504 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm variant v6

```console
$ docker pull matomo@sha256:b38857024c83a976168e465415879c08785c837559c196d8de9ee5ceb2527428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59532340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8230318ab3cf0aa8b5baac55eb35a00d09d5f958e63871a6edcf5d561348c081`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:21:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:21:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:21:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:21:52 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:21:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:21:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:24:56 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:24:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:24:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:24:56 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:24:56 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:26:21 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:26:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:26:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:26:21 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:26:27 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:26:27 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:26:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:26:27 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:26:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:26:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a7c0fd01aa85d53a5cc462735eb1cd908410a74091bb824d85314c572a2e98`  
		Last Modified: Wed, 15 Apr 2026 20:25:02 GMT  
		Size: 3.5 MB (3543068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0990a4f4213cfb6f619b810861edf0e55ff77432a3a9995933d5e5e0f25b962`  
		Last Modified: Wed, 15 Apr 2026 20:25:01 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c4bf762147116095a30f26ea107900f28361d1ed6bcae3c7312e6e16503d86`  
		Last Modified: Wed, 15 Apr 2026 20:25:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611c551c89d0a52d0c1fc742df48242b4822774aeb29969a04de89b831b84d2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:02 GMT  
		Size: 13.7 MB (13709885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5ade602d1f9497bdb9f1408e2550053a861b3b97d3825ec1db2a3d0455503`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56588352628b072b8435ef48b6525542156117d05dc3638e928af0056385309`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 13.7 MB (13674677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268fbbb176b6d34f57da556ff71567e0c3b3c8a511e1cf4ed34733eaba6187ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e012c1772b42d6b1fba0c2455214494ec06551fd4a67e2fcef1658f848615`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 23.2 KB (23201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc79448a1b097592a03822eba5c5d849e0e0adbd86a3409607fbc6466cf075`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e05eec180821df7fd20ebc57b940908cae6bb1d78f21f26ea0f3ff23119e46`  
		Last Modified: Wed, 15 Apr 2026 20:25:04 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b4b62928d31fc023fe056b60c75906405dc312d724f2d47a6bd4498dcaff3`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 2.7 MB (2686952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2c55b51319db330e583fc26fa9c77527aa6075f531f51dd01d668039179dd3`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4ad977afb62e4095af9c745fee6f6d05a85151118b8f48dcc8bb784984afb2`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 22.3 MB (22284594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec77782c804a00e8db37bd0ba12f04377223228bf59f6a25ef615e020d5f3f0`  
		Last Modified: Wed, 15 Apr 2026 21:26:34 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2179c12fd7a900f1c8042cf4b706ca6414dd3c7b71719524bef2721377a53eb`  
		Last Modified: Wed, 15 Apr 2026 21:26:35 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:6e22bc5b50f784a0aa793edc6260acc0d4a3877c05f60395cb027490264508f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68dbf4995f06f7d183c25729167ac29de1950690d609f88e58fef5b771bd816`

```dockerfile
```

-	Layers:
	-	`sha256:4f0a3c077e84e19c591f72e07f35d0294eda015a1a10af99866974dae2460959`  
		Last Modified: Wed, 15 Apr 2026 21:26:33 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm variant v7

```console
$ docker pull matomo@sha256:db6e31bc9e56c7124d54f5138b60dc7d5293a05db2bd10f8b239393f0961ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58136619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02bb9d74ed40d1ca91e6155aa232c1266ddfbb733000a67eb8b39f3fedc9093`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:21:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:21:16 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:21:16 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:21:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:21:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:24:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:24:24 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:24:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:24:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:24:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:24:24 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:36:58 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:36:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:36:58 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:36:58 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:37:03 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:37:03 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:37:03 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:37:03 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:37:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:37:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1b303a0989ba45e4f7b30cb9937c77a13a6d2c7ecd4eb8917f1512079f9f97`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 3.3 MB (3343367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfb6dec2dbf14603e2027ed5b971b0cded429fa6c207d9d90b199acc9cb3f9f`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae7b5f922f713096ada0c57083da1371a86516392d3d545429f9e6f086cfc1`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd82f5c870f06ad0977d75bfd5f221698844492f83e81d648b6df4d92191d57`  
		Last Modified: Wed, 15 Apr 2026 20:24:31 GMT  
		Size: 13.7 MB (13709890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319ee333590a57384eec8d838e3097a7bbbaf98511fa5f754866f9c060f4ee53`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6db70784fe0b64129cd81fcc768162b61cfcfc6046390d05cccaf7bc7b34a4`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 12.9 MB (12905191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2b25dcc6fc43cce4d7cb7527e44400765b559a9be6f70a9f0b870f5431a16`  
		Last Modified: Wed, 15 Apr 2026 20:24:32 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc4e71b3774288941b5f1bfc7d26b51a56816bc620b4dc0adda2a995fe29d10`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5dbac3789d20b6f7fdf3f3626bf3319aed3094a4b8438530220ba321dbfbf`  
		Last Modified: Wed, 15 Apr 2026 20:24:33 GMT  
		Size: 23.2 KB (23225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c39b81bd3ed013ae106fd28f7de2a7f5a334afda4037ae7ad637f3deab270`  
		Last Modified: Wed, 15 Apr 2026 20:24:34 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30741ef8f428a294b3752c060c636de14f63c81af6838a2d87d652a5d761135c`  
		Last Modified: Wed, 15 Apr 2026 21:37:10 GMT  
		Size: 2.5 MB (2549152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cff83a4640159a1c39a4e122eadce7420f7c4b0a3cc60c02b368d6fba4ce686`  
		Last Modified: Wed, 15 Apr 2026 21:37:10 GMT  
		Size: 322.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85b2a3988d4dbb4905615749cc0e1ee60cd6c15ab8fce8bd83368d30a949bf`  
		Last Modified: Wed, 15 Apr 2026 21:37:11 GMT  
		Size: 22.3 MB (22284595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092227d820bd4efd03c085ffef1c200994de3d55222b5dad7ec30bc80b4513bd`  
		Last Modified: Wed, 15 Apr 2026 21:37:10 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e6f3346bc4998e779a11a623f40d3bafbcc6735024f682d9727810a2e4e59a`  
		Last Modified: Wed, 15 Apr 2026 21:37:11 GMT  
		Size: 821.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:a27373a579bf1332be9ac9a1e4d3c2602c83d6258c6e8a0b68e9557622b78a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762df55010d7192b5e92dab8aca42e93d29c649709d66ea0d2f20dbe9a1c517a`

```dockerfile
```

-	Layers:
	-	`sha256:2ee57c82275e330a6db543385c928244d0cdcd18d2c572132b4786db1f7b2417`  
		Last Modified: Wed, 15 Apr 2026 21:37:09 GMT  
		Size: 31.6 KB (31610 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:14f7d4262342893add2bada263de60f5c98d205fd01d834e1a3714e2923f37c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf2c472c92fe16d966e3422b8025ebd56708fc944e132d6ef1fdd077845a405`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:31 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:16:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:52 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:19:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:19:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:19:52 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:19:52 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:52:11 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 21:52:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 21:52:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 21:52:11 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 21:52:17 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 21:52:18 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 21:52:18 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 21:52:18 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:52:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 21:52:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f88c471740fcb5875464e516549da32c6c706f6987bc05fbbb6fd513a5802d`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 3.6 MB (3596129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eab76c94334ac507bd24480ab30256763b2b3d9cbee2101f931af7891065`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e2ccbab69dff79d74edc28fd92dc771024392d7f27df7019a0996222edb8f`  
		Last Modified: Wed, 15 Apr 2026 20:19:58 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b53c8276cf1764bdbc2a8cc4bd82d17c9abcec1caa79e755d4bb8f6cd08689`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 13.7 MB (13709885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c9424747f4f86a2634299b5c26a2827b3fee39c8784a2cffe3db0dcccfbf2`  
		Last Modified: Wed, 15 Apr 2026 20:19:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a7eb2230420c7fcbaa60c52674a748d09f2ceec7a1d09bb2384d3e9e4dfb9`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 14.7 MB (14702729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f864aebee5b8c62db6cc183f3cd9b7cda0fec6d388db0af242bb2496252e6b`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de20756a108dd2bb386335748415a405d248e1ab311f95e986cf3b417ed4163`  
		Last Modified: Wed, 15 Apr 2026 20:20:00 GMT  
		Size: 23.2 KB (23213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84abee5e477c51afcf6df1e875a6d0c7b98a1ceed1df6f1b371d717edad39b06`  
		Last Modified: Wed, 15 Apr 2026 20:20:01 GMT  
		Size: 23.2 KB (23224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce22a0940badf7da9b32f48d60afebdc96dc96c225a972f67e8092b3457344e6`  
		Last Modified: Wed, 15 Apr 2026 20:20:01 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9bb764d756634d173bc061c2687846671bab4bd6160912282837e5796249aa`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 2.8 MB (2836752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b9405104ba2e4253333c12827eb1fd88d41702d848ebb4ab872a93f53616cc`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0187d8ba993d4f71202c944c0cc26a0bc6175d0d0d9a5e95d8915788a5f256`  
		Last Modified: Wed, 15 Apr 2026 21:52:25 GMT  
		Size: 22.3 MB (22284595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1b33ffe95c13f6ae24da99909f33c6e8b52b9da34561f028fc79035f1b30b5`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139ff0cd3e24d4773e1d0ae622aaa12ffb918780190141d0b527a67e174d886f`  
		Last Modified: Wed, 15 Apr 2026 21:52:25 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:cbcecf2d401ad25baca20f95b77a54169f126e78cecc67fea7936f2f5e4c4ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4deaaa4428ed1a094857259aee37a53fe2d9ef4b7ba3e1b83a53888d20d7eb`

```dockerfile
```

-	Layers:
	-	`sha256:9c012696aaac20769638f74632f1ae4e6b13a76b4f27a6706581769ae3574634`  
		Last Modified: Wed, 15 Apr 2026 21:52:24 GMT  
		Size: 31.6 KB (31638 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; 386

```console
$ docker pull matomo@sha256:43a47187b21146af2ff0fabf2fb213f0644517eba079cde205a01356a5f747ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61714302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2da1ab54f59400b6588b37da5aa4e8836b685406adfe73457c3bc73ea16d4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 22:21:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 22:21:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 22:21:20 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 22:21:20 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 22:21:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 22:21:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 22:24:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 22:24:54 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 22:24:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 22:24:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 22:24:54 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 22:24:54 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 23:18:34 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 15 Apr 2026 23:18:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 15 Apr 2026 23:18:34 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 15 Apr 2026 23:18:39 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Wed, 15 Apr 2026 23:18:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 15 Apr 2026 23:18:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:18:39 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 23:18:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c62319c64ecbc8864f653b3190fe2930cd0d7d729dd495e4f110d82beb5a8cf`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 3.6 MB (3625741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b237d5e55c87544bf498ed4aa2213ff7f3202b6e8ac11c0feb4eef6dc60561b`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce09e8975bb1abc7c27969ab796d05155e31bf9607dbc4d8d6b9869d6f42f2`  
		Last Modified: Wed, 15 Apr 2026 22:25:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba374fe7ae564b24b876c0e37c0e24ae10295833b103ec997c6f4d51b33a2618`  
		Last Modified: Wed, 15 Apr 2026 22:25:02 GMT  
		Size: 13.7 MB (13709870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1068ef912fbd9b5cd23278793990a073d89428d5fffb6721e01c234f10214b9a`  
		Last Modified: Wed, 15 Apr 2026 22:25:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e808d6508c20e9c7b0fb968a894ef6f3a08518435e4e95508d14a683736b4`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 15.5 MB (15507087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e4133cfa5665ce34eef08043c23f2f0dba6eef44cfdd177b97398f5bba9523`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536bae25de12f93460507a4870f8205b06a2eef459609bb23b73e1bd928c055`  
		Last Modified: Wed, 15 Apr 2026 22:25:03 GMT  
		Size: 23.4 KB (23399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada671ef1cb78b082bc30975712e67aa71c719e0155289b05390c82eeca47ee7`  
		Last Modified: Wed, 15 Apr 2026 22:25:04 GMT  
		Size: 23.4 KB (23417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1be0d762f8603f63ac3e25a8914ead38c4303e1cdf95c608adcbae90b5d06`  
		Last Modified: Wed, 15 Apr 2026 22:25:04 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db0ff674de354f9976f4cb4de71124f3d857265205fc44e12f9299de000d7b7`  
		Last Modified: Wed, 15 Apr 2026 23:18:46 GMT  
		Size: 2.8 MB (2835001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcd35b688436da9ddfb97263dc980ed1181f789206ee83e21624e9d32d741d`  
		Last Modified: Wed, 15 Apr 2026 23:18:46 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1eff2cde0cd64891546c2c0520a6e0e85baef86ace82ccbc1b93af20549984`  
		Last Modified: Wed, 15 Apr 2026 23:18:46 GMT  
		Size: 22.3 MB (22284481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcffa4a67e26c61cab98382350dcc6cfb6832986d90ff9b17b3d16d9fdfd4144`  
		Last Modified: Wed, 15 Apr 2026 23:18:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845e3234a7a6d16502c5dab54f4b301207d30fcc5cb5d8498f332d1603a28631`  
		Last Modified: Wed, 15 Apr 2026 23:18:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:067e8865347eaa0811d1d4d7a31ebb5b6e5d92441ef65fbab1ac2a371d11e9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9425a3a80fcd0478859560c46b989e3fda02d500ceb18edaf8d33bd99323187`

```dockerfile
```

-	Layers:
	-	`sha256:b66b4afe30159998ad9a7a5da61f7c1ef93afaefc461e3afe3f5dbf95d840f59`  
		Last Modified: Wed, 15 Apr 2026 23:18:45 GMT  
		Size: 31.5 KB (31468 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; ppc64le

```console
$ docker pull matomo@sha256:3e617269a39433d9749e62793320d365c0c92b2c484aad1843febb2775cb2805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62442317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76506ba2465bd3366303eb15bed3b917c7edf2910b082b54d720ae23b3e987fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:26:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:27:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:37:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:37:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:37:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:38:00 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:38:00 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:38:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:38:00 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:38:00 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2026 01:19:34 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 16 Apr 2026 01:19:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 16 Apr 2026 01:19:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 01:19:35 GMT
ENV MATOMO_VERSION=5.8.0
# Thu, 16 Apr 2026 01:19:45 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 16 Apr 2026 01:19:46 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 16 Apr 2026 01:19:47 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Apr 2026 01:19:47 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 01:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2026 01:19:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0370fd1370a54392f3444f77669b0c6655267b3ae193cf4de50a9871836636e7`  
		Last Modified: Wed, 15 Apr 2026 20:32:23 GMT  
		Size: 13.7 MB (13709879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5dbe897696d0b00e89cb8cca0978c45cfac755af8488d2743b4d1d0e8349b9`  
		Last Modified: Wed, 15 Apr 2026 20:32:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed748167a4ba110e55bf836859404ed0d07c8012c0a38120a6a71eb553916df`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 15.7 MB (15732363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e837ab2c17d3b0ba367d2b928038674b2b671b658d5d1a8d2c7c6887717a6b7`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281189f4b70a3abcf43f4fbb010b7a91d30476a4f755d51d6b0dca53f4c4c6ba`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0d3b6b2ac74c55e87998f3778dd5acb7b98b2ad5d5cda294b7423d2989ac16`  
		Last Modified: Wed, 15 Apr 2026 20:38:17 GMT  
		Size: 23.3 KB (23253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f01cc8a62ac057a37f08692e3d3ca7a19a514bc8c37ba1f784049e37952d7f6`  
		Last Modified: Wed, 15 Apr 2026 20:38:18 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7972d182997daa1a63f9c8de270a132f3ad0996cbd9de17bde03407f51bf9f4`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 3.1 MB (3056093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3598cc0908f0c2d5cda65c7f1af0b4ad6e183703917fa8562d330bb4339360b9`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b5090403ade59177504bd26bfa58fab9976a7b0b3c39985d0dee964e051c65`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 22.3 MB (22284602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dddfd69364781e3e6c2eb3ee4be29f10236bbdff770bc351a2ade1ec2f9744`  
		Last Modified: Thu, 16 Apr 2026 01:19:59 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71581fb99af588d7be69dfb6b528305486bcc448c5dff1b7dfd1a24d9cb2f4b2`  
		Last Modified: Thu, 16 Apr 2026 01:20:00 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:b22dfa92ab3bf45360b491181f79ac3dffa7980ede5c046fc6606b1bde28259e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d33f537552d2a51ed36e452a5f490541088fca77afe2edaad81cee667289fde`

```dockerfile
```

-	Layers:
	-	`sha256:f612ac6c8fd2eebb37620715b21d375af7bbf9a96996e2a33b1fc2a9ec56139a`  
		Last Modified: Thu, 16 Apr 2026 01:19:58 GMT  
		Size: 31.6 KB (31552 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; riscv64

```console
$ docker pull matomo@sha256:2c069dd59077c23dada2943fd180fdb220741765e0309749f1f4a56acfb01b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60726324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414a4b5c2a6ca7bad2c9f6f70dc5c83f7fad0054d249cb153fac079ec4d00fdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.4.20
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 16 Apr 2026 03:22:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 16 Apr 2026 03:22:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 05:19:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Apr 2026 05:19:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 05:19:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 16 Apr 2026 05:19:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Apr 2026 05:19:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2026 05:19:44 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2026 05:19:44 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Apr 2026 05:19:44 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Apr 2026 05:19:44 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Apr 2026 05:19:44 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2026 23:45:12 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 17 Apr 2026 23:45:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 23:45:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 17 Apr 2026 23:45:12 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 17 Apr 2026 23:45:33 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Fri, 17 Apr 2026 23:45:34 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 17 Apr 2026 23:45:34 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:45:34 GMT
VOLUME [/var/www/html]
# Fri, 17 Apr 2026 23:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:45:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b4fa4e03a41893883792ee4048e5be20691de7211e35a2a172723216fa8a57`  
		Last Modified: Thu, 16 Apr 2026 04:21:29 GMT  
		Size: 13.7 MB (13709907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476302825d394ab9e227dbc6c9b962133bd1e7955ae20467d45109b6fcf1a7b1`  
		Last Modified: Thu, 16 Apr 2026 04:21:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e6b11a11df7b142f2f72f47441134f2dea9f81752b8af4643ad157bd4f7ea1`  
		Last Modified: Thu, 16 Apr 2026 05:20:38 GMT  
		Size: 14.5 MB (14463523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccddcff8df9f124f53d7f0c3cd362f4e501eb585260cb68aab0946a400e49c17`  
		Last Modified: Thu, 16 Apr 2026 05:20:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd51b4405f9696a0061622be43058dd51c509ce8944908208539350d5bd6d897`  
		Last Modified: Thu, 16 Apr 2026 05:20:36 GMT  
		Size: 23.2 KB (23243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19640a83bf529fc44644d01cb849e5881a0806e197267c01ed234cb601e01408`  
		Last Modified: Thu, 16 Apr 2026 05:20:36 GMT  
		Size: 23.3 KB (23261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfc73f78721d63719063106d8bd4e69aba98677503906be7d7cdd6efb9bff6d`  
		Last Modified: Thu, 16 Apr 2026 05:20:37 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704a80fd9694762a35e270d5af27a0e15b8bbf8ce5442ea905dba125b467e9b`  
		Last Modified: Fri, 17 Apr 2026 23:46:24 GMT  
		Size: 2.9 MB (2885009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e91f22ef73e9672dd6e3d354cf638f83d5e981d0644d7992f7fe585f8e374c`  
		Last Modified: Fri, 17 Apr 2026 23:46:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271545d130736b98973b78e7bddbffb4c4016cd94ac97a425f53c5e4ade7c87d`  
		Last Modified: Fri, 17 Apr 2026 23:46:27 GMT  
		Size: 22.3 MB (22284594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f99afed4bf18ec3d58580cca07e99f3244481bf8d1b9ee7bbf75adf3660d4e9`  
		Last Modified: Fri, 17 Apr 2026 23:46:24 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcf84f38dfbdd62eacc4a267517d922199233d0590caf10ee7f11729d45155e`  
		Last Modified: Fri, 17 Apr 2026 23:46:25 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:7eef629f5e1f63665fbffcb666fac13c8a0518a886e5799f58f444f1883430f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a56b89da63d22b82b2d0ec949962013d9efec4e60cbb4b258fcc79a3622dbd`

```dockerfile
```

-	Layers:
	-	`sha256:27a8a5a8b5719b232e3a6b417f3ffa634b8a05fd20985828786fe77d3eda4ba9`  
		Last Modified: Fri, 17 Apr 2026 23:46:23 GMT  
		Size: 31.6 KB (31552 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm-alpine` - linux; s390x

```console
$ docker pull matomo@sha256:eec14288bb38131ad4473c4744adaa7e35424f4e32e7ee9c2023373d1779d59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61426824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f083be08b99fc30e20322187562d43cc16b78e82377d7040dcfc1570daedf0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_VERSION=8.4.20
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 15 Apr 2026 20:16:19 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 15 Apr 2026 20:18:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:26:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:26:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:26:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:26:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:26:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:26:29 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:26:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:26:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:26:30 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:26:30 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2026 00:16:24 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 16 Apr 2026 00:16:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		freetype-dev 		icu-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 		openldap-dev 		pcre-dev 		procps 	; 		docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .matomo-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 16 Apr 2026 00:16:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 16 Apr 2026 00:16:24 GMT
ENV MATOMO_VERSION=5.8.0
# Thu, 16 Apr 2026 00:16:29 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		gnupg 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apk del .fetch-deps # buildkit
# Thu, 16 Apr 2026 00:16:29 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 16 Apr 2026 00:16:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Apr 2026 00:16:29 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 00:16:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2026 00:16:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816b342f273c114d9278090832c6b271fa133343c6cc14c8db27aad0433c7e9d`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 3.8 MB (3786986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40fd55f34e09a431ffb1541581fb4b2fad1c949d00d3718c054f6a585dedbbe`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93e9efb3f33cff64fedaa7b934bccba27be41ab8437362ef089937721401080`  
		Last Modified: Wed, 15 Apr 2026 20:21:11 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adefa755b1cbede3245ba350573476b4438d2c3a375101c6553fcde8df5d943`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 13.7 MB (13709892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4adca3f5704531af4fde0978117a15a124923c7e965172a5d0bb1d9fd326e`  
		Last Modified: Wed, 15 Apr 2026 20:23:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0defdbf2ba8615afbca8a0d1bfb648f2dbbd17603fe56d07c6ee5f8d4d0d2b`  
		Last Modified: Wed, 15 Apr 2026 20:26:56 GMT  
		Size: 14.9 MB (14946590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f0d2a9c2acc44acc378d8d7aa59111cf8221ffd69d95d7a6999955f35fe09d`  
		Last Modified: Wed, 15 Apr 2026 20:26:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689498889cc21894baf940c5494c0f97d27acf8dd2b3ca587252825dda967ee4`  
		Last Modified: Wed, 15 Apr 2026 20:26:54 GMT  
		Size: 23.2 KB (23234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694ba63a331296afb74fd3621407ce230372e05b0b2381d225713d7b781af44`  
		Last Modified: Wed, 15 Apr 2026 20:26:54 GMT  
		Size: 23.3 KB (23257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6618c20be4f399ddeebdf0c1a60c3656feb24e5eb57fbe81a52c49b0d9259a5e`  
		Last Modified: Wed, 15 Apr 2026 20:26:55 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384704e8316816dd8feb34fbcbde504aa62cd06f07fb8e3118ec81479ee60340`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 2.9 MB (2910838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd055c2e270cd72a6b80e51a049d94d07e8ccbf0c8d7c8799bbf82bc5fcb2493`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47e22974fddaa636533bdde7be656b253afd709938a7e246280ca3a0945b26d`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 22.3 MB (22284623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78c27e0c6ef68a3a02f85083cbe7fbd3b4038c0adb9a8764cead2a154bb6b2d`  
		Last Modified: Thu, 16 Apr 2026 00:16:40 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f22f96a49d7f79f45350eab1c6b79be94c2917c72e43eb4fb429098a81a19b`  
		Last Modified: Thu, 16 Apr 2026 00:16:41 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm-alpine` - unknown; unknown

```console
$ docker pull matomo@sha256:cb4cc1cd3723cb8978bd1ebc2ea5fcdf17634b13d3c06aab25845c4cf160821b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d61d0da716c7d14c4f2cc5bdc9f39500166ce93321a10b81db8f6444d0c378`

```dockerfile
```

-	Layers:
	-	`sha256:34e6fbb66b9cd18d1835e7c49a4ba9077d41ba53c197e6726d28b2f7b50c7902`  
		Last Modified: Thu, 16 Apr 2026 00:16:39 GMT  
		Size: 31.5 KB (31504 bytes)  
		MIME: application/vnd.in-toto+json

## `matomo:latest`

```console
$ docker pull matomo@sha256:d6daf1cd148fdc8b4b896b2f5bd8fa10ba99c0fcf464fc86c00fe352f8ca5adf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `matomo:latest` - linux; amd64

```console
$ docker pull matomo@sha256:12c152741a75162431fe589dc58010ba84e2bec65c4ecc70143d55c4e2553737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204385414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02018cb5db2c814c3cd9fb610752f770bacf3b0380c02a5e210026b6095a0ad7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:24:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:24:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:25:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:25:04 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:25:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:25:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:56 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:56 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:56 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:52:44 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:52:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:52:44 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:52:55 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:52:55 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:52:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023baa873c0991ddaa7419301cf610d5e56ceb38356f1845ae0e94eb05dc3c9`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574faee95b5376fc2f0f3f093a9e6780a97d7eedc2da840e55380b1d36f85a89`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 117.8 MB (117843202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa6ce5874bc20b89543cd80d41f58507e071af1977b4fc38fe6a13ca83fdeb`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcafbe281a6757cd10d2aea9b90f3636b474dd2516c0980d602df86c6d4781b`  
		Last Modified: Wed, 22 Apr 2026 01:28:18 GMT  
		Size: 4.2 MB (4226905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c19f6aeb84e92127e2e3d01ae0c2404b696e34500cff3e1730ca85603f24ae`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ed48780967058ba90258dfa165a33a65ef90d6260c78464947bb8732c2091f`  
		Last Modified: Wed, 22 Apr 2026 01:28:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a3c22f89f33eacca27643c304fbf4cdced1a494513ba0684cd5faf51ff50a`  
		Last Modified: Wed, 22 Apr 2026 01:28:20 GMT  
		Size: 13.9 MB (13852567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7e42314878fa75790cd20ec64c41553110fe17f16b9c26967a225173a8acf`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c72387956fde81883201db10160d5778cbc5b4846c394578385ffadd64ade`  
		Last Modified: Wed, 22 Apr 2026 01:28:21 GMT  
		Size: 13.6 MB (13557477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae044dcde24485109733a3bc78f06686efea05cd32c03f0c38c68e2f825a8b00`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de552cfaae1b01c9edff1ddfa947b594abc5c5cd7e5935083ef66faf36a2e64`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a166fb5f1996a6802829599fa567e0f5051d57568f2922b032eb0402fe03cdff`  
		Last Modified: Wed, 22 Apr 2026 01:28:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aafaa0f9a2d4557c2e9c1f953def4005d036064e46b0d8226bd8aa3047f10c`  
		Last Modified: Wed, 22 Apr 2026 01:28:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2456ddb90857497cb87ca412dfc2f926ab21071759cf8fcb9a903fc7f38bc1f`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 2.7 MB (2717845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc0226b1100105f4d89cdf4bcf367da0f16e6606031f8f1c2a01494a8ef71cc`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906f8621388502a1c2fafadad71dfc4f8e6a79c0f3968c5e19ac3e3ff9914f6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 22.4 MB (22400019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eed11ba24da6d3ddc5fba318e47ac47c9eace9fba0f69c65f1ec68d9db43a04`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09df151f9988ce5a0c814ce4e9d8c3b6ba17c2f3552077dc6cd497b584327c6`  
		Last Modified: Wed, 22 Apr 2026 04:53:03 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:bb49764520a93d3fadb85fe316c6c91c38b0d19b7f270bf74188a81e1f457a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ffd650e6dd4076605c2b6b683b5cc5faab13fcbf9150d7b757ca61fbabb1b5`

```dockerfile
```

-	Layers:
	-	`sha256:80bec4086b4c60d81e45a4f6d2bdde09f55a31b64da8d3f8a8b0226929bebd68`  
		Last Modified: Wed, 22 Apr 2026 04:53:02 GMT  
		Size: 37.5 KB (37471 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; arm variant v5

```console
$ docker pull matomo@sha256:b3f79e04d9b94de7b50b88dfdfbfa132845da9c7c6e4a96372f00c2265f912b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096adafe94dbb74320d05d940b1a9e5ec6f5eac8667ff3392a8eb6b57d13d6e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:27:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:28:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:28:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:28:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:28:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:28:10 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:28:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:28:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:31:37 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:31:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:31:37 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:31:37 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:31:37 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 03:41:49 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 03:41:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 03:41:49 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 03:42:05 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 03:42:05 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 03:42:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 03:42:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab8cd142c874a4a2116214700713c2dec92f9352b96761c33107037fb9f0d57`  
		Last Modified: Wed, 22 Apr 2026 01:31:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccd9fa364a1786b392bac2e6ddd6745d7ce20e23d3d55e5dea7f9550e1299d7`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 94.9 MB (94884502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2affe866774915b1ac9a46a4e1ac18de29da227b2d5a68bcfd8c3c538e7b7d6`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80b088c9aeb209cf831aef8b763b0ec951fff041e9f33eb8457a075d2631ccb`  
		Last Modified: Wed, 22 Apr 2026 01:31:56 GMT  
		Size: 4.1 MB (4089308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6d32ed0510893abbd91f5e84dca0a9241e463b74e591f0100df6bb9c725623`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c8c0d10e5b9e10c1dd295649dd23ec4b53c92bca9182c071138a5e19d42d9`  
		Last Modified: Wed, 22 Apr 2026 01:31:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a080db7c5dc718990269dc0f1f41e1ff18d27fefe892e5d28132340c72c9`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 13.8 MB (13849980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1c211cec5c80e05741841fad4f75d84ce5ae2e3f18171df44c774b5de93330`  
		Last Modified: Wed, 22 Apr 2026 01:31:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729daea6a9d1fe569b7a314fda12a22849a3e8fca3f0f6258dfe0b5d8222098d`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 12.2 MB (12206143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378076dd33dadd4c5e3699bb5f0d22530b9631762f33e38ace0f9ced22b890ed`  
		Last Modified: Wed, 22 Apr 2026 01:31:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2380879c990070fe22833595bddb7e02c9b0ee05c886afd7343a6a0f1eff2a`  
		Last Modified: Wed, 22 Apr 2026 01:32:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff707614457b67b0eb77d55973fc3d28054243f45091bf9d0997d370f60df5d4`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5655cb2fd9ecf9b2f590ce94143aaf2a2b527fbe2489f5b3780216e7ae9c24`  
		Last Modified: Wed, 22 Apr 2026 01:32:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d7df617229c5cc1a9a119d1a416cc5a5ca4690a3c1f5b28eac6de4189d1020`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 2.5 MB (2540941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d80a4659a3571e68d354a2656794a7e7d82c6666ee8425b2d70e39489f2daa`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76978f69025491f93184f38ba37d08d7cb833167a5867ab287ba88542f00f547`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 22.4 MB (22397964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7764c5d0265720d63f293ae158d0e6d6b9d2ed1f8910051b1cdc7570adcd7d5a`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f8c981c39ae50f561ff131ba6812c46579b2eb0d1a7a9c731f9d5e4393c726`  
		Last Modified: Wed, 22 Apr 2026 03:42:13 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:f99d9eb764a1c4bfab790795df645bba9b3938d285255f316807dafee16d4168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8332b81849e2103dd20bc7855d23d32a991eafa638521b6b03e7ddfe0fe94964`

```dockerfile
```

-	Layers:
	-	`sha256:e48f117027110118d1c39af8234e7fbd20682416aed9f39c73e1a3690b46eef5`  
		Last Modified: Wed, 22 Apr 2026 03:42:12 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; arm variant v7

```console
$ docker pull matomo@sha256:704ea7b9198d0ea68b00d8502802cf9d8bdf423cba5ad6c46382d1a9ad4b5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166515903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dfa22ddd64577d28b1e403be4579b1a089eda6ccfe933ac6c43d305499cc32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:29:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:29:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:29:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:29:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:29:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:29:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:29:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:32:53 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:32:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:32:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:32:53 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:00:33 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:00:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:00:33 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:00:45 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:00:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:00:46 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:00:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:00:46 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5106b06fd3c072093bded94807949d02b5d151d8aa469eeb46a006453a7965c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355c944c4093dc300ebcdafb3bda8a6c9ec4d565280f4214da78dcb5c72d8e8`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 86.2 MB (86247520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a3ee64c140bf6e6df68932390ad89442245fc71e2957dffcd5fd91b5d25c5`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8490fa290792bd4ae1508b2e69453cf84b93a093779bd2af997a7ac80f5e85`  
		Last Modified: Wed, 22 Apr 2026 01:33:10 GMT  
		Size: 3.8 MB (3757190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a76912f0330b5a8e70a8fe111b069c3d44062696c997577bb47dd4a4b8b525`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ef1f39e2cbd10d3c21fd5b455d521b8f52edac13cb84361830d0401e056cac`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efef0f29c620f3102b1cb37a57abdb740e18afa37345163f546b45b7e315db3`  
		Last Modified: Wed, 22 Apr 2026 01:33:12 GMT  
		Size: 13.9 MB (13850104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178f3b58b928248d5313cea7c2af0b1191a4134e5a2ea89dcefbeee3867e9558`  
		Last Modified: Wed, 22 Apr 2026 01:33:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9701abf00c86fb9ba5d35d547ea7424a7005a7054ac5a6a99ac57e7f7b0bfa52`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 11.6 MB (11617459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1893df0361b2d097c967eb96fb1a8ed66537461ffa47cfaacbd00525053417`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9137d5f6e1867a22561c5d4852fe69d4d5871d641401476fa35959cefd60b9`  
		Last Modified: Wed, 22 Apr 2026 01:33:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344333c00c42b7386ac635f2edc6f7eea53ca2fa38185bcfb85c9c47cfccd2f0`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d097e3f5dc408f7a2ec0f1811eeef125ae55df101558b0b59f1472f8ccfaa7`  
		Last Modified: Wed, 22 Apr 2026 01:33:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd7af921602983bbb84f849980faeae03206451c48016c267efac138fb85d2e`  
		Last Modified: Wed, 22 Apr 2026 04:00:53 GMT  
		Size: 2.4 MB (2423407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd46eaa7f0b8afc693ebc9ac147abaa96e690a6a2fcda89c5adeed6b99dd674`  
		Last Modified: Wed, 22 Apr 2026 04:00:59 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192108aa8a7e7c0156e5d9c86e0ff96c4653ac3d439d341f16057d7e7ee8d02`  
		Last Modified: Wed, 22 Apr 2026 04:01:00 GMT  
		Size: 22.4 MB (22398176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaa66c3db7078e11ce7a6b35effa084a27f2cd317004b643e0d8f5db9d6d83a`  
		Last Modified: Wed, 22 Apr 2026 04:00:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0b8da69cc5561177aed4321e855591775749dcd99c365d47d899fdf5b59370`  
		Last Modified: Wed, 22 Apr 2026 04:00:57 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:2c46c268c61a1ecd5dee08fd6d61ba7cbfd21f3b433de455979424cb92e71042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96950acdfa31d5d16bc845cf7ce279205260039bfb15d82725e61367e7d3fd48`

```dockerfile
```

-	Layers:
	-	`sha256:ffe614280a9b04b1c586f7c9faeb6c8b6c9372de7ad4b4e512fac579471a7ef2`  
		Last Modified: Wed, 22 Apr 2026 04:00:52 GMT  
		Size: 37.6 KB (37604 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:ab2dcb212c07347abe77449f11cad81b22120cf0dc07e197d68270ade1dba465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196769775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14945bc3708b1df92ba2b2f5fbc29866180f097e40b3ae2491f7aa51b25089a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:15:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:15:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:15:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:15:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:15:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:24:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:27:46 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:27:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:27:46 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:27:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:27:46 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 02:41:00 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 02:41:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 02:41:00 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 02:41:11 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:41:11 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 02:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:41:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887e7361c4edf16eb4272307ea2ee57447cf2ec134af0f0326596d3c94a90d7c`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391fd317e2422a2b998a5b8f46476782dda67b0195c064eccf5d895e482ad1b`  
		Last Modified: Wed, 22 Apr 2026 01:19:38 GMT  
		Size: 110.2 MB (110165312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18568485fa5a6e44bf015471b704446b95da6eba7e85f8f6cac1dc351aba16c5`  
		Last Modified: Wed, 22 Apr 2026 01:19:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc61f4154b4e36f9f3303c2b5d7cc39748b46c166e3b463351a9e8cd220f168`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 4.3 MB (4305491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc86735d128f1fbd8106cc32d6afae7a900147daa337150c4739d4f1da4346a`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5795b9e26f314196881b133a91769e53e2828131d098f8db7d9a800b3e89e`  
		Last Modified: Wed, 22 Apr 2026 01:19:36 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5502f96df57cbf4d7939c397fd68491b3e4dc7ff372c63a924fa619428d5ce55`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.9 MB (13852179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c671d94ce0c6c5a51de7fc69370d23707fb0718409f951b587be6798c77cdb`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325d25ee42064c543212ea6c19bbac76a85d4adc1cf6dfcd77fcbd4fe2382b1`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 13.2 MB (13206146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b47d3caf75cacc27de055e12f70c9488af4a77ec463a8a8803aea30d969715`  
		Last Modified: Wed, 22 Apr 2026 01:27:57 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab2816bd1e826aae48479663d523550acd969be5b93285569dd982e03a671af`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0f0dbec67a1da7c28e365dadc3da7041014b5b9baf54c270e51e230514fa8`  
		Last Modified: Wed, 22 Apr 2026 01:27:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e7217b1331d5942ccaacf9df0f007a688d6cc47181ba879aa1f856ac11fcc`  
		Last Modified: Wed, 22 Apr 2026 01:27:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa4922aa898ed8d63dca36bc92280eb42fe3d79eb890ddbb2259d0d6f5e41c`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 2.7 MB (2689943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f80fc04bf2842b7907c34cc355b9fbf3a8bf4c940f016885d0c1ac2289bea5`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c238b3cab631145cb2c7fd748f13647a154c52bd26f015e00814d91d30229bf`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 22.4 MB (22399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933121251f2ea8358e789aba4823d58ed5e7d70fccfab2b7639e3a1c51299521`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f08ca589b4bae468116a8f6db8123fa341908d69ef11acf6ae82b48772355a`  
		Last Modified: Wed, 22 Apr 2026 02:41:19 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:863bad92be9713ba8bcb7beb234be02780085f33286f8e8084008465d3d017e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a11b51a0968c2cf96156db8040090822cc3639a9958977f3d751d1729e91825`

```dockerfile
```

-	Layers:
	-	`sha256:1416c764e4d00d79fc909cbe75de1ee64470178596ed648380f6ea85b2359296`  
		Last Modified: Wed, 22 Apr 2026 02:41:18 GMT  
		Size: 37.7 KB (37654 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; 386

```console
$ docker pull matomo@sha256:1c1309fcf70db7d5aada1313f718e3e18653afdc5ff156e0a617eaf48a950ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204710405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1045868eb2c98cf46a416f775849eb27fb25286f9b71a40d65c7023392d62074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:22:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:22:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:25 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:22:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:34 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:25:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:34 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:25:34 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 05:10:32 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 05:10:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 05:10:32 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 05:10:43 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:10:43 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 05:10:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:10:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ad892368f928cf2c1259fdac7b49dec39b5e0100dc38505086d1f04fb0223`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a854b9375cf76c04d007410d1b4f9960253c91e039f3fcb12bd3c7da649d1`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 116.1 MB (116144340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b221c038be8eef2d78c984f7ad0d2dc0453d8cdf3bfc51ad75822776b02c5`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea166db99c0aa8459ec40867c9181d68e865592724270ab960b87a59316cef`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 4.5 MB (4458361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e72ff3928a5ae8b1b558eef86bacf78c1a2d3acee46fe57fbd521c584e8e925`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4831e8917f639e8f5338c7edb49dc14aa2d40befe0ab2492f12791411ce60c42`  
		Last Modified: Wed, 22 Apr 2026 01:25:56 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba0ba05e513a80b82c62a1f5983b0933fbd3dfee5e689cea629457ebedbb230`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 13.9 MB (13851522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ab312dab66ebf333df3271b5f453521908be468732a06d8501f0c05010dcbb`  
		Last Modified: Wed, 22 Apr 2026 01:25:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0409a251efd274db5d34c0539ddf36b203537156fff65d0dd99d6206eb755da`  
		Last Modified: Wed, 22 Apr 2026 01:25:58 GMT  
		Size: 13.9 MB (13858390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c38f71c21793b514dafb1af49df5345e3a36057bd995386b1721dad70ae5c1`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e3ac463e003ef2a90ed29684c1fec4adb899f721d8ca37df7bdc97f93e810`  
		Last Modified: Wed, 22 Apr 2026 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abb31896c1032bcf7ef68bd4c309fec9e010b234c4f1ce7bf73c77d7e652cc4`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2e5cc369f5d824ad4e235d2ad3a85a02ecec99498753828309af3d8497942d`  
		Last Modified: Wed, 22 Apr 2026 01:26:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe74de20b0aed283f8dfacadd066c1b866e7e713365c92add76f3eb93a3142f`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 2.7 MB (2695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f70249788be758fa0c374f2201e7ddd74a626cec88d83d55f7f3dbc5336329`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ecb4969fd8c7e45f3b01fe4f7674cdf2a81ddcbab2fcd06f95732737d687a0`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 22.4 MB (22399199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6baa5a4e1ac6e37fe0663c2a16a7460de7d4da7e2d9ca774be8bf8f24ab90e`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4d6c98ecf0f190733724883fa2dcfd119ddf57870ea4a110d054bb067bd05`  
		Last Modified: Wed, 22 Apr 2026 05:10:51 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:07afcb4a3f8ef2f649b1062a2d05b6c9edd68ca33220ab0afe16dd6c1159a6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305e68ddb09754704bb1eedd924f9f348dc2105efd8751945e851f3cd7c15b50`

```dockerfile
```

-	Layers:
	-	`sha256:76a872aab9742b54def28f8f9f09f139870219db07eafec324889e38707ff6a9`  
		Last Modified: Wed, 22 Apr 2026 05:10:50 GMT  
		Size: 37.4 KB (37416 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; ppc64le

```console
$ docker pull matomo@sha256:558b509b6c438846c89e60d7ffddafa641cd764bec4f6cfd5f0afeba31d71466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201268007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b0a0f46052ab0d0d7faa5e005cd429839904c722c8e11194972de9c7108608`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:54:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:55:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:55:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:55:46 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:24:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:24:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:24:29 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 02:24:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:24:30 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:24:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 02:24:30 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 10:55:21 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 10:55:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 10:55:23 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 10:55:44 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 10:55:45 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 10:55:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 10:55:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab63631568fe36922db06d590c893408dd270fd36872c90416de60627387ddce`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 4.9 MB (4881692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8438bcf1abed6360e9adac08f804567924b049146c3294914aa102a3f7c41821`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e295926cdc5af3d791955667e4175ebedf05ec97080bd65bd6d11dabf8992`  
		Last Modified: Wed, 22 Apr 2026 02:01:32 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286ae5221aff2ed1a4a8a4baf4172ad032a7bc332f63f890612205f59604724d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 13.9 MB (13851763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67505e93e2a17315b3576e01845784735fd7612b2eba5ee18fb5e1825fc5a4ec`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c411040503656e63e555235609eca014c8a578020fd6fde25775feb51770f`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 14.0 MB (13956005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d038fd0dacac84a920cc05f508ee5bb0e0c9d08d1a72f3d96e5f75fe524595`  
		Last Modified: Wed, 22 Apr 2026 02:25:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce972e1f08c44df934bf2f5a50d413fa96defc3a3e5af20f6031c30f82275300`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c414f8be1c63ac3c42a432d3030e7c783159d103fd4e5ea6b8df58e8ddfab0d`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53be4ec9fb48b51715a67384041424d5e3e0e3468e2d9182dc45ad510e144a87`  
		Last Modified: Wed, 22 Apr 2026 02:25:11 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e884c3d1fa913f34c366a6fc98547d1ecb5b9a27bb1240460902988fc3b0e011`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 3.0 MB (2974034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e2227d7fb70d54ba4b77dcde32ed88eaa5c3f8f8dfbf1cd1ae8b0b99ad878`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dbd12cbf47f04953f09756fbf5445ccad7f5ef3bd747b030e6665e3a5338b8`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 22.4 MB (22399966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8bf5242f2944c1380e67fdc6dc45d28378163497c60bb8cd85b2e5b755313`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19871154c75f6f17ec259370a7742b4dccce1bb26d6fd0c5c1c80710563430`  
		Last Modified: Wed, 22 Apr 2026 10:55:59 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:d9af1012a7106008ad18566e1e554936ff4d4f022d85bdcfa51a76b580738c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97b8ae50ab4be24e976ede726bf8780e1f869f862f8280567dd5fb333468e07`

```dockerfile
```

-	Layers:
	-	`sha256:c3509d9b911e4d1b3ec37730332352101ca474bd7ff9f59709e048ba9e1376f7`  
		Last Modified: Wed, 22 Apr 2026 10:55:58 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; riscv64

```console
$ docker pull matomo@sha256:1b1374d4bf1624ec39522f6940af9e6b78bfd5f869278ffeb9e6c4bf0b4cb928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233788266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4a814b40196d1c72ad00aafed53c670ab9aae9c4d1c996b9814241f18e6086`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 10:45:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 10:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 10:47:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 11:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 11:52:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 11:52:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 11:52:41 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Fri, 10 Apr 2026 16:36:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 10 Apr 2026 16:36:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 17:30:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 17:30:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 17:30:52 GMT
STOPSIGNAL SIGWINCH
# Fri, 10 Apr 2026 17:30:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 17:30:53 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 17:30:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 10 Apr 2026 17:30:53 GMT
CMD ["apache2-foreground"]
# Sun, 12 Apr 2026 13:02:30 GMT
ENV PHP_MEMORY_LIMIT=256M
# Sun, 12 Apr 2026 13:02:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sun, 12 Apr 2026 13:02:30 GMT
ENV MATOMO_VERSION=5.8.0
# Sun, 12 Apr 2026 13:03:52 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Sun, 12 Apr 2026 13:03:53 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 13:03:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 12 Apr 2026 13:03:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b2e954d1af938a2aa1efed6d1a75219119a7c274202f00263add011b1df0cc`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a48bd384ede4f10d9953221ea6e7789224aa0530f583111e9dba0cf9112c87`  
		Last Modified: Tue, 07 Apr 2026 11:51:01 GMT  
		Size: 146.6 MB (146578969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501093af7cdf85fd36ee8c49559dad0e13d98dc1c2b5ba69bad0819ca64aae9`  
		Last Modified: Tue, 07 Apr 2026 11:50:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1748d653b8c3ed98b870438732aa56def2ef4f267a38a228a8d4e1a775744da`  
		Last Modified: Tue, 07 Apr 2026 12:53:25 GMT  
		Size: 4.0 MB (4031244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79c952e0710b8d660c2b70f3e9f2716a16833b628e3b2dd090af31c1cf7438`  
		Last Modified: Tue, 07 Apr 2026 12:53:24 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe6480453dd1cec4db695c1e657272ce31a8c86abec42383da6aa9846d7dc4`  
		Last Modified: Tue, 07 Apr 2026 12:53:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dacce83cf82615cd1d4a6c1a86cea6e40883d3a42ad8656c9b8763530155814`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 13.9 MB (13866799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3323b96cffff08af8f445b80f611ebe68799371d01077775a0c3f4567380bd`  
		Last Modified: Fri, 10 Apr 2026 17:34:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08e4e9e187467f7ffbcfe1cdf4d10ee90f6ee36da3b522274275365cc718ee0`  
		Last Modified: Fri, 10 Apr 2026 17:34:06 GMT  
		Size: 16.0 MB (16013910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb761f6a2a209495608bb857bb80d3d0d0aa4de2fb075e52945a24da89addada`  
		Last Modified: Fri, 10 Apr 2026 17:34:01 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ced9f37602f905311a1e2a29a005c079a57757cdbf7e7fb075022b1a0f660b`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494a5659332e0f15ed2f4d61e062b27c51744e0fa85863035bb125c624a2ad0`  
		Last Modified: Fri, 10 Apr 2026 17:34:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6cee257162c3d59f0cd7d2be13c20ecd7f6bf71c712eecacc44cc33a5fec83`  
		Last Modified: Fri, 10 Apr 2026 17:34:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c54731eefd24f5be8c3be0e167304e36cc69b70462507d80ccee20c97285125`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 2.6 MB (2614022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93170443e6c9159fcbd88f4c341eeeea304875579d3f0a96e2d394517a45ab0c`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72489f0fe05b81788af39c9e702ce18d653102a5f9d70840781a6456c6da216f`  
		Last Modified: Sun, 12 Apr 2026 13:05:15 GMT  
		Size: 22.4 MB (22400287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29582f6aa97de83cc2e3b1070f8e16811e430db99830c4548ff4151cef5d682e`  
		Last Modified: Sun, 12 Apr 2026 13:05:11 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae08e7812254f8597aa1f47af714fb516cac8f33972c277e72c29956b6ef64`  
		Last Modified: Sun, 12 Apr 2026 13:05:12 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:044fd16450e94817d1f1ebc47d8b8d9709562399d3f06bd84151c253155e6ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8cbd64c659d77d407cb66fe3189531945fc5fe28c9849fa3a4e57c61cada0`

```dockerfile
```

-	Layers:
	-	`sha256:791843956f9e2428ebb0d78e1b2c97d5ddb76f0011b84c41f30227973e1d00db`  
		Last Modified: Sun, 12 Apr 2026 13:05:10 GMT  
		Size: 37.5 KB (37544 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:latest` - linux; s390x

```console
$ docker pull matomo@sha256:6cf85e049fc320cd8aec35cc44d082d802da2c38536f6bbdd501de2103e81c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179059874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995327f35af3666a70c2b8f73cbabc6e04075ad4e578d7161973c87c00ca4aa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 01:23:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 01:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:23:27 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:34:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:34:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:39 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 01:37:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:39 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 01:37:39 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 04:41:27 GMT
ENV PHP_MEMORY_LIMIT=256M
# Wed, 22 Apr 2026 04:41:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 04:41:27 GMT
ENV MATOMO_VERSION=5.8.0
# Wed, 22 Apr 2026 04:41:38 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 04:41:39 GMT
VOLUME [/var/www/html]
# Wed, 22 Apr 2026 04:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 04:41:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ece9a9560b771b29f91d1b2fa69377a7a6998382890ab15dc4a92ce806048b`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ccbb849cf7d524fb26003a40a6f2ddbd73713723d4bf57178fec331c8472df`  
		Last Modified: Wed, 22 Apr 2026 01:27:55 GMT  
		Size: 92.6 MB (92573082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdb404da573a86ead75a2c55d7c0f8bd69a0480a6e1e9d1e17b114c37703861`  
		Last Modified: Wed, 22 Apr 2026 01:27:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7964dc0539da49b7d15124dd7f7170a7706b36795438d37e1b510fef67d922`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 4.3 MB (4329303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d928c48d6c321d2eeb66c3c389766cf9ae0d3b52927919a0fb9928aa3790f1`  
		Last Modified: Wed, 22 Apr 2026 01:27:53 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505cc4503afd2ec97db21c3221acd45b9429c93ad112050f26555547d7899269`  
		Last Modified: Wed, 22 Apr 2026 01:27:54 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ccf2ac717c82b15002dd84ef1d42b8130bd9336b5ee96c48db314d863c1a`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 13.9 MB (13850951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d18571a8b1fd3a48f17e0ed57746721b5633a3d9d6fa17bea75e647e5dadb2`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af7cd74da0af1e5075282c2cb414e4d83acaeeb6bd637c46acbf94b5414eaa`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 13.3 MB (13311877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d5c986b0140b3c1c0aadeb97c7c15b48faacd44db4831ea9d0d2fffab85e97`  
		Last Modified: Wed, 22 Apr 2026 01:37:58 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfd187c896be49dc43ba8e03a8e69c5e53fe53aec2711d75d512f702105a9e6`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c1dcabe41bbe8315743a1f135c7e213230ec4c4802210eac62355753a21234`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f3b59bcfa40537a6d7da3db395965ad05e8bb13ba9c58d1bd555b7be4cdcd0`  
		Last Modified: Wed, 22 Apr 2026 01:37:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12d807e0e3c374569c0b1e1b7e34053e827157eb1bdaf0a8d4352ed9566c33`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 2.7 MB (2748316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bcd04f47c821ef46e5f55b5e15f7b9ab6e8255eda8e16a77b1c0651c988eb0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3591996980aec43931f2cfd37dc3c0d7757b9e8252e4c9da2ac3ee6f7ac5da`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 22.4 MB (22398820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93afd3e6d8bb757c222e5ddb8be065f77013e9147fd82999457b98952f458bd0`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d977a5ee6fe1cdfefa7fd25d7e089a23e5adc1380e201464878e0cc3358b254`  
		Last Modified: Wed, 22 Apr 2026 04:41:51 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:latest` - unknown; unknown

```console
$ docker pull matomo@sha256:35e05b0967102445629beffe14fdb57e770914fa2607f0247303bcb44928be5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aee6ace1d2419bac32bedf90aece37b63bb8077a84f38e86eea3c24580010b`

```dockerfile
```

-	Layers:
	-	`sha256:bf0616b74b590e9ac3532d9d0e1826d70f42f64c7bdf51345482ea2dabca15b7`  
		Last Modified: Wed, 22 Apr 2026 04:41:50 GMT  
		Size: 37.5 KB (37466 bytes)  
		MIME: application/vnd.in-toto+json
