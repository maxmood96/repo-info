## `drupal:php8.5-apache-bookworm`

```console
$ docker pull drupal@sha256:dfee99356a9fd95e134e4832f1eb03cc9dde14df886e1b8f3efff7158ec53b35
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
$ docker pull drupal@sha256:137e902258d037166b57c3de250a34ac4f864e237bee80ab563b23df534dfd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206091175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d26d1dff5f1ce098d058655209929b554dd2253d1b1e23a7806e9e9d9d7e7c4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 16:41:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 16:42:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 16:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 16:42:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 16:42:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 16:42:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 16:42:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 16:42:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 16:42:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:17 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:17 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:42:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 16:45:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:22 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:45:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 16:45:22 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 17:42:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:42:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:42:47 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 08 May 2026 17:42:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:42:47 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:42:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:42:47 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:42:53 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:42:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5142b1fccf39f1b049467e836511b100c17d21c8887919f22ee24ab81d12304f`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e14c2a627168e2f2b5e87f93ed94137da43027ca732141f2f6d9107539bcee`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 104.3 MB (104337467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406993ec00f341f7dd77823b3ab0c66e45dc122c34088ffbdb79dfe52cb0f7c5`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50addec1c3650c0f76c520567f35dd34e3af1eaf0f34266534c8fec90ac799f1`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 20.1 MB (20141995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da0c179b698932815051bc8a18e3ab717b327d5efd5950ce20c0c51618f4e52`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477be35abce0d2406eeb9201500bd418710d3fa0d0f8848fc3aee4628c78df1f`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e761c9912d136f19457120191048791a533e2ea51390c7d68de5f468d0814`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 14.5 MB (14522360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beec4a29564d2871d42d813cca14396bdf79858ba25e125d6f1bb7e0818980e7`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc90ee15f5f9a658e99a3ff132b8c20da6c2f0c575a0e21a11113031cff1ca7`  
		Last Modified: Fri, 08 May 2026 16:45:47 GMT  
		Size: 15.1 MB (15128169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966515dfc0fd462048c774d776833c15614e6f9c634189e28d56ca2363ca6b62`  
		Last Modified: Fri, 08 May 2026 16:45:48 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70ec6a4cb64e63ac9575c882ccca5f4ab659d374c9578d3bae13ddadfa5a334`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb967e1284333c6097d4aa8274ed7daa81dede131fb395f29560f198e92e36f`  
		Last Modified: Fri, 08 May 2026 16:45:49 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef4d32848c04c6a6fb5b924f61e0988c2ecd5e24a35d8d4762ce740da6db3f`  
		Last Modified: Fri, 08 May 2026 17:43:09 GMT  
		Size: 1.6 MB (1575940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8c336a47b00af09c53a57987f749912d887774094234cbc484c9b1b28e8db`  
		Last Modified: Fri, 08 May 2026 17:43:09 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4c41667e8d6e5c4e96b3d3c15e73a850563baa0f55c6adf4571810755e6b87`  
		Last Modified: Fri, 08 May 2026 17:43:09 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2122c4242cc0cd7b06daf6a6853adb0bc64804fcc05d5e7610983af05ab0686d`  
		Last Modified: Fri, 08 May 2026 17:43:09 GMT  
		Size: 790.8 KB (790766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f678388746085f8add8b0b563a42312eb7d79119ca8e5b40b131462874ca2be7`  
		Last Modified: Fri, 08 May 2026 17:43:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab722810bc87ef29e2df2d09f7ffa8e25fd62c8857fa61fd366a20b3de528ba`  
		Last Modified: Fri, 08 May 2026 17:43:11 GMT  
		Size: 21.4 MB (21352084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b6f7902472e754041e018ba089971c93ea5d6ccd6fa3e5bdc8223735eb6fa4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7091205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c1ebd00822e600f8860e125bd7efc1b9cbbe9d1e366c2e55e605efaa7ed309`

```dockerfile
```

-	Layers:
	-	`sha256:35b646cd03d7d791e077739034629f9d59e20690a000663407cad2d2c784f818`  
		Last Modified: Fri, 08 May 2026 17:43:09 GMT  
		Size: 7.0 MB (7049659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713966286707ebe75cab623c3e8c852a72c3126293dbab06a9113489986420be`  
		Last Modified: Fri, 08 May 2026 17:43:09 GMT  
		Size: 41.5 KB (41546 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:b65aa833ac02bac27fcb953d2ff3bdd646e995388a69a36d5eba7ec0d4213aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169506642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b7e1bc8d7f7b482fb17594d4b78235037d67b18055f391a0ee12e820a3bed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 16:41:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 16:42:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 16:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 16:42:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 16:42:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 16:42:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 16:42:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 16:42:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 16:42:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:13 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:13 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:42:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:06 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 16:45:06 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:06 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:45:06 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 16:45:06 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 17:42:42 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:42:42 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:42:42 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 08 May 2026 17:42:42 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:42:42 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:42:42 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:42:42 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:42:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:42:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d578f138102fbe22b19eac9077140db968075954e2b8bbd0f2d0168642da1af5`  
		Last Modified: Fri, 08 May 2026 16:45:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55f985affbd6c79df82b6901637f3f7dd80abb9733055c4af9dce693cb1e55`  
		Last Modified: Fri, 08 May 2026 16:45:24 GMT  
		Size: 76.2 MB (76156110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd65d77c801f159850792800cf6a41f22f3d58bc6f6c3ff43bd671ca4613c241`  
		Last Modified: Fri, 08 May 2026 16:45:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab68d4e74c736272ec6113ebda48fda1c5069f5f95a2a452bd1cb3a51d002b3`  
		Last Modified: Fri, 08 May 2026 16:45:23 GMT  
		Size: 18.9 MB (18850772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c625e991eb02a6d6c0ff1362e75e3f71a7ed0c80904596a7da254320c298f6`  
		Last Modified: Fri, 08 May 2026 16:45:23 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7f17f849b3de4143bded440efcef1b52601a13ee122420b8f2f0812928bc1`  
		Last Modified: Fri, 08 May 2026 16:45:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab267f947ee6c3ceee9b474186f7421a5294540b3f69e3737d34707278afba6c`  
		Last Modified: Fri, 08 May 2026 16:45:25 GMT  
		Size: 14.5 MB (14520334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6791e26f607a46a8f69e6274c30199731b4ab6a4c6d3a4bb2faf2773181d1c`  
		Last Modified: Fri, 08 May 2026 16:45:25 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4e59bdaf80dff3f0fbb86d2be8fa85da5a0f7c69c71d24e37eeccf542b2acb`  
		Last Modified: Fri, 08 May 2026 16:45:25 GMT  
		Size: 12.6 MB (12593213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1b25ee5828945184ebaceefd41591c17c88a5b8e6eb2b66d87e1eb2909dc94`  
		Last Modified: Fri, 08 May 2026 16:45:26 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a82cce8835543be53efbe1eac2a28ec319c2667b5bdf89a76d61e03f4c4bd40`  
		Last Modified: Fri, 08 May 2026 16:45:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70654807a9a0c10f92121a49854f76ddf8caebe882564abee9646a0949a4a9ff`  
		Last Modified: Fri, 08 May 2026 16:45:26 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35267753784f22d6676015000c84a6cb11af3b90c69523141fbf80d0204b3397`  
		Last Modified: Fri, 08 May 2026 17:43:23 GMT  
		Size: 1.3 MB (1295496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7299bc8ccc2f8fa0df2d8d12a737d68f476faf426a8e2bf4d247074be8bd98d`  
		Last Modified: Fri, 08 May 2026 17:43:23 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2042fd6f5a639d3cb8ded2dcb9fb6f0969b4ad28ffde14e8d5ae4671824f26f`  
		Last Modified: Fri, 08 May 2026 17:43:23 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3ca5dce3f7246f5ac46a550e5bb4e65c4484ddbbb0d0aa728c495cc691de07`  
		Last Modified: Fri, 08 May 2026 17:43:23 GMT  
		Size: 790.8 KB (790765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5144adac2c7740204d54f333d54a0c92864a3e9a834f7ebbb28dda524ae4db6`  
		Last Modified: Fri, 08 May 2026 17:43:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecd2d597399640ceb9450715d764af3aa6603166ae8014770a07fe8efe0c257`  
		Last Modified: Fri, 08 May 2026 17:43:25 GMT  
		Size: 21.4 MB (21352366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:322be336548198a5038d091bee94dad4a5085f032082a94c671edddfc1daf6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f782fb8afd6ef8974b366b8228fe4a88729860b7202e683c633879e013946022`

```dockerfile
```

-	Layers:
	-	`sha256:7c6b53818cc9ee32a82d4532ac49b656f2df5e1ec048f3abca7af0158e5027d0`  
		Last Modified: Fri, 08 May 2026 17:43:23 GMT  
		Size: 6.9 MB (6862995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:812dc57b7daf0bc4dc67953d87f55b9f65b10ab6bd0ac515b6aef2922871b54a`  
		Last Modified: Fri, 08 May 2026 17:43:23 GMT  
		Size: 41.7 KB (41680 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:032b1a1927a5bc8093684d001f10e353b27d05a77db86284a7b0b54643d40624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199356019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5897f745492e8596fef13d878c39258b43e0ac4f36695983bc8ab44d036ff5d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:22:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:22:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:22:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:22:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:22:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:22:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:22:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:22:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:22:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:22:52 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:22:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:22:52 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:23:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:23:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:26:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:26:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:26:05 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:26:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:05 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:26:05 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:26:05 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 20:32:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:32:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 20:32:47 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 08 May 2026 20:32:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:32:47 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 20:32:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 20:32:47 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 20:32:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 20:32:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f88c1f2f6755c3ed8761539be43e80ebd31736472ae401683eb4d6def8afb`  
		Last Modified: Fri, 08 May 2026 19:26:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720328d2ecd0dc6ddf27086d3ea0e612273df0d5b505a3b377e29340e0b4e7bc`  
		Last Modified: Fri, 08 May 2026 19:26:30 GMT  
		Size: 98.2 MB (98170655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ecf23677fc9a629944111b55356d97dc44cc52e8151d37b63dbd08fa4c2067`  
		Last Modified: Fri, 08 May 2026 19:26:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801973399c6faadfab635503c4621095f3822698de0c0d6bdbfc8a56352f65cf`  
		Last Modified: Fri, 08 May 2026 19:26:26 GMT  
		Size: 20.2 MB (20165948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95103a4d65391ff9cac68a42a5e4d3b9da1853c899695317f1a24e7bb1fac86`  
		Last Modified: Fri, 08 May 2026 19:26:26 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7049a1584509da6bf3c36e10f70b3d7d8cc34de7a69977634e2f1a37d673a04`  
		Last Modified: Fri, 08 May 2026 19:26:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9aa326eca76407fef7a5c20d2349c8b34bdcd0d2f93dcb0938b0e715fc6b54`  
		Last Modified: Fri, 08 May 2026 19:26:28 GMT  
		Size: 14.5 MB (14522049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c163b003467404524e4c33eac90d7377c6ee3bed686c08457f36fd61752a76`  
		Last Modified: Fri, 08 May 2026 19:26:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c1110fd79168f8305f34bf1543daacb2878bba11733cd90a945db79e329068`  
		Last Modified: Fri, 08 May 2026 19:26:28 GMT  
		Size: 14.7 MB (14668926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa15251a9e9e9d097cfc764b4cf9cc3d924506ef7efff0f5febbadd5927789f`  
		Last Modified: Fri, 08 May 2026 19:26:29 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dad03696952b7ab72ac00f2b01832eb168dbcfdbbe639a7a2dc4324f97b3df`  
		Last Modified: Fri, 08 May 2026 19:26:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d0b3394513d9225c0672198327133241095916da468ec6f34d4d17930bc4d2`  
		Last Modified: Fri, 08 May 2026 19:26:30 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bd9a5e73945768520da27109d90fe51e01cd039104e3cb958982cd8379ff81`  
		Last Modified: Fri, 08 May 2026 20:33:14 GMT  
		Size: 1.6 MB (1563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c50b99405c190f6c6bac9c7713df5b96083823751a774fd7c0d4ab9890ff6c`  
		Last Modified: Fri, 08 May 2026 20:33:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2827486f788e695dee35c2b578cb59638e7deb239fe09d759a494e383d1c38ba`  
		Last Modified: Fri, 08 May 2026 20:33:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71589bc0c3ba9fb11a411e895dc17a4a49f7b47041106d1750d5ddfeeb328116`  
		Last Modified: Fri, 08 May 2026 20:33:14 GMT  
		Size: 790.8 KB (790767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449f3ee4ea67df4d20af476b50011bfa0b6becfe24ca5db20f12c715488968d9`  
		Last Modified: Fri, 08 May 2026 20:33:15 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48de149d64ccd8a27189137722fbd980dbb96f0853c2ec5fdf939bb6ebfbedd5`  
		Last Modified: Fri, 08 May 2026 20:33:16 GMT  
		Size: 21.4 MB (21351893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:30e2e8d226c2472bd164d9f37082dcc562febfbb9a5571589b4835ec5baa60f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7119786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e20809d48a841193a6f42b5036471935ac30b6fe045fd5336007bf778356a7`

```dockerfile
```

-	Layers:
	-	`sha256:d310784d1b19caf8ee33f108970ca5a4be9ef006c1f0005cb0fcc9bf94314c6d`  
		Last Modified: Fri, 08 May 2026 20:33:14 GMT  
		Size: 7.1 MB (7078072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c5d97e945b9a167bdb871838b3a2d5a072908b8988c9e912b53709f2d8c45dd`  
		Last Modified: Fri, 08 May 2026 20:33:13 GMT  
		Size: 41.7 KB (41714 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:41cfe43b3cec99035171efc795106a567d55c8bf212ca0cb138b4da2772ea1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205206402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dfbce031f4646f6ed931697688ea51318af0ad9e4108f4ff7282edbb05fabd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 16:41:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 16:41:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 16:41:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 16:41:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:41:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:41:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 16:41:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 16:42:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 16:42:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 16:42:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:42:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:21 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 16:45:21 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:21 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:45:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 16:45:21 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 17:43:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:43:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:43:12 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 08 May 2026 17:43:12 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:43:12 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:43:12 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:43:12 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:43:18 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:43:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ceab9188c99bb4807b7b5b31c76962e728b9040bd3676ebeeabf72b13d039523`  
		Last Modified: Wed, 22 Apr 2026 00:16:30 GMT  
		Size: 29.2 MB (29221696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1361d5190dfc552b6e79276af41e2cf774c973381269527a45c17421e37c7e`  
		Last Modified: Fri, 08 May 2026 16:45:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4271f4d1520ccc7e655f65f68810fb105776f3d9cad5bea9f3c3f356e4fd9b0`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 101.5 MB (101530119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431c4de1fad63bf01f302458c5fc0c75463135514699a769e42b950aaba77ef`  
		Last Modified: Fri, 08 May 2026 16:45:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034711b7ab78b4837017b587d481eeb1c5faf69a03e22465dde629df5b13e29a`  
		Last Modified: Fri, 08 May 2026 16:45:42 GMT  
		Size: 20.7 MB (20666017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f8c9483e949cc5fac19b3f4fcf6fc97dc55d28ff1d87f7c1b6af8fc32c31c4`  
		Last Modified: Fri, 08 May 2026 16:45:42 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab061ecc3c0c9943280453a71f9b0024b724ef5c3c20c7255770cec8da36d1d2`  
		Last Modified: Fri, 08 May 2026 16:45:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c3d50d56f176de1adbf9c96e9685a518fc3d39319e6b1ea41d9009a15942d`  
		Last Modified: Fri, 08 May 2026 16:45:43 GMT  
		Size: 14.5 MB (14521416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d277459a878124fb12907893e1f813210f0257046ce62d46c92340cb971140e3`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb658f2695a726c668f8adecff63a08831545c2f99d518ddb5e21b283908d349`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 15.5 MB (15470299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf00c9a2ba29ab9dcc5d4ca287e71c86fb01347b470244d47c46fe34dc76f5c`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fde48cb20b739c9bb05a581dc617fb65b77e3a570f1705a1e8ab22998fe0e1`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e133291defe39092be58bff0923760ca6b21ec42b2138873afacf293eead49`  
		Last Modified: Fri, 08 May 2026 16:45:46 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923e2099a3dca86cd032c6db6c555a413853146ab5e1c0232b58c45597b4f45`  
		Last Modified: Fri, 08 May 2026 17:43:36 GMT  
		Size: 1.6 MB (1648040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e8af6cb1bade27aa296e6e4868ab27271546b3fe895b110da66ffd6dc00161`  
		Last Modified: Fri, 08 May 2026 17:43:36 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0b467dcd1031439ccc6fd56eb8bad471946b37154427a253ed5b25da02f84`  
		Last Modified: Fri, 08 May 2026 17:43:36 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993ce582fad99df3e09fc17d2f6f8ef2a57ecea1879412a475be4c9c126b70c9`  
		Last Modified: Fri, 08 May 2026 17:43:36 GMT  
		Size: 790.8 KB (790765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f2ef34a958945976254ceecd26c1c0e1f4d37498a338ce24f46e1b40f9498`  
		Last Modified: Fri, 08 May 2026 17:43:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31f93dccdc3dfd058e5894f88329aa7850f547cfee0cbcb331223cb99ab9a7d`  
		Last Modified: Fri, 08 May 2026 17:43:38 GMT  
		Size: 21.4 MB (21351897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b5e4e48b65eccf2ed6b91d635ceda1fbf6dcc399b6e3aead65f88647641657e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7070908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637acc3280ee5f7933e2f9b2e305649a5ed0fbeb460c117444a70d84bddeab33`

```dockerfile
```

-	Layers:
	-	`sha256:5709b600b2f206100f936c516793e5a7b5b4f5153f6a488e3bb0f5863f98cf8f`  
		Last Modified: Fri, 08 May 2026 17:43:36 GMT  
		Size: 7.0 MB (7029407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f8723f557ba5f66efe2430e36e7471a353083072a6a91a9fd035ff15701961`  
		Last Modified: Fri, 08 May 2026 17:43:36 GMT  
		Size: 41.5 KB (41501 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:b98b72815fc53bc4d2c88072bafeffb5dd4af74d37ba36928612d3d631badfcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.1 MB (210115459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b22a6791202b84e5aa30aeca7195adaba5d16dd2c45feeebe376daa4daf2113`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:06:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 02:07:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 02:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:07:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 02:07:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 02:07:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 22 Apr 2026 02:07:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 22 Apr 2026 02:07:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 22 Apr 2026 02:07:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 22 Apr 2026 02:07:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 22 Apr 2026 02:07:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 02:07:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 02:07:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 02:07:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 02:07:26 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 02:07:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 02:07:26 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 02:07:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:07:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:12:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:12:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:12:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:12:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:12:49 GMT
STOPSIGNAL SIGWINCH
# Wed, 22 Apr 2026 02:12:49 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:12:50 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:12:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 02:12:50 GMT
CMD ["apache2-foreground"]
# Wed, 22 Apr 2026 09:42:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:42:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 Apr 2026 09:42:52 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 22 Apr 2026 09:42:52 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 09:42:53 GMT
ENV DRUPAL_VERSION=11.3.8
# Wed, 22 Apr 2026 09:42:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 Apr 2026 09:42:53 GMT
WORKDIR /opt/drupal
# Wed, 22 Apr 2026 09:43:14 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 Apr 2026 09:43:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26f9cb740e187cb4772a93e40939279f04db15bf332e83c5cdd82d6ce0cb373`  
		Last Modified: Wed, 22 Apr 2026 02:12:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4da74e371512d746b2064ab8d31082a214f396711c5c5b0a83fbbeda17bc3c9`  
		Last Modified: Wed, 22 Apr 2026 02:12:46 GMT  
		Size: 103.3 MB (103331324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17bb927e267eaeefb0c6a9975a32dd0392b377723db62da1e6f3dd18551d32`  
		Last Modified: Wed, 22 Apr 2026 02:12:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd7d7557407cc09e157b3fee176ef0b1202f95ba262da669b3d80691d5444b`  
		Last Modified: Wed, 22 Apr 2026 02:13:20 GMT  
		Size: 21.3 MB (21332401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8486ed7b77df9a774e468d76a0cc26a6c58fc862e7c28c3222c466746a8888df`  
		Last Modified: Wed, 22 Apr 2026 02:13:19 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac646ce77b0d0ade4a8b976daa89b261e397f5cf791999732637a76c8c1f998`  
		Last Modified: Wed, 22 Apr 2026 02:13:19 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a30f008fd0567a78850441bcc6e7f3bd0e8040a7104a5ad0f745e2963ace0`  
		Last Modified: Wed, 22 Apr 2026 02:13:20 GMT  
		Size: 14.5 MB (14484021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fada423018462dad689e36882fb6c9fe56decbd7b451e8277a95971793189674`  
		Last Modified: Wed, 22 Apr 2026 02:13:20 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca0eba23c1918f1063b7104c04d6fd4206e6fb86ae6fde768ac029384256375`  
		Last Modified: Wed, 22 Apr 2026 02:13:21 GMT  
		Size: 15.0 MB (14965742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6893234ed6c9ce06ddb44a07c2bfb74cef9d36f5ae7490f4919eea818b5e9f`  
		Last Modified: Wed, 22 Apr 2026 02:13:21 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cda9f5773bb7392547e18e1b4e7efe2b72dcb2fdacc3fd40f9b77dcc7ac9b7`  
		Last Modified: Wed, 22 Apr 2026 02:13:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b21ec97d0b21a6ab7356f8abf330f25584fa56f4380f163064783b2d9e6067`  
		Last Modified: Wed, 22 Apr 2026 02:13:22 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c0237964e6025f3c4000d388c36fc501abee53f67f79db59fc3f4cd99ffb50`  
		Last Modified: Wed, 22 Apr 2026 09:43:50 GMT  
		Size: 1.8 MB (1775935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed9ec677032ba6212581a07c5f9faef594c4d252b2e729a1368cf8d287b3f64`  
		Last Modified: Wed, 22 Apr 2026 09:43:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5437be533e10d913a95ebdf9a0737182bb9c9031407d4fdf107d1823d1ac4cd3`  
		Last Modified: Wed, 22 Apr 2026 09:43:50 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb45b8e4a0d730486e47aabeeaecab6f7f01ac6a969d1586d344a6f9df752594`  
		Last Modified: Wed, 22 Apr 2026 09:43:50 GMT  
		Size: 790.8 KB (790772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e16e9e1156abc7ac9e66145752949ca717f33a2198219691aa3867517faff9`  
		Last Modified: Wed, 22 Apr 2026 09:43:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831552a1756121ec55161c51223daff0f7959ea6c93d2301d0f45022c58b266`  
		Last Modified: Wed, 22 Apr 2026 09:43:51 GMT  
		Size: 21.4 MB (21350686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:de1f1e6f9526335741829d9193f0d76fd542e7239c822f70ad43680e7f5d6fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7068091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408c708d4d53d9aaf28291d81407716e4ccac158da79e9a329e0876b6838db9b`

```dockerfile
```

-	Layers:
	-	`sha256:88a313a1af1dd2767b514b851061562a3f58c59d4e2010a13db5b6fd6b2cf949`  
		Last Modified: Wed, 22 Apr 2026 09:43:50 GMT  
		Size: 7.0 MB (7026485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b796b2aa97cc38c7b131c5f434ec9abe1229e94976344c780f64909ebd39f8ab`  
		Last Modified: Wed, 22 Apr 2026 09:43:49 GMT  
		Size: 41.6 KB (41606 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.5-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:3c916d4806b07b5d1e9eca4302e09a6b2e95be423ed07a056c222219f8e7b56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181311851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709ba75a8ae34f77fd79223c82eb9fa135816031a7d521826f73712220b50e38`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Tue, 05 May 2026 23:25:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 05 May 2026 23:27:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 05 May 2026 23:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 May 2026 23:27:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:27:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:27:50 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 05 May 2026 23:27:50 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 05 May 2026 23:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 05 May 2026 23:29:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 05 May 2026 23:29:46 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 05 May 2026 23:29:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:29:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:29:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:29:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:29:46 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:29:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:29:46 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:45:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 16:45:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:51:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:51:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:51:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:51:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:51:08 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 16:51:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:51:08 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:51:08 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 16:51:08 GMT
CMD ["apache2-foreground"]
# Fri, 08 May 2026 17:41:47 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:41:47 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 08 May 2026 17:41:47 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 08 May 2026 17:41:47 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:41:47 GMT
ENV DRUPAL_VERSION=11.3.9
# Fri, 08 May 2026 17:41:47 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 08 May 2026 17:41:47 GMT
WORKDIR /opt/drupal
# Fri, 08 May 2026 17:41:53 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 08 May 2026 17:41:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89426b8fd56cf7223dcb6f2d483a28c283ea2b89b935bab9c163d3ed348cfb24`  
		Last Modified: Tue, 05 May 2026 23:40:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961f6f8d278a8cf07820de911bea1c70cd3c2595a84e262b33067b67264439f5`  
		Last Modified: Tue, 05 May 2026 23:40:26 GMT  
		Size: 80.8 MB (80830056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3959462e04a24bdbdff8d971b3748ac4a219124937bd4265cff676d017337e45`  
		Last Modified: Tue, 05 May 2026 23:40:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81a36cd0003653fcc9d5a28f09c0aca7f9d3ce01274d1e14ba717ac3d5662db`  
		Last Modified: Tue, 05 May 2026 23:43:29 GMT  
		Size: 19.9 MB (19919712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6101a773496c431976a17f66fdac09846d7174072eafdb85fb965ff9c5e0c0`  
		Last Modified: Tue, 05 May 2026 23:43:20 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8033a487ee62daff228daabe4336e00fb85cfde34b5a6947e26463f310701e21`  
		Last Modified: Tue, 05 May 2026 23:43:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d36cdced3c79391ca6790587b0556c375274ea6d51bed1bd4266917b4d58e7c`  
		Last Modified: Fri, 08 May 2026 16:51:28 GMT  
		Size: 14.5 MB (14521522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166207ff649c7b7625b4d8572fef46c0ee69ffca511319b930ddb54e1017f0b8`  
		Last Modified: Fri, 08 May 2026 16:51:28 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8855eccfc1d5daaef09e62d751fa3c96bb77c0708d5c96d2966c1389617e1711`  
		Last Modified: Fri, 08 May 2026 16:51:28 GMT  
		Size: 15.5 MB (15513300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3f08a98c17817e13f39084ae97cdf6d33c120798e9324cf01299c5b9aa74c`  
		Last Modified: Fri, 08 May 2026 16:51:28 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d016537a376b060cc7e454ef5b7eb2e6ea0fe3ea3061eb94cd9aaa747715b2ee`  
		Last Modified: Fri, 08 May 2026 16:51:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3932efcf6844d3eb4efd970002ab50060f8bdc82118c225e1fafb93fb0e85d11`  
		Last Modified: Fri, 08 May 2026 16:51:29 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3187d2f0b3a8c52e7f2e55455b7783a84333c919091d43031fd4c7ca009181c`  
		Last Modified: Fri, 08 May 2026 17:42:23 GMT  
		Size: 1.5 MB (1486352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0527ae11724d2c8233fdd43d0ff9d6e84d942d7df3a4d5e44ba272ecb4c7afb7`  
		Last Modified: Fri, 08 May 2026 17:42:23 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f527291c839c753806338a8597428a5b8b63113af322bf8e0fc3ae9cdf1cb8`  
		Last Modified: Fri, 08 May 2026 17:42:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148021b289edd3924435aa65604249d42baf42a0e441f46a201cbf766d96fe71`  
		Last Modified: Fri, 08 May 2026 17:42:23 GMT  
		Size: 790.8 KB (790765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c987a2707b1d2ff87e8489696c4437aae7334732abd3faffd1d894f57a916e`  
		Last Modified: Fri, 08 May 2026 17:42:24 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7ef2d08dbbdd450d76d8b6c7cc5ed6e7ab2788d97f907b25d4c8ee00a30f56`  
		Last Modified: Fri, 08 May 2026 17:42:24 GMT  
		Size: 21.4 MB (21352406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.5-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:56ba12fc07fdd7259cf1b878fa2c068403ca3779f60fccfd08124203b485f240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6928399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d21a665bfb80107e8ead6395ab5fd646c8f6952e0079ac4509121e83173ee7`

```dockerfile
```

-	Layers:
	-	`sha256:fd34d4a1f77cae9f92ab43dddb80f4e1b37326e8cccfabfa692579f51e309190`  
		Last Modified: Fri, 08 May 2026 17:42:23 GMT  
		Size: 6.9 MB (6886861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c95bb26f479b2c18ec5b062307f0a6390e964b0ce63990c6e3d59112e344865a`  
		Last Modified: Fri, 08 May 2026 17:42:23 GMT  
		Size: 41.5 KB (41538 bytes)  
		MIME: application/vnd.in-toto+json
