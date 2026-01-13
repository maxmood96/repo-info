## `drupal:php8.5-apache`

```console
$ docker pull drupal@sha256:04de555c078eaad1416070e1ec001eba92d099c3fd9128e6977383dba810ff3f
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
$ docker pull drupal@sha256:3fc34f590ab7d9aebe5f9ba44bdd0cc23aba090a26f5ab1d74a77fcbf7a26514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205050046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a039a389f718bf0f1afcee6202c80970fe0e2617b2d9b34138442e57987ead08`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:47 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:26:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:26:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:26:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:26:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jan 2026 01:26:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jan 2026 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 13 Jan 2026 01:26:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 13 Jan 2026 01:26:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 13 Jan 2026 01:26:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:26:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:26:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:26:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:26:09 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:26:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:26:09 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:26:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:26:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:28:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:28:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:28:53 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jan 2026 01:28:53 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:53 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:28:53 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:28:53 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jan 2026 03:54:36 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:54:36 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:54:36 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:54:37 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:54:37 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 03:54:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 03:54:37 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 03:54:45 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 03:54:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0894c8cb09b1b41dd430e1ef8997630afd24341d3b8d157d04695ea580c7bd37`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd5902c21615c08a7c847a69b9a78a27bfc7ceacda616b6c3781c223455ce8`  
		Last Modified: Tue, 13 Jan 2026 03:47:25 GMT  
		Size: 117.8 MB (117839733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b14ed89b5a3cdeef25fde01ab50dd6bd073470d9d89d32272a19f6ce9ecbca`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9fed03f3d534f22ddbd148b58f0abddc6dbcb9834bd3863e2bb1ce2e38de4e`  
		Last Modified: Tue, 13 Jan 2026 01:29:25 GMT  
		Size: 4.2 MB (4226866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697d003cc1e79973206f4631a9e8461e46d18e8b77235fc097446265c576ff91`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3668ab0034faee8030f4de776fcce75df99dc6cc082b06e5c7db604b948437`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38c1ca52946e12b9862b4b77dd1a4d270a5ddae47a474ab25f744fa4df24c59`  
		Last Modified: Tue, 13 Jan 2026 01:29:26 GMT  
		Size: 14.5 MB (14492662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb2b314f0b40970b26a6fef9ff9f7f0fa31be8afd5d47177d945fb30f38b831`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7099bfd4483657db8b6ec1501741cff3fabbc473a7e6301220ecdfc3cd0fb48`  
		Last Modified: Tue, 13 Jan 2026 01:29:27 GMT  
		Size: 15.0 MB (14976667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45a78daf1a45eaf9970576105ae3955b22f9d64eba5ceac3ed1907e2884c68`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2211cfdc76dd8bed48c492ff2ee55610d1e6265f2656be85eff67b5450a0dd54`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b552246fb218fa79e8be2e19e098407312769b03ef4804dcb75988a6fbea92b`  
		Last Modified: Tue, 13 Jan 2026 01:29:24 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d7d247b02d3e0073bec13dcde99a6ca53cfb4daa360f64bae0807c61447f48`  
		Last Modified: Tue, 13 Jan 2026 03:55:12 GMT  
		Size: 1.7 MB (1657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0f899ff9121e86048ee6f448675eb85187fb58c19365d842c47e30ef52dc88`  
		Last Modified: Tue, 13 Jan 2026 03:55:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fc8d056843d7254842642897486b84062c3d636904554282d0f85025fa4c66`  
		Last Modified: Tue, 13 Jan 2026 03:55:12 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f358fb7e2be36e34ed0ec545b4557a44621d6586932a6559ba3f27dd8ecb6dfa`  
		Last Modified: Tue, 13 Jan 2026 03:55:12 GMT  
		Size: 776.4 KB (776360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96afa23ab1a12af82ceb97a2d46802b19adeac0684b8f3584b81cbc2b33dba32`  
		Last Modified: Tue, 13 Jan 2026 03:55:12 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad40714d044b79b1969b4399e18ca5a1984728b9b0c8d2d8f89bdaf80b3cecd`  
		Last Modified: Tue, 13 Jan 2026 03:55:14 GMT  
		Size: 21.3 MB (21299926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:baafd46a54406e4fb4d53d98b38512b9728358285a45d8bdda41910fe132f836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcfd47c81f039c8d5bf253e943f80b24052ef660b7148035a1161434dd2e606`

```dockerfile
```

-	Layers:
	-	`sha256:bba417d6407e16ab21877f704f4663daa3082db1adeb802307a5915ea3d87ad5`  
		Last Modified: Tue, 13 Jan 2026 06:09:00 GMT  
		Size: 7.3 MB (7337276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d953ef410723fbc48aa30204dc9aae3002898d48d78502bc660c8c1697e230`  
		Last Modified: Tue, 13 Jan 2026 06:09:01 GMT  
		Size: 44.0 KB (44017 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:4527e4f6c168d3ed4834ab2d25e5dfbb01769d03194d8bb334492377f8eec3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166647586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276f0e37c0bfd2a9f7e94d30044a4e04c787ee3913a53ea77d1c016aa607e7e4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:37:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:37:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:37:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:37:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:37:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:37:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jan 2026 01:37:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jan 2026 01:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 13 Jan 2026 01:37:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 13 Jan 2026 01:37:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 13 Jan 2026 01:37:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:37:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:37:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:37:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:37:58 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:37:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:37:58 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:38:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:38:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:41:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:41:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:41:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:41:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:41:14 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jan 2026 01:41:14 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:41:14 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:41:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:41:14 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jan 2026 04:25:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:25:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 04:25:54 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 13 Jan 2026 04:25:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 04:25:54 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 04:25:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 04:25:54 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 04:26:01 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 04:26:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c0773eb89d9086b7c7751a19095a873033cf4c013b11bcc41ead4d228c8777`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3478622e266c826dd019a0ecd6faccfa094de8955eef9474b82701ed4aac0a1`  
		Last Modified: Tue, 13 Jan 2026 01:41:53 GMT  
		Size: 86.2 MB (86244741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085a5e4431cb5a8a2eac33930285cd2696e6eaa6463b1a900ffbf395e0ee8665`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a152659ba0dad6454710822f4bdb708e28e8ab8081faa7309fa67c2a3c38d7`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 3.8 MB (3757578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73425dfb8006208ba6109ae621a5dd5444c0bc7a2c95e788433fcfb312380f2`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66268bab7fd6b0f2b1d70dd35ecfcd4c882fda845e4d55834369561b2d8bfe2f`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd32f600c82dc3111d5aa20c35e2bf5af914b1bdd3fcea3aa415f0f35702928c`  
		Last Modified: Tue, 13 Jan 2026 01:41:43 GMT  
		Size: 14.5 MB (14490469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dbaad02524950a59cfcaf9a752e99b72394517210308049bb31b3e2b440674`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70feb649e5a2c3bb224ee9e293b0680e839ba7ebf5d5702eab009a0334a650e4`  
		Last Modified: Tue, 13 Jan 2026 01:41:43 GMT  
		Size: 12.5 MB (12493102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e30193055ce8f87b56e942599fb3f292eae7caeb1f59b491763731d17ba3bc`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe9cbd797df7f7c8bcbc590115dbaeda80485d74751475d7e1f6097d61de2f0`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2c3e2d0a8b9b6d26da8121d0e6207a95d762e19b7d9c79f35b7483a0d1f965`  
		Last Modified: Tue, 13 Jan 2026 01:41:42 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d37bb802c3223de973ceb7c9dee2c66dcc4fa3f8613a990bd96d7e0b12861c0`  
		Last Modified: Tue, 13 Jan 2026 04:26:26 GMT  
		Size: 1.4 MB (1371006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deee4aeed5e328728e85da0f19e7f2dd39d986ebf1d9aed91b8c53593a4224dc`  
		Last Modified: Tue, 13 Jan 2026 04:26:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0167fe8c733a385aa9c839cf65be0fbf601034ef5f137fd61b3115c767f18b7a`  
		Last Modified: Tue, 13 Jan 2026 04:26:26 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fdacd4ab49b0c65d8782f8bc2ebebe9c21662634ebe8d2dc408d03e36c8ddd`  
		Last Modified: Tue, 13 Jan 2026 04:26:26 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce676ba4b475a00308ec5578c84c7c11e950f189d6e718b5c0b8a23b3bf7432`  
		Last Modified: Tue, 13 Jan 2026 04:26:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d079c56629f770df31a95f057450037bc87b0021cc7a808b62095a4857dc7b`  
		Last Modified: Tue, 13 Jan 2026 04:26:27 GMT  
		Size: 21.3 MB (21299587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:050de6493545f1dc17cb96292caae3ea8886dea2047a9bc9a6091723265354f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0884871188dbb08431b628dd99ecab316d19ff52f3f632624863f76c9c36f114`

```dockerfile
```

-	Layers:
	-	`sha256:dc8ead474f3676676f65e674fd78dd5989e78b828c3dc1a8c362928d3d0075b5`  
		Last Modified: Tue, 13 Jan 2026 06:09:07 GMT  
		Size: 7.1 MB (7141189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63395ad0d6827b367637362148d00a443720ad944a2477c2aaefb7ba54c0aeb3`  
		Last Modified: Tue, 13 Jan 2026 06:09:08 GMT  
		Size: 44.2 KB (44214 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:e387e1f29e6866dcaed37ea56ab02b7ca805911e2e1423f3039fb7c08d1e8aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197343769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be747221052b26adafa13b0fa2fe1b0656746d58a428a966a32c33a454005df2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:26:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:26:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:26:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:26:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:26:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jan 2026 01:26:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jan 2026 01:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 13 Jan 2026 01:26:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 13 Jan 2026 01:26:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 13 Jan 2026 01:26:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:26:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:26:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:26:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:26:23 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:26:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:26:23 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:27:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:27:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:30:26 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jan 2026 01:30:26 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:30:26 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:30:26 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:30:26 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jan 2026 03:58:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:58:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:58:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:58:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:58:19 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 03:58:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 03:58:19 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 03:58:26 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 03:58:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aae841def89ebae39788d4c9a0d4f4e82da0176fa42fc4c512832c7bf6b878`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c729aea8a44a97fff496bce2b4991c8261ac2da43237b82a5b0a9c95e289f14`  
		Last Modified: Tue, 13 Jan 2026 01:31:09 GMT  
		Size: 110.2 MB (110164236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d7c7d26b9adaef6201c83642b06da448b8eba2c6c0d07900f9f478b048f451`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b84e1625b9dd611a757aca5128d6e1a3d943dca03b3ae49ba98c671cf37c9`  
		Last Modified: Tue, 13 Jan 2026 01:30:58 GMT  
		Size: 4.3 MB (4304894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0081c7983742d3ffaef4e713d6001894f632bbf72aed06cf790d38163f1e6b`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501a66294018b5ac2c9cc986d325878cb628716ca43baeeb9fb258cfa9d439f`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb101b7af45810eae8485c3ff248a29215af59de6195cee8d4de7191bd70a0bf`  
		Last Modified: Tue, 13 Jan 2026 01:30:58 GMT  
		Size: 14.5 MB (14492351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690b3d54fc48af6988a43d6aa88d8bb296d5978bd0bb2466fc41e50f4f1f62c0`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f61c964412f02d4fd2dbc2bd5c33cdced65d834a5d2a180ff850579ff6d215c`  
		Last Modified: Tue, 13 Jan 2026 01:31:00 GMT  
		Size: 14.6 MB (14550359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354e074508978f03622be3fb15f3948fe88fc51586e710121a85260313fc41ef`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744f26854a7a314e711cad67de4d88f23e0fcf189f2c3541ef4154b9549c0a73`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a521e72b9d2c6349dd2ee1d6ef693f394f90217309c11fdb64f9e0c7b1130d2`  
		Last Modified: Tue, 13 Jan 2026 01:30:57 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9656e4d821f50123c63717b9f61e3ec07f59a75e7e260219da90df6096bcb52`  
		Last Modified: Tue, 13 Jan 2026 03:58:52 GMT  
		Size: 1.6 MB (1615239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f65bdff7befe3c07e9fac3f76739e2615f0dd3a43207fe34986e40e933cedb`  
		Last Modified: Tue, 13 Jan 2026 03:58:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b337f71cb58c877c021e08d694c1130fc7d4ad65c0c46eb64198a8f483ca0710`  
		Last Modified: Tue, 13 Jan 2026 03:58:52 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1517f6a67c1b0f9b173dc53b7a1c8ffcf2bc0c8ce97ba6eaf679baaa774db54`  
		Last Modified: Tue, 13 Jan 2026 03:58:52 GMT  
		Size: 776.4 KB (776357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6798dc7a4603cfcfaf6bffe436a993152348043821d70a2a546c0dea1aaf8c`  
		Last Modified: Tue, 13 Jan 2026 03:58:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ae77f8a3debfa598fd7faf548cce46f18ed800392e62dd2bb2ad31c67e3bc`  
		Last Modified: Tue, 13 Jan 2026 03:58:53 GMT  
		Size: 21.3 MB (21300117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:870088bfdbcd02229d3032385f181345e6ff1ccc76a1c4d8accbc2c0d81d0382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c29a21ec43986a67ff7be8225a46c6b8b011c7a8c1027fbbf9df5bdcc140cb`

```dockerfile
```

-	Layers:
	-	`sha256:3eb721a83aff30bc2f630789e7787655d6f40688b4c6f3484d8040dcd76483e2`  
		Last Modified: Tue, 13 Jan 2026 06:09:14 GMT  
		Size: 7.4 MB (7434674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dd82ac1e6511d4f784a2fa82a90b279ba8879be1b78711ff2b9b9dd2de322d4`  
		Last Modified: Tue, 13 Jan 2026 06:09:15 GMT  
		Size: 44.3 KB (44287 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; 386

```console
$ docker pull drupal@sha256:d5f1fdb5685493a1e710c22e16de4e9b4aa5d5fe5c098c0bae511af1921f93b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205521751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42e130d96a4fc8d724b4e84ee604a4e8322cb6eecc8b9d6c948df49a610fdc7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:20:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 13 Jan 2026 01:20:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jan 2026 01:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 01:20:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jan 2026 01:20:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 13 Jan 2026 01:20:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Jan 2026 01:20:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Jan 2026 01:24:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 13 Jan 2026 01:24:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 13 Jan 2026 01:24:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 13 Jan 2026 01:24:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:24:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jan 2026 01:24:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jan 2026 01:24:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 13 Jan 2026 01:24:53 GMT
ENV PHP_VERSION=8.5.1
# Tue, 13 Jan 2026 01:24:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 13 Jan 2026 01:24:53 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 13 Jan 2026 01:25:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 13 Jan 2026 01:25:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 13 Jan 2026 01:28:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 13 Jan 2026 01:28:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jan 2026 01:28:18 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Jan 2026 01:28:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:28:18 GMT
WORKDIR /var/www/html
# Tue, 13 Jan 2026 01:28:18 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:28:18 GMT
CMD ["apache2-foreground"]
# Tue, 13 Jan 2026 03:04:49 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:49 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:04:49 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 13 Jan 2026 03:04:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 03:04:49 GMT
ENV DRUPAL_VERSION=11.3.2
# Tue, 13 Jan 2026 03:04:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 13 Jan 2026 03:04:49 GMT
WORKDIR /opt/drupal
# Tue, 13 Jan 2026 03:04:58 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 13 Jan 2026 03:04:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8369f640b231b1401b7d449762834ddeefa9a57fd4d60367314c84321df736`  
		Last Modified: Tue, 13 Jan 2026 01:24:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3747baa55e2f282ae63bcc61be5c7fd7e0b426b9e47385cde52471043cfdfadd`  
		Last Modified: Tue, 13 Jan 2026 01:24:40 GMT  
		Size: 116.1 MB (116138801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf69d5a30c876a7d474df68eaaa5989099ba4d9a82ea902471c76912653e0b7`  
		Last Modified: Tue, 13 Jan 2026 01:24:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a7d819cbb07412585a763bcea7dc99ec8d5e259df8951e08127242e75a0161`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 4.5 MB (4458210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e873548d17ea263403d7598fe4feabcc684863b9fb73d098fff8905d2aac5b4`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f1a9368aadd3d6e174791b27c82a2e29bb7e2417e753e97e2d03bbb2987c51`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10bb7a1c195b78b4c0cecc8a9e684815b97b078a4ddf9742895c2681bcb7c9f`  
		Last Modified: Tue, 13 Jan 2026 01:28:37 GMT  
		Size: 14.5 MB (14491752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733bf9d8af9ec364597d92fc479ccf057b21b41fc4c196dc5f2f85f2b8bb7492`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325c97df283eaf928021e3ae5362085d8db76c445af4b7fba682dd44ed53277f`  
		Last Modified: Tue, 13 Jan 2026 01:28:38 GMT  
		Size: 15.3 MB (15323821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59735c33eda626c4a1fd20fa8a08f52b39b3a655577a8ef715f253414441097`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af10e2b688ba850f5f0bd0a1d358aaad312a30925fff479e65878660b51efbed`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922eb0820b58d4998cbef4c226bf3b63c5512b6945e13ab544bc32cd66603b3a`  
		Last Modified: Tue, 13 Jan 2026 01:28:36 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f56853391e4851e0bd569ad9c1e20fa0ac4a5f8b7763ff185e1791ba908284`  
		Last Modified: Tue, 13 Jan 2026 03:05:23 GMT  
		Size: 1.7 MB (1737978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa73548416f08f23fc8688de9942dc035509ca8fc9236f0e7ffc61e794bd18e`  
		Last Modified: Tue, 13 Jan 2026 03:05:24 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f839a659dc949f3d810ed48e54d541c04466728814d87a144505f664bd646`  
		Last Modified: Tue, 13 Jan 2026 03:05:23 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76837463993cbf689df292e6f5084267e172d05126ce67d4b1923039035348cb`  
		Last Modified: Tue, 13 Jan 2026 03:05:23 GMT  
		Size: 776.4 KB (776366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489f221e9996bf691e715a60d85189085a9ecf1d0484ec5df0061023a07a41ad`  
		Last Modified: Tue, 13 Jan 2026 03:05:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c6d42ee5dbbb4187d9f378b1702cb58948537b6e97c843a7f5c7538451c82f`  
		Last Modified: Tue, 13 Jan 2026 03:05:24 GMT  
		Size: 21.3 MB (21300185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:c3c6e3798bde068f73354cfd6067c8d0f4dbf8d32641291763a84606f0936ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7355020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761693e792e9ef8196528aad5923dad4116002c5eedb281dd61e0869473ac317`

```dockerfile
```

-	Layers:
	-	`sha256:f64940bb3c0c58d240a38e087695c0ba26aa0e61bc306ced0e02b15c9b255abf`  
		Last Modified: Tue, 13 Jan 2026 06:09:23 GMT  
		Size: 7.3 MB (7311088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1586d1e593aae589780b80aa2f1f6d0729be2aae55cf4b49ecd7a57ccbf0802a`  
		Last Modified: Tue, 13 Jan 2026 06:09:24 GMT  
		Size: 43.9 KB (43932 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:2646eefaef6f64d232bfa4f97be7d01a817074621ce3836fe95e3daaa29baf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201488069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc75036bc61d5dde4697815fe564db0d858b679ba5f48c0da6af3123ac5424a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 16:33:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 16:34:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 16:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 16:34:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 16:34:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 16:34:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 30 Dec 2025 16:34:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 30 Dec 2025 16:36:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 30 Dec 2025 16:36:56 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 30 Dec 2025 16:36:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 30 Dec 2025 16:36:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 16:36:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 16:36:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 16:36:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 30 Dec 2025 16:36:57 GMT
ENV PHP_VERSION=8.5.1
# Tue, 30 Dec 2025 16:36:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 30 Dec 2025 16:36:57 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 30 Dec 2025 16:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 16:37:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:08:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:08:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:08:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:08:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:08:31 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:08:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:08:32 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:08:32 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:08:32 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 04:27:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 04:27:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 10 Jan 2026 04:27:59 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 10 Jan 2026 04:28:00 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 04:28:01 GMT
ENV DRUPAL_VERSION=11.3.2
# Sat, 10 Jan 2026 04:28:01 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 04:28:01 GMT
WORKDIR /opt/drupal
# Sat, 10 Jan 2026 04:28:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 04:28:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f57655a18e58caec8202718b81878a0a323ee7dc860ee03487665b00f17d4`  
		Last Modified: Tue, 30 Dec 2025 16:39:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8947d9b26fd5842181dbfa0476ae87283eb4ee0896468eef4401a617eae0fb`  
		Last Modified: Tue, 30 Dec 2025 16:39:26 GMT  
		Size: 109.6 MB (109598066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0082faf6428f6d353e1b13563b033f41260118184f280753196d05c13071880e`  
		Last Modified: Tue, 30 Dec 2025 16:39:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b63c4a61d4b49ce5d925e39c85d4f52dc3cd4cc958d4ee1ffd76afdd821956`  
		Last Modified: Tue, 30 Dec 2025 16:42:06 GMT  
		Size: 4.9 MB (4876281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dd5b36fd570706834188e16c9158c88b808bcd775a9f1d2c47ac8c28e8f787`  
		Last Modified: Tue, 30 Dec 2025 16:42:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca68b845272e472735e5c188416362bcc307f5ce82cf119788bcfef161baae2`  
		Last Modified: Tue, 30 Dec 2025 16:42:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1876ea3dc8c82b928ec64a104b44a7e7ee76de7465391c2e41907bbf0f4d8e99`  
		Last Modified: Tue, 30 Dec 2025 16:42:06 GMT  
		Size: 14.5 MB (14491871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fb70aaccba58e91050d13a523ebd2dc7bc14fa978198d0a7c9d8993d4ac75b`  
		Last Modified: Tue, 30 Dec 2025 16:42:05 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dedac25d4be28fa26acbc56ea2f526de99e134d2fb45f63f43d81bf29fa23c2`  
		Last Modified: Fri, 09 Jan 2026 23:09:03 GMT  
		Size: 15.0 MB (14996563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e4fdc8fda1cb4ced61edec9bcb7b8b9b82675e18842c8c9b367ed649726c5`  
		Last Modified: Fri, 09 Jan 2026 23:09:02 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5652a40c5e708ef47b6d581168b0d1000c51f1d9c80a6dd5676e7313388bd2f`  
		Last Modified: Fri, 09 Jan 2026 23:09:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba63e2317e77ac6d3aeded10053908dae5045114f4397333f43ae004f25b71`  
		Last Modified: Fri, 09 Jan 2026 23:09:03 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86947a0757625267ba42f1653d858b582bf8299d978287aeb57af8852ee0aeae`  
		Last Modified: Sat, 10 Jan 2026 04:29:11 GMT  
		Size: 1.8 MB (1845919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90558a769518c98df3b415bcf0b97710083b68287a1e5577623de855274d871f`  
		Last Modified: Sat, 10 Jan 2026 04:29:18 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b680ec67130acca54e2562e8b27a573dea9a856bb23d07e1198805994bdc4`  
		Last Modified: Sat, 10 Jan 2026 04:29:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e7851a3331514928e925269c7c3b833fe401fed82ed7e9bc9f34ad21c4219`  
		Last Modified: Sat, 10 Jan 2026 04:29:11 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b35530f57556a78f67ffe84fa59cecc8f23db4394a56fa84ce06b0e303771`  
		Last Modified: Sat, 10 Jan 2026 04:29:11 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e56c7ff48852ea2a5a6f993e5421bd8498ea0a27c8e5386bf95a8479983ba0`  
		Last Modified: Sat, 10 Jan 2026 04:29:12 GMT  
		Size: 21.3 MB (21299941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:65436139ee9e53d27f49a8bcf105a86d92100ee82950f3e33fa4dc4b17c11ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd234a59ce673ab77a7222ecbb39373ae9ca54ca23cd90f517f703dbf5eb2d1`

```dockerfile
```

-	Layers:
	-	`sha256:861d5599fc7a757380a35bee1bd6df1b2c2471d20e143d7fb7047b29edcd1dc9`  
		Last Modified: Sat, 10 Jan 2026 05:57:54 GMT  
		Size: 7.3 MB (7336951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de15a625568836d927525c3657a520c2f413c3bdb649201f975f1625de14adf3`  
		Last Modified: Sat, 10 Jan 2026 05:57:55 GMT  
		Size: 44.1 KB (44125 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; riscv64

```console
$ docker pull drupal@sha256:1ae0a2e99e662080e6af97c75385d4f91e55ab751870e28076e48def0d4bc04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230953579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11c84551b41c6aabf804f095f3680e084791cf2ccfb7d4fdf57bc2fe5b1c367`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 08:15:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 08:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 08:17:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 08:17:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 30 Dec 2025 08:17:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 30 Dec 2025 09:23:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 30 Dec 2025 09:23:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 30 Dec 2025 09:23:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 30 Dec 2025 09:23:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 09:23:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 09:23:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 09:23:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 30 Dec 2025 09:23:41 GMT
ENV PHP_VERSION=8.5.1
# Tue, 30 Dec 2025 09:23:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 30 Dec 2025 09:23:41 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 30 Dec 2025 09:24:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 09:24:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 10:21:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 30 Dec 2025 10:21:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 10:21:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 30 Dec 2025 10:21:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Dec 2025 10:21:40 GMT
STOPSIGNAL SIGWINCH
# Tue, 30 Dec 2025 10:21:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 10:21:40 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 10:21:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 30 Dec 2025 10:21:40 GMT
CMD ["apache2-foreground"]
# Fri, 09 Jan 2026 01:15:34 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 01:15:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 09 Jan 2026 01:15:35 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 09 Jan 2026 01:15:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 01:15:36 GMT
ENV DRUPAL_VERSION=11.3.2
# Fri, 09 Jan 2026 01:15:36 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 09 Jan 2026 01:15:36 GMT
WORKDIR /opt/drupal
# Fri, 09 Jan 2026 01:16:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 09 Jan 2026 01:16:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44b1edad4acbdf2eb79bc4ed79ff402d6af38c94857a826c4e8f406f68b8b4`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a8c50b15f754f42cc587a4d423f958f4de65b8cc8da75adfbac833ca87e54`  
		Last Modified: Tue, 30 Dec 2025 11:32:37 GMT  
		Size: 146.6 MB (146578538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4346525b0d45631b779c99bb99caa2632c2822ec686a160c5f4d23f9cfac4217`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bca231363c25a411c4c33686ab17aa12a7dd8276276a14a5eb068e3328f54ed`  
		Last Modified: Tue, 30 Dec 2025 10:25:13 GMT  
		Size: 4.0 MB (4033815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d81e12f16042f0d6da524da8e9a8b9b54d6bcdee985c63873f3ee0cb3f7d8`  
		Last Modified: Tue, 30 Dec 2025 10:25:11 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aaabcb5d55099899a4e7c7e005825b56e9f3eb25eeff883d76c801dc96de9c`  
		Last Modified: Tue, 30 Dec 2025 10:25:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476af5e32c2985737409b02ad2f582f08b736e4a6e203f5c9339de4c2cf75c80`  
		Last Modified: Tue, 30 Dec 2025 10:25:12 GMT  
		Size: 14.5 MB (14491737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61c8606d4b76be54f932f3d3ab70e1cf895f0948fd8402330be5b28aa71cd3d`  
		Last Modified: Tue, 30 Dec 2025 10:25:11 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09076ddb16c4b9d03e8565cda74f0499b65a65c267cd04313fb1477178ff82cf`  
		Last Modified: Tue, 30 Dec 2025 10:25:12 GMT  
		Size: 13.9 MB (13919433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9fe48661723ac71a5b2fe5c83dd009d2845532d400cefc6bdc77dedf36d511`  
		Last Modified: Tue, 30 Dec 2025 10:25:11 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be06ec93168cdb79a31f8ef41e468c4cb2bacc30427084d57731a58b4867c4d4`  
		Last Modified: Tue, 30 Dec 2025 10:25:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16093438a6e9767561b6b0bde067174f2441893aba0ab6d0cea625adc8fb689c`  
		Last Modified: Tue, 30 Dec 2025 10:25:11 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1183be2f77fce65e037fe52273b42c6862bf35060dba13e777478df502f174a3`  
		Last Modified: Fri, 09 Jan 2026 01:21:16 GMT  
		Size: 1.6 MB (1574181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f307ee86b779826c4f3a77ca5acf5d4a25c933f15ea039c55ac62b4c18285a2`  
		Last Modified: Fri, 09 Jan 2026 01:21:15 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60877f4487f25c995e77cd948377456a6b7cbc24f0230a07b24ccbbf1176774b`  
		Last Modified: Fri, 09 Jan 2026 01:21:18 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26de3331646403e0b36422277bd7f880ca92c654b9fe8c37e83b182be6aee80`  
		Last Modified: Fri, 09 Jan 2026 01:21:16 GMT  
		Size: 776.4 KB (776366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ab05d59244c15d356c3b00b2948afb2a46b9e9c86c26d7d7100650c77f718d`  
		Last Modified: Fri, 09 Jan 2026 01:21:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40627a2c53984b0f74651dfa7cbc391858fff8b23a15c5180e34848e36cd3334`  
		Last Modified: Fri, 09 Jan 2026 01:21:18 GMT  
		Size: 21.3 MB (21300186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:71f490ba093755beab60abc3a84cf8724e8bf87d4bd3c4f526085b5e71ef4423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf63f5df2aa0277b0e5f84b32546341dbfa030ab6b0edc78213d8832685d977`

```dockerfile
```

-	Layers:
	-	`sha256:82da141f927d25ba6c27824cc7d2c8f05c3a1832e358683f9496a0b3c70d0942`  
		Last Modified: Fri, 09 Jan 2026 02:57:55 GMT  
		Size: 7.4 MB (7408920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332387db6b8244a2b2da2d65bc9196ba58143543774de71765d58066e8508b62`  
		Last Modified: Fri, 09 Jan 2026 02:57:56 GMT  
		Size: 44.1 KB (44125 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache` - linux; s390x

```console
$ docker pull drupal@sha256:2b8b75fc910febe61b005ca25bed1c8f2b537fd22aeddf9e52011cc4bbd98143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179267602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057115cae5f8af33438d4fc47985b1cad143b842c9737a59f14cfeb3320a6d00`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:20:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:20:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:20:14 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:20:14 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:32:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:32:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:32:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:32:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:32:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:32:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 29 Dec 2025 23:32:09 GMT
ENV PHP_VERSION=8.5.1
# Mon, 29 Dec 2025 23:32:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Mon, 29 Dec 2025 23:32:09 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:44:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:44:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:48:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:48:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:48:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:48:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:48:10 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:48:10 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:48:10 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:48:10 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:48:10 GMT
CMD ["apache2-foreground"]
# Sat, 10 Jan 2026 01:16:34 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 Jan 2026 01:16:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 10 Jan 2026 01:16:34 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 10 Jan 2026 01:16:34 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 01:16:34 GMT
ENV DRUPAL_VERSION=11.3.2
# Sat, 10 Jan 2026 01:16:34 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 10 Jan 2026 01:16:34 GMT
WORKDIR /opt/drupal
# Sat, 10 Jan 2026 01:16:43 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 10 Jan 2026 01:16:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef34cd33906b4e4d8a4e27681bb0df8433a46a78ec86fe6d78d47fd04f4fb78c`  
		Last Modified: Mon, 29 Dec 2025 23:23:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5ffddb206f617060b180d3b9744cda1b79b0b7b5fb203e9e3e1d7d9c2a8d45`  
		Last Modified: Mon, 29 Dec 2025 23:23:57 GMT  
		Size: 92.6 MB (92564912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26919535fcd0454eb2f96d2316d6f0f13f070dd1aa1989067eeccd258ff913c`  
		Last Modified: Mon, 29 Dec 2025 23:23:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adda8534408b8e787fd429b357f8b8e06a958d1407a0ddb091a47aab326993a`  
		Last Modified: Mon, 29 Dec 2025 23:35:30 GMT  
		Size: 4.3 MB (4320891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996319a94576f425407c0aa9bae2858d5f33d0f9f489a64fab72ab488d8ebbe3`  
		Last Modified: Mon, 29 Dec 2025 23:35:30 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec5b50577d73eee019605d9f48252d2348fcefcd4e389ea95ed4d6c541848bd`  
		Last Modified: Mon, 29 Dec 2025 23:35:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c3073a53b9cf3c7e9a537166bf5387c7b7b658246a1c964169b24f58f83ce3`  
		Last Modified: Fri, 09 Jan 2026 22:48:34 GMT  
		Size: 14.5 MB (14506274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddfffd7e34e8f5aa843b1309bf760abf1ae21cdcef54af714008167f6bc37d3`  
		Last Modified: Fri, 09 Jan 2026 22:48:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2edc894dd8b60d4d0f5c1d11f9daf4b3cb9596fa1e4f965b464cda8306fdff`  
		Last Modified: Fri, 09 Jan 2026 22:48:34 GMT  
		Size: 14.3 MB (14283128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33eba8f2d31546561ea2cdf801c2fd782d75c9b20eed0e60f2519edb327b539d`  
		Last Modified: Fri, 09 Jan 2026 22:48:32 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52a16f9477e228532181e04b50a08533021e6e71f84cb0ee3b850af4dbe6724`  
		Last Modified: Fri, 09 Jan 2026 22:48:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6d42571b5e69f4ffd8462946185f1ef596ab557fd4027aa3ad9c35282a4904`  
		Last Modified: Fri, 09 Jan 2026 22:48:32 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65e374290562d6c63e6fdeebf4fcb82c232c78049780e5b185b172402c390c`  
		Last Modified: Sat, 10 Jan 2026 01:17:18 GMT  
		Size: 1.7 MB (1675344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495db1ff27bc9e326e10ac928cc46d371a360bc8563fa757987f991837c6ff32`  
		Last Modified: Sat, 10 Jan 2026 01:17:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b674f4fa0f26449f3d71aa0eea3a59a4faec58d31a79f264f6831922e8e5f2e`  
		Last Modified: Sun, 11 Jan 2026 13:19:15 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666bc21dec39b9ff12a03e711db404d6274b539b700dd5532522c6503d473fce`  
		Last Modified: Sat, 10 Jan 2026 01:17:18 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46023ae1d64d65eba38bf659c2e1631c0c0b67057a3ebb4e697b5e0c78338a0`  
		Last Modified: Sat, 10 Jan 2026 01:17:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc07f467cf61eb6d7dea5ca3e905e9b6ce782b2c3ce47abbf16a8390f3a15b42`  
		Last Modified: Sat, 10 Jan 2026 01:17:20 GMT  
		Size: 21.3 MB (21300099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:982970dae2107e8bbe59f3d1eeb1519fb5166493ba42c2ce67e1edb2d1c12dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c629f5c5e418844cb3720c5e75e3cfd34ef81b06e8488e19d57ecd17f59cd756`

```dockerfile
```

-	Layers:
	-	`sha256:0348b6057764a38c435c98d1b019716499e845a946ec816254557c6994846c44`  
		Last Modified: Sat, 10 Jan 2026 03:14:18 GMT  
		Size: 7.2 MB (7154328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cfb0aa95e69605c1dadaf2f8a5388142bd187cc88aa2de6d6051fedb05d09a`  
		Last Modified: Sat, 10 Jan 2026 03:14:19 GMT  
		Size: 44.0 KB (44010 bytes)  
		MIME: application/vnd.in-toto+json
