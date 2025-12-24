## `drupal:10-apache`

```console
$ docker pull drupal@sha256:170c01173013ed5f35c969bffbd2eb38bf22116c5c9bc8fd509b1a34e2ad4652
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

### `drupal:10-apache` - linux; amd64

```console
$ docker pull drupal@sha256:5502d7372459fccb2e0fe9e0d283af7b1614ba7b6c6778b7ffd750976564b7cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203496843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b4dd651ee2e0a95fc76882c48a68bfe0987e40c6646f7f3094a8a1eee9522e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:25:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:25:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:25:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:25:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:25:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:25:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:25:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:26:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:26:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:26:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:04 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:04 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:26:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:02 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:29:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:02 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:29:02 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:14:30 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:14:30 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:30 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:30 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:30 GMT
ENV DRUPAL_VERSION=10.6.1
# Fri, 19 Dec 2025 02:14:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:30 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:14:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:14:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d7a8b819572ce9f69fcad0023e25405745aa20bf8ee62e18ff9b000fe0edf`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003ddc7327755214a52a3889badc1c1dd6f17e0cf4957dca4364d920c3caf3d5`  
		Last Modified: Fri, 19 Dec 2025 01:30:01 GMT  
		Size: 117.8 MB (117838248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb00a27bd0aa538641d91c4178b2de1202e2cbd3be316301d26d3afde7c3a8d`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6572af695e2c8d5a8bd895973f75dd6da564e31ba0dc9b665c4cc3b8f4e43d`  
		Last Modified: Fri, 19 Dec 2025 01:29:36 GMT  
		Size: 4.2 MB (4224568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cf978b748bd47232a7004ddd31d5f14529ba9214c60b73784be6741b524cb0`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275193bb4ff00300ae56a857b50436863c2604cf5ea812144420ceaa4417313f`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9752f22b1b6fbef2cb5ea49c10498d40cbcf86358eafab00c2a28e695dd5b158`  
		Last Modified: Fri, 19 Dec 2025 01:29:38 GMT  
		Size: 13.8 MB (13827324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b735179e4fe2e0c204d23f2205b19bf067e1135a2b543ba52c226cceef069f`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73add53d6fde600c9a843c62435c655d71a3b7358182ecc4fc68194e01397cfd`  
		Last Modified: Fri, 19 Dec 2025 01:29:36 GMT  
		Size: 13.5 MB (13533040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e75b521971bf6e3e005c811e30179c317b9f08448a0e8952401a8512feb5586`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9d46402fd99792eabbe396b9d79a209ce2669874d76b3928aade6ea44b439`  
		Last Modified: Fri, 19 Dec 2025 01:29:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9424ea5416128accf4cc484524bdbb2e61ce55a1d4b985e904894d0442ad56`  
		Last Modified: Fri, 19 Dec 2025 01:29:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86273fbcf3a7ac3239c21369ea1ba1cc2486d43188a93b1be5f8994423aaf8bc`  
		Last Modified: Fri, 19 Dec 2025 01:29:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b08a65a2929f4108870f3733bf1de709780cdb244d90088929a890cf90a1072`  
		Last Modified: Fri, 19 Dec 2025 02:15:01 GMT  
		Size: 1.7 MB (1657347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64aee397f7105e35a0e8eb6d6729415f91595160d4497a4fa84373d9b717fa8a`  
		Last Modified: Fri, 19 Dec 2025 02:15:01 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca019e0e2c3b9c51144e192ae2bbb05da2a6664ca92396be92ab7a0d0f1f60b`  
		Last Modified: Fri, 19 Dec 2025 02:15:01 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67086cdd8ee3b9fdfab643e65fc90a59f280aefe19931fd4f0e7ca84b0debe4`  
		Last Modified: Fri, 19 Dec 2025 02:15:01 GMT  
		Size: 778.0 KB (777997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d1f8c6e8f91cf2b2318fbe57015d5c2a256eb081feb9086b9b4085c60692e9`  
		Last Modified: Fri, 19 Dec 2025 02:15:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc95f7aede946308f960ef21eae80a3a587d1105e74134012085f1288b3c0bec`  
		Last Modified: Fri, 19 Dec 2025 02:15:06 GMT  
		Size: 21.9 MB (21855399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:572a801feba2ec6e16e46dda1aa91dd9176a66bc701780d19176483f0e428d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7378915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7280fcfc59c8c0e1400cf7bca45ee7f4aca72b6907ee2dcb902677a2d3bccb`

```dockerfile
```

-	Layers:
	-	`sha256:fde3f2162853a023c38d229ed94d5838fb03791c3a824e1f2e00042800b64765`  
		Last Modified: Fri, 19 Dec 2025 05:53:48 GMT  
		Size: 7.3 MB (7331972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e077833f5057d4e1a56b38fd06a1e4d15913faa6b217f971d682e5a53e28ce9a`  
		Last Modified: Fri, 19 Dec 2025 05:53:49 GMT  
		Size: 46.9 KB (46943 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:7813445e280ec1c9158c7834b078717eb0eef015f784c33738f41f40d2568c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165654286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975d39fd2ff6a5f35b5c7a5282a95380b1170b2292ee55def02e352b4f1ee0d3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:25:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:25:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:25:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:25:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:25:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:25:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:25:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:25:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:25:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:25:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:25:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:25:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:25:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:25:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:25:52 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:25:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:25:52 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:26:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:28:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:28:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:28:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:28:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:28:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:28:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:28:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:28:58 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:28:58 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:28:58 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:21:04 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:21:04 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:21:04 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:21:04 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:21:04 GMT
ENV DRUPAL_VERSION=10.6.1
# Fri, 19 Dec 2025 02:21:04 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:21:04 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:21:12 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:21:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b98077e56e9a52af225d61ff83733170f6c88b27895a8ce3282e2f0cc3bcf7e`  
		Last Modified: Fri, 19 Dec 2025 01:29:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75936ea9785ecae3144094370cd4e579df80b0b5c55db2c88068851bb259a3cb`  
		Last Modified: Fri, 19 Dec 2025 01:29:36 GMT  
		Size: 86.2 MB (86246253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b509a11e7b40929a9fa4ae105a93916654784e026bec64681beb38be0936a1`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726f88c9fca0ba163dfc8917b027830cb047dafdcb54733753c07b2f5df97a73`  
		Last Modified: Fri, 19 Dec 2025 01:29:26 GMT  
		Size: 3.8 MB (3752412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32672fa2dbe5f496ea112ddd274469fcee44312e363b7492dde4283875a2b39`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c05361af8e0cd26978bea998619d22e81dd0913d01453079c92307ddd01fdae`  
		Last Modified: Fri, 19 Dec 2025 01:29:26 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4d3494b23f103555e21728c0e9867c5d9437f10eb0e206099c337b7c321854`  
		Last Modified: Fri, 19 Dec 2025 01:29:28 GMT  
		Size: 13.8 MB (13824767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705bb1b987959f83f907db66a75d329bbb732992833ec0a3a3e49587449fa588`  
		Last Modified: Fri, 19 Dec 2025 01:29:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a1623a25ce42cd5f9c9f5f806b2436040e76022bad4a7fbc0cb1cb9cbd1fa6`  
		Last Modified: Fri, 19 Dec 2025 01:29:27 GMT  
		Size: 11.6 MB (11610368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50398f20aef7e46e32d6acd08a20e2ddcc718f6d3427238cc1102818afc2d975`  
		Last Modified: Fri, 19 Dec 2025 01:29:26 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195674d95453791e54871c62e100a12bf3d1082757d6e20d121ac815778d22b6`  
		Last Modified: Fri, 19 Dec 2025 01:29:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682f6703d19ea21931975bfd02a25b9eb32a523cc3340ddb750731d6ecf39b6b`  
		Last Modified: Fri, 19 Dec 2025 01:29:27 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8cbb8263843e4f8f88ec9ed817d5a245281f36dfcbae336575466b93c4bb3`  
		Last Modified: Fri, 19 Dec 2025 01:29:27 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64062c8f4bc517f0e0b04372c993d2faa0b334e4c19b24a065cbc07ea0bb0b2`  
		Last Modified: Fri, 19 Dec 2025 02:21:36 GMT  
		Size: 1.4 MB (1370566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fabf84390efe8656b4ad46a8f37aeead903f2c0a9c4fd12216f98ec8b4f529d`  
		Last Modified: Fri, 19 Dec 2025 02:21:36 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae2c1d04142368555b815f6c3f97681cedf38157ad4c8aa5ded964d5910b0b4`  
		Last Modified: Fri, 19 Dec 2025 02:21:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bf7efe407acbb8f18d0107b2c0f0e7c547017122dc1cbf0d064037c31f4f71`  
		Last Modified: Fri, 19 Dec 2025 02:21:36 GMT  
		Size: 778.0 KB (777998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8e699a089381cee59ae8f87814bf24da7f31b54222a18e5e2dbe25fd8d6960`  
		Last Modified: Fri, 19 Dec 2025 02:21:36 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf509416bc45eefc7ef998e4dc46643e02f4f034ea1741071d92fb26ebce4fe`  
		Last Modified: Fri, 19 Dec 2025 02:21:39 GMT  
		Size: 21.9 MB (21855492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:eeff96ab4fe6d583d4f11cbd8023d4d45592a374d81cb8f882d023064e764a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60b742d44ff4f206615a5b736544406c5ecfb7e70b13895cb12214fc92e89dd`

```dockerfile
```

-	Layers:
	-	`sha256:15a1dd4c2c71682d5fcaf9555c7bbd5e73fc40d33b7a916fc9b2db3074cacbf0`  
		Last Modified: Fri, 19 Dec 2025 05:53:56 GMT  
		Size: 7.1 MB (7135933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084b6a1bf6b4fee024224c54c43defab81171e5890a081f739880ed42edbb7b5`  
		Last Modified: Fri, 19 Dec 2025 05:53:57 GMT  
		Size: 47.2 KB (47188 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:0ff4f626c777421661e19af123ff0224bdb234e09647e548935ce3b703987dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195874835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8cb81d613551c768e9898e66d2c03b54018f14d71c1f467fb50c5a95a3eef8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:25:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:25:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:25:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:25:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:25:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:25:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:26:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:26:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:26:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:06 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:06 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:26:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:20 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:21 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:29:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:21 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:29:21 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:14:55 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:14:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:55 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:55 GMT
ENV DRUPAL_VERSION=10.6.1
# Fri, 19 Dec 2025 02:14:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:55 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:15:03 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:15:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39eeccd0163eb65ceb3aa0887bee05133fb1ce6d736471e1351aa0c13d1d774`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a165053d2a394aa37254544528d9acec320476c1a8ee7d5157358ad135588d`  
		Last Modified: Fri, 19 Dec 2025 01:30:07 GMT  
		Size: 110.2 MB (110162664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754488ffda4bc040a4853eb622ea0d10cdbbdaac99fc4946338809ed77aa8c48`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc1d1daa492ce189403cdd31379b838c08af999d8a5a9784306df45f607cc7a`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 4.3 MB (4302287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c3751ca1e08a720e2542804958c7da679fe5051b134a2c649ee5badb761e60`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9301228dc60220133d59bf509ada5e09fabd80787daefd9990ca5dcd29d85880`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f90ad2f4828b87e6d715d79df902c305e52a0c12d4e11c8b3e81276f98daa85`  
		Last Modified: Fri, 19 Dec 2025 01:29:59 GMT  
		Size: 13.8 MB (13826889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d606766cef837b6af41a0d2de64c86000597e0a65a078578403ab1ee653b37b3`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440ba1f26bdfb3b0117375dd82d0e0c3412f7ea7cde8eb11318b5b867efe333b`  
		Last Modified: Fri, 19 Dec 2025 01:29:58 GMT  
		Size: 13.2 MB (13190958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9c0db7824d2d8e2c98a0ce222218d2acc81b2301e999e2de0324bb5e68a1da`  
		Last Modified: Fri, 19 Dec 2025 01:29:57 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dc82650b6dcf5e29b17b36b0c7a91d45728c6c2443a3eda632100b9b467dae`  
		Last Modified: Fri, 19 Dec 2025 01:29:58 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db0fdfe5a6eff8a8d5c392267421e70eeb67d1b1aa41ebb759c8cae97f90075`  
		Last Modified: Fri, 19 Dec 2025 01:29:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efcf397185d4874f3e9640e67243b24e5c6fc23ff38989e32f3743c1f197baa`  
		Last Modified: Fri, 19 Dec 2025 01:29:58 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ab953e399f59a880099a0d8d9adc2b4879bfc98e76ac5b22a70d001c924d48`  
		Last Modified: Fri, 19 Dec 2025 02:15:29 GMT  
		Size: 1.6 MB (1614537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb21748a998cfc33ae58d6c4e31c385836d8b24f3bc06c4ccafcaaa50738e4`  
		Last Modified: Fri, 19 Dec 2025 02:15:29 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1c34ecc75704fdd3db1de6245e44dc174f63a2113640d8c14089eaee409864`  
		Last Modified: Fri, 19 Dec 2025 02:15:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ef7809768ed458983381c3bcd83ad77297fb0cd09aaa4f841ff3b70bcd5298`  
		Last Modified: Fri, 19 Dec 2025 02:15:29 GMT  
		Size: 778.0 KB (778003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1802a6fb97cafe128419b2382cec37e589783d26ff1a424fb2289ef73a46396`  
		Last Modified: Fri, 19 Dec 2025 02:15:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3fe3f6ebdfead42d659c5c9ff3bd62a20aaf81073d86418df6c22b02e2bc47`  
		Last Modified: Fri, 19 Dec 2025 02:15:33 GMT  
		Size: 21.9 MB (21854448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:c2853b33d0143a06ed0fb3c95e73eab59e87f985ef1e08fc73073c7a15946d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9754fc5c9b89eabf4cf968960ada67cbc04a5cba0e204ddc2fbece00729f9cc0`

```dockerfile
```

-	Layers:
	-	`sha256:6e00e3e64111a7778c9eff2ba5503f7acc92ee77f8ec37eb5db0a447be46dbbb`  
		Last Modified: Fri, 19 Dec 2025 05:54:02 GMT  
		Size: 7.4 MB (7429442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa00e32bd71286fc7e7acc77dd3baa32fd61064cb41aaf931cd454771b02f6f7`  
		Last Modified: Fri, 19 Dec 2025 05:54:03 GMT  
		Size: 47.3 KB (47286 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; 386

```console
$ docker pull drupal@sha256:9bfc6bab8c11bcba0a036574afa541395e1563920fab5ad42613ab564d8a3ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203919633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f09607bb997d1fcb14908104dcef28d1b6b87382b8ae8adb510acd527cf3215`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:26:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:26:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:26:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:26:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:26:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:26:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 19 Dec 2025 01:26:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 19 Dec 2025 01:26:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 19 Dec 2025 01:26:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 19 Dec 2025 01:26:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 19 Dec 2025 01:26:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:59 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:59 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:27:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:30:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:30:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:30:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:30:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:30:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:13 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:30:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:30:13 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:15:02 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:15:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:15:02 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:15:02 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:15:02 GMT
ENV DRUPAL_VERSION=10.6.1
# Fri, 19 Dec 2025 02:15:02 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:15:02 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:15:09 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:15:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933b29f273e1b8e65ecb9a890c9fa7afe8e264bd0a2fc1fc95f2e5d98893d1fb`  
		Last Modified: Fri, 19 Dec 2025 01:30:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d14b3cad35c2b570fe2c7ea6dcebf9185be29f3506a6291462770c5c66c0541`  
		Last Modified: Fri, 19 Dec 2025 01:31:07 GMT  
		Size: 116.1 MB (116138529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045fbd1c3b46f30780de3381dcf0adbd256328f9682570523c05dbb7fb4edfe6`  
		Last Modified: Fri, 19 Dec 2025 01:30:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c22a9ee2ced0c63e2c899aa8566fc3cb6e4fb4cb37053869c56cacf95892e4`  
		Last Modified: Fri, 19 Dec 2025 01:30:46 GMT  
		Size: 4.5 MB (4455939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4197d13c1f0781a26428e284bbbcff1a1da10a20ff2914973466f7d72e928896`  
		Last Modified: Fri, 19 Dec 2025 01:30:45 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3534812f9d013c24df1bb6b3e61a15204248aebe3f8660f31e8663c8d1e48dd4`  
		Last Modified: Fri, 19 Dec 2025 01:30:45 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f2b034e0140fce4e3cb2bf8a215bab445552f475fa4ad8db982285f4e2a3a`  
		Last Modified: Fri, 19 Dec 2025 01:30:46 GMT  
		Size: 13.8 MB (13826083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e8f660bd2126ee48e945c55fe89f2d96de89b8f50356311ed5d9c6da90b0e6`  
		Last Modified: Fri, 19 Dec 2025 01:30:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67815cf193f74f5e6d893224bc823971139fd28cee9de2f160cf02ff82d3d2f0`  
		Last Modified: Fri, 19 Dec 2025 01:30:47 GMT  
		Size: 13.8 MB (13830287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8823f1ea99b4a02d295ece186770413c7b6621157a43918530078bac2f742453`  
		Last Modified: Fri, 19 Dec 2025 01:30:46 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b108db71dedd19045be76c4e0a9445ea9f5e35da6494c0245ec26520ae12d29b`  
		Last Modified: Fri, 19 Dec 2025 01:30:46 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db25af3eac29721caac9304d806419d3e861879a400fca0029b437961397bfa`  
		Last Modified: Fri, 19 Dec 2025 01:30:46 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbb4132fd0ffb4e9fad09a2d8214f8349ade17834f5636451b5a5f3cc32b2f0`  
		Last Modified: Fri, 19 Dec 2025 01:30:46 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6c4ad18d0116df55e94c05bf1d8418301f2423daf9ddbf5e49cae8e6a5df1d`  
		Last Modified: Fri, 19 Dec 2025 02:15:33 GMT  
		Size: 1.7 MB (1736929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4858d8759250884701560e00d326ca82245284c8149f51ae26cccec69088febd`  
		Last Modified: Fri, 19 Dec 2025 02:15:33 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397edff9c8fc34c273b8c0f7ca8926308d31e3fee4151e4ecf1a7eb0c58f1858`  
		Last Modified: Fri, 19 Dec 2025 02:15:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ce0340da5a687a9a97fcd57db7135faefc44f7398bd7cfa8d8c231434d4bb6`  
		Last Modified: Fri, 19 Dec 2025 02:15:33 GMT  
		Size: 778.0 KB (778001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dc1a30217c57cf7500b315def894460f733945c7a0c7756f537fa20decd708`  
		Last Modified: Fri, 19 Dec 2025 02:15:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79872b03d7930fc2094bb2bdd1b9918650c6e01ea557dc44b3b5567805778189`  
		Last Modified: Fri, 19 Dec 2025 02:15:36 GMT  
		Size: 21.9 MB (21854369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:06b8184469b562ddf2a48d74feb4ee9fec5743d44a305a0ff93708a728ad6b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d68a44587b72593deb5690697a994d6bb0a88a9250b98892a3f36f22c7d4466`

```dockerfile
```

-	Layers:
	-	`sha256:92c5a7a68333c0c94d27911361d5d4cc747ddc02e02d7a46e58840d902caaa0b`  
		Last Modified: Fri, 19 Dec 2025 05:54:08 GMT  
		Size: 7.3 MB (7305754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e25749128c5ae517372176519d88634dfc047d6e929bad4f66e920ec2e4c6a`  
		Last Modified: Fri, 19 Dec 2025 05:54:09 GMT  
		Size: 46.8 KB (46827 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:5fd5199051efca1428728ee6e3051b56cf1bf2b7c4c8a5f918d39808aadf2b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200334941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb01bba1b47f7faca39a1c19cc51795ff6c5d2ebaa36e39a29b98c815f1021ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:35:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 00:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 00:36:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 00:36:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 00:36:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 00:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 00:41:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_VERSION=8.4.16
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 09 Dec 2025 00:41:46 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:49:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:54:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:54:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:54:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:54:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:54:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:54:13 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:54:13 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:54:14 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:54:14 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:54:14 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:32:10 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:32:11 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:32:14 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:32:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:32:18 GMT
ENV DRUPAL_VERSION=10.6.1
# Fri, 19 Dec 2025 02:32:18 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:32:18 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:39:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:39:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e968a4c552b5d63962c849d9412a26339a7f50c4b8dee90079284c674840b8`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30124c487aeb9dddde3de1f906a208cb9bd0ae4a03d96c1622924a8622e568`  
		Last Modified: Tue, 09 Dec 2025 00:41:59 GMT  
		Size: 109.6 MB (109597911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd51466d9c6ea60e911a8b8d548a3ce159de7cc08df81891f748149917d7196`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cdd7fdbb4f498b6540140a43b62e20227e731c816b54e09c4166f8ff8637fb`  
		Last Modified: Tue, 09 Dec 2025 00:55:22 GMT  
		Size: 4.9 MB (4876044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662dc1d5e5e4a3977cad81ad0301a23d9a7c393028d08dafd0f088f67701014`  
		Last Modified: Tue, 09 Dec 2025 00:47:34 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e1761af690f425f7869d904bbd39508f379bcb057f9a915bfe9e5a5ffac93d`  
		Last Modified: Tue, 09 Dec 2025 00:47:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974ecba88663d99ab052fe23ec2d76caf3a3c7591b314016829c52b6a9234c9f`  
		Last Modified: Fri, 19 Dec 2025 01:54:49 GMT  
		Size: 13.8 MB (13841862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0173c4a259a8bb37cce00a47d437423bad637f34b046ae8f7a0d64c8786434b`  
		Last Modified: Fri, 19 Dec 2025 01:54:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed68720b3edfb1ce4f493ea4f6efbdf8b3a2f42144dc04857d242b8ff7319b9c`  
		Last Modified: Fri, 19 Dec 2025 01:54:50 GMT  
		Size: 13.9 MB (13936518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d4899884cea81de78bfb1e813ea7d690738136766d2cdf66f9b9471de8b514`  
		Last Modified: Fri, 19 Dec 2025 01:54:48 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121ba313e508fc092f39398a9bbc8313f28fa4dd25b11e116c4c0162f0dc1efd`  
		Last Modified: Fri, 19 Dec 2025 01:54:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8529f176034b4af0be430d91fac756e9e5c3631f79058a1592777722b796a7f`  
		Last Modified: Fri, 19 Dec 2025 01:54:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f06d482132d774bf62e6406ef0b01719f32dd3d91fbf3353859e299b3124ca2`  
		Last Modified: Fri, 19 Dec 2025 01:54:48 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b8fcff95ccb3601aff547396b4d50e22254800785112d167b8cc22d1001a76`  
		Last Modified: Fri, 19 Dec 2025 02:33:29 GMT  
		Size: 1.8 MB (1846802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9bbe77314596e4adc9522b4331898bc778aca844cebac8f007bb04ddc943d2`  
		Last Modified: Fri, 19 Dec 2025 02:33:29 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2527d4ac468639f68ff16c8368adefae6173ff8d72c94d6531c922a54b5fa8`  
		Last Modified: Fri, 19 Dec 2025 02:33:29 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ef19a42a76322e18fbf0e0527e26d1c486c0e83e395beba537f68d53f3ac63`  
		Last Modified: Fri, 19 Dec 2025 02:33:29 GMT  
		Size: 778.0 KB (777996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdb46374edd64e46ca41f67f2a0f6e9236a4e74b7a8a93d585ef72bcef5a258`  
		Last Modified: Fri, 19 Dec 2025 02:33:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8805826bf6fd1c213e0b245804e4529d9369ca5a32cbe37a3af7753de0af928f`  
		Last Modified: Fri, 19 Dec 2025 02:40:12 GMT  
		Size: 21.9 MB (21854497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:177bfbd445cfec64d33311d6196210b52b09467b5e4a6d2b4b4150d15204b351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7378967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d68776abacefaf7b443c70d96b586b28143a966b446167f9a9af71893f3d8ec`

```dockerfile
```

-	Layers:
	-	`sha256:1db151364420b49292116e32f3d5564bf2e93e0ef328eb8d98d7c22c8b7844aa`  
		Last Modified: Fri, 19 Dec 2025 05:54:15 GMT  
		Size: 7.3 MB (7331881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8db7ab248bc76591e06838233d6ff41bfcbba976529c24d443400b38c8697e2`  
		Last Modified: Fri, 19 Dec 2025 05:54:15 GMT  
		Size: 47.1 KB (47086 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; riscv64

```console
$ docker pull drupal@sha256:2599bd328845dd6ddeb22e7fcb1e809ca2e39a7c5e9908910e79f3ed006d9261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229912614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82805a401503b5402cb39bf8156b11d7972f25da893a200b8b1fa4fd38a69386`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 08:01:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 08:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 08:03:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 08:03:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 09 Dec 2025 08:03:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 09 Dec 2025 09:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 09 Dec 2025 09:08:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 09 Dec 2025 09:08:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 09:08:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_VERSION=8.4.16
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 09 Dec 2025 09:08:26 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Tue, 23 Dec 2025 07:45:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 23 Dec 2025 07:45:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 23 Dec 2025 08:38:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 23 Dec 2025 08:38:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 23 Dec 2025 08:38:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 23 Dec 2025 08:38:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 23 Dec 2025 08:38:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Dec 2025 08:38:34 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Dec 2025 08:38:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 23 Dec 2025 08:38:34 GMT
WORKDIR /var/www/html
# Tue, 23 Dec 2025 08:38:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Dec 2025 08:38:34 GMT
CMD ["apache2-foreground"]
# Tue, 23 Dec 2025 15:36:55 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Dec 2025 15:36:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Dec 2025 15:36:56 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 23 Dec 2025 15:36:56 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 23 Dec 2025 15:36:56 GMT
ENV DRUPAL_VERSION=10.6.1
# Tue, 23 Dec 2025 15:36:56 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 23 Dec 2025 15:36:56 GMT
WORKDIR /opt/drupal
# Tue, 23 Dec 2025 23:36:57 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 23 Dec 2025 23:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53d28a615a791c3859b4a1756ba700dc2c4f69377eb59f2058ba63d00e0869a`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8434337c0c50639ecc5b6dc774986d4e9420e3476e8e2468932a6a85632eb`  
		Last Modified: Tue, 09 Dec 2025 09:07:07 GMT  
		Size: 146.6 MB (146578870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e90ba410db15c99bcf35ee3bbf15863cbe2650207953ae1e912e0e6bf7fda0b`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e74b4e149c4738e4a9c37f39d8a642897edbd74a4bf14ea4f27d976938c2b0f`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 4.0 MB (4033863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951f674e0bc56dc657de8b096a1cd8ed3c4b0cbb2de5d3a05d6e50989e9b86ab`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c810195650744e7970d6163d3e7b56ea79e2877073201e867cf1c229807a8924`  
		Last Modified: Tue, 09 Dec 2025 10:10:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ae4c646d007bfe96242d1c2902bc322877dccce4372274e17638520781cc9c`  
		Last Modified: Tue, 23 Dec 2025 14:42:43 GMT  
		Size: 13.8 MB (13841752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec0811bea28fa53fdf658d458083abd3a0be5804c1c88c8915caf5eaec78dea`  
		Last Modified: Tue, 23 Dec 2025 14:42:41 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccc0d14bd11977da5cc7c5d975fe16bdff1a27edfd709bbe161a3a408f961c8`  
		Last Modified: Tue, 23 Dec 2025 14:42:44 GMT  
		Size: 13.0 MB (12971484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f55ee712331d31223de7e8340183ca732b29ae2430b453b71feb185f5ef5ce4`  
		Last Modified: Tue, 23 Dec 2025 14:42:42 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eccae2fc2fc57d49287779ec38c978780c982d2c7bbec0adb91d7bd74a08cb`  
		Last Modified: Tue, 23 Dec 2025 14:42:42 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625d60c67b26fbfbbc4b111eb4269e65259c633f8d2121320c491383b30a4de`  
		Last Modified: Tue, 23 Dec 2025 14:42:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23322a0b1428789cc8115a607e8f9693fe925d04cb5335f071fdaf4f3a0dd594`  
		Last Modified: Tue, 23 Dec 2025 14:42:44 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5422ff07e1b2faa9ead4989455fed6d5ac966c5cf893684f89a78d46049bbb`  
		Last Modified: Tue, 23 Dec 2025 22:47:54 GMT  
		Size: 1.6 MB (1573664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2edf00b0f7b43202aeb3640bd95cc19b1ba72b2e8c7de5fc537c93a78e045a`  
		Last Modified: Tue, 23 Dec 2025 22:47:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80c281c10c6ea49890d9c5c098f81141761008372facd52145c6fa4286cdf51`  
		Last Modified: Tue, 23 Dec 2025 22:47:54 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fdf14a7dda71c8c28df1fc622645a2a8349c1d60b00dbee5f2f507f8e63580`  
		Last Modified: Tue, 23 Dec 2025 22:47:54 GMT  
		Size: 778.0 KB (778003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c101c9a9b5e5c334edaa9a9db70300048b135bccd7171f8afdede3ac0b7b6`  
		Last Modified: Tue, 23 Dec 2025 22:47:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a41a98b8a81a99de93fbeba61f5ff4ddd424ae3f72475f0be3d21110155c7c`  
		Last Modified: Tue, 23 Dec 2025 23:41:52 GMT  
		Size: 21.9 MB (21855372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:5f9db281ce72759e095595dc484d502b94909ba7d715dbb2858d2348fca26509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a277234c019c607909dcb01f17b487397df71eb70ac0970016b7b4f4556ae1`

```dockerfile
```

-	Layers:
	-	`sha256:76650a30df5ea6e9c4a6e8206a37f094955eabd53450bdb3068859fdc319aa62`  
		Last Modified: Wed, 24 Dec 2025 02:53:43 GMT  
		Size: 7.4 MB (7403878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca83a9258b9041d5f24578b6df2d062874fab46c77cab7f32454ce7b9c465b5`  
		Last Modified: Wed, 24 Dec 2025 02:53:43 GMT  
		Size: 47.1 KB (47087 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache` - linux; s390x

```console
$ docker pull drupal@sha256:c76c4d37f9b5d0fb797ecf85e2a49f7d7fc93eda52fc2225a76b5cbf85812c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178178306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668a4425c29db9daab61a3c340e56aee48390d32205194755915d3fdd29006ab`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:37:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:37:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 08 Dec 2025 22:37:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 08 Dec 2025 22:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:37:30 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_VERSION=8.4.16
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Mon, 08 Dec 2025 22:37:30 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:25:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:25:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:01 GMT
STOPSIGNAL SIGWINCH
# Fri, 19 Dec 2025 01:29:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:01 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:01 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 01:29:01 GMT
CMD ["apache2-foreground"]
# Fri, 19 Dec 2025 02:14:09 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Dec 2025 02:14:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:09 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:14:09 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:14:09 GMT
ENV DRUPAL_VERSION=10.6.1
# Fri, 19 Dec 2025 02:14:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 19 Dec 2025 02:14:09 GMT
WORKDIR /opt/drupal
# Fri, 19 Dec 2025 02:17:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 19 Dec 2025 02:17:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06325ac7d48e9543412848e1fa70a7cb9a579c86f688b2e2e9bd944346590fce`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a4b708d85d9501bc1929ab5cadbcf5d4c4bca40490257ace724e13a60fcbe4`  
		Last Modified: Mon, 08 Dec 2025 22:41:12 GMT  
		Size: 92.6 MB (92564698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d9f5a2f9a70ca9e903eb070a1168477352c4a37bbecf3ddf16c7afe71c0e`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92dc5e34b4915edbdad5123bd5ae0d2c6a40e6471d283ad84545bd68e81f92a`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 4.3 MB (4320856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5ee5f503eaad0fe4d32cdc7ac6d3f69c18294139afbeddfa165cfa252fda81`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeb52f4bcf5819a6d5437fcce1e1e4325546addfcf171571a63a6d4fcf38a2d`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a27bc8f5fc21afd186ad6133449138e15bc9cf5c63ee3741d12360fea891e7`  
		Last Modified: Fri, 19 Dec 2025 01:29:27 GMT  
		Size: 13.8 MB (13840897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7252cb9686846a958bf0a5a3cda67f70fc8c1519992b250fe7ccb4f5ebc674`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90faa2ba0930090fc2bbbb058952b473d6edd2aa6fe81eaa9f5a47562a95e300`  
		Last Modified: Fri, 19 Dec 2025 01:29:26 GMT  
		Size: 13.3 MB (13302002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526984dc43955b994154d664342e00c516ac5cc445de0ba5be224eadeafe83f`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c420a82e938eb1203af9f5ed80b1c4c0d12deaa9e5cd5995a64b67c63419e809`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef13b2b844c13c8a0c458d08fb59612efcca6d28a8e20410a492399381c2cf8`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b5696768de94c8dc40783370f28533dae26a0dd3f48d873f621aae31ae86ad`  
		Last Modified: Fri, 19 Dec 2025 01:29:25 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4512004b0f5194e79ac29d329a7ab18072f7a00fbb2a2325ec05ad1ceb12368`  
		Last Modified: Fri, 19 Dec 2025 02:14:55 GMT  
		Size: 1.7 MB (1675584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79836a2480dbe6df3f81e340a68832c94dbcebc09d9a646062d75e983f6a0676`  
		Last Modified: Fri, 19 Dec 2025 02:14:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4c19844fdfe3d4fd6fd241f6639ec23ed5d6433213ae0dccdd294a4fc25040`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afaf1ff6930d6f91495f16d9ccadcfc3bb285ae6760078dd89c7a1c98aa8c720`  
		Last Modified: Fri, 19 Dec 2025 02:14:56 GMT  
		Size: 778.0 KB (778003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdf794ef67504d0fe7543ee5425442e44b969cb2d8120cbb4d62a17ea6ab63d`  
		Last Modified: Fri, 19 Dec 2025 02:15:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a27db01715d970014422ea42964d851cc2eab16c9f2e442be0fffbeb8d7047`  
		Last Modified: Fri, 19 Dec 2025 02:18:19 GMT  
		Size: 21.9 MB (21855451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:79cc651a6ff0c8658d075d388edb7e6e3310e877da38e68e1fcc797c3a5cbf57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96810f6e76783a4b2d628c84e40a39842fdc0fd97e7554290697e3b1e44b85`

```dockerfile
```

-	Layers:
	-	`sha256:e11a76401bfba80bd91df28a79dffd53ecad96f46e5eb28dc115a1d4bda9126c`  
		Last Modified: Fri, 19 Dec 2025 05:54:27 GMT  
		Size: 7.1 MB (7149222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bfd3896844966533903d47ef2c5fecac0c080d1c612128e05b3c34d94e13d`  
		Last Modified: Fri, 19 Dec 2025 05:54:27 GMT  
		Size: 46.9 KB (46936 bytes)  
		MIME: application/vnd.in-toto+json
