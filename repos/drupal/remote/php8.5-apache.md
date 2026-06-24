## `drupal:php8.5-apache`

```console
$ docker pull drupal@sha256:068437d3670de68d7a35d4953c5cd06c30562613c60cbda723f906f9c1ec7e86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:php8.5-apache` - linux; amd64

```console
$ docker pull drupal@sha256:2280055b0f434804a20f751e558e314bb9e32e3dc3c3352a28658102dae05a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214617834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc44294725301461fdc7960897e3f705894414d14cfe1beafc69183657d84f68`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 24 Jun 2026 01:22:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 24 Jun 2026 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 24 Jun 2026 01:22:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 24 Jun 2026 01:22:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_VERSION=8.5.7
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Wed, 24 Jun 2026 01:22:33 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Wed, 24 Jun 2026 01:22:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:22:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:25:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:25:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:25:30 GMT
STOPSIGNAL SIGWINCH
# Wed, 24 Jun 2026 01:25:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:25:30 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:25:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 24 Jun 2026 01:25:30 GMT
CMD ["apache2-foreground"]
# Wed, 24 Jun 2026 02:29:44 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:29:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:29:44 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 24 Jun 2026 02:29:45 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:29:45 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 24 Jun 2026 02:29:45 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 24 Jun 2026 02:29:45 GMT
WORKDIR /opt/drupal
# Wed, 24 Jun 2026 02:29:56 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 24 Jun 2026 02:29:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a467f63f31d2616c310055046c605a93ea1fe48078c67861e78cf37d279d7777`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cd8cf70218fc4e56541cb3e05a22d4ab3812f5f4c5e22072f81d2011085ce`  
		Last Modified: Wed, 24 Jun 2026 01:25:54 GMT  
		Size: 117.8 MB (117840326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bdf34c4bd20e1485cd978330852c28fc37950991d9f50dbd56c921a19888db`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ea8a1bab4147b513a7ad6eb3e6fdd3cd19a1de388dbd02bf25a9f72d69bc74`  
		Last Modified: Wed, 24 Jun 2026 01:25:52 GMT  
		Size: 4.2 MB (4227893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058b513747a49aada290a9d5cfebb843616877aa75899b059b173eb25cd3367a`  
		Last Modified: Wed, 24 Jun 2026 01:25:52 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0505689d8e529d2f24e7b00c74f96ef76fa09b59a03d10b47fd302d6ea5ea2f9`  
		Last Modified: Wed, 24 Jun 2026 01:25:52 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd730ba35bdcc39ec39bc1802e39b0914b8a0e1e091a1f69075215680ce6a6b`  
		Last Modified: Wed, 24 Jun 2026 01:25:54 GMT  
		Size: 14.6 MB (14564396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b84428c4b87ed572e1c8adf9a454e07198354f1b2bd817c550d242a951fc41a`  
		Last Modified: Wed, 24 Jun 2026 01:25:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2d5de34f5d1d82e05215d69feab39d7a24f836e339648a645e8730db37a05f`  
		Last Modified: Wed, 24 Jun 2026 01:25:54 GMT  
		Size: 15.2 MB (15172107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6193db2487e8554044a1e179710db14adba06d7eb410d1855bdbc100d4f78470`  
		Last Modified: Wed, 24 Jun 2026 01:25:55 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934c7105d35abd7833dced2ce557685b63d638b703db77920401b6c9e72c30f`  
		Last Modified: Wed, 24 Jun 2026 01:25:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dfa111f2e4a005e4c55b49d3e9234634eac508ee9b8a800a97236da009bfec`  
		Last Modified: Wed, 24 Jun 2026 01:25:56 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581e4565e6c445d8b8ca668c9525e0a1aa72df3acdc691c13d1cb59f258c241`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 10.8 MB (10813812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597a2788ce434b5baae796d57bb3f1e800ecbb43248a778a55da759b0d42cc9f`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b83cad2fb1913c5a28a36c205e1c5bbf7cd89ab1f231003c756d847865438`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72addd6bedb2a1f8b36b321255189d4935a3befb4ffe866e87313d01c97ea3`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 823.3 KB (823339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0839c19f490a0a2ea96fcef7d2a70cf9e9c8b05d77052ecf598ce053a38ce85f`  
		Last Modified: Wed, 24 Jun 2026 02:30:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32522e079d8e1f5f6e6c9a955dc54392d1aa2af1b8421976522f4dfef66c6c09`  
		Last Modified: Wed, 24 Jun 2026 02:30:15 GMT  
		Size: 21.4 MB (21384389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:b6c5b54d949dc0071207069be56ed11e1cd208130998820ee1218d60c8b6c99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7503407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e333583226646458438f77eeca31663c059c5f8d2f7750f29e47dbe03857821`

```dockerfile
```

-	Layers:
	-	`sha256:d25a2adb7de0db8fe89bdea57a8bb1905d83e77ed5470b343cefb10d48e0f3b7`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 7.5 MB (7459221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0c86b9362772e5133a556e56c099dfc0171e45032ef62e7217d6095bd5ba78`  
		Last Modified: Wed, 24 Jun 2026 02:30:12 GMT  
		Size: 44.2 KB (44186 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:2ca406f5b3153f1e2eef0be6746be95be163c3d952bdd7052171d431a84d8bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172212030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888699fac8408a9c24073a113ce07d27de78e2d6539ebd99662c77671fd1014f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:25:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:25:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:25:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:25:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:25:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:25:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:25:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:25:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:25:48 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:25:48 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:25:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:25:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:29:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:29:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:29:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:29:02 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:29:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:29:02 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:29:02 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:29:02 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:24:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:24:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:24:38 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:24:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:24:38 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:24:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:24:38 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:24:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:24:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a5096c8e315268d2e6e3c3324a9b6a68b349959f9c1321bced1c8ce4e6508`  
		Last Modified: Thu, 11 Jun 2026 00:29:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b51cc1d4e0fad8159186b5df96c242bb4ab64e6f8dd8dfff388b824acd9e6f`  
		Last Modified: Thu, 11 Jun 2026 00:29:21 GMT  
		Size: 86.3 MB (86255562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dd2c90ceba4df47e0f9b43e63fba9a63557f2ceb0d1cd7d8d831172ba11b1a`  
		Last Modified: Thu, 11 Jun 2026 00:28:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d67f4c23ff291c5e2b6f7657b4be47ebf6007d89a2aa56579f8cba6f1e1e94b`  
		Last Modified: Thu, 11 Jun 2026 00:29:19 GMT  
		Size: 3.8 MB (3756645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b3ef2d5513951600653f0f033088e3776c475752c6d8e632b57c61e895dff6`  
		Last Modified: Thu, 11 Jun 2026 00:29:20 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa1b54de2549bf804e8952445709f7a066e95237360bd285fbe8ef3888b602`  
		Last Modified: Thu, 11 Jun 2026 00:29:20 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0556823464f807caeca9c418f41ddf66982355ba104d704b687c247e84069f9`  
		Last Modified: Thu, 11 Jun 2026 00:29:21 GMT  
		Size: 14.6 MB (14562034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f9ce99c5489a330f2b966a19de31e5bcfb32b3ab3dcd84a2b3ed0aba2849cd`  
		Last Modified: Thu, 11 Jun 2026 00:29:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2f1686d45428b4b431e2cda0bcfa2fa2ef5ff1223cb343ba5a269703e19c0`  
		Last Modified: Thu, 11 Jun 2026 00:29:22 GMT  
		Size: 12.6 MB (12623802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350e2aad5d9205097703053cc1b5bb913255fc9687437c18a92ff47c95d4ecf1`  
		Last Modified: Thu, 11 Jun 2026 00:29:22 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993d57213e4836c036ee5c8907ae77b1ce165b2ae0189431e41cad5b90d2d882`  
		Last Modified: Thu, 11 Jun 2026 00:29:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a499580c7acd85faf8f6d9755a5bcb22ea3e609e0a487234b889faab4bb47e6`  
		Last Modified: Thu, 11 Jun 2026 00:29:24 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc2aa3d512b28eee9a723d42a66133054846b6093b2cc9aef60325f43df57`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 6.6 MB (6589641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03edbc2d723ebab345e5f397d775fb730e98b48ce466ca8e7f8fed6bd77da263`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c5f962cd1d4237b2660b51b6202fd1c62997f8b381409cdbc12db60fd6b8d1`  
		Last Modified: Wed, 17 Jun 2026 22:25:03 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fb92249fe3ac057ccddfa1ddf8ef3be537c56d65ad309944debcc80ab3f22d`  
		Last Modified: Wed, 17 Jun 2026 22:25:04 GMT  
		Size: 823.3 KB (823339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d2d94a75e17288e4e29ce45b3def6867ec787adb0e86cb05aedcd30a9c773d`  
		Last Modified: Wed, 17 Jun 2026 22:25:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dac6927ec464d436015c12105dbee875ae3589e21c928c2242ca8210a2c9c3`  
		Last Modified: Wed, 17 Jun 2026 22:25:05 GMT  
		Size: 21.4 MB (21383843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:6adf9a9e913749064108178b6715af90303cc7ec519b352fa1d72a4e3e5386bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f8a21f3da40ea42b5c7f5442a9443e0ec81bd5e800f7e762cba50ff48666cb`

```dockerfile
```

-	Layers:
	-	`sha256:927d8a9b9bb55487f43cb0edc7f5bc34c9239b0fceab161c25697e4252aa578c`  
		Last Modified: Wed, 17 Jun 2026 22:25:03 GMT  
		Size: 7.3 MB (7263425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c888bd824e717e7570446eb840a90dee0b7e97a71562089ff24b78e9171ebe5`  
		Last Modified: Wed, 17 Jun 2026 22:25:03 GMT  
		Size: 44.4 KB (44378 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:dbdc1b79ebdccdf08ba5b3f7ad3d2c7b5f8dcb3380d8d1cab7a6e6ddff2c2818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205462524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b64e57b702b87f468a45e0687e3e828b8dde604805bbde71cd5c753ccfef713`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:24:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:24:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:24:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:24:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:24:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:24:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:24:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:24:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:24:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:24:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:24:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:24:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:24:26 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:24:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:24:26 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:24:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:24:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:28:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:28:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:28:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:28:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:28:00 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:28:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:28:00 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:25:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:25:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:25:47 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:25:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:25:47 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:25:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:25:47 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:25:59 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:25:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d707d1aedb1e0ce5c0ec9d74a7406eb41b011e9ffda95573996d5664b29978`  
		Last Modified: Thu, 11 Jun 2026 00:28:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc76b9b839d43aac3d144509a9e90a57deb1115c4670de46bc505524a748607`  
		Last Modified: Thu, 11 Jun 2026 00:28:25 GMT  
		Size: 110.2 MB (110168385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf3fa0141d4e2eefc6c0da69f756b025b631789681780575df180924f272ae`  
		Last Modified: Thu, 11 Jun 2026 00:27:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4489707afaf2d240ce1f456d04b1a4c44d1d44a78790c629e1891dd3a5e42b`  
		Last Modified: Thu, 11 Jun 2026 00:28:22 GMT  
		Size: 4.3 MB (4308294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b982f4e9832e6b013e57bb89360f9e074459d002acdbd391e5e12a412e19e185`  
		Last Modified: Thu, 11 Jun 2026 00:28:22 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bea9ab77373812d767039598774a3545087b21b771f6ca84c0ba0f4298fdddb`  
		Last Modified: Thu, 11 Jun 2026 00:28:23 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b836e57477aa87e2a42bc51e0bdfee66faaea208cab92fbdfbaf157c31293f0b`  
		Last Modified: Thu, 11 Jun 2026 00:28:24 GMT  
		Size: 14.6 MB (14563941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036ddfedb5fe4af93fe3a8512c22a7346a3f710911bfe5422056ce354c3a8ad2`  
		Last Modified: Thu, 11 Jun 2026 00:28:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42810b67f444c1834597bfeec90c8e6a7bdb7a1270f8421fd23888c8fbebda9`  
		Last Modified: Thu, 11 Jun 2026 00:28:25 GMT  
		Size: 14.7 MB (14734170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b071eaad8b5f41285d2879b659260181c5dc2aee36e18535c13f828aa76dad`  
		Last Modified: Thu, 11 Jun 2026 00:28:25 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978d30103ed8e955632a4c2e2786e513398fca86e8eb99eb3de47f87ac5723aa`  
		Last Modified: Thu, 11 Jun 2026 00:28:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc8c8ad7bcd84ebbed1b909b8ab3eb00543f0534dde0f9a7913ba09eb6614c4`  
		Last Modified: Thu, 11 Jun 2026 00:28:26 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06392a7aae08a37cad8fe1ea2c7860a63a0bdfdf311ae9e34aaa606d85d4308`  
		Last Modified: Wed, 17 Jun 2026 22:26:18 GMT  
		Size: 9.3 MB (9325492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed82bedecb78fbd2b7d5db0fe21287b1222073b684e9dd29bbd543cee02c3dbd`  
		Last Modified: Wed, 17 Jun 2026 22:26:17 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0676a27d5ed9c79e2f82d772bcdadab7cf3c1f0a01786c60d9076d49f692e31a`  
		Last Modified: Wed, 17 Jun 2026 22:26:17 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5d6809be2cea08270881f7d7b4550df7025964a65999420e5376b15654106f`  
		Last Modified: Wed, 17 Jun 2026 22:26:17 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0661be2c4e38346397fbda589ec8820c5689e722f64efa5ba3329fd2006a544f`  
		Last Modified: Wed, 17 Jun 2026 22:26:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195629aa9da9e7fed332758ee55cae0380ed9ee8d30bf2dfbc63a6db35ff5b7c`  
		Last Modified: Wed, 17 Jun 2026 22:26:19 GMT  
		Size: 21.4 MB (21384209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:635b071f422ef22358ecda7035da3baf1b3be099907541b85208dea0466ead33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7601159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b6d1c0e83a3204c0175470040c70ce43c5e6042374fbf072e66abd9a90bb68`

```dockerfile
```

-	Layers:
	-	`sha256:e2999a0ebdcebca70e4969057420f9089280198992657e76e741fda5e3ab068b`  
		Last Modified: Wed, 17 Jun 2026 22:26:18 GMT  
		Size: 7.6 MB (7556708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b2f9d19d11010dbf70f3c9df55cbae01d18e7b4a80b1f156c6f4b395031f43`  
		Last Modified: Wed, 17 Jun 2026 22:26:17 GMT  
		Size: 44.5 KB (44451 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; 386

```console
$ docker pull drupal@sha256:97e5749dfa3f5c87ac848fdd42082ee883d9ae16570d80050da5c99cd54f7b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212675097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117ccdff8b33e13e9dbce19cd752f5f71fb6c7535a44ab7891aeac97da3d7d3e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:18:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:18:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:18:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:18:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:18:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:18:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:18:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:18:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:18:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:18:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:18:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:18:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:18:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:18:57 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:18:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:18:57 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:19:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:19:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:22:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:22:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:22:30 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:22:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:22:30 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:22:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:22:30 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 22:22:15 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 22:22:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:22:15 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 22:22:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:22:15 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 22:22:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 22:22:15 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:22:21 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:22:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5f619280ad652990fd1f4bc2786c0a2eff440abccb5682b363c6ffdf954f41`  
		Last Modified: Thu, 11 Jun 2026 00:22:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871f18ca81a72be829f68922671c4c57129dba87eb918fba93607d2c542d49dc`  
		Last Modified: Thu, 11 Jun 2026 00:22:53 GMT  
		Size: 116.1 MB (116142365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049e67dc81f55d81ca9066229a1a51ffc314ef037f1013154dfaf4c712264c99`  
		Last Modified: Thu, 11 Jun 2026 00:22:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb301a7b992778dc292ef4317ae416814bd449f62a97ab829690896304b5a23`  
		Last Modified: Thu, 11 Jun 2026 00:22:51 GMT  
		Size: 4.5 MB (4459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f69d7a97f5a9b0db0f18c2c88f56726f8cae6f1dcf87e3fd1e39875aa11f2b`  
		Last Modified: Thu, 11 Jun 2026 00:22:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f237c819c6f549e6063a833f7f3c2664115670b15ac856336dd505dd89cee2e`  
		Last Modified: Thu, 11 Jun 2026 00:22:52 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3ce4f2d174f9f7d1f5d4dc5749b134de514a9eeffd8d1105bd97a2cbe9b3d`  
		Last Modified: Thu, 11 Jun 2026 00:22:53 GMT  
		Size: 14.6 MB (14563143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034a0a2380918f46828dc0e2068e8bc25c40412917ee5e29b699829fdd0019a`  
		Last Modified: Thu, 11 Jun 2026 00:22:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447878f0c708aaeeb6ba94d0eda6c624cec83648b3d7691b2e31aaa76991fca`  
		Last Modified: Thu, 11 Jun 2026 00:22:54 GMT  
		Size: 15.5 MB (15527694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6a63ef6a5eecf778f6ee10e596c1ebd35d0634600f91c5f3bd0c8050dfe88`  
		Last Modified: Thu, 11 Jun 2026 00:22:55 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f576c2830d6a8d6cac239e9f1505489e99a6848fb1c78ba6ec70cd9caedbb3`  
		Last Modified: Thu, 11 Jun 2026 00:22:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b33e18e1d097905ba2045c5b7dbd9ce858d787b2935bf1cb34ff72912f237e`  
		Last Modified: Thu, 11 Jun 2026 00:22:55 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11a28546faa05835e68fe38958cb97685dafa1327bf6271c159ce05f2f4033`  
		Last Modified: Wed, 17 Jun 2026 22:22:38 GMT  
		Size: 8.5 MB (8468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508378649bc3da7aa264d3e7256d5175e16d2d9e1ae1a07470841ed8164d1e5b`  
		Last Modified: Wed, 17 Jun 2026 22:22:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa2db28f64edb7bd6619e23c769b63fc9247998b327501d68be325e1284922c`  
		Last Modified: Wed, 17 Jun 2026 22:22:38 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d330f72f7a2a6d027acd0d0b7361392f3fef81dde62f5d3c7a7e71ad765572e6`  
		Last Modified: Wed, 17 Jun 2026 22:22:38 GMT  
		Size: 823.3 KB (823344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e858443d7737b6b4542da85504b43fb7daec91da4d7878e089a0ccacddbc5cf`  
		Last Modified: Wed, 17 Jun 2026 22:22:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd0d8d749657b47af52ccb437c1df6f5f237dce319daa6cc084335c4a9a6251`  
		Last Modified: Wed, 17 Jun 2026 22:22:40 GMT  
		Size: 21.4 MB (21383786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:3dfe9c33e41c30770aec329de3a6a9a88ba26edb2d2688dbe8e50653fea9e965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f397a0d244d7af649ac18b004b2ec501553edf7945bb104912a4f655e932db`

```dockerfile
```

-	Layers:
	-	`sha256:113c782933fde319ce81ebde8ea181d9bdbde98f5f7e97318cfa8ce16e1d9c61`  
		Last Modified: Wed, 17 Jun 2026 22:22:38 GMT  
		Size: 7.4 MB (7432839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b1f4e5a6a814ff78c1409bf8b669e688f5f031c357e53476c5305245bec30e`  
		Last Modified: Wed, 17 Jun 2026 22:22:38 GMT  
		Size: 44.1 KB (44095 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:f894bea7d2637423e1ca279f5199516cc94d8e1608292ea0c72456df2d49cc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208861835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc8b68a50b018831ce52d45ee1fa3a78707b50f88826e3bae97ba3f5f3b66c1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:00:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 03:01:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 03:01:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:01:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 03:01:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 03:01:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 03:01:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 03:04:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 03:04:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 03:04:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 03:04:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 03:04:38 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 03:04:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 03:04:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:09:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 03:09:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:09:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 03:09:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 03:09:16 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 03:09:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 03:09:17 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 03:09:17 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 03:09:17 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 16:32:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 16:32:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:32:20 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:32:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:32:20 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 16:32:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 16:32:20 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:27:53 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:27:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76942a34176bffe275c52bbf371c6a83affed73bab30526f495165cbc094b557`  
		Last Modified: Thu, 11 Jun 2026 03:06:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d446e1e0a4b12d658b3e858628249ee37b9a22d29bee0c2dd4686159c2e43988`  
		Last Modified: Thu, 11 Jun 2026 03:06:22 GMT  
		Size: 109.6 MB (109598344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e8bcde33298859f8eb941222505617b97a665c07395dc23100212e1d7a25d8`  
		Last Modified: Thu, 11 Jun 2026 03:06:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f7d51c61734b9f5fbda00c651630c71a2ba54dd9247e49484c77277fe2ce0c`  
		Last Modified: Thu, 11 Jun 2026 03:09:41 GMT  
		Size: 4.9 MB (4883580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b6856b13dd8027fcf9d867bed35ded648e583baea3696392c17d0fa8bcaf36`  
		Last Modified: Thu, 11 Jun 2026 03:09:40 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8920a67f463e815da5e5dbdfa3a5ee6626ca03e2d3a8f2c577e66b82002ed9`  
		Last Modified: Thu, 11 Jun 2026 03:09:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd5d668f3f31250157c40ab92db19207763ebcabab808b16d85f889edb72d9`  
		Last Modified: Thu, 11 Jun 2026 03:09:41 GMT  
		Size: 14.6 MB (14563324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4506e486561dd7e4c19ba4effa91dadc5a343f48fb185f51452d8a5b9fa8c14`  
		Last Modified: Thu, 11 Jun 2026 03:09:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a983142bb10fea93c735037c1087f7dc9a6ea359c81ce98f4271b069fa91634`  
		Last Modified: Thu, 11 Jun 2026 03:09:42 GMT  
		Size: 15.2 MB (15163688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60a93c58da9b8fec909ae5e8c42f518bd3623dd76baf0d046246f4eb6f76c10`  
		Last Modified: Thu, 11 Jun 2026 03:09:42 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7656dda6951e5e1f86c0bd743bceddd3b2131784697058c6c85035b3c6422a62`  
		Last Modified: Thu, 11 Jun 2026 03:09:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89656368c89ac09110d7ee24d49fe189c3327264e7fe515004ab77752625298e`  
		Last Modified: Thu, 11 Jun 2026 03:09:43 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a0721660a8f039a1eb1cff8e8f5f49ae4a04ffbed6b6a5edf38c43cf38e2ff`  
		Last Modified: Wed, 17 Jun 2026 16:33:20 GMT  
		Size: 8.8 MB (8833231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fc575619c74c77db320d547d0e614e3e4314fe2aabdbe41962b31c204796f5`  
		Last Modified: Wed, 17 Jun 2026 16:33:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecffad3f55c3832f9342625d47dd2d53bac9b5ae30e77db4fd9ca8dcd145dd3`  
		Last Modified: Wed, 17 Jun 2026 16:33:20 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3909b4c887d02c1e74f9c50817789b054df040d57e7c4310cdcce8dc55a8facb`  
		Last Modified: Wed, 17 Jun 2026 16:33:20 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a23b262cb658bc9b3dbc148c0c73c92e5f50244c84d34cfa13285ad1e8224a`  
		Last Modified: Wed, 17 Jun 2026 16:33:21 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bda25e5db4efe3e3bbf8a065e3b41e9e3b8b69742761d5bf7b00844e609dce`  
		Last Modified: Wed, 17 Jun 2026 22:28:34 GMT  
		Size: 21.4 MB (21383797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:442ae937c56882357b5bcfe395444a8633d14a399118c24c3ffda5d0f272df20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7503899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0036e14215314aecbc1fd10f2b2bf5e4d5acd5927a4b64addab1eed5cd63d7`

```dockerfile
```

-	Layers:
	-	`sha256:f092fd5ba8e4179096d544fa862b3382d70fda20b9625b2705d3bf5a986ecf8e`  
		Last Modified: Wed, 17 Jun 2026 22:28:33 GMT  
		Size: 7.5 MB (7459611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a82aab3202b3d5e0c05d858d865058db28b3f11af049b445f06e42fa4e110b7`  
		Last Modified: Wed, 17 Jun 2026 22:28:33 GMT  
		Size: 44.3 KB (44288 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; riscv64

```console
$ docker pull drupal@sha256:b961bb1fb49ef24dc18f59f004a0ff8a0f730286b5991201a92d0338f5a0f028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236851661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ab999b3021e3422731130d96e500a27819b9e9c318bf978ac339e0a53de66`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 06:14:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 12 Jun 2026 06:17:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Jun 2026 06:17:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jun 2026 06:17:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jun 2026 06:17:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 12 Jun 2026 06:17:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 12 Jun 2026 06:17:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 12 Jun 2026 07:23:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 12 Jun 2026 07:23:44 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 12 Jun 2026 07:23:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 12 Jun 2026 07:23:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jun 2026 07:23:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jun 2026 07:23:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jun 2026 07:23:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 12 Jun 2026 07:23:44 GMT
ENV PHP_VERSION=8.5.7
# Fri, 12 Jun 2026 07:23:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Fri, 12 Jun 2026 07:23:44 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Mon, 15 Jun 2026 03:08:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 15 Jun 2026 03:08:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 04:04:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 15 Jun 2026 04:04:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 04:04:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 15 Jun 2026 04:04:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 15 Jun 2026 04:04:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 15 Jun 2026 04:04:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 04:04:45 GMT
WORKDIR /var/www/html
# Mon, 15 Jun 2026 04:04:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 15 Jun 2026 04:04:45 GMT
CMD ["apache2-foreground"]
# Sat, 20 Jun 2026 01:16:02 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jun 2026 01:16:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 20 Jun 2026 01:16:03 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 20 Jun 2026 01:16:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 20 Jun 2026 01:16:03 GMT
ENV DRUPAL_VERSION=11.3.12
# Sat, 20 Jun 2026 01:16:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 20 Jun 2026 01:16:03 GMT
WORKDIR /opt/drupal
# Sat, 20 Jun 2026 02:36:27 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 20 Jun 2026 02:36:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d877ba68e482a33a75fd5c2ad03cd220a291d8e1a9914f9501f41f97050fdf6`  
		Last Modified: Fri, 12 Jun 2026 07:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbcfd8d49be980430164d80eb573cd408281b5735067cbdbe0d0ff42f6a5f62`  
		Last Modified: Fri, 12 Jun 2026 07:22:03 GMT  
		Size: 146.6 MB (146585237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cccce4250e607f18d72142d293e6bb27d27ab552c53e10d06fef4ba0a75bca2`  
		Last Modified: Fri, 12 Jun 2026 07:21:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981f275425f8f07adaa4ba9e0158bd9fcfffb4a7bb018e881532deba25018fa`  
		Last Modified: Fri, 12 Jun 2026 11:01:38 GMT  
		Size: 4.0 MB (4031718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dce446512cd614425e3443122bcc3947f736b37c4111dbea78bea63f0b63ac6`  
		Last Modified: Fri, 12 Jun 2026 11:01:36 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad447ad570ca47d55772051c544a84727baa9604a853d461942c3a96c44adf`  
		Last Modified: Fri, 12 Jun 2026 11:01:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd59f0eee5084203e7bfc34f6ac3147954fa97e31f955f9622e8b7cb65f0e92f`  
		Last Modified: Mon, 15 Jun 2026 04:08:00 GMT  
		Size: 14.6 MB (14578889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ac3c8d0a43563f21766293ba4f28de134a9e03d03862097233260f34e1c0d`  
		Last Modified: Mon, 15 Jun 2026 04:07:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99437d30d2d16a30b8aaa3800872250e420a4ca1ca7cc819d5fd13d0d1f99fc4`  
		Last Modified: Mon, 15 Jun 2026 04:07:59 GMT  
		Size: 14.1 MB (14084784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b27c6bc6269a82f153a24a83884195620a972a0e8bbd20c429741e2b35cd364`  
		Last Modified: Mon, 15 Jun 2026 04:07:55 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63add33a74f14742dd9983ed76efaff99e55efb438bb54b9b0edf6ec5c0b37fe`  
		Last Modified: Mon, 15 Jun 2026 04:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1b78e26718e985c15ef053ee772e313d24b0aa36f917ec7610594583db6d7d`  
		Last Modified: Mon, 15 Jun 2026 04:07:57 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb360cdb6c97858625ed0e4ab4159bcdd706bd47fbc979b1151d36d341d9f08b`  
		Last Modified: Sat, 20 Jun 2026 01:21:51 GMT  
		Size: 7.1 MB (7075047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917499b0eb0d5ef87b95adf0e6f65ed875ae59ceb82c82233540693b67e49c4a`  
		Last Modified: Sat, 20 Jun 2026 01:21:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5603f5493e0a9914582ab76f0de7b1a56ca71c806e7cdab6688f737692f6f3`  
		Last Modified: Sat, 20 Jun 2026 01:21:50 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93583af3dc23297fe215880bab300392bf8d2c65f623b201a93e55443bdccccc`  
		Last Modified: Sat, 20 Jun 2026 01:21:50 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e736e3aeb83c5e725bb5da709f5e5aa42a48c5c15a11b5628567ece1c6d10594`  
		Last Modified: Sat, 20 Jun 2026 01:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d7e7c242cbfabf49fadb94072e351cba42c5e49be194d6e6a531fad2b6f4b2`  
		Last Modified: Sat, 20 Jun 2026 02:41:22 GMT  
		Size: 21.4 MB (21384124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:75c0927c6e23f322971e1097d3860b09588c5dda098631fdb63ea3b418a243fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7575508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fbd27abaad1d1fbb6176ffb041d4a5c68b3e37215142dbcb1546369315c537`

```dockerfile
```

-	Layers:
	-	`sha256:fa4b112c61b7ec712283f8a26f7a829d10fb4e9062b054facaacc13bb611ec18`  
		Last Modified: Sat, 20 Jun 2026 02:41:20 GMT  
		Size: 7.5 MB (7531220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c96184e5cb5f234e83bce0d25e40d2b7b17c94652e736bcfa64320c29eb879`  
		Last Modified: Sat, 20 Jun 2026 02:41:18 GMT  
		Size: 44.3 KB (44288 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; s390x

```console
$ docker pull drupal@sha256:9ccd075c37358cc020984579dfbe930f9683e23e608191d423b47497de16112b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185351050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e6b65506815b8c5eabcedd895f6cc60dff7697a5d1bd537ed763bc8e416b4c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 00:23:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 00:23:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jun 2026 00:23:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jun 2026 00:23:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 11 Jun 2026 00:23:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 11 Jun 2026 00:23:56 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 00:23:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_VERSION=8.5.7
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.7.tar.xz.asc
# Thu, 11 Jun 2026 00:23:56 GMT
ENV PHP_SHA256=01ba2ed1c2658dacf91bebc8be6a4885f69b811c7993831fc48e26107ab29985
# Thu, 11 Jun 2026 00:24:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Jun 2026 00:24:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 00:27:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 00:27:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 00:27:57 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jun 2026 00:27:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:27:57 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 00:27:57 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:27:57 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jun 2026 16:39:04 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jun 2026 16:39:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:39:12 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 17 Jun 2026 16:39:15 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 16:39:18 GMT
ENV DRUPAL_VERSION=11.3.12
# Wed, 17 Jun 2026 16:39:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 17 Jun 2026 16:39:18 GMT
WORKDIR /opt/drupal
# Wed, 17 Jun 2026 22:23:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jun 2026 22:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f12811ca8054d10a6d855c99328a1f0623889381d202bba7392d112bc3de481`  
		Last Modified: Thu, 11 Jun 2026 00:28:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c3c60b41e88a2039142613d746976cbbd5c2d61145b36679028c24bf550936`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 92.6 MB (92573159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39530e62e350f67cad534ea575f3024d4018b676be4212ebd0ff185c2f12e154`  
		Last Modified: Thu, 11 Jun 2026 00:27:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af8a8d7637b102b0927b2fe4838bd66d078d8497c6b8daf69a1af6de3c05716`  
		Last Modified: Thu, 11 Jun 2026 00:28:28 GMT  
		Size: 4.3 MB (4331367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81831958195a79868b988dbf00474aa90e83a65b5efa30da45faafb7f722895e`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9f6ef9d8cf0e08bf1a5c2cde718210376f9ed42f8dfe2ea97190ae4a2709b`  
		Last Modified: Thu, 11 Jun 2026 00:28:29 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c2336ee91fb278b497773f594e71eb087bedbbc5620cb4ea6f028d26515304`  
		Last Modified: Thu, 11 Jun 2026 00:28:30 GMT  
		Size: 14.6 MB (14562719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f493b1b69479792c046e893862b319d37a32a2edd14765616a2c18b117885c`  
		Last Modified: Thu, 11 Jun 2026 00:28:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a990e8f9b3181f97f85c90f8aaaa4a9593d874f605ca17b015e596cc0b29e`  
		Last Modified: Thu, 11 Jun 2026 00:28:31 GMT  
		Size: 14.4 MB (14442465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8d0221baaf1b10fc458c270e01a80224a361599d98d5a8ad52e24264ca363f`  
		Last Modified: Thu, 11 Jun 2026 00:28:31 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac90ea599cfe6842782adc72fab97a846bf8cce763691e845cfb3ed11fda41c`  
		Last Modified: Thu, 11 Jun 2026 00:28:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ccf0436ed46397b823ddae7f4009c835f6b14860f060fec58685f795c62b4e`  
		Last Modified: Thu, 11 Jun 2026 00:28:31 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd8be980032378a2345008435c301f5b627a27987338ddb915fa505404dff2f`  
		Last Modified: Wed, 17 Jun 2026 16:44:56 GMT  
		Size: 7.4 MB (7376465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1965cbf7fc97148a83a588a827a9a5058efbf2722cec250291a038c4e7abf8`  
		Last Modified: Wed, 17 Jun 2026 16:44:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc7888077558d0bf2cb2160fd503c9201959274b6c392a7a621342fb419c4e9`  
		Last Modified: Wed, 17 Jun 2026 16:44:54 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2cf7fca5e133dff3101c91697366655440255ecacd98396b4cdb52146c3512`  
		Last Modified: Wed, 17 Jun 2026 16:44:56 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72215f1a5ae872da5472f72b83a7bbadf447ac9f1abde2d9c7439b8b8767e52`  
		Last Modified: Wed, 17 Jun 2026 16:44:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a136369b0b48739372e2269d0bd2babcce7a0e7ea5b3c4ef82331e77c8dbd0`  
		Last Modified: Wed, 17 Jun 2026 22:23:33 GMT  
		Size: 21.4 MB (21384004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:a4d65fff7e2e3df6e562d2a3c7a3cd7ae9e965b17f34d984d5ece20354848235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7233418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c0dda00ca97f4e42c71240b36144db6f65519fab96071bc0c9315e0c4dec08`

```dockerfile
```

-	Layers:
	-	`sha256:dd603f70d9f4b5b141f548d0878161fac6c8cfa2dc53df12e7ec64972787e648`  
		Last Modified: Wed, 17 Jun 2026 22:23:32 GMT  
		Size: 7.2 MB (7191444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a4e0f1e14d6f83e8fb9371d5941e6236a1a313a8715c06a537b71588326f866`  
		Last Modified: Wed, 17 Jun 2026 22:23:32 GMT  
		Size: 42.0 KB (41974 bytes)  
		MIME: application/vnd.in-toto+json
