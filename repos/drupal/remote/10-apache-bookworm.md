## `drupal:10-apache-bookworm`

```console
$ docker pull drupal@sha256:77b8617723293cb60f49dddb4db215187094b6c41bde97679235fe6a1778b867
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

### `drupal:10-apache-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:ff6052b32edad44049aa3d683367dc1a8821b044719dd3e8382ed96701b204c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201212502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54205fec73a5e01354cba9f0d66080a3074f7ad9672e79f7c9fa10a86518fa66`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e004e38cd923e1e05927f28863da55672f2765a6c354ffeaf1aac61fddd950`  
		Last Modified: Tue, 14 Jan 2025 02:33:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0335640eef2cdbb512bd83dca7eb9bcffd9d2e2639583384f7e3d81d819434`  
		Last Modified: Tue, 14 Jan 2025 02:33:27 GMT  
		Size: 104.3 MB (104345447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9228f3fa46c10a3a1eee49639e1d97125655453d5e8c2a042527a9a980022202`  
		Last Modified: Tue, 14 Jan 2025 02:33:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d4a5a93692eba2e8d66dec3d5095cfcec86714313aeeab55a2adc7f3b9b561`  
		Last Modified: Tue, 14 Jan 2025 02:33:24 GMT  
		Size: 20.1 MB (20123730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ddef6aec1821efe140671be155ec4d4d85c19dbd0c622fa19a42fa9b9aa5a1`  
		Last Modified: Tue, 14 Jan 2025 02:33:24 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37b14f2c9cdd4f964e93a22a35e8d51502e4b9c55d5744bf8221a040c8a03e`  
		Last Modified: Tue, 14 Jan 2025 02:33:24 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a2b56ba197e0b67a94e653d913445e1eba3d4b427aa8054dcf2c526c57d097`  
		Last Modified: Tue, 14 Jan 2025 02:33:26 GMT  
		Size: 12.7 MB (12653151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c436b244b8d28def78b05796883b5f523e7fa565a19da8726dcf17418708d1`  
		Last Modified: Tue, 14 Jan 2025 02:33:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ef6ef33f8bc47b5efd65a524dce6280a9fae07083be14761cb799941ad841d`  
		Last Modified: Tue, 14 Jan 2025 02:33:26 GMT  
		Size: 11.7 MB (11652465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe7fe859d09012ab92706dc5db2e143387f0be2f1737eefaf2aa33e0b143b2`  
		Last Modified: Tue, 14 Jan 2025 02:33:26 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbe234e29095a38e267e15befd51391a61ebd68a04441bdf4b3a90f4b3bcbf5`  
		Last Modified: Tue, 14 Jan 2025 02:33:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2f883095aaa1107121693d7419a7df9d6fbafc03601e599540f287ca96065e`  
		Last Modified: Tue, 14 Jan 2025 02:33:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9564c8b235a6311ac553e56f25364e08ab82c7ea094de1a9597fff2b810a6b73`  
		Last Modified: Tue, 14 Jan 2025 03:22:22 GMT  
		Size: 2.0 MB (1999791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3a15b32cd4b38f28f210dcb9c60750a2ca665febda2c7789a1c3665a4688e5`  
		Last Modified: Tue, 14 Jan 2025 03:22:22 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097b5a25684f47551aed5a7c4903700fd04407bb917106fe053527532d1d112`  
		Last Modified: Tue, 14 Jan 2025 03:22:22 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78cbad28261ae2a0a8bf85ba0b6ed18e38b6c25bf3ea737fa660da151731f7`  
		Last Modified: Tue, 14 Jan 2025 03:22:22 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694a9cf389ecac9f872dc3f393b0a4c838accd42f335e67e7743ef5d7ee3d57b`  
		Last Modified: Tue, 14 Jan 2025 03:22:23 GMT  
		Size: 21.5 MB (21477361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:11386f746ad9f31c89785431eb24f883e1ac8eb8bb82087eb7bfc8c01c7fc9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6892173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22277daafd98340ca2c1b26d16083641ac57d048fb467222f17e30302b92105`

```dockerfile
```

-	Layers:
	-	`sha256:6f01c445b252f284a2496d5781668dea63876d532ea1fbf47a42c67b23d9dafe`  
		Last Modified: Tue, 14 Jan 2025 03:22:22 GMT  
		Size: 6.9 MB (6851131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9aadffc3553d9855ca045d30a9e41cea3e2702326d935a207beb16ef2444130`  
		Last Modified: Tue, 14 Jan 2025 03:22:21 GMT  
		Size: 41.0 KB (41042 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:9419232a1811461affbf1e13dbf235b5a4d26b3f12afea6af57c21f637a1b850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (165032997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50f7ad29041786641341c2602a35b44fdceccf35219d4aeecaeecab1df696bb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f371487cffce8356bcfafa73641fa9f2323f8772bee294bab86eafd60098c3fa`  
		Last Modified: Tue, 24 Dec 2024 22:46:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4642677cc143257aa73de7964d6b5cc5b6060d2a6edb9a5ddd3be8f1945443b`  
		Last Modified: Tue, 24 Dec 2024 22:46:20 GMT  
		Size: 76.0 MB (75969024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc80a55774350869ee992b98dcd86030b72390bb6be124ca4de61219527683e`  
		Last Modified: Tue, 24 Dec 2024 22:46:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a47f58182addfc006a08b0f176b99027cafa95cbb11bd8c2a67cea998652ef`  
		Last Modified: Tue, 24 Dec 2024 22:51:10 GMT  
		Size: 18.9 MB (18857375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489299adde02364094cf7b587949e62efb94af380c86790375890e5970e48964`  
		Last Modified: Tue, 24 Dec 2024 22:51:09 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f182d84621ff8030b0063e0c13b0e085d2c01da0e1058aaf33a38c64516b003`  
		Last Modified: Tue, 24 Dec 2024 22:51:09 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af623922dc14d16cf50e56974bb1e3cb3b67c906b20fb6615703191f59f1891`  
		Last Modified: Tue, 24 Dec 2024 23:19:54 GMT  
		Size: 12.7 MB (12651212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fa5845cf9b2e054d723ce873b43b0df1a1b73ac935ab518a09bfcb89227e62`  
		Last Modified: Tue, 24 Dec 2024 23:19:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33116d28723c3b7ecd43e386fab9ad2ec37059cb09b985ae39a4372c3428fa8e`  
		Last Modified: Tue, 24 Dec 2024 23:19:55 GMT  
		Size: 10.0 MB (10040894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e623219990fd2786a56b9432297efd7e3f2a33fe5c3dd899fd95e7782bc03c2`  
		Last Modified: Tue, 24 Dec 2024 23:19:54 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7f050c053f206f521698efc9960af2c00935517287c5e1f1953b5b3b338093`  
		Last Modified: Tue, 24 Dec 2024 23:19:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c0d64d0ef6d25c998562031fe27ca1661e4b4fba40993ffdb05affa19d857e`  
		Last Modified: Tue, 24 Dec 2024 23:19:55 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd416511799a21e50b9dd0281a60dfa383b3511409120ff1ff5d65dfed3c07d`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 1.4 MB (1355033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d546ef738e2ece6110ffabc3eca773c0b5fd7c4bb3d7733565305db3cc6f34`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df356092af2185fa7894c7b2e676ef55035ccba9b4e151e0d74e37429f200aef`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 742.2 KB (742242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04bc9a16c854dec0b59db1b9585f553ef30cd62945ca4ed99063264b1687fa6`  
		Last Modified: Wed, 25 Dec 2024 13:05:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e380d13f1baaad89b6e0f3d0927d647b49f22b1f6f94659bdfe6e4e3dc7db7`  
		Last Modified: Thu, 09 Jan 2025 12:39:15 GMT  
		Size: 21.5 MB (21477807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:b6aaff185e0a3a88fdca96366d9351970af3af14215191919febad47338e38cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6707485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f602988457dab5387b8106fce3b90fc60423b44f7a7e78736cc61b6638237f2d`

```dockerfile
```

-	Layers:
	-	`sha256:c3c9af0f6c38f933fe10be80fee3438e6341692a3ea7d1c974f2a8dda3790d90`  
		Last Modified: Thu, 09 Jan 2025 12:39:19 GMT  
		Size: 6.7 MB (6666213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32447df6146af884b1cde8facf84ac4f88ffe8d49f28757a667b023b45db522`  
		Last Modified: Thu, 09 Jan 2025 12:39:14 GMT  
		Size: 41.3 KB (41272 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:fcf1bc96844ad2d8b48a24410ce617ff9562a7ebc20bd40e3fa2737fed99e128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194899928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6560317c59d42ee2cc934f7b1b48ef3fa0deb77275df3b4f222f7a3973ebc9f0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6de54321d531850ff87c6246d4017603a5b45913b21b1ac9fec3f05fbfef635`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdf08462934214f25431962b05d5cacd6c3f869869f8db5363e56c95c2bc31`  
		Last Modified: Tue, 24 Dec 2024 23:07:23 GMT  
		Size: 97.9 MB (97936231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9687803207cdc9b6efb7871b95e27621a8a6b095ab542b254f0ecc6d9f697b`  
		Last Modified: Tue, 24 Dec 2024 23:07:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c85655b9cbf2eb17eb8b5f60129702dc98ba0a66c0702618db93a9ccc8124a`  
		Last Modified: Tue, 24 Dec 2024 23:11:04 GMT  
		Size: 20.1 MB (20120902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19158f224f42298adef7b5830217f5a6d43a9e3025997c52bf103c2099eeac3`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3a6b915cc6eda19b3e2bc89aadd18d243bb9a1c06307453f890619d373a20`  
		Last Modified: Tue, 24 Dec 2024 23:11:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e78c77837824251aace1541825d6601923f21e2ee313ee9a52a38ae0a505c2`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 12.7 MB (12652941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695c5b3307a6d2076daabb4f5c018ebae4ef009e3efcbcee963cb714557e50c6`  
		Last Modified: Tue, 24 Dec 2024 23:39:03 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8326c89bd989feeeeb960c54e281d47c971efa9bf65b6fa1de6e571f0c5a9b57`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 11.6 MB (11645033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de671d24a51145bc481e0dc81541df0b172584690dd3d56daf9966853393abba`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ef53cc750aad9f3f053519758a892eefe7f61ae19ffd2b2f1add65b9e8df32`  
		Last Modified: Tue, 24 Dec 2024 23:39:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe0df954404086f024b3660bc6719b221414982771d88556a71f01c0756342`  
		Last Modified: Tue, 24 Dec 2024 23:39:05 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8128cd195cdc58ffcead38e9b5b3410f49bcbce892fe763e62722cad0984a5`  
		Last Modified: Wed, 25 Dec 2024 08:15:58 GMT  
		Size: 2.3 MB (2259217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972d55a8c3f1fceee50979eb71256714900d10e5859bfa20ddc428e0adfd3c9f`  
		Last Modified: Wed, 25 Dec 2024 08:15:57 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e8399ffc8b3ed8f5e4217a257995bda009615760ee078c23c39abd0817744`  
		Last Modified: Wed, 25 Dec 2024 08:15:58 GMT  
		Size: 742.2 KB (742241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f738e78b64472f2c7908bc5b6cf598b5f9f77111a95986fe506e93dd4d5eb03`  
		Last Modified: Thu, 09 Jan 2025 08:51:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312111bb56b0b2577d0607251f3a8eca43ec568691ded3586b6c520c2f56f1a7`  
		Last Modified: Thu, 09 Jan 2025 09:01:59 GMT  
		Size: 21.5 MB (21478739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:681fd8bfcd0771a56b9797c4200114a63449df90e6c2b378ab1cd844491d5199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6921075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebc2c8b8e71fadd800ae1f992473583f71653067f23df498e1f903c3a95af36`

```dockerfile
```

-	Layers:
	-	`sha256:c71ce7527253964bcec89f5b6329bb9c5a63dd8bfab71df21bac1bc0d61a25fe`  
		Last Modified: Thu, 09 Jan 2025 09:01:58 GMT  
		Size: 6.9 MB (6879711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8527b187df570bd03f1b84380d6d5c62a3ab5576d88468057a51c732af520f36`  
		Last Modified: Thu, 09 Jan 2025 09:01:57 GMT  
		Size: 41.4 KB (41364 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:76df0454b2ce8e182dc06e80db8627575267554fbb341c6827130fe27a8b7b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200138338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a013d75154c98867967f4a86e9c946cc00a66b667c047e509d4277ee5da3e2fb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1733c98f5ce4b2e4a07bba13ceefa5a9e0b2e3810b1d5b3c853d85f50e95657b`  
		Last Modified: Tue, 14 Jan 2025 02:32:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d75044ffada003ba246bbb0732a4bb3ede3e67e279a769c0b71a384340419`  
		Last Modified: Tue, 14 Jan 2025 02:32:10 GMT  
		Size: 101.5 MB (101513269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b484d7d17287d6986cf9e0b10edfc7e5445c81a541f7123151afc7516e63b41e`  
		Last Modified: Tue, 14 Jan 2025 02:32:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ea7b29eddf758d2e1729ede31c22ab815b3400a222bbb2a1d3d30307f58785`  
		Last Modified: Tue, 14 Jan 2025 02:32:08 GMT  
		Size: 20.6 MB (20638496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de42e260ba75e4b9a450b5b8672c1c2c80c351d96404c3f7dfe4b8f38c39481`  
		Last Modified: Tue, 14 Jan 2025 02:32:07 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f5042b7bf5d4fa2cfbcd0c46d1383f7ade040cc1fb7f3d5fc5d5039a4fa0bf`  
		Last Modified: Tue, 14 Jan 2025 02:32:07 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901de1b20e5a8b93e4d2e86864f29059fc9d0c3aa4414487f36c1a90aadd52cf`  
		Last Modified: Tue, 14 Jan 2025 02:32:09 GMT  
		Size: 12.7 MB (12652211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf8724845971b18f80a101ec4061c04a2f650d680b3a721e6d64775e6b3b93e`  
		Last Modified: Tue, 14 Jan 2025 02:32:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda3f326c32c79ffa46ddeeca894accc1ac3e3a46f88b6fd70672f359a5f8d76`  
		Last Modified: Tue, 14 Jan 2025 02:32:10 GMT  
		Size: 11.9 MB (11868831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70b4ff2ef01d4ecd1e9de1ea1ad2b1529a8c4fddd6f021eceadd1eb411973af`  
		Last Modified: Tue, 14 Jan 2025 02:32:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0feed133755db8940da9d98e00fa518bcbd00b4289c5edd42bae2a4cb676c62`  
		Last Modified: Tue, 14 Jan 2025 02:32:10 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d0778b43de5415ae651dedd0671a84bae58acf27f9b17e4c43f3689a5a5e79`  
		Last Modified: Tue, 14 Jan 2025 02:32:11 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42390b016d4c6b4781574fe28e3d9acb7b9cdca3cc983148d513dbbde0390ade`  
		Last Modified: Tue, 14 Jan 2025 03:19:15 GMT  
		Size: 2.1 MB (2052364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37131d384fcd2c7c3cc47449bb704ec281411e09f59c55a0c3399a6fc00190d`  
		Last Modified: Tue, 14 Jan 2025 03:19:14 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa8cc232f1582d9b1fc09a986a9b76d0fc7a8cd55122749c549b91dcd58097`  
		Last Modified: Tue, 14 Jan 2025 03:19:15 GMT  
		Size: 742.2 KB (742243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241485cebd91e2d76ba5838e740299aa9a5f4b24e1039aad38728bf15d366acb`  
		Last Modified: Tue, 14 Jan 2025 03:19:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57d8d13c588ae121d9bf78f0697a56d0de53a8dc3fd904bf698978db4249688`  
		Last Modified: Tue, 14 Jan 2025 03:19:16 GMT  
		Size: 21.5 MB (21477440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:47aca14b85b871aa2f431a64dbd24f6a6e6711d61765927347f89325fd9f4a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e51385f62d659d7df996b8db500c2b9728da88af34fe8c4f6eeb1c5f47ac98`

```dockerfile
```

-	Layers:
	-	`sha256:1ec4d38fb3c36f4ba8e84086c3f05aa2576c768ae9121c46b4b865209cbb0e10`  
		Last Modified: Tue, 14 Jan 2025 03:19:14 GMT  
		Size: 6.8 MB (6831332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f7436c85519568eb3ff989cbf902c043c411e6c3491be66724e9ea947fb7b9`  
		Last Modified: Tue, 14 Jan 2025 03:19:14 GMT  
		Size: 40.9 KB (40929 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:1059a4fd0a07e23940bd1025c8014f741b87ab30073d6a339556931780e46618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205301496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac88a9c66c5e2a90968a61ce7ee7e203e28615f7c0195734272ae7159ea71a39`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d132df684634db62d3c01ce1613d6eb2566301af85c63410ac30f024166112ae`  
		Last Modified: Wed, 25 Dec 2024 04:36:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd875cb56d0accafa903279e20e2f4504ccbb9a52d3356e35159318d6e6cac86`  
		Last Modified: Wed, 25 Dec 2024 04:36:04 GMT  
		Size: 103.1 MB (103128544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c503622cfce9dd90835f8eb52e082345bb8d299e64a5d12507cacb0203fab6`  
		Last Modified: Wed, 25 Dec 2024 04:36:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc535b192e7a86a518e6f79725942e51c09ecbfe2b3a18e1ac7ba323d04859`  
		Last Modified: Wed, 25 Dec 2024 04:40:54 GMT  
		Size: 21.3 MB (21308315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144b282eeec3a288e4659f298308f4f6703eec9b9e924a1bc18380740166116`  
		Last Modified: Wed, 25 Dec 2024 04:40:53 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c966348685f6c718513b59fe339b4bee7adf696c1a64b706b268a42add51d3`  
		Last Modified: Wed, 25 Dec 2024 04:40:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29d50b4f1e285c244e4324c36587ef40c6303dace73509d894b84ea80bf9fcf`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 12.7 MB (12652618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22adf2d96b60ab542db7a096a3bb2c3195157a601383fad623fc6367053c47a3`  
		Last Modified: Wed, 25 Dec 2024 04:56:59 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37f1b1d57f37110f81d4a078f8175054eada4816fd5fc09315c50a6e3b1eef`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 12.1 MB (12066812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa57954973561f716294764feeb9d66eec42853a91c104738ed2bef1a9b1a89`  
		Last Modified: Wed, 25 Dec 2024 04:56:59 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c8375eb0a20f6d4a36273848105cade616c208a30abbbb68569c6be0ff36`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2087b80ff4dd0882aca3215f601fd961c2ab1d6afbd56b38847577668b07be9`  
		Last Modified: Wed, 25 Dec 2024 04:57:00 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be2ccede99bc11a157ddc7c8c61379d22d3d68be08847419567fbbd0bac015a`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 1.9 MB (1855974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86f9edf99c58d90c4a2d2bf2a8f12d854add7386600806456e06a6c68925dd4`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290eca3313b4114059e49a88f6abba71b3b3d0aaf745977c8c38ff61073179f5`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084dd00d6aa34e0f1c07405cbed0df9ff7e1a8eafad46e884fea656f6b705f62`  
		Last Modified: Wed, 25 Dec 2024 09:48:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d440eb7211178aaee63fe7571df00d0d625715ac49f65d711c121354d91710f`  
		Last Modified: Wed, 08 Jan 2025 00:38:43 GMT  
		Size: 21.5 MB (21477840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:70d1683d213e8611a69788b813f41534521da42b0a39686e6388984f78fc3fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7626193cbcd0a12e421c761f5a92d9a2ee67652fbb8d8b17897c89d7421874b`

```dockerfile
```

-	Layers:
	-	`sha256:1fd5db634ee0ed4d6d6f11c3b8293663733ee3b3b0eb1ace124fec3346c7c320`  
		Last Modified: Thu, 09 Jan 2025 04:10:27 GMT  
		Size: 6.8 MB (6828229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d64d97246fe1cfa07dded73bbf5a6bec87735f72c9224168c4441caa2fb71d`  
		Last Modified: Thu, 09 Jan 2025 04:10:27 GMT  
		Size: 41.2 KB (41184 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-apache-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:b3884174ddfbc5c08fddf6f87edc8b18da42416b18cc572b01760993f5a80ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174701368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938a0bd79039b20f56c3cacef7f699af96b04db1a3bef8180632996bd5e749ed`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 19 Dec 2024 18:32:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 19 Dec 2024 18:32:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 18:32:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_VERSION=8.3.15
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 19 Dec 2024 18:32:34 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 18:32:34 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Dec 2024 18:32:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 18:32:34 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 18:32:34 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Dec 2024 18:32:34 GMT
CMD ["apache2-foreground"]
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV DRUPAL_VERSION=10.4.1
# Tue, 07 Jan 2025 04:57:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 07 Jan 2025 04:57:29 GMT
WORKDIR /opt/drupal
# Tue, 07 Jan 2025 04:57:29 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 07 Jan 2025 04:57:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00cbfa93c448a5709b2ab89b4eecafcf312bab962f82f649a898256b58523f5`  
		Last Modified: Tue, 24 Dec 2024 22:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457328e6b14be13d9f88b508b5952998504e5014f0290e6e1be39897bab54ba4`  
		Last Modified: Tue, 24 Dec 2024 22:49:55 GMT  
		Size: 80.6 MB (80624323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9339c0eb88e9961929bd0005c1c4f86104f98d5884f539ed8d91ef9f169fd7`  
		Last Modified: Tue, 24 Dec 2024 22:49:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47fb800ea78c724c59025d5ac46e9c60dea88853ca2b4ae21855f62533c1a76`  
		Last Modified: Tue, 24 Dec 2024 22:54:21 GMT  
		Size: 19.9 MB (19895315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd195bf1bc34d371e309aeabf0a6d8810a778544fb754738ceebbed7152b26`  
		Last Modified: Tue, 24 Dec 2024 22:54:20 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc4a7840b6ec52c065ff2d8ad71af54e6267fa1bbca2329da95e751d55ef9cc`  
		Last Modified: Tue, 24 Dec 2024 22:54:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400d26f2f55018b7e7b0bbffdd3462b86f62449aec1bc9013517df4f60215c96`  
		Last Modified: Tue, 24 Dec 2024 23:09:45 GMT  
		Size: 12.7 MB (12651596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb15368ec111af0f656249c9045540822eb93e74689511313971471f8871cee`  
		Last Modified: Tue, 24 Dec 2024 23:09:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27911a224835a99e6f020384734fc6bcd8794b421d63b7af081a51de72ccbf`  
		Last Modified: Tue, 24 Dec 2024 23:09:46 GMT  
		Size: 10.9 MB (10871221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f62abd26f3d7b459ed85116be0fc8678c6dd16a65f900f22c87570fd1129001`  
		Last Modified: Tue, 24 Dec 2024 23:09:45 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe609398dcdb76ffb760305a258f951c538099c6f6e28f10c76461cd3431e31e`  
		Last Modified: Tue, 24 Dec 2024 23:09:46 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50956637c0d421cb78660bfff0559b28f257bde9283040f193d89dd6f1bbf82`  
		Last Modified: Tue, 24 Dec 2024 23:09:46 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317ff096b48d6e6bd7f00537eee8017248f3e194f6177d6b4413c73962e4ce0`  
		Last Modified: Wed, 25 Dec 2024 03:32:49 GMT  
		Size: 1.6 MB (1553579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ebf83222a8dad654d474eeecad0abe92b8d495e58113b491db8fd429bd250b`  
		Last Modified: Tue, 07 Jan 2025 19:25:29 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eeefaf6bae6d8de5b542cd19c5d00859041b215a2ddea7cee47a9f33334718`  
		Last Modified: Tue, 07 Jan 2025 19:25:29 GMT  
		Size: 742.2 KB (742242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6616f16b7bfdf84109d2e79a74eb71e2e47b6cad1a3ca3aff4291808c0c863`  
		Last Modified: Tue, 07 Jan 2025 19:25:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e25d542f3c39814a9b35ebdadba0efd9672f17aebb9a8d1d5b03cb5fee16b2`  
		Last Modified: Wed, 08 Jan 2025 00:36:03 GMT  
		Size: 21.5 MB (21478283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-apache-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:f1ddc385791b6efce4fae1e2f9be0a2aa262b1c9c36f1c8b64b3e4b11081bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22401f098dce87f7ee34833ae790af0c4ecbd8bcfcbca8ad6be8e97a83caefd1`

```dockerfile
```

-	Layers:
	-	`sha256:bd7559278d5fac9c979ef15a211d28ad1c9ec089853ee931d26ba36d9b797d37`  
		Last Modified: Thu, 09 Jan 2025 10:32:12 GMT  
		Size: 6.7 MB (6692555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5fba3ebcb91c592995eee945b9a1e2b34e469f4020a7ed7b243e91ea0b4aa45`  
		Last Modified: Thu, 09 Jan 2025 10:32:12 GMT  
		Size: 41.0 KB (41036 bytes)  
		MIME: application/vnd.in-toto+json
