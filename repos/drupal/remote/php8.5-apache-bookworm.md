## `drupal:php8.5-apache-bookworm`

```console
$ docker pull drupal@sha256:8de924fff66bd170653f6439598c521dfc2816735ef95e250546bfb1f415700e
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

### `drupal:php8.5-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:6c838f97ca782657fccee1d172428c869fa1d92a552629df4c8f24e690c732c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214321696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1625a64edaa0920442524f61076418d8ca424ebc0ee982744aa54680f9e4be9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:22:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:22:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:22:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:22:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:22:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:22:52 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:22:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:22:52 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:22:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:22:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:25:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:25:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:25:47 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:25:47 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:47 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:25:47 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:25:47 GMT
CMD ["apache2-foreground"]
# Wed, 24 Jun 2026 02:30:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:30:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:30:10 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:30:11 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 24 Jun 2026 02:30:11 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 02:30:11 GMT
WORKDIR /opt/drupal
# Wed, 24 Jun 2026 02:30:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 24 Jun 2026 02:30:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c18c3d75c2b00f1d746f40c703e914250ba02ce4b792fe2e7874d004b0038d`  
		Last Modified: Wed, 24 Jun 2026 01:26:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ea14db1bae0b3678be05cb991f8a163e16c87428ed8c08ac8b2a6558639be`  
		Last Modified: Wed, 24 Jun 2026 01:26:10 GMT  
		Size: 104.3 MB (104344501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980911e68efc263e3be9633faf5c6502eefa2faedf67d9ad5e72f2f99e658f41`  
		Last Modified: Wed, 24 Jun 2026 01:26:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa95473dddae6f600733eccb929e44d77fe30c3354941a777f76728a94942d`  
		Last Modified: Wed, 24 Jun 2026 01:26:08 GMT  
		Size: 20.1 MB (20142226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f0ac9e7581e59495d43f6f2686b67abed98d9c39bcb89335b910183b0627b3`  
		Last Modified: Wed, 24 Jun 2026 01:26:08 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddf53ccdcae71f41cc9e69be3c94d18f9b151dbb915d4b29f4725a9e310f9b8`  
		Last Modified: Wed, 24 Jun 2026 01:26:08 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8249d356acb453bf5e15e8303931186859c187e41c35d8a6192c70a6353d0479`  
		Last Modified: Wed, 24 Jun 2026 01:26:10 GMT  
		Size: 14.5 MB (14527082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4947fe5b7526fb2de637b0af161c600845bfdcf09772b12998587275d33c920f`  
		Last Modified: Wed, 24 Jun 2026 01:26:10 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf3e4ee6d7eeac803b680c4a98693b8b107dfed21ed5e0a070d728c271d00ae`  
		Last Modified: Wed, 24 Jun 2026 01:26:11 GMT  
		Size: 15.1 MB (15141398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30014f0aac015ac0586c258f83933bd021eb0313e0ae5dc5c7ad139cdb9c259f`  
		Last Modified: Wed, 24 Jun 2026 01:26:11 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdc5d8d3e17626770cc471840034d8cf5fc1bd9b239e3c09091608377d847d7`  
		Last Modified: Wed, 24 Jun 2026 01:26:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a7edb565a33a85f76c0964fba38f274f646fae117ce183bcfa6a839e54d720`  
		Last Modified: Wed, 24 Jun 2026 01:26:12 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a66ad3e16021d868bd2647994a59363b221e0a7c17843a3adbfb4a085cb0d7`  
		Last Modified: Wed, 24 Jun 2026 02:30:35 GMT  
		Size: 9.7 MB (9715035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fb609a987c398c38fbc4de111a4da28450764e00a2b0353ec9836127edf5b5`  
		Last Modified: Wed, 24 Jun 2026 02:30:35 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e45d86471a1d75c9db9f7cb0a9c50e7667212245716d7fe204929c75dbf4f8`  
		Last Modified: Wed, 24 Jun 2026 02:30:35 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd028f13376397fabee5f0b9f0c0ba9241e8804d1fc12c923742d90cf7694bd`  
		Last Modified: Wed, 24 Jun 2026 02:30:35 GMT  
		Size: 823.3 KB (823342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd72e5849f33f28a52cd5b3c35dfde878e349dd7e0c81c558b212497fc67f4da`  
		Last Modified: Wed, 24 Jun 2026 02:30:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462d151bcce56163db0b5a145062fe1dac128e0d1cca6cc034c475e44d574de9`  
		Last Modified: Wed, 24 Jun 2026 02:30:36 GMT  
		Size: 21.4 MB (21384314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:6f6f3229682d622cff38d1aa76fdd4c91b1f17572043f6339913b43f0db732f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66076adce11e9dd94e90ba91e25f34b9bf4ec9a0df3d3d2c18f00181bc93de89`

```dockerfile
```

-	Layers:
	-	`sha256:a39c0dd6b00cf14d02c587e9b0c30f7d129939ad29cabf335343259b3d07f984`  
		Last Modified: Wed, 24 Jun 2026 02:30:35 GMT  
		Size: 7.2 MB (7150295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c214d29cd4bf5e3782c39bc45c8028e17c226c7d1d69f8964da809db94f6cbd`  
		Last Modified: Wed, 24 Jun 2026 02:30:34 GMT  
		Size: 41.7 KB (41708 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ea3a99f136c3bba7f4ae29df2eef3aa9b74c40c61cc8a146879e9cec44f7e8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174623927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d94e26c1ce6dd585daee4fb7a5fe0a8bb1d402304a2ab4aea42dbca6a11f0c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:27:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:27:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:27:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:27:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:27:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:27:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:28:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:28:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:28:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:28:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:28:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:28:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:28:04 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:28:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:28:04 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:28:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:28:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:31:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:31:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:31:04 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:31:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:05 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:31:05 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:31:05 GMT
CMD ["apache2-foreground"]
# Wed, 24 Jun 2026 03:56:53 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:56:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 03:56:54 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 24 Jun 2026 03:56:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:56:54 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 24 Jun 2026 03:56:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 03:56:54 GMT
WORKDIR /opt/drupal
# Wed, 24 Jun 2026 03:57:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 24 Jun 2026 03:57:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f90378e203cbbf7c38bf57b18d94cec1d15839956be43f5f9647aa7b97c35c`  
		Last Modified: Wed, 24 Jun 2026 01:31:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693e00faf3ca9348fe09e19bf72257509be1934c5a061a94ab9ff90cef1cce91`  
		Last Modified: Wed, 24 Jun 2026 01:31:23 GMT  
		Size: 76.2 MB (76154426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee28e921f02f250a94675f85482c9766d4f5ced6d80405b00f8a5fffda272be`  
		Last Modified: Wed, 24 Jun 2026 01:31:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d842c2fb1bfb43fe2f0e7002d159a992a31d0b69679165fe4dda1e8aca9fa580`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 18.9 MB (18850451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05421b020aff4441c1fb8dc3086911610da7148f75e994c591c780a47d21599`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232937b4d06b47b6bcda7b0189cb3605fce874bf900defaabfcc92b55c0b1b63`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e776cf0fc6e039d19bb642a123d56efd0c806db1ccee1627c3505b1a76703037`  
		Last Modified: Wed, 24 Jun 2026 01:31:24 GMT  
		Size: 14.5 MB (14524976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af267ee0cf820aa9250842e9efbd7d23ab2e6654c32f68b4ebeb9979ed85aad9`  
		Last Modified: Wed, 24 Jun 2026 01:31:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d625d84ee0497382bd7e4974d77410b3a5224699c2670e9cbdb36c9fe39b1`  
		Last Modified: Wed, 24 Jun 2026 01:31:24 GMT  
		Size: 12.6 MB (12602798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334d585984029566edf4ecc98a9f0eff13be278636c743de0c45e1004079ec90`  
		Last Modified: Wed, 24 Jun 2026 01:31:25 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa74b20055bb65dacb9c8cc6d091841da4d5020acce84560dd557e10adf26c`  
		Last Modified: Wed, 24 Jun 2026 01:31:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f47daceb91d4a9136591a8241be34086a27979a44194941f0872a7d71841e9`  
		Last Modified: Wed, 24 Jun 2026 01:31:25 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c9823361154688f11801fa791cbf86bca0cae8edd1aab69152ccd16872a10d`  
		Last Modified: Wed, 24 Jun 2026 03:57:19 GMT  
		Size: 6.3 MB (6333006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35cfbbe7584596b66deda91175b74f359bde1413de1e55332fd4c78acd032b`  
		Last Modified: Wed, 24 Jun 2026 03:57:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fcef0e50e551dec41c054d50619eb84db1427fc9b413568846f636e68817d2`  
		Last Modified: Wed, 24 Jun 2026 03:57:19 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a3abfe1044c88b78cbb768b0e4905d7107d8f869fa54da66807c13caf0365a`  
		Last Modified: Wed, 24 Jun 2026 03:57:19 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea617a06e31e6f33cfb5e6edd8ee0b6cd0d8b32656baeae0a9f7655c39692868`  
		Last Modified: Wed, 24 Jun 2026 03:57:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c000bafbb1525ea13ba23d6c0aa7026c8b0cdc62a9f7b5a7c1caabb06c4b5f90`  
		Last Modified: Wed, 24 Jun 2026 03:57:21 GMT  
		Size: 21.4 MB (21384240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:0a02b25bbb5deb5d6ea7f6204de5b282d6bd97d5e2d0c294a059567c32d34c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7005687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ed95c646388d6a8eabe26a1424c6062fc99b297903585da6e9825c0ce3c000`

```dockerfile
```

-	Layers:
	-	`sha256:84966b3740852b5980b32ca5504dc38719dfb36d112eacc7344d92f3521dfe84`  
		Last Modified: Wed, 24 Jun 2026 03:57:19 GMT  
		Size: 7.0 MB (6963844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e65c4dd9e43a36e04bdbf2ca5b7244b2a0128538834a8f4db889404fb28b9c`  
		Last Modified: Wed, 24 Jun 2026 03:57:19 GMT  
		Size: 41.8 KB (41843 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d82b3dc51cfa5d81c780bcc33edc6a64fb06f59f9b28e91353f3966f3009e8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205501043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74184978ee414cd9b5c80050b0fba5a22c0f7c3952959836b8e89d86da477712`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:23:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:23:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:23:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:23:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:23:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:23:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:23:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:23:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:23:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:23:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:23:21 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:23:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:23:21 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:23:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:23:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:26:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:26:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:26:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:26:30 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:26:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:26:30 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:26:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:26:30 GMT
CMD ["apache2-foreground"]
# Wed, 24 Jun 2026 02:37:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:37:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:37:17 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:37:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:37:17 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 24 Jun 2026 02:37:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 02:37:17 GMT
WORKDIR /opt/drupal
# Wed, 24 Jun 2026 02:37:24 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 24 Jun 2026 02:37:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e61177314a754000e2982c2cb520dc26f5b6283db3907f93d9c70b6aa0cb349`  
		Last Modified: Wed, 24 Jun 2026 01:26:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41afbaa08b8c8d7c89ed5f7b3d94ada166d4e1175be49979f89d40ddd1faeb`  
		Last Modified: Wed, 24 Jun 2026 01:26:53 GMT  
		Size: 98.2 MB (98178477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a5eb364eb3e5ac5563656abc141f4e49afbcd28c7834ecd05359ff0bf5282b`  
		Last Modified: Wed, 24 Jun 2026 01:26:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8525a82be1d307578b6b7a6737fd4d65fa4257e9fd1c96e9285adaac7fa949a6`  
		Last Modified: Wed, 24 Jun 2026 01:26:51 GMT  
		Size: 20.2 MB (20166562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a50c0ff0b5ec208f5d5dd7830480c959f0f190e506ae44f820fc82766775c1`  
		Last Modified: Wed, 24 Jun 2026 01:26:51 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1636f198725e7bc070bd31660ee6144619d2ade6b093d568746cbeb36ae4e`  
		Last Modified: Wed, 24 Jun 2026 01:26:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f41c84ff1e60d40e4369f2ec2ae01b03ab6e575ad90720ae3fc3d60d2e87611`  
		Last Modified: Wed, 24 Jun 2026 01:26:53 GMT  
		Size: 14.5 MB (14526793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14da347b7727c972bde6961a7dd8869388ed0494633e2e2c89feab78f088b426`  
		Last Modified: Wed, 24 Jun 2026 01:26:52 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadc00e3e53ac229337106f8089924717e3816f8a1dd5bc11f1638d8d324c684`  
		Last Modified: Wed, 24 Jun 2026 01:26:53 GMT  
		Size: 14.7 MB (14684809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9c1a0420bc96279f81f6877b253694b10f742c3b3da1ddbec7468468c48f21`  
		Last Modified: Wed, 24 Jun 2026 01:26:54 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491619e8c88ce345a7dcaa49b5d7d59a4bbdb3573278dd922a79dd51b5bc989`  
		Last Modified: Wed, 24 Jun 2026 01:26:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e98c9919c32d81b64e452478adc37c248d0074c9280f4e1b607b4fe2d09e88b`  
		Last Modified: Wed, 24 Jun 2026 01:26:55 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33589c64dbfbc0c1ba6e0dfae64dcb2157f27b76e6052e4c530422c63faf064`  
		Last Modified: Wed, 24 Jun 2026 02:37:43 GMT  
		Size: 7.6 MB (7608213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1befef47f036b7147f8f14751cc1c83376d5d9a9b632404c7824a44a72591251`  
		Last Modified: Wed, 24 Jun 2026 02:37:43 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e61fa31a7bd85b697da2ef1a517ab6095cbf821e9f68bdf94eeaede8d304391`  
		Last Modified: Wed, 24 Jun 2026 02:37:43 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d3e35534e6aa0f15d597a12854397412459af34b20abfb38656627c02f5389`  
		Last Modified: Wed, 24 Jun 2026 02:37:43 GMT  
		Size: 823.3 KB (823344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52717790247e0d880eb6385fcf376e3348197e55bc21ef13c636017dc9499050`  
		Last Modified: Wed, 24 Jun 2026 02:37:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1772875f892850ef715f7f99208512ac8fcaa1b7ad76b4b320ec9d238181fd`  
		Last Modified: Wed, 24 Jun 2026 02:37:45 GMT  
		Size: 21.4 MB (21384258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:45942b1d553452d67ebe175e313c4fdd142dffb01182863386735151240a3676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451f9540ae00b398204058dbbdb594e33f129c109ba7c8ab86cc53375dadcb83`

```dockerfile
```

-	Layers:
	-	`sha256:ebbb32f8930d421b804f34c927494ba29b49a3667b92b8f5a535e1779b8e1c24`  
		Last Modified: Wed, 24 Jun 2026 02:37:43 GMT  
		Size: 7.2 MB (7178779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f68a3615361eaef950cd69e0db5ac2dcab4a56933566e00758554d625ee9dc6`  
		Last Modified: Wed, 24 Jun 2026 02:37:43 GMT  
		Size: 41.9 KB (41876 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:cda0892f386f2298116e6fb8ce031db35460303be5a35abc68dd02e5894c2a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210214892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b69b4132d36241691cb7b64a6a55ca38dfe4110502e593999a95e064ed0bde`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:19:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:19:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:19:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:19:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:19:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:19:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:20:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:20:00 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:20:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:20:00 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:20:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:20:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:23:28 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:23:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:23:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:23:28 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:23:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:23:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:23:35 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:23:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:23:35 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:23:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:23:35 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:23:42 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:23:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb0c8c72b4e1426304e46511f9acd004e3d19ac0f8e60c84d09d6c1f94be000`  
		Last Modified: Thu, 11 Jun 2026 00:23:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e446bb4f64170bbd544cd502a35060557e49defad8139c7fc19bde65b2ee58a`  
		Last Modified: Thu, 11 Jun 2026 00:23:51 GMT  
		Size: 101.5 MB (101536860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9616a92d330e2fddb2b865dedc8c51d0a0f82ab634cb3294622a41ac2f3361f7`  
		Last Modified: Thu, 11 Jun 2026 00:23:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6825dad5f4707b4da79a299fe5838aa2ea999847e70827c83b54f3ac2696b733`  
		Last Modified: Thu, 11 Jun 2026 00:23:48 GMT  
		Size: 20.7 MB (20665695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651494a554c945d1bc8a9c38bbd9cd904cb5158003f63b212319a7a86c50fb16`  
		Last Modified: Thu, 11 Jun 2026 00:23:48 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f8001f000d0760fa689362ecd249d1542f5332588d96c4dec49215eefaab05`  
		Last Modified: Thu, 11 Jun 2026 00:23:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07351a3e564bec335f6609fec39782d21c2db5f7781d47433d725e18c094bea0`  
		Last Modified: Thu, 11 Jun 2026 00:23:50 GMT  
		Size: 14.5 MB (14526090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a39b638f97a27a1388ad315f829acdaed3996b9684d0d4ca071050e9e5fcb6f`  
		Last Modified: Thu, 11 Jun 2026 00:23:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc39dbd9d8a3243dd44394d2adfc2996f897c82f727479dea2d6e380e5d2f26`  
		Last Modified: Thu, 11 Jun 2026 00:23:50 GMT  
		Size: 15.5 MB (15487567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5976f59dcaf5b52154274e1af705b890d2806dd247d19c7e31f432cd16207017`  
		Last Modified: Thu, 11 Jun 2026 00:23:51 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa1ece39ed3b8305cd2bb4f0d0a4af2f66db2541a891fba54aec466335ad3c`  
		Last Modified: Thu, 11 Jun 2026 00:23:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8285f40d0dfc91863038c06c6b7b259e4d71d20a964f4c35d6a28b288ebc23d9`  
		Last Modified: Thu, 11 Jun 2026 00:23:52 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef93685aed8cd92a8fb62ac43143ebba9f2bff964321d364079e823227d902f`  
		Last Modified: Wed, 17 Jun 2026 22:23:59 GMT  
		Size: 6.6 MB (6559342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8178270a1c999a1092b4bca2a8443afa20097ac02c4d7f9d64c01c45349ac281`  
		Last Modified: Wed, 17 Jun 2026 22:23:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe30f9dcb0649d76d92b2ac869869fbdc5a28be47d4bf3aa75e7be0ede59523`  
		Last Modified: Wed, 17 Jun 2026 22:23:59 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99da04335555edc97cb0d00ed0bb4a740714b76ae6aa7648457ff54de484895`  
		Last Modified: Wed, 17 Jun 2026 22:23:59 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c563b12e5a78cf51f3a148d7b92009d7d1a3377cafd1bc1d8fd934d2026da6`  
		Last Modified: Wed, 17 Jun 2026 22:23:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfb30214dc5d27770d20b09a669439a2278dda262a97a689b1e8e7a0794fee2`  
		Last Modified: Wed, 17 Jun 2026 22:24:01 GMT  
		Size: 21.4 MB (21384064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:67e0996af01f9b55722910b60cd97e60f352d6dc6edb1811c9fda78da870cf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7164975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84e80f98e5a1ac1ddc5fee917a02bd7359ac40ae8c061f5830c98648534454`

```dockerfile
```

-	Layers:
	-	`sha256:a62f96c6eae6941c4e9e2d63b380b6850993fbe19fab75c20c8d8b44c15d6277`  
		Last Modified: Wed, 17 Jun 2026 22:24:00 GMT  
		Size: 7.1 MB (7123311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f081fc54bfef4a67849f42a86e5feed665bb43f367d779b8f018f56b21e3a506`  
		Last Modified: Wed, 17 Jun 2026 22:23:59 GMT  
		Size: 41.7 KB (41664 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:9413a1d57ad7f131f17cc7f0d10a578b154ed6d429ed0c43b8d5aa4f0c6ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216851690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b194f0608b590ed20cf8f85b118231da9b459a8e8e0794d931c85c1c904d2939`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:11:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 03:12:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 03:12:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:12:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 03:12:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 03:12:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 03:12:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 03:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 03:14:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 03:14:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 03:14:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 03:14:53 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 03:15:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 03:15:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 03:19:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:19:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 03:19:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 03:19:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 03:19:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:19:33 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 03:19:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 03:19:33 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 16:34:40 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 16:34:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:34:40 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:34:41 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:34:41 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 16:34:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 16:34:41 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:29:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:29:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f401effa3d6714ddb79ba94727795c8f0a3a88062ac122b5ee2b0e8569182b`  
		Last Modified: Thu, 11 Jun 2026 03:17:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240f00b5b075e0ec40f2f3588739804d321a9e2a31a0cc00af6e3a278e020250`  
		Last Modified: Thu, 11 Jun 2026 03:17:11 GMT  
		Size: 103.3 MB (103334125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0f2e18a8eceb1609665b9d19e05533e28d58fec8497b4915edf3585bc68a5`  
		Last Modified: Thu, 11 Jun 2026 03:17:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a05a0266369b3c5d29abc9937572a5304dba0263036108ba471fd1b198e131`  
		Last Modified: Thu, 11 Jun 2026 03:20:01 GMT  
		Size: 21.3 MB (21333938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e015947f7c149906d4247585ea0cf14955eecf5a551cbec15e0715f260ee7f0b`  
		Last Modified: Thu, 11 Jun 2026 03:20:00 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253f39cd570c2a553c8d84e262880bf813fa0dc7c859fe1abf85b47bfbfefaa0`  
		Last Modified: Thu, 11 Jun 2026 03:20:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d16037bc6ea5ad2ece6e03704bea95de98fdb70335309f9fb2c52e71b6600`  
		Last Modified: Thu, 11 Jun 2026 03:20:00 GMT  
		Size: 14.5 MB (14526518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d7f40c39e72a069ea3b56d4fd119e786e5930848663a05c3f2d8667a3a25be`  
		Last Modified: Thu, 11 Jun 2026 03:20:01 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58ab722bb4dc6aa8401f3766817dc95cffb1a24de99d09c698365ea115aeb6e`  
		Last Modified: Thu, 11 Jun 2026 03:20:02 GMT  
		Size: 15.1 MB (15133251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4238deaa9779c9dbcbeaf441205e61b53ddd480e34e3aacbf0d3e981174353e6`  
		Last Modified: Thu, 11 Jun 2026 03:20:02 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55c6a24752d27aac22320cbfa4d31bf84317801ed9fbc390c7c828ce0103dae`  
		Last Modified: Thu, 11 Jun 2026 03:20:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bcad87a1500c24183a479c7cba17cc43baf4757f731f6de19a3a35fc7625a9`  
		Last Modified: Thu, 11 Jun 2026 03:20:02 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dedc5f8d67a34ce59bccd36c6e6279bca62ba1abcb5d941c9787e5adde95a1`  
		Last Modified: Wed, 17 Jun 2026 16:35:45 GMT  
		Size: 8.2 MB (8228155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d073805c2df09db2420916ffa90a13a7d4e465253c24b20b09e82bb71816b89`  
		Last Modified: Wed, 17 Jun 2026 16:35:45 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b1cd979d33aa74ae1c3171d1ed6d854ba0c19c8871575cf982e2a94e442cc`  
		Last Modified: Wed, 17 Jun 2026 16:35:45 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cdbacf9c1ecf0958e8c211c61a943f8d52f55feb101300e66da1ca7ca9fb14`  
		Last Modified: Wed, 17 Jun 2026 16:35:45 GMT  
		Size: 823.3 KB (823344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03166d017a1ce4d9ec611261d5286f2ffe35b63ce3eef451120b22654ae5ef36`  
		Last Modified: Wed, 17 Jun 2026 16:35:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f992444d1738b78ca26b96b85c66f15cddf231b10e5dfa3013a6e4a1a09e203f`  
		Last Modified: Wed, 17 Jun 2026 22:29:37 GMT  
		Size: 21.4 MB (21384228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:bfdef891dcc5f5c2ae74f08e530465c74a492d34e8c3354359d7b53934f9f405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7169287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a05527e8a399be83dc3aaf7309f3c0dc936a548d92574861f15cc56e50a339`

```dockerfile
```

-	Layers:
	-	`sha256:aca50009409f451902fc4e79a765e3f434b71441819c1e785462dc29589a697a`  
		Last Modified: Wed, 17 Jun 2026 22:29:37 GMT  
		Size: 7.1 MB (7127518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7722b375437ea865aeb31ef19d26f687d427ae8df1ffebf0f132cca59a7067c`  
		Last Modified: Wed, 17 Jun 2026 22:29:36 GMT  
		Size: 41.8 KB (41769 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:ec9a420e298b8e38889749eaf8d5f6b7c18901d77370f11fb5926a9eed6d665b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185394527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfed53a63071ae2fe77ac7435a9e74cf867675d93a1e282a80290bf3ae325ab`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:29:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:30:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:30:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:30:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:30:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:30:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:30:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:30:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:30:49 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:30:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:30:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:35:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:35:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:35:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:35:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:32 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:35:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:35:32 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 17:08:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 17:08:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 17:08:45 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 17:08:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 17:08:53 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 17:08:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 17:08:53 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:23:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:23:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760bd98ba6f0dd242612b772363db9255777926da7a6de678aecf2f09b8d5732`  
		Last Modified: Thu, 11 Jun 2026 00:35:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67c915a547eb9b0822aa7ee67c5e7ecc13a91135df9ea75a1bc931a92c4d2fa`  
		Last Modified: Thu, 11 Jun 2026 00:35:17 GMT  
		Size: 80.8 MB (80829344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ec25b7891427e77853374900796edc8ff332bc21cb7b919324f378695e981`  
		Last Modified: Thu, 11 Jun 2026 00:35:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff87533fc6ce2cc27ea6fc98a8ad365f202059a976a90eb88a9e5ada587c869`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 19.9 MB (19919167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d853badeade8087e2e91365ab8a8094c92ed367d01c47a0c04a34e847be56`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594731f96f9f714220f03b14ca6aea7d1f24f21d6d2f25ce308d3271d7852dc8`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6de136b656cbab62c00b269e7940ba68724f930fb6f7ef4e5424fc79fffd45e`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 14.5 MB (14525308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992d704578101684e2b2d4ebd1f5874868093f343b1b5e82e928a484e9e2da91`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43792a132d5cdcd3e392fee3a1215f61639cb538386887ce6d5540e5e145c6e7`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 13.7 MB (13674331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691c45aa525164f9c2e5cfc62fcfea861938da174bf7e22e48af19394b1fa982`  
		Last Modified: Thu, 11 Jun 2026 00:35:52 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbead012b3213b3efa43d0a72644759b3f3a3b66ef6a4d4d0fa0ff25524f836`  
		Last Modified: Thu, 11 Jun 2026 00:35:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b85859da9d25bbcc0047f4cb4b1b467bf3550bfae23b1238522d9e73b63487`  
		Last Modified: Thu, 11 Jun 2026 00:35:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26307187df935b2ce83199b165e9e8ee99ede53c19a73c7cf3e79e7f90ec0ce`  
		Last Modified: Wed, 17 Jun 2026 17:12:27 GMT  
		Size: 7.3 MB (7339466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92afa3a242937cba8e3f00b644c52c67bdf61da3c349f1ed37f91f0baca46b32`  
		Last Modified: Wed, 17 Jun 2026 17:12:23 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5974ad1cfdcd68203a4ca91bb17a4d3b33dc0356dd4f24586989dba9736a10c8`  
		Last Modified: Wed, 17 Jun 2026 17:12:23 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e2ace9a2f8a17786d475aa0d1c82f0638a04acca97c3e65767fcbded030690`  
		Last Modified: Wed, 17 Jun 2026 17:12:24 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b536c556d65f5935ff3a0de00c78b223eadafa5e02c79d141d67690b6e886d`  
		Last Modified: Wed, 17 Jun 2026 17:12:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcf08461202aa970c031f11eaa63e1de5c952fb3c263625cffab78a13fa642c`  
		Last Modified: Wed, 17 Jun 2026 22:23:46 GMT  
		Size: 21.4 MB (21383906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:11a39bf4ca10c1ef3ea1a418be2f33d8357aad115715e3e2bbdaba27f5f88e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24ad2974fa4fa5806bb71a90fe89529b01f1babb7c931d5499216a68b92deb9`

```dockerfile
```

-	Layers:
	-	`sha256:dd1204b018a177c0abeb904a9c5a04a4415260506e742ef0adc59915eaf76d00`  
		Last Modified: Wed, 17 Jun 2026 22:23:45 GMT  
		Size: 7.0 MB (6987426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a882d1819d38b5747e93d0fd23f61cb420d19b93187a870d6e5e1411ca7a87dd`  
		Last Modified: Wed, 17 Jun 2026 22:23:45 GMT  
		Size: 39.5 KB (39503 bytes)  
		MIME: application/vnd.in-toto+json
