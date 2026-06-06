## `drupal:11-apache`

```console
$ docker pull drupal@sha256:e3a4b1ee4355a1778526df3684394132586f75adf7e1ae159a372b06e21bb7e3
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

### `drupal:11-apache` - linux; amd64

```console
$ docker pull drupal@sha256:26a167c586f18783a0fd6f1c315f1c54f06da769694b1f2e3e44b958cd907035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.3 MB (203304128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba577893d1e9fc7b705b6b73c82f94f3fd1d14d7c6e1e798a3137a421f32e774`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:39:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:21 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:26 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:41:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:41:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:41:57 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:41:57 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:41:57 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:13:41 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:13:41 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:13:41 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:13:41 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:13:41 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:13:41 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:13:41 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:13:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:13:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa2f07689a8ad2be828279559aee2d6217b59dce1c72812d9f1f99c46e83e3`  
		Last Modified: Fri, 05 Jun 2026 22:42:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00af46a6fb8d65b4c2cd5136c18b998028dbdb4724e88728a803eaf1d9bbecb`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 117.8 MB (117839883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ed921f0d21f57b3c511330dfafa30f7a598848ad987b6efd843aec0a6def0`  
		Last Modified: Fri, 05 Jun 2026 22:42:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ede3a51c79f8280b31d50617fad94e5e2f3990fba30ffc8bfe32d5236c2dd7`  
		Last Modified: Fri, 05 Jun 2026 22:42:17 GMT  
		Size: 4.2 MB (4227864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223b96e16b4976bf5a9ad173107c1f4b197c6f8a90e0c76ac31b0c05c3588a6`  
		Last Modified: Fri, 05 Jun 2026 22:42:18 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0253b1139356babd7b596fbd44778193a283e0ea1529839ce01ad00d846e7a38`  
		Last Modified: Fri, 05 Jun 2026 22:42:18 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3166beeb233be6875c4147cc838995077dceb1627063e0c253b76be1a852d96e`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 13.9 MB (13898678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405a149b5346b0287a179a63ded29b93cc303c6e4da9df237aa5f7663a3831b8`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba30ea08bda1a4cc3213719a634028d2fcec91aa30b2ec9e4c619720fc155ba`  
		Last Modified: Fri, 05 Jun 2026 22:42:20 GMT  
		Size: 13.7 MB (13691044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7806628a945adad88843f81e60ea823b6eb8acb6e29bda1b00268f1a7fca51c9`  
		Last Modified: Fri, 05 Jun 2026 22:42:21 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6df911884cbfe0001ee99fb42df5721698c99e8dd5bb1af062bdd520fed721`  
		Last Modified: Fri, 05 Jun 2026 22:42:21 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac6491fcdfec5ee6a149377ee56ef4a2ba5622d8bab357ef5badbd58e1df1dc`  
		Last Modified: Fri, 05 Jun 2026 22:42:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d0b50770cf8181da2166dd5de8426248951e3f11b385c311a0c1a5124a076e`  
		Last Modified: Fri, 05 Jun 2026 22:42:22 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d466c14b02a76f1ff6c6746e39e5a606e806c2d16a3a2e2bc32ab10bdd18f7ff`  
		Last Modified: Sat, 06 Jun 2026 00:14:05 GMT  
		Size: 1.7 MB (1658956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a3f81631539ea26d8415e71e3774590c893667aae1fa7c2e57642bf09690ba`  
		Last Modified: Sat, 06 Jun 2026 00:14:06 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f6e1d584cfd494d074f39c5fa3f751d971e340a9d7bdd6f5a9e57c1af202ab`  
		Last Modified: Sat, 06 Jun 2026 00:14:05 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a366801b9a413d9a80afd22da4b1adf608b9f79acd7a1f92365f05ce7eb4f2d`  
		Last Modified: Sat, 06 Jun 2026 00:14:05 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ca1bf38cf24fd604105796342b6e94859d57b1b27e50d77f1b8e0d59666a35`  
		Last Modified: Sat, 06 Jun 2026 00:14:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889b6c406aa1da6f460540de30e0ed1dc56e1273581db6d74c1f8114240f7da6`  
		Last Modified: Sat, 06 Jun 2026 00:14:07 GMT  
		Size: 21.4 MB (21378031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:7e52ff9ed0a527cc82582c2f34d118b71165d4ce7e29706bc01637869c3d033a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73288bb86cb078af198cc581726415ed4cbcc2e83588486095d226b0323ec44`

```dockerfile
```

-	Layers:
	-	`sha256:61e9386a08e1d7c7a771c3a207d7fa6eea7329c5e8e2488f0b4f8c90f6336d26`  
		Last Modified: Sat, 06 Jun 2026 00:14:05 GMT  
		Size: 7.3 MB (7342511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc682a0c4d1c8066f8576c64d26a0aaeb24ede1ca90114a22efe1f37654c3428`  
		Last Modified: Sat, 06 Jun 2026 00:14:04 GMT  
		Size: 48.8 KB (48799 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:4d051cda8ae01f03eed2f8d34327cefece2b2bd1c7c3a0b9b45a48f7938fd493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165406394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd87028a66fdd83f749898d408b9422cc7586bc9dac223f7944272f96c50d39`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:39:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:28 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:36 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:36 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:47 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:48 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:48 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:15:27 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:15:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:15:27 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:15:27 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:15:27 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:15:27 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:15:27 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:15:40 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:15:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef49eb4129cb389ab49a4d1edb009a8397667aa1a5a5a25c5fe09d2555c0e4fc`  
		Last Modified: Fri, 05 Jun 2026 22:42:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6367a2b5c37154791cd30e344f8752ad05592a3f102084d184ac119bc6d7950b`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 86.3 MB (86256157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9309e35ce84e354961e3afd02de3a72f241f3b1460a323eda422c15b695543`  
		Last Modified: Fri, 05 Jun 2026 22:43:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0d964487f564b6dfeadb20c5fff09fe1df38a6c9d46fd37ad133bf8918e53f`  
		Last Modified: Fri, 05 Jun 2026 22:43:05 GMT  
		Size: 3.8 MB (3756685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c06cdcd530eb203db34b94a8afd9932168fbae523ea2c6e8a8ce886a4af733`  
		Last Modified: Fri, 05 Jun 2026 22:43:06 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113509df834836f0475b5a2f2e19589fa95bfe00c206ca57094305cc15bf8c32`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6f4de93d6be1c989b55a76daea334c3fcb1409d7fd9438d45d45579a94b744`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 13.9 MB (13896005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e4225a6ba24de6db35f1b12a6e46e90302e7d5ccab0c77dbeb54901ef6d6c8`  
		Last Modified: Fri, 05 Jun 2026 22:43:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45aa4ee8f5c467421c32a6e5a246f174accf76c226b5069e7d63b5d8f61f19`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 11.7 MB (11712268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f495d0bfbc535f696d03f3c519b27abeb5ecb8c8bfdf3329ae9da3bb9e42f302`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93caf799ddda63f51f7a21efea228ee1dfbdca9b9ae13fc553bfcb0d000ce346`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459f7a2eb197aef2c8c84366628a0402c16e3aaf4e09486cb0c05a5658f89287`  
		Last Modified: Fri, 05 Jun 2026 22:43:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f37676ccdb442a364c69c9d8896b4f91526107a0d6e4b649a158fc6bfd0160`  
		Last Modified: Fri, 05 Jun 2026 22:43:09 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01a3e546f01dd8c74cfefacff5498b6e245f001c464b43cc8ebc660201029e`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 1.4 MB (1371533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacea3548f59a075cb0b211d8ca12518e57d1e5b6a2cdbf14bb3d05b4cc9588a`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ce8e27711943f48c4c5081d9efb1ea3353f0049d0204cb6e263f5b4a7d9eca`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ea51d74d7b9dfe6a492cf9c394bc724ab9c9dd08ec6195c7929c0f6029179f`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b543ce01d9a5b1cc271a7b981fa55767a0ab595067c4e5d6997cf1602375c9`  
		Last Modified: Sat, 06 Jun 2026 00:15:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac3cc8dc69e6a0efdfdde83fb67d200b3dbaf8205c06bfd347788f8692fd8e7`  
		Last Modified: Sat, 06 Jun 2026 00:15:59 GMT  
		Size: 21.4 MB (21378146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:10c13e3d1034558a6da68c0298c22b18edea6dadd564bf045e6b5a87f2209ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7195614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385aecb229d3d3a2c527e62cb8b7a3a8f009e3e1911311c8cbbccdc22df9f746`

```dockerfile
```

-	Layers:
	-	`sha256:931502937c9921dff84b603b0036d4e502196e546857b7d729dd51efafbcaa9e`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 7.1 MB (7146520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb47a2b0ac870892e2242361ade1ddeeaadf4e325d10d482494686332fee884`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 49.1 KB (49094 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:61bedddb5ac20afad8708ac35ae8aee5571fdc749a303c36f7f570f5f706b02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195679430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3453328939e30a440196c62199a4f543d1c32cd3f2da2dd7b9cc7ff509b445df`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:38:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:38 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:38 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:38 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:38 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:13:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:13:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:13:24 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:13:24 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:13:24 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:13:24 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:13:24 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:13:30 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:13:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ca734afc06998cc4f469d46d7ea72ebe993b64300582fa19dadf760777d16`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59526dcf80a0c0a7c37013ed0742cbfd2896a4817db99f2bf2a4c5de829dacb9`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 110.2 MB (110169134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0476155b25748c07c80dae6490653f5e448ceec83aca078540f2a445829b1c7`  
		Last Modified: Fri, 05 Jun 2026 22:42:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7e4e26cbc5e7ec40f197b561c548d521ad703e9c12dca6ced20f8c1b64273`  
		Last Modified: Fri, 05 Jun 2026 22:43:00 GMT  
		Size: 4.3 MB (4308172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7aed88e2e78ce24c3af427e303d304b2f871abdef109566e0d94a32b91ec8a6`  
		Last Modified: Fri, 05 Jun 2026 22:42:59 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0812317ab085f405383e23b0f3d4ecc4929ef770fca793631e3be7e94f600`  
		Last Modified: Fri, 05 Jun 2026 22:43:00 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2b825dc1b8409e1bd52d7a3b3eb1a9b371a6ff431a86b8244e717bb4ea13bc`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 13.9 MB (13898308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b323b6ea7172ef2c98c5d34dc925223748bf5bcc4fb844939e9b4e229ef517c2`  
		Last Modified: Fri, 05 Jun 2026 22:43:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0c91725ddc70a56d006a136b82bc420ea438a86760ff5697a6843df5090c49`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 13.3 MB (13338628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f79777aa9c5694485f0fd5c66481eb57912a5d866cb94b83c1dbc3c7ac36d81`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b2d572ceebb95ceafc03d938614476c4d6dc4b6b6269174f7df9f271ae4c1`  
		Last Modified: Fri, 05 Jun 2026 22:43:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3a4c5525c34dcb8f795daa01a06232d5a8ec5744f7ea32a24a680bd37dd97`  
		Last Modified: Fri, 05 Jun 2026 22:43:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c81cd241d73959c6db6cec284b640d26831e691013fa670935c5d93f4f9bea2`  
		Last Modified: Fri, 05 Jun 2026 22:43:03 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0297b1e427e84c59e5f57ade9066c22a25bb10bf99ea77a2aff53e80612b1a8c`  
		Last Modified: Sat, 06 Jun 2026 00:13:49 GMT  
		Size: 1.6 MB (1615424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b910bee772506a566780a75ac52e9ad3480aebcc030955c611b553199d88d299`  
		Last Modified: Sat, 06 Jun 2026 00:13:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6908dd6fc9976975d13a9dcbf43444dbfb0b4c83bfce989f644c10faf6a0789d`  
		Last Modified: Sat, 06 Jun 2026 00:13:49 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d8b5f1ecef73d9973edb6b447ff731edf21bc7bf9b26513cbba3f57879ce68`  
		Last Modified: Sat, 06 Jun 2026 00:13:49 GMT  
		Size: 823.3 KB (823344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82daa8b7085f57b45fc04e321020a9bec16c7e1bcd44f092e9b7bff642fdca73`  
		Last Modified: Sat, 06 Jun 2026 00:13:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b99820d5ab22c63d8275d8d3649a8a3d9fd1f0764a89a90c9d831a14041cf5`  
		Last Modified: Sat, 06 Jun 2026 00:13:51 GMT  
		Size: 21.4 MB (21378076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:efec9d4d141c2915660ed2ab353b2fa5cd545ee09ddcc65d1b351ca4080ce999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44061dfc34844209fcef04f2cfbec92ccb54da48b6f5c9255189ec8295bb9c`

```dockerfile
```

-	Layers:
	-	`sha256:fa86a42d161654e24f4a9418b1f5eaf9a21822419415be33e2ff311efb0e5686`  
		Last Modified: Sat, 06 Jun 2026 00:13:49 GMT  
		Size: 7.4 MB (7440045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f17cea194b914aba3ea175a14d354b1de89d69bc656c9dba262f9651c8a2e10`  
		Last Modified: Sat, 06 Jun 2026 00:13:49 GMT  
		Size: 49.2 KB (49215 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; 386

```console
$ docker pull drupal@sha256:c158e720aad885f596eb43703fc5082e0aa73f2597cb25593ee1ebfef7e365c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.7 MB (203728377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596bb2eecb475edf370a44743031674141ad0530e293d6455d7dd679c9650ca3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Fri, 05 Jun 2026 22:38:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 05 Jun 2026 22:39:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jun 2026 22:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 05 Jun 2026 22:39:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jun 2026 22:39:15 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jun 2026 22:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:21 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:39:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:07 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:07 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:07 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:07 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:13:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:13:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:13:22 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:13:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:13:22 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:13:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:13:22 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:13:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:13:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ca734afc06998cc4f469d46d7ea72ebe993b64300582fa19dadf760777d16`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d740fa7e6837d80b1e04704f9c826afb84614d0ae758f8904665acd449aafe3`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 116.1 MB (116142193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da462e12d196369d393599d669ddfb1524d415a8d36fb2ce1390b2f05e46f343`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4602c55c0f71750b4b8a70c5ac33b7372b06f1754c15a97b1db5720faaf2f6d8`  
		Last Modified: Fri, 05 Jun 2026 22:42:26 GMT  
		Size: 4.5 MB (4459159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef107ef7934abace6976310ecdfe9596971080576c11a4e885cbcb201b7cec50`  
		Last Modified: Fri, 05 Jun 2026 22:42:27 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d64c752c2c00bc0341d336eb708f0edb8577f364587e49b997637be91f51863`  
		Last Modified: Fri, 05 Jun 2026 22:42:27 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf8cad72ee668d3bc49d93323d01860360678ab389d9ebd57706a0b1d5a27eb`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 13.9 MB (13897515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2363aa8225c0535ea2d19e7c744a722c019e5e7577aa677c90aaac99bbf44c6`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc5078b97fdabfb77ccc5a379fddf75f58e181f8094a06d5adca56f45c1d55`  
		Last Modified: Fri, 05 Jun 2026 22:42:28 GMT  
		Size: 14.0 MB (13988055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a60493158bff33ed907925f5b7516f927a9bc4af4c1cad7a28a80ae463ee73`  
		Last Modified: Fri, 05 Jun 2026 22:42:29 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d8f67303c7306033e175897c5840ef369f3d0437d3f32e7a0138b24c6295d7`  
		Last Modified: Fri, 05 Jun 2026 22:42:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3512886fadf9d7fbc67b7f5289e56439af41d1755a7db5829b053cc2993ca7`  
		Last Modified: Fri, 05 Jun 2026 22:42:30 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464ea7db1775cb7c4c2379aff6ef7528001daafb896c2e2d88e622766c192d4`  
		Last Modified: Fri, 05 Jun 2026 22:42:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08254e245c5a66842ac8d1a5ce71f19ae2cb60f8a076bd27744d7cf5e296561`  
		Last Modified: Sat, 06 Jun 2026 00:13:51 GMT  
		Size: 1.7 MB (1738296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efe9e78e396c5a2cd979d072cbeba39a64dc4ee23e1ce25632885c1358c3f40`  
		Last Modified: Sat, 06 Jun 2026 00:13:51 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4920f0b739274c7b5f39a989e69f04eec74ccb1c7d8cf1601f9fc3ed68d0e2f`  
		Last Modified: Sat, 06 Jun 2026 00:13:51 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45b83d321d85ab2e35cc85abe6520450e1d68397eef4007bd31347e1794763`  
		Last Modified: Sat, 06 Jun 2026 00:13:52 GMT  
		Size: 823.3 KB (823339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2a0a4c833bb1ca43bd9be717086feddfe680fa7195457641f5d8fecfb7a4d8`  
		Last Modified: Sat, 06 Jun 2026 00:13:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bb5e3ee72e0ad6a474189ec8331853f29827407a5a36a735c9a6c90c0a3d96`  
		Last Modified: Sat, 06 Jun 2026 00:13:54 GMT  
		Size: 21.4 MB (21378074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:c95d1c5aff097826d6d5cafc92e051ae5300968e653dbdbb24a4c3addbc94aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b77ef0f3a73ae5c892ed730b9a1cfd69ba9136ffba054becf2ad999d4daf75`

```dockerfile
```

-	Layers:
	-	`sha256:ba10e910245a842950a54f8f8dca1d28244ac7795945c96d16d2c6f0bb1b837d`  
		Last Modified: Sat, 06 Jun 2026 00:13:51 GMT  
		Size: 7.3 MB (7316263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7806e83d1f22ea81ada04396bb6be11ab94e818ae65b9bfc8d5259615088b764`  
		Last Modified: Sat, 06 Jun 2026 00:13:51 GMT  
		Size: 48.7 KB (48655 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:a4755fd5f7e72f51cc39aed6a0b0583d63e4a9162c2c77e5de974073ae936c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (200985069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bcae10595c7e48983339c4ba3e4345e4e7e95ff50abee43e2ca2d536090139`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:26:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:26:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:26:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:29:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:29:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:29:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_VERSION=8.4.22
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Tue, 19 May 2026 23:29:19 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:38:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:38:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:43:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:43:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:43:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:43:51 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:43:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:43:51 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:21:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:21:52 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:21:52 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:21:52 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:21:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:21:52 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:22:08 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:22:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b651a003498bd50572d1189161afddcb900241800cb6d5d0bd7a8ce4500633e3`  
		Last Modified: Tue, 19 May 2026 23:31:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd8ec5f6bfff3150dfdb7f9ba59b5b8bbd45b012ab504b03e5eb22da1815753`  
		Last Modified: Tue, 19 May 2026 23:31:29 GMT  
		Size: 109.6 MB (109598335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c429ba9d511a0b12b2e87806d0728dcd1c7b4dcadf247dfaf38502d93c30cd5e`  
		Last Modified: Tue, 19 May 2026 23:31:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0111aa5024092ef6e35218a2a5c87fabbd8071beebd70c36829523f28c0d71b2`  
		Last Modified: Tue, 19 May 2026 23:34:38 GMT  
		Size: 4.9 MB (4883387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bd5ecf3703d3e85307529fda185e272f3b0c333f01de176345c03f9489ac78`  
		Last Modified: Tue, 19 May 2026 23:34:38 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa5d27bd8a219cd7f3cc53de0c430d125200a13be2bd7468c706ac1923bcc7`  
		Last Modified: Tue, 19 May 2026 23:34:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2e5f6a80b46b08a6e4c44005092a44282dd4f852c4e75710a8baad958376a7`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 13.9 MB (13913049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb74339744d2bb31e8fa8a58dfdee161ffc46c70022a1056a126d980b8acb39`  
		Last Modified: Fri, 05 Jun 2026 22:44:13 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d4f87f2add2b3569b179f01fa8ab12367c102f8de4fcd9da9b2ad095625f3`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 14.9 MB (14933963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b576e37457d6a6a9446c9126a625daaa8b4a7a0607c626bdce9ab3c4ced30`  
		Last Modified: Fri, 05 Jun 2026 22:44:13 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f65c0f891b405eadf31d0b9a99fb78dd88c97ae9d31d3219797d54df73900b`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7e88062b15a9aebc5978fcad77bf0e1f72a4e49e54fffbebbab76822269a1`  
		Last Modified: Fri, 05 Jun 2026 22:44:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c010a08a8429ebefb875f77de8d5332019ecee75ce7d7ad84188956471d3761d`  
		Last Modified: Fri, 05 Jun 2026 22:44:15 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3404419580307ce1dfbbbbfbfe2779bce935ebf6019b12be513bb7edec68c02b`  
		Last Modified: Sat, 06 Jun 2026 00:23:01 GMT  
		Size: 1.8 MB (1848049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea8e6583c773b68c02e289087b6cc8ee932a17e5bd219c6d7faa853892dbc5`  
		Last Modified: Sat, 06 Jun 2026 00:23:01 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4573575bd084604d5a61a7dcf9470c2310ef181c53052f801eb20c7113b2d472`  
		Last Modified: Sat, 06 Jun 2026 00:23:01 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18891219988a5233187a1641a9b4dab0d9292e92fbb20b621eb355bed267f8d`  
		Last Modified: Sat, 06 Jun 2026 00:23:01 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40737e19d178c2dab94ad45b43858d147073fe3f3b922b53ed906ad50bfe801e`  
		Last Modified: Sat, 06 Jun 2026 00:23:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa31641e09286c9b0693fefb4b497653f5059e4f030ebd68fb7107b6ead7add`  
		Last Modified: Sat, 06 Jun 2026 00:23:03 GMT  
		Size: 21.4 MB (21378046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:dc18335af26b5915625324fa57732732bec5e50391170dda7346f97d2b35674a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bed4260336358367fd3542a072520a0632ae6ea000aefc1359bd2678d5fba1a`

```dockerfile
```

-	Layers:
	-	`sha256:a0af2c6ced19793f1265108f4f0a24cdc9b837d5abe50b5a262d7239576920b9`  
		Last Modified: Sat, 06 Jun 2026 00:23:01 GMT  
		Size: 7.3 MB (7342456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe437db08c5f44bfd9a45ddd04fe08008dea8ac6432497b72e3433364a457d64`  
		Last Modified: Sat, 06 Jun 2026 00:23:00 GMT  
		Size: 49.0 KB (48980 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; riscv64

```console
$ docker pull drupal@sha256:85daaebcffcf4676d26dadc6ad2ccd5a5110ee0d8a9481b24c1ae519794f10e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230434256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2089d1293edc5d74924ba39bece7edd347ef4f110cef28db049c8d1829bb228e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 11:59:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 May 2026 12:01:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 May 2026 12:01:47 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 May 2026 13:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 May 2026 13:07:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 May 2026 13:07:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 May 2026 13:07:18 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_VERSION=8.4.22
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Wed, 20 May 2026 13:07:18 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 23:39:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 23:39:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:34:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 06 Jun 2026 00:34:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:34:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 06 Jun 2026 00:34:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 06 Jun 2026 00:34:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jun 2026 00:34:05 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jun 2026 00:34:06 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:34:06 GMT
WORKDIR /var/www/html
# Sat, 06 Jun 2026 00:34:06 GMT
EXPOSE map[80/tcp:{}]
# Sat, 06 Jun 2026 00:34:06 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 14:21:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 14:21:52 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 14:21:52 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 14:21:52 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 14:21:53 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 14:21:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 14:21:53 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 14:22:37 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 14:22:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3f1ce6bdb422619d5f28f3d354ac88efadf525446aa4cc0a2cf6d208358da0`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2278d8aba6744e8388864d93d2ccd060b4b5b706da0855420292afc7562eef8`  
		Last Modified: Wed, 20 May 2026 13:05:36 GMT  
		Size: 146.6 MB (146584901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f680f6a3aa4a44306703b8a92e46d186729d6e1435771fbfda06e18de5ebcc5`  
		Last Modified: Wed, 20 May 2026 13:05:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887cf26ec25a917a3969775023d91d64e52e0fc30b0f1e2c5a326ce664b36942`  
		Last Modified: Wed, 20 May 2026 14:08:12 GMT  
		Size: 4.0 MB (4031581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e116995318a8f16f6dd281e40820dba3f5cec3ccbf8b001b5f77cc47621731c`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c0690c9ca74d867f3cd4b9dd3884b132b21d1a7e60c2dfcd33fecaa0fb76f`  
		Last Modified: Wed, 20 May 2026 14:08:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7a69052f93439401ee9adcedc5320aef0c13722b845369517295bd31611a7`  
		Last Modified: Sat, 06 Jun 2026 00:37:17 GMT  
		Size: 13.9 MB (13913045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68a248916ccb178799c1313c3d1ea27736ea8b52a4d4f6513c0b19a3e7e64a`  
		Last Modified: Sat, 06 Jun 2026 00:37:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4949ded7197465efa8e4b8b7a0f131f2e4eccdd315689aaa8dfef3bf6f9794c1`  
		Last Modified: Sat, 06 Jun 2026 00:37:17 GMT  
		Size: 13.8 MB (13843863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b72ac70c5be3c7bd296791af3f3ba8cdd66f384960c921b23847d951492c23`  
		Last Modified: Sat, 06 Jun 2026 00:37:13 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2a4aa8bd5133f46b99cf7aa1043d06f0c1e7b3e350c805575371d0dec2f38f`  
		Last Modified: Sat, 06 Jun 2026 00:37:15 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fbf081147678681ff6439b820cb5c59a07faa9973bd7e49d59da912361e3f9`  
		Last Modified: Sat, 06 Jun 2026 00:37:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c55a722ce1b1a8a539a10faddc8d92f856f1c510a433e44b6fe773b24e46f4`  
		Last Modified: Sat, 06 Jun 2026 00:37:17 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d9e5e07b8cc7ed571d68bf9c001f63ca69c2c2735f130e8444dd9239ac691d`  
		Last Modified: Sat, 06 Jun 2026 14:27:17 GMT  
		Size: 1.6 MB (1575466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee88b221d1d38b07e72343f616f1f3bed3d89c1451177fa4f6930e346ae8058`  
		Last Modified: Sat, 06 Jun 2026 14:27:17 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c7cad332576f4de97d8903b350f295bebe29815f9a91c5f68bb6a8eb28492d`  
		Last Modified: Sat, 06 Jun 2026 14:27:17 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2187a6c7af9e9e489e27514a01dc81790db180d65cb2a4df323c202696a34f14`  
		Last Modified: Sat, 06 Jun 2026 14:27:17 GMT  
		Size: 823.3 KB (823346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11af2c4b8b6c1d3301c89156541f3a06e806e63ccc2e363bdc4ed65518f5791`  
		Last Modified: Sat, 06 Jun 2026 14:27:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f9fa7ea50faf98b5814adc9531a0e13677173b5d7706841e5dc6a6339dcf0`  
		Last Modified: Sat, 06 Jun 2026 14:27:21 GMT  
		Size: 21.4 MB (21378009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:ef902d5e4acf42d15a1485d86feb2a0473a4b27b4fbadfbd7b712e171f93b41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daad7c15aa8d67a6a2959f58d0d697ec51624b939c9d3409164cab56aa070aa`

```dockerfile
```

-	Layers:
	-	`sha256:5a25883e32ca636632937daf5c88f4fb3a5d960bcd43254c4027093a84de5bed`  
		Last Modified: Sat, 06 Jun 2026 14:27:17 GMT  
		Size: 7.4 MB (7414453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acafa9c49c5e7bd091b5efb5c107c92b22ce4bbde6dbf495b78e52f012fcffa3`  
		Last Modified: Sat, 06 Jun 2026 14:27:16 GMT  
		Size: 49.0 KB (48980 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; s390x

```console
$ docker pull drupal@sha256:7948eb5468f447a2b4dbaa0b1188f6736a92f00f7e3c8a02719ce4846a220a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178737713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967d2bcd32c7d7c06f6b8fee6faba01141e3d08328b5653e7a70216cc95a36b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 May 2026 23:02:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 May 2026 23:02:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:02:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 May 2026 23:02:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 May 2026 23:02:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 May 2026 23:02:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 May 2026 23:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 May 2026 23:15:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 May 2026 23:15:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 May 2026 23:15:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_VERSION=8.4.22
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Tue, 19 May 2026 23:15:45 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:38:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 05 Jun 2026 22:38:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:24 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jun 2026 22:42:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:24 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Jun 2026 22:42:24 GMT
CMD ["apache2-foreground"]
# Sat, 06 Jun 2026 00:14:50 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:14:50 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:14:50 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:14:50 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:14:50 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:14:50 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:14:50 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:15:02 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:15:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1087ace6d8a95de6d5ba6626cddbda1ecb704acfedcab9fc24bbddaeebaa5b09`  
		Last Modified: Tue, 19 May 2026 23:06:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513d8548dfe51b95cc99361a5b774bcb84552bc0e57dcd5972f102b817050b1e`  
		Last Modified: Tue, 19 May 2026 23:06:08 GMT  
		Size: 92.6 MB (92572581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368b4298afa76b8d0d3fe67adad21cd322ad1fbe8cafe7a6fc389402a64f720c`  
		Last Modified: Tue, 19 May 2026 23:06:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69802b23e76e35fbdb804fc768929bb7d0d9730c1794074087914838e039dfb1`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 4.3 MB (4331254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf14ea595e215f29b109496dcba14ac0984ae8902bfa7af6f9b156c5e218e59b`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33986b7717407e319d3f2841bc991f0b444cff0b2b8bda61be7f014154d2484c`  
		Last Modified: Tue, 19 May 2026 23:20:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f7bdd7c348c1336403029eb24b4cfc6bf726014f960bbd6847e29db809a653`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 13.9 MB (13912253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69e778f7c4eedf2dd20c9aaaed9f625ea8391ea137a2c2b0a3352d696a251d2`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517bd214162a1a413f7f554c5e033938dfaac9f902869f3ba9b03dc61063fb04`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 14.2 MB (14191079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ed4de46510d84a3eaf6ee8c58e8a0b9925a4e11c80ccf3f29887b0273bbf64`  
		Last Modified: Fri, 05 Jun 2026 22:42:43 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7027dbaa21b5515fda4679f8104c88eef9a35c26bdedd7fe7f3f03ce21c8cdf3`  
		Last Modified: Fri, 05 Jun 2026 22:42:44 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a662bae0eb4d9b3d9349d22d5cbf4806f3b6313bd0e4325dd7005f1e6567df59`  
		Last Modified: Fri, 05 Jun 2026 22:42:44 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8027a1444fda70b3209fd01700201147af1fcc1eae4a15b5014a2c09468a2f`  
		Last Modified: Fri, 05 Jun 2026 22:42:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8f8d8fb4059a246b1a78cf1699169da4f1aa8681792b8c1e9cf7086d882f43`  
		Last Modified: Sat, 06 Jun 2026 00:15:28 GMT  
		Size: 1.7 MB (1676781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c499346d6c7ff26f3badd0e0c93a764b9722cb55f19ff430bafe733c93020c`  
		Last Modified: Sat, 06 Jun 2026 00:15:27 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf0c50db802adc1f7227542fca36582078377c82a5a99383eec979ae882fcb9`  
		Last Modified: Sat, 06 Jun 2026 00:15:27 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247d34a5cfc3c065a6abbc436f7d3fd1eda887d8940860a2af884fe1b4601f99`  
		Last Modified: Sat, 06 Jun 2026 00:15:27 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1603f1026280099bd79403fed74bb170d973d5f1d5918f1658d3b4cf4410a187`  
		Last Modified: Sat, 06 Jun 2026 00:15:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa145fbef309c3eaaa2d4386bdeb1a6d1cb5d9907072ee485c530ce8a3772804`  
		Last Modified: Sat, 06 Jun 2026 00:15:29 GMT  
		Size: 21.4 MB (21378063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:110708c169d97603836ab5b1ec37e2d2a2aab77ef7026a75ea7d850af3d94a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8034fe89c4ea5bad2fe3eec2822e0eaab0756ccdafd2ae2a55eae7ae82d628c2`

```dockerfile
```

-	Layers:
	-	`sha256:eb6b5ae941fa7fb0e026f644850c6149cbb89eebe215c215532eca308de22852`  
		Last Modified: Sat, 06 Jun 2026 00:15:27 GMT  
		Size: 7.2 MB (7159761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dab06af91d15775b659bb71c5097ce7aa478c330b0c9658ac94f77740ed790d`  
		Last Modified: Sat, 06 Jun 2026 00:15:27 GMT  
		Size: 48.8 KB (48793 bytes)  
		MIME: application/vnd.in-toto+json
