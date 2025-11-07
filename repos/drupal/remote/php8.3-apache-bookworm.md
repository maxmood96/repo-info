## `drupal:php8.3-apache-bookworm`

```console
$ docker pull drupal@sha256:1f32ee4485d41dc24e1a5c32a6add73cdc06094c317b6afd1c0dca91622b7056
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

### `drupal:php8.3-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:ff375fe97e6f7fe77b114307412796fe5ef2adb9cde1f33aa0e0706bdceaaadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200044448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352a80228dcc3a71e5d77ff31be1336bcb4434a7741a7360f504cfdeebfd878`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:20:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:20:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:20:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:20:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:20:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:20:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:21:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:21:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:21:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:21:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:21:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:21:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 00:21:04 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 00:21:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 00:21:04 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 00:21:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:21:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:23:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:23:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:23:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:23:39 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:23:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:23:39 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:23:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:23:39 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:40:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:48 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:48 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:48 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:41:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:41:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2e93808f0dc619ce5bc8554dd7820c7e1e2e5921922001bfe70716a28d449`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7c67586ceddbfbfe3398f6a2103d1135f66f549a20eb1e21c9428e401bd4a8`  
		Last Modified: Tue, 04 Nov 2025 00:24:19 GMT  
		Size: 104.3 MB (104330347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80154db780f3355493cb1ebf1260359fe9703b84719b9c6dce5279d03a3645af`  
		Last Modified: Tue, 04 Nov 2025 00:24:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4410dc47491cfd93eb6276649815ee7deab8fa9dbfa71fc440708993fda1ed68`  
		Last Modified: Tue, 04 Nov 2025 00:24:11 GMT  
		Size: 20.1 MB (20131766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93665cb6d3945b5605c97634aa1e9ef1de377a63a5443531c3f12144daa42165`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f881d087b627315939ffba37f7c3b19cb19617faa181fabffddf0bd32c7f62`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57e8a983a040e6d3c66034e03e23b8f32700d2ea96704b2ab3cd78d70c6b790`  
		Last Modified: Tue, 04 Nov 2025 00:24:11 GMT  
		Size: 12.7 MB (12721429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8fff9591e51f61cb8cdc929a80bdd98c03bcb41a649bceb6011948231666fa`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474f2c5bd6cf8615e23945eb0a713ae0d77b0e8768fe7d684e5ffda46e4cc41c`  
		Last Modified: Tue, 04 Nov 2025 00:24:11 GMT  
		Size: 11.7 MB (11669661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b274c85fdcc4cf2b4da285779c888b5aefb5096fc2f70e2de6ce476752f7a26a`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4b0e5e9658cd103a9599013486e84ce2e715137466be692a6aae6ab604a172`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b15b7b4e73928f0788e80c606ddaae7c505e2859cdd3610305fbd47b0a5ae9`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16d029d1f57e78715bea6d39e166a700216fccd2d08e91e4288c981ad03a217`  
		Last Modified: Tue, 04 Nov 2025 00:24:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d461a714fbc4af84de0b9cbbc3cd9ce87fef7f656f2e376a9b399f54f3da773`  
		Last Modified: Fri, 07 Nov 2025 00:41:31 GMT  
		Size: 1.6 MB (1561381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e45027fea3c472b4125b071266550ac74af6bec7fd5333261e563a79e633c9d`  
		Last Modified: Fri, 07 Nov 2025 00:41:30 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bddd6c422de6ad123998db52f7cbda1400ec54ea4094e9a0e7e81686b35289`  
		Last Modified: Fri, 07 Nov 2025 00:41:31 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881d30c992341533b8374b4b07550257745c4d37c94f503ea4a227c580f43b56`  
		Last Modified: Fri, 07 Nov 2025 00:41:31 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eadb415c50c0b368783068dac938036afd7cd38806dea22983b3b094d8e16b`  
		Last Modified: Fri, 07 Nov 2025 00:41:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45860b0dfa3d0f4db52e460ca6364280f72bffc61fed9bf0d9a0563b7d2a5aa1`  
		Last Modified: Fri, 07 Nov 2025 00:41:33 GMT  
		Size: 20.6 MB (20643405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9bee20b272f3d7a54760e451db9ef8a5979da9d1a86cf59324d302a4d718aa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7095719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149fd1965c1f160b64f7e23e54a9dc0cc6265b7fc0fa8a0ac6e3f66548eedad4`

```dockerfile
```

-	Layers:
	-	`sha256:816130571b6c0cd41349bc356350597eeaf1b1b1336dce6712543455b1b9a4ba`  
		Last Modified: Fri, 07 Nov 2025 02:59:59 GMT  
		Size: 7.1 MB (7052928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7903d30705e0b190d470d459d90c79620cdc178556e5ffab26d98e6af64a319c`  
		Last Modified: Fri, 07 Nov 2025 03:00:00 GMT  
		Size: 42.8 KB (42791 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:060abc7bbd43be1bd9c1c5bcd63e6fdcbb2d83915a9e75a4e799069ac1c9df49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164410560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ab19bb7ce8bff45430316021935bf9f7e60cd638e09d59de12dbcfd12a5e57`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:18:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:18:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:18:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:18:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:18:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:18:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:18:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:18:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:18:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:18:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:18:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 00:18:20 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 00:18:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 00:18:20 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 00:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:18:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:20:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:20:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:20:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:20:59 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:20:59 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:20:59 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:20:59 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:20:59 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:42:35 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:42:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:42:35 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:42:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:42:35 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:42:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:42:35 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:42:43 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:42:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bf2b1d162dd7f682aabfcab1417edecc1852eb47e876b367f581f4c0e32633`  
		Last Modified: Tue, 04 Nov 2025 00:21:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37dcf79ac1ac8b49d060c7843bc47c6af5bbe6c0e0ab9f95aba9f684ff6be9`  
		Last Modified: Tue, 04 Nov 2025 00:21:35 GMT  
		Size: 76.1 MB (76148800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8794d7ffba692b00964880302af973a8359a319a33e28f7d724398c0bad2ad47`  
		Last Modified: Tue, 04 Nov 2025 00:21:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fbadc2f3cd9145f013bb329ee53f0125686835cf00522a43b11bd5e13ffdbd`  
		Last Modified: Tue, 04 Nov 2025 00:21:31 GMT  
		Size: 18.9 MB (18860064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a876313a9870b3177a815d0fb85a1d5486cdf116d4ac54cde33e5d292d3a4aa`  
		Last Modified: Tue, 04 Nov 2025 00:21:28 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641fe3e0432156c36d06abf5ede7d83251de38573dfda131f3dc8179e2c11ebf`  
		Last Modified: Tue, 04 Nov 2025 00:21:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1509fa8059d69c85ef09fa7c67e80cf169d286ab99e6a305187905fa7a225bc4`  
		Last Modified: Tue, 04 Nov 2025 00:21:29 GMT  
		Size: 12.7 MB (12718952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df781fba3e6c5b6e9deddeff74dee1cfcfb957cbfe975361446d087611c6c57`  
		Last Modified: Tue, 04 Nov 2025 00:21:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f688fb2e3df46a164a9a8fc1315e61682e65216ea1513777028b73da91b3ead`  
		Last Modified: Tue, 04 Nov 2025 00:21:29 GMT  
		Size: 10.1 MB (10064214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e937acff2da76d1ad31544f9e1c173d60c34c46c6b7bf2ad557e03e81dafc98b`  
		Last Modified: Tue, 04 Nov 2025 00:21:29 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d0fee20688612bd434f46950c5209a665e7e7b676543f7d7783af0806a5ded`  
		Last Modified: Tue, 04 Nov 2025 00:21:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768caba77af319ecf7848bfcc49ad1646fc7d97c9fcb34aab962c4f0fa56ac3c`  
		Last Modified: Tue, 04 Nov 2025 00:21:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb3aa714d23e16b07ad32aa15d83e092b794b9599306faead75e25a96923bb7`  
		Last Modified: Tue, 04 Nov 2025 00:21:29 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111e8ffe0f274c3ced86b61263ac2050b0c35ded9a93ead4e2f0a36238d2d4d`  
		Last Modified: Fri, 07 Nov 2025 00:43:07 GMT  
		Size: 1.3 MB (1285176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5afe98d321d4e9fa69868cbfeefaed8177a79e469db3a4ae9e260f06f8a70`  
		Last Modified: Fri, 07 Nov 2025 00:43:07 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417038213b54cdbd7e56612131512f37bef7fe3917788a4511ab081acf734da7`  
		Last Modified: Fri, 07 Nov 2025 00:43:07 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662bdffd670e8095befa9fa86ba70a688c38f3d8c8617b62690787374fb0af61`  
		Last Modified: Fri, 07 Nov 2025 00:43:07 GMT  
		Size: 751.5 KB (751478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff9a6948d59ad72792188445697768f1721c46c72c73c21392e35c0460645c6`  
		Last Modified: Fri, 07 Nov 2025 00:43:07 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf1a3a81d787a6f665e9c2459a556c327f83215f5ca6324249b4ccf6480f28d`  
		Last Modified: Fri, 07 Nov 2025 00:43:10 GMT  
		Size: 20.6 MB (20641349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:09bcaedf872a401f61c2897d0c7adc7217531d9ab50932ade998cf4702ad4813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6909186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47af6390fb1938ffdb0936ffc3b7b2fc1d7d336cbf2bb1ea54c02263ee01ccd4`

```dockerfile
```

-	Layers:
	-	`sha256:7c8e4554ea0c6741ccdfbd9bc1e92412170d0085206b60e92b9f41b47a43fd52`  
		Last Modified: Fri, 07 Nov 2025 03:00:11 GMT  
		Size: 6.9 MB (6866264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aebc18981e74d72a6a43d6d28ac736867a22b205e50e841689eddb92e3bd60`  
		Last Modified: Fri, 07 Nov 2025 03:00:12 GMT  
		Size: 42.9 KB (42922 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5852340230c49f80c52e146030a6f02e0122ac66c37f30669fdb294817e26009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193785227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b098dcbd8f41c9ef29cf5f3f5bb9b0ed10643fa87d6f8f5d972f33f9f1723571`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:22:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:22:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:22:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:22:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:22:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:22:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:22:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:22:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:22:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:22:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:22:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:22:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:22:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 00:22:52 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 00:22:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 00:22:52 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 00:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:23:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:26:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:26:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:26:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:26:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:26:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:26:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:26:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:26:31 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:26:31 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:26:31 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:40:28 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:40:28 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:28 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:40:28 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:40:28 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:40:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:40:28 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:40:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:40:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ee40eea51878ecf8202f11f133e1d76bd549eb98f169906cf2059c57a557ed`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d322fd7cf2be704ea118627ef890de73c47b84af9f76f21f2c596268317a3f`  
		Last Modified: Tue, 04 Nov 2025 00:27:07 GMT  
		Size: 98.2 MB (98165645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af464e5dfbe731bed200ad5746a8a613cd315c79416b099a06d98b145f872da0`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa58735ebc0207d9561709d0c0e1a94f02eefe0aef190fd4d99e03980afc32ac`  
		Last Modified: Tue, 04 Nov 2025 00:27:03 GMT  
		Size: 20.2 MB (20159060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c0c2f5103b0c2baa6fa705bfafadee23d0207b2686a05599a7873976695500`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cfdbf02d384b5afde96a18c348f6ada6e269d49722ad3888c24cfddfceb559`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f74cd8410ba952aa069ad5c5fa8c533efdc622eeb7f0965fbfb4f7a28912145`  
		Last Modified: Tue, 04 Nov 2025 00:27:02 GMT  
		Size: 12.7 MB (12721092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f7fffecd67839e42cec7be9ea349858e6338226efc1ec95dd675abbbd30872`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c6ec0e02c73208e759dc83d96cd14a1b4101a164f5e0753b6eef48ef1adfa9`  
		Last Modified: Tue, 04 Nov 2025 00:27:03 GMT  
		Size: 11.7 MB (11685629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9d1cdc7e3c82cf62862d674747259f3634d490910d442ecb7460f5ec59f87`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d17dd7a6531c79347704baa6593f678f15eea3354a7b51f59e5dc3c391ab88`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1805a533fe91782d34bbab573994147ba6bdd0ec06ed35f9b9c3f7d0bc2f6a`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d8e5e601a072b6c79b856ff337b13d56118b5f0cb2b58e2660d82ae89039c`  
		Last Modified: Tue, 04 Nov 2025 00:27:01 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9209ebb03f8fe984ce698507cb483b8da8ebfeee23a22f40cd493d7140e30f3c`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 1.6 MB (1551516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139300cfd4be3103e61531c62ac9e27bcabdf81d0d71b7db2d35da80dd26a025`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c0247e50ed92b2b134d05002484b28f106ae2a3f1fbb643740437089a1502`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053ca4e6c8d532b77a18686acc9752ad869f7f7d55435f9707d4919dd693dc7a`  
		Last Modified: Fri, 07 Nov 2025 00:40:58 GMT  
		Size: 751.5 KB (751482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedf4a3c881581520e0ab99f21904ca760a746d792681b54e9706a5099e4afea`  
		Last Modified: Fri, 07 Nov 2025 00:40:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4cabd02cf71e7730c5b4213318042bde4c01688dda31d382647e134b221993`  
		Last Modified: Fri, 07 Nov 2025 00:41:00 GMT  
		Size: 20.6 MB (20642017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:72e87f70283c63b0d716ea7030004b402e42efc5428c561e2bc327b8cb8636e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e104a7cdbb8d94e0b023aaa9bd7f0db294abb17d6381f980e491fb7872335b32`

```dockerfile
```

-	Layers:
	-	`sha256:2555d5c048814ff3051c618a09dc2b5166b3f708b2b042c8b56bdc27d3b5416a`  
		Last Modified: Fri, 07 Nov 2025 03:00:17 GMT  
		Size: 7.1 MB (7081341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72957a0524ab4b9fe371287f9c6c0cf0ef0629ea71294b046c21ea9d9291a301`  
		Last Modified: Fri, 07 Nov 2025 03:00:18 GMT  
		Size: 43.0 KB (42959 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:1bb21cb664c276ed4a810d4f76534f27be077ae56eaece8ad791b41d1250db3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199029966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d01e7bf65abc7680c721e210d1fa52fa52ae23a312a3e844a2530929c142d70`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:16:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:16:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:16:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:16:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:20:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:20:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:20:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:20:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:20:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:20:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 00:20:03 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 00:20:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 00:20:03 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 00:20:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:20:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:22:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:22:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:22:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:22:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:22:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:22:32 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:22:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:22:32 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:22:32 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:22:32 GMT
CMD ["apache2-foreground"]
# Fri, 07 Nov 2025 00:41:07 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Nov 2025 00:41:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:41:07 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Fri, 07 Nov 2025 00:41:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 07 Nov 2025 00:41:07 GMT
ENV DRUPAL_VERSION=11.2.7
# Fri, 07 Nov 2025 00:41:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 07 Nov 2025 00:41:07 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:41:12 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:41:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea05e97d8338547d515f35616ad7672a5a4dacdfcb9ff63b0357533482b78c74`  
		Last Modified: Tue, 04 Nov 2025 00:19:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0619f5bf7d90aff005ac2167dad5223d5400ad88fa73624d8bb7a38fb46042ac`  
		Last Modified: Tue, 04 Nov 2025 00:20:11 GMT  
		Size: 101.5 MB (101518113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa58ecc2a118ec492d2306d4b68ab71f53a03f33016e82bbf6c96992c2619764`  
		Last Modified: Tue, 04 Nov 2025 00:19:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a77cfd1c86a761223316c70f4b8592927557c99e72707fc84f53153fc2b0a09`  
		Last Modified: Tue, 04 Nov 2025 00:23:03 GMT  
		Size: 20.7 MB (20658439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73ad2a8f13f8e3c8811b7b53623d032292a4889001ea0a95d24f4d143d58a5b`  
		Last Modified: Tue, 04 Nov 2025 00:22:50 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837cd3368568e14969ba78659df3af83ce20d67fbec814253347118f60fbe2c1`  
		Last Modified: Tue, 04 Nov 2025 00:22:50 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc735c62a1a7c7dc7d9e6c154e76a071f8b8ae01a99678777b12220b4165195`  
		Last Modified: Tue, 04 Nov 2025 00:22:52 GMT  
		Size: 12.7 MB (12720368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d010806a7897fbbf2daff0e39e998646490f86943b2e0a0449c73c9e4f92b2`  
		Last Modified: Tue, 04 Nov 2025 00:22:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b826770cd79de90be7dca0c1fdc071020223310e6779bc7c188bf1637a1f3`  
		Last Modified: Tue, 04 Nov 2025 00:22:52 GMT  
		Size: 11.9 MB (11884853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9850cf3aa33e345246f8722d16f904fe0b33db46535974a609b6c2354973cb`  
		Last Modified: Tue, 04 Nov 2025 00:22:51 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efae9fe22471568e43588eb62bf6ac148a0af71b78cc1cca65ca0545d25d4d7`  
		Last Modified: Tue, 04 Nov 2025 00:22:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a78e10a5461f7ec41de865c2d86af3d631517aa07981e441c6388108b80a9c`  
		Last Modified: Tue, 04 Nov 2025 00:22:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f51402c31432aa3907791e16c5f2dd3fb3b2359c3afba3fa096cb4e021420`  
		Last Modified: Tue, 04 Nov 2025 00:22:50 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6686b971d26a6e348c62f66c27759bb7725bcd863444fd0d5aa85cb25b4691bb`  
		Last Modified: Fri, 07 Nov 2025 00:41:34 GMT  
		Size: 1.6 MB (1636893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb226c323ee2dac8674e64fdd1bcc5c3806aa2c99d128176d540ebb19c0fc2d`  
		Last Modified: Fri, 07 Nov 2025 00:41:34 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42585e4d45853795c50675ae0743ccb778187ba7ce140a9a01dab12a174e0e3`  
		Last Modified: Fri, 07 Nov 2025 00:41:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb1999d310f30b9b887058156d2fa09ef17eb69df05892e92292ab45769416`  
		Last Modified: Fri, 07 Nov 2025 00:41:34 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea106a2badb734bb13e20160f9e12367cd23d8031dba75649b64686cd84ff74`  
		Last Modified: Fri, 07 Nov 2025 00:41:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2681526564ee47d1c3a73d9ff54ab4be0c4d48fec23e0f6f5496939915c06f2`  
		Last Modified: Fri, 07 Nov 2025 00:41:36 GMT  
		Size: 20.6 MB (20643558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:30fedf1efcb3cdf90d1f0d10b908ea002f576644b7adf27312d0382b2bda90f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053fd5f1748d418ac8edc6e59d238386b5086cddf66a6112ad96c67a2a15f0c1`

```dockerfile
```

-	Layers:
	-	`sha256:7eb3a5ea86feeccb915e009a02d7f24e142d93902722c12a1cab540a53074a2f`  
		Last Modified: Fri, 07 Nov 2025 03:00:25 GMT  
		Size: 7.0 MB (7032676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362221a0e00f177a01ca94699507b81dc4ac1cb745cb7b8fa4c4b17f1fca58f9`  
		Last Modified: Fri, 07 Nov 2025 03:00:28 GMT  
		Size: 42.7 KB (42746 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:45f3939e7bdadd63809b3b361d578c8c81edfc480a56d70063ffff256ed0bf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204687500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5948547d4de6548880e2043cdf6b3723e5b3fa861ed03bde948586b774e570a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 02:33:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:34:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:34:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:34:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:34:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:34:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 02:34:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 02:42:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 02:42:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 02:42:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:42:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 02:42:01 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 04:06:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 04:06:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:09:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 04:09:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:09:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 04:09:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 04:09:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 04:09:48 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 04:09:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:09:49 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 04:09:49 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 04:09:49 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 16:16:38 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 16:16:39 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 16:16:39 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 04 Nov 2025 16:16:40 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 16:16:40 GMT
ENV DRUPAL_VERSION=11.2.7
# Tue, 04 Nov 2025 16:16:40 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 04 Nov 2025 16:16:40 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 01:00:13 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 01:00:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2423ff8a5d9e5803ce51c4bee23a305ce775f33ac0e1498c84052d0e8fbeb72c`  
		Last Modified: Tue, 04 Nov 2025 02:40:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d4bf9d38282d902e4e65ff38ac946e13144e841061113ca97aee44f4413c20`  
		Last Modified: Tue, 04 Nov 2025 02:40:57 GMT  
		Size: 103.3 MB (103328858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b331438757ee31483215b6dd106186ef28c3d99b0849f835e85e4cba07a27b`  
		Last Modified: Tue, 04 Nov 2025 02:40:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4f0a77689b5b972d24113ea299100c1a0d18a46a41dd0688dbeec9193dd5c1`  
		Last Modified: Tue, 04 Nov 2025 02:49:44 GMT  
		Size: 21.3 MB (21317849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b992e275af09d1f3142c007faa97121b28d014f4fd52e3fb4d61ab4618c85e2`  
		Last Modified: Tue, 04 Nov 2025 02:49:42 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273cced39343969a12d6439d8b0d6f90309922a8572726a8a55c0f4675362179`  
		Last Modified: Tue, 04 Nov 2025 02:49:42 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4982cc27b13e80b0cc44f36fab1125343d3f7eec068836dfe2118f8b506dfc2`  
		Last Modified: Tue, 04 Nov 2025 04:10:28 GMT  
		Size: 12.7 MB (12720788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458bb4ec1c131c27e40f295e8284d8ce6a99fce001c444d54e5edb6321e0604b`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd709b05d22e451fb5a2854c10314670acd0bd50f609d69fa2c2044efaac60`  
		Last Modified: Tue, 04 Nov 2025 04:10:28 GMT  
		Size: 12.1 MB (12084910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfaad676e33e251c3fa5aae794751cbe32a8721669dbb35a46c4296396ebfab`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315458db3cab64e270e7db49a435fc380ccd93f99d7f6126fdd524300a6b0eda`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b2a147d0211f65d44684937a0d2b99092c9a400075a19eda7d5e464771238`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2570e88d2c102d7f528b7e7352f1658976621a66efa563677954a78188fc5c5b`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565f95f63d2be37c68a93dbd1f644241c1166daaa37bc3b59e0ba7711182c641`  
		Last Modified: Tue, 04 Nov 2025 16:17:42 GMT  
		Size: 1.8 MB (1764826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf563fc6318ed47ed778c920e3550f939d64c8f9252e7a4122462c375f55055`  
		Last Modified: Tue, 04 Nov 2025 16:17:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a582d29eb896e06e0a5f42f175b6e93398755bc3d84b872b6acdd400a8cdda3`  
		Last Modified: Tue, 04 Nov 2025 16:17:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3571df0c8be88c9439ad2e69a97721a3137e963cd06cbf7c5d57a83e585954`  
		Last Modified: Tue, 04 Nov 2025 16:17:43 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62bc14cf9f237c56e4d270b7eb36c4a603023241f990be63a782e80d3486ead`  
		Last Modified: Tue, 04 Nov 2025 16:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a337b063eda1915343af06c1cf2334aff1381728b2e45e21e22ec7d091172dc3`  
		Last Modified: Fri, 07 Nov 2025 01:01:18 GMT  
		Size: 20.6 MB (20643457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:9f46dab9dd012be401212eeda796bb8e69d64e8254b14dc919b0e3b1543baf5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7072615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2758eff8dec3318d200072389fdf568032dc7ba6f58a4d843a1b678428fed821`

```dockerfile
```

-	Layers:
	-	`sha256:547b161a26ef7887fb5f4ac2291d5824178404c2503049a37fcfff7b495be006`  
		Last Modified: Fri, 07 Nov 2025 03:00:35 GMT  
		Size: 7.0 MB (7029764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9334c4f6dc4e972089fb020815eee675fa720115641550fee56b9a23113d13b7`  
		Last Modified: Fri, 07 Nov 2025 03:00:35 GMT  
		Size: 42.9 KB (42851 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:d738671ee814d40bbfbd258416c96c6c3bc09209eb892f16b1f80f78ec130707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174100891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedf6dc422f93f940a3b4e4f9770bebbd68a069dc9bdde77f28d8f8c3faa17c4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:29:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 04 Nov 2025 00:30:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 04 Nov 2025 00:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 04 Nov 2025 00:35:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 04 Nov 2025 00:35:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:35:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_VERSION=8.3.27
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.27.tar.xz.asc
# Tue, 04 Nov 2025 00:35:49 GMT
ENV PHP_SHA256=c15a09a9d199437144ecfef7d712ec4ca5c6820cf34acc24cc8489dd0cee41ba
# Tue, 04 Nov 2025 01:14:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 01:14:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:16:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:16:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:16:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:16:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:16:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:16:49 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 01:16:49 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:16:50 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:16:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:16:50 GMT
CMD ["apache2-foreground"]
# Tue, 04 Nov 2025 10:07:53 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 10:07:53 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 10:07:53 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Tue, 04 Nov 2025 10:07:53 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Nov 2025 19:36:15 GMT
ENV DRUPAL_VERSION=11.2.7
# Thu, 06 Nov 2025 19:36:15 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Nov 2025 19:36:15 GMT
WORKDIR /opt/drupal
# Fri, 07 Nov 2025 00:57:33 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 07 Nov 2025 00:57:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de54dbb81980c9b8d3c221063f25b8474ca2be777ee639ae7b090f0b6933433`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3263ba1b0b7542bbb392f8a89ebf9d5562c8e7a8d05dd575aaae0c51490011e0`  
		Last Modified: Tue, 04 Nov 2025 00:35:33 GMT  
		Size: 80.8 MB (80826218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c66245e37d456fef550ca4136b0b6f8bf79ff609208f0f6a1a952faf0bd6a42`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d886063e6a65a87446dbef8cf7d4ac5e0be955ef53742cbf993f02b0aaaa4e68`  
		Last Modified: Tue, 04 Nov 2025 00:39:58 GMT  
		Size: 19.9 MB (19910158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1e04afbcc9c41c784462e4aac422fef0d41cb802f6e761b7c0b09e2fbf9df`  
		Last Modified: Tue, 04 Nov 2025 00:39:56 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c8df14519eea8fc933faf236a723ee6253b8948a5b7ff5b8e7560685817f5e`  
		Last Modified: Tue, 04 Nov 2025 00:39:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b702a7d559000ba088b8e00418f029ba48556dc9c52530327f93980cd423d16f`  
		Last Modified: Tue, 04 Nov 2025 01:17:17 GMT  
		Size: 12.7 MB (12719487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5bccbc14216b0d681a86a9111b31d5cf9a503d3ac934d79c7d6ddbba871051`  
		Last Modified: Tue, 04 Nov 2025 01:17:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3769090bc78e4992fad0f227c6db17812d4f8dd43481676f43565fb27ea9cbd`  
		Last Modified: Tue, 04 Nov 2025 01:17:16 GMT  
		Size: 10.9 MB (10881580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d242f3795454c5d75763bba00f120f8844eecd729e8022154047711ac9a47f0`  
		Last Modified: Tue, 04 Nov 2025 01:17:14 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be6f89e3366c58a065bcd69b9591f23644df154685bf92adc80daeacee27a24`  
		Last Modified: Tue, 04 Nov 2025 01:17:14 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97be0b4eed89ccf0e1f2786a4585e68bbbe698a3017f0bdd46adda3059654330`  
		Last Modified: Tue, 04 Nov 2025 01:17:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca52666d5ff3df00d4b532583dce7bbb8f314e091574d2c181380af897adf8dc`  
		Last Modified: Tue, 04 Nov 2025 01:17:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf66013c7d405bc56935ff1b6eb55e5f38ac020b40d986e436092aab81866e4`  
		Last Modified: Tue, 04 Nov 2025 10:08:33 GMT  
		Size: 1.5 MB (1477536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd8f7ae21edd8d38c02baf9496ea6acbc390eed2ef129b987494e53c22b9425`  
		Last Modified: Tue, 04 Nov 2025 10:08:32 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965629a683588c0953bfdd7fc619fdb2d51075e130651e5b1f7f6f22c0068c8d`  
		Last Modified: Tue, 04 Nov 2025 10:08:33 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ceb170a5184eb3cc60ceaf3a0bbf9536eb510bf7bdba125ace57bbc9428c36`  
		Last Modified: Tue, 04 Nov 2025 10:08:33 GMT  
		Size: 751.5 KB (751481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8045a99ffa54941f2bbc90802023df61c22a52aae047388079c009469dde20e`  
		Last Modified: Thu, 06 Nov 2025 19:36:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b557db202ed1fefce4864af7da19eca79f3fbf481458f5a185232b80878a93`  
		Last Modified: Fri, 07 Nov 2025 00:58:04 GMT  
		Size: 20.6 MB (20643456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:235f09df04be59de2d7d1913150625e46304cee6d0de0cf9586589f213452e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6932914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2895c83b8b55be2de330408bf9394bb3e39c17c16d702ab67d6b179016763a9c`

```dockerfile
```

-	Layers:
	-	`sha256:47238771680d79c758619f00824338ddebbddccee4235797c3cb0a8678942f37`  
		Last Modified: Fri, 07 Nov 2025 03:00:42 GMT  
		Size: 6.9 MB (6890130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a769d26a64c5707a34def3f3996a72662afe4f2933f8f4a530d12cf30913d`  
		Last Modified: Fri, 07 Nov 2025 03:00:43 GMT  
		Size: 42.8 KB (42784 bytes)  
		MIME: application/vnd.in-toto+json
