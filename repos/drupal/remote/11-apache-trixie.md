## `drupal:11-apache-trixie`

```console
$ docker pull drupal@sha256:5eb6cf8169350722357fc76ce28ea4411f454156661cee08ecad5bab69a1fdc9
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

### `drupal:11-apache-trixie` - linux; amd64

```console
$ docker pull drupal@sha256:78ddbb9e71c1d4de335261cd4b5d1dbe9610137cdb3ba8787d47da59fe690b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.8 MB (202795601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977f84be626a7ad11a6679b79fe94463643c6b465d873110616b2dd226d71968`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 13 Aug 2025 20:35:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 13 Aug 2025 20:35:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_VERSION=8.4.12
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 13 Aug 2025 20:35:19 GMT
STOPSIGNAL SIGWINCH
# Wed, 13 Aug 2025 20:35:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /var/www/html
# Wed, 13 Aug 2025 20:35:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 20:35:19 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7d57eb145c727fd42bea60344c7374f0d3436415e0d8fea06bab5f9dcc9c45`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e84808a09800799297467cf6757d23c36562d0421500eaa8009eb830ff25f6`  
		Last Modified: Thu, 28 Aug 2025 18:19:18 GMT  
		Size: 117.8 MB (117834245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f3f0775bd8677e6d9afebece0e64068654133cca804a58a4142c5cc0ba3acd`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6890624c3adfd3a1bdc9a1ef87167aba9c9bd9382f349d8a8c55bc069d1114`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 4.2 MB (4223789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd81635072caae8c0b139876c6d9b269da7bf704e28c802cb1e0e7fff6a831`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3904703ccac320dcd3fea48bf1395eeb0af10650168ea9027fadc28d22d4af`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b15de76778c4ac6b1ce195f0b9d465a745e80b364692f2ce9bb2c5e88d0a1a`  
		Last Modified: Thu, 28 Aug 2025 18:19:07 GMT  
		Size: 13.8 MB (13802580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67916c4c9c0b021b7f6e8c647f0e89e2e8b33471b32a11bc8fa6eb9d333a6bb`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7f2ed1b3a7ee51cacd4118eb95dffd40d1c2e75da8974f19a337b2085330a`  
		Last Modified: Thu, 28 Aug 2025 18:19:07 GMT  
		Size: 14.2 MB (14213470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3ca3df03da55c3ccd7f38281517a945a9586d7712f53b567c2036805b06722`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72763bb5b9c3240e370543e7c38685af83c59973aeaa4704bdf092769c0f09e4`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2215e01ad48ec0310d339a14ec84809a59d1a851365e368eb4cf3d2a2d5cfafb`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a5f0483900ed4d9e0c336398717361227c642959be4e5925d0723ea85069ee`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13b729f4d3d548e7c437163071cad4592ae3f9d3040e26f4d9e9f5631e01903`  
		Last Modified: Thu, 28 Aug 2025 19:09:45 GMT  
		Size: 1.7 MB (1655906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8601bc893d43b6867c273027038a32c70af1d7ebf3c5c57bc18fed4b3864ca3`  
		Last Modified: Thu, 28 Aug 2025 19:09:44 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae70846567867272966e14e2fe3d0b3d87174b310c38d47c55f99b10cd586c37`  
		Last Modified: Thu, 28 Aug 2025 19:09:45 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976b0ad16b20f4b12981bc6df5e98c15d85d22848364b7a44689272de8a355c2`  
		Last Modified: Thu, 28 Aug 2025 19:09:45 GMT  
		Size: 751.2 KB (751222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d76fe6c312f12101fc7aa90f654238917d8f582cf121b690abb888ee988264`  
		Last Modified: Thu, 28 Aug 2025 19:09:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1146bf09eb4e4468ccb2aa96b1782d1adcdfd67fd5af31ead20e7960929249e7`  
		Last Modified: Thu, 28 Aug 2025 19:09:48 GMT  
		Size: 20.5 MB (20534683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:588c345c798ec21a5fa6687d1e8a5f2da87afbf284a53c76de82207c760d6f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabba4c9439084f47e2d9bd3f64144163091f7b319ca115dbf8ada554e82ab8f`

```dockerfile
```

-	Layers:
	-	`sha256:c4a31d55f6e59d4d51bf8b54f689062c9ceb020879327c9299b62af05258788c`  
		Last Modified: Thu, 28 Aug 2025 23:04:55 GMT  
		Size: 7.3 MB (7343069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535d0d96a0feb1b1840f19bfab9dad833dc6bb12f5a65d20c67ab4fcfc891814`  
		Last Modified: Thu, 28 Aug 2025 23:04:56 GMT  
		Size: 49.0 KB (48986 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-trixie` - linux; arm variant v7

```console
$ docker pull drupal@sha256:3c3d9e29bbeaeeaea20896a58ccb3fa60c4019f130391aa72e65809cb7919337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164964795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7b893f2eb673f8ccafbc768d48730dcf9ad45fe07e95d268c089c5122cec4c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 13 Aug 2025 20:35:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 13 Aug 2025 20:35:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_VERSION=8.4.12
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 13 Aug 2025 20:35:19 GMT
STOPSIGNAL SIGWINCH
# Wed, 13 Aug 2025 20:35:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /var/www/html
# Wed, 13 Aug 2025 20:35:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 20:35:19 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f783066fe233d49b725a424d9e4e2edf03ec368e8008a7100235b31d55c72428`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def7928390388cc2020246549215f695478752f6ae67568af1344eee2f6088ce`  
		Last Modified: Wed, 13 Aug 2025 03:03:28 GMT  
		Size: 86.2 MB (86243176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decd14e90655d8988225e174f3bef3fbd8abee342388203104f64e9516432f7`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372110111ee86e66c1b99c7148a9a3a4e350c9b9c4843f501f3c831128011fe3`  
		Last Modified: Wed, 13 Aug 2025 03:08:13 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721b3bcfb16aff30d3a16d797f1847f5686541c5e5390e6d2d1d8e947baa2f68`  
		Last Modified: Wed, 13 Aug 2025 03:08:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fb1db8d532ffaa5e1f6b0f06e0e76396d505ed544ca2b1636fa7de235e998e`  
		Last Modified: Wed, 13 Aug 2025 03:08:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c8bcfc0b5f2af29c6fa2719fa75049aac7700b0afaf910dc1eedc2a344ca9e`  
		Last Modified: Thu, 28 Aug 2025 18:27:09 GMT  
		Size: 13.8 MB (13813356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11a6d60f7744c66b32a9231ddd8f24fb1dd77dc27e5f6d03697492c885d8b9`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fb861533277915a1de63fb5de3ca7c1d9eb3e64a898026370c9516dce108f0`  
		Last Modified: Thu, 28 Aug 2025 18:27:08 GMT  
		Size: 12.3 MB (12286498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d8fe9f632da0ebf1a625dd1ee712095009d54c73cc05cbff939284013e94b0`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c2bc75353a0f2e1d1ebcbcfeb7479dba1c366382ee31f4788f3724e478965`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce23df2cebdad049308df94268747e4b32c14ad6fc68a17bd114ee5eaf9f776`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23eefdc8501db9313e0feb50cea365dd37c9ecf8e529ba136ad4f1eafcd87de`  
		Last Modified: Thu, 28 Aug 2025 18:27:07 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ec7782293d9a2275b3395d3c30f53c235ae959b79c5800ae4fb946fafe43f8`  
		Last Modified: Thu, 28 Aug 2025 21:37:12 GMT  
		Size: 1.4 MB (1370075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfd8223457d507d7b0051d7c859b3b765cad9227a6af0ff2e2d4d84813db818`  
		Last Modified: Thu, 28 Aug 2025 21:37:12 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fde3575a76373e1ad0563a3b9407b578d99c7c626cbece0a337880954a38ab`  
		Last Modified: Thu, 28 Aug 2025 21:37:11 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d336bdbf3f045833ac067fe23ebdd0b254fa66d881e4eb20ce15cbcb65cfcaa`  
		Last Modified: Thu, 28 Aug 2025 21:37:12 GMT  
		Size: 751.2 KB (751222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76be227bbe267113696b659c283566b38b80d17d01246962f0a6547e5e3540c3`  
		Last Modified: Thu, 28 Aug 2025 21:37:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5601aa8d6a7c9c928b61930dd356836e4462e3e9e6a4949a704d17080b771`  
		Last Modified: Thu, 28 Aug 2025 21:37:14 GMT  
		Size: 20.5 MB (20534773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:d4958abcc0eb68aff28b9df9b36c19f1b21d072b2c3e3ce29a547be636aada99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0f22098308cb6ec6789145060a0d517945922a293dd82926e5ded64b245cf2`

```dockerfile
```

-	Layers:
	-	`sha256:7d7371fe73d33c314a384453539ede06a0ce29cb61f31f23a000e1e12176581a`  
		Last Modified: Thu, 28 Aug 2025 23:05:02 GMT  
		Size: 7.1 MB (7147078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a5c5805b82aff5a6edc5b6b647d4c6a7174cfebd1e16fd05a8bbc955d3b0b9`  
		Last Modified: Thu, 28 Aug 2025 23:05:03 GMT  
		Size: 49.3 KB (49276 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-trixie` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c63e2fcd05c6bbe83aad5347b2e9e3ede09ecee4da8e993e27f26299946f622d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195154509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da61dd48b04d700aa5e5364dece00244c246c931d06e8ee70101cf1570564cd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03022ec7f33593ecc2a3aeb663cc554de1d9e62087a60919464202ee9a290e`  
		Last Modified: Wed, 13 Aug 2025 03:18:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bbeac273051d37a774f98368f1d00d339ab0541a559de53da0b53ac9ed0340`  
		Last Modified: Wed, 13 Aug 2025 04:59:11 GMT  
		Size: 110.2 MB (110160214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720d4bdd0b0544aeede4fb064271ee7a67ad806bfbd73e41d86f4e6f668e942`  
		Last Modified: Wed, 13 Aug 2025 03:18:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b60b975d3aa1da608092d98d515a7eabb380c32e0ce8665d6baeb34900e88`  
		Last Modified: Wed, 13 Aug 2025 03:22:34 GMT  
		Size: 4.3 MB (4301196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0cbd12c10a655d9a291a27411ec20303518b47026b2a5ff68efefdce0c5f78`  
		Last Modified: Wed, 13 Aug 2025 03:22:33 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5af07a95e93ac686b42bdd804cb31c9e9d61785169b5f1732a608c6611c6eda`  
		Last Modified: Wed, 13 Aug 2025 03:22:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7fa94eb72c435c4083d9edc8b47e47b39e59a55fb54184866959b8f040ffa6`  
		Last Modified: Wed, 13 Aug 2025 03:52:41 GMT  
		Size: 13.8 MB (13798251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ad0cf00128779599907c2446913a6d0780a3de905cfdac0abb2958134e0d15`  
		Last Modified: Wed, 13 Aug 2025 03:52:40 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b7371082d881a40f8b1b20902b85b25841220f942814ff7f04e69eec9c6b73`  
		Last Modified: Wed, 13 Aug 2025 03:52:42 GMT  
		Size: 13.9 MB (13854418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505edd4cc5e6ae0fc0e80a082a63f25224dcb6763e843cf3292ab43da414a33d`  
		Last Modified: Wed, 13 Aug 2025 03:52:40 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcb6566ae54375615f1dcd3d7202e3215887da36263b16ad19cebc99aaa5cbe`  
		Last Modified: Wed, 13 Aug 2025 03:52:39 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e8d87df64f09284a573fb29b85fe1fc88bfa6d3e30b4d7a8263e43c99c8095`  
		Last Modified: Wed, 13 Aug 2025 03:52:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3306a8685b9c651ab107b54b9446111b1ea6587831ebf403cda420a21c5e256a`  
		Last Modified: Wed, 13 Aug 2025 03:52:37 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6a501c2d6a8f52b08ddea293428c3182a962207fce03448f213577ee798923`  
		Last Modified: Thu, 21 Aug 2025 17:33:22 GMT  
		Size: 1.6 MB (1613124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498829b9b286071991235a4f4d1c01c286fa5118aa2a16237ba5230aa04af722`  
		Last Modified: Thu, 21 Aug 2025 17:33:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca7fbdbbc1522ebfd8daf883cc649708bb3f7c63813bbb8c3d39345c900ba20`  
		Last Modified: Thu, 21 Aug 2025 17:33:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020965924d6bdfdd10792c43a950c121093fde33c935561227ff84ad1616bd0c`  
		Last Modified: Thu, 21 Aug 2025 17:33:37 GMT  
		Size: 751.2 KB (751223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85175eb953ea44d411aadced7e6b00d5149b6c1ced83e27cf0309db3823f4574`  
		Last Modified: Thu, 21 Aug 2025 17:33:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab047bd4c82fa066167631c924f7fb6a795304c471053311ffc7c8e4762a4f13`  
		Last Modified: Thu, 21 Aug 2025 22:36:02 GMT  
		Size: 20.5 MB (20533609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:34489f4d35ac93af86cb7c194a24ce3511d97b1b4782f314affe318f935439b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384057fe9e477b46a4d046aa1b2be2d80ef463874ef33c62c5ebb3dfe8089b72`

```dockerfile
```

-	Layers:
	-	`sha256:ec848391c86cee3308254dfb14f670bef90a3127bf432b039128fefd613030c4`  
		Last Modified: Thu, 21 Aug 2025 20:09:40 GMT  
		Size: 7.4 MB (7440611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf7e056e4ca441779f997d64ae4f35f87a831ed7bf5f363bbc75b0095356cd1`  
		Last Modified: Thu, 21 Aug 2025 20:09:41 GMT  
		Size: 49.4 KB (49401 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-trixie` - linux; 386

```console
$ docker pull drupal@sha256:472e640833bb2c92e63e5970a5ebf752aa2ffca1bccf3e180939ba3ca313c166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203215386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f96c1a72b89bdfc34e6cc430339e78e41460cec8ebec88148d925f556cb26a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 13 Aug 2025 20:35:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 13 Aug 2025 20:35:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_VERSION=8.4.12
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 13 Aug 2025 20:35:19 GMT
STOPSIGNAL SIGWINCH
# Wed, 13 Aug 2025 20:35:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /var/www/html
# Wed, 13 Aug 2025 20:35:19 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 20:35:19 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba52183d0662821bae443d97871b085d0bc60505c7deb7b350f08ccf9621a3b4`  
		Last Modified: Thu, 28 Aug 2025 18:19:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b81b95736d42dcad298b1a99ec5d7cf65d7a1a2057b9fd4902f6d39e1cc322b`  
		Last Modified: Thu, 28 Aug 2025 18:20:00 GMT  
		Size: 116.1 MB (116135170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65d9e7bf4a5d2c5719dca9109f0e7737c76b663d170c9615fcc8c7abef84625`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d6d52760a95f9b3ddac4226928965599cf7a6efe654fb36a28b834937184eb`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 4.5 MB (4455055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61d06578fdbacc02983e45f0477e6dfb98ff4ceb7248025d60c0e97c78d83a8`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9da60ef281aea664c931de61ad8f417b406e38eaeb38aec7671793f580c5b2`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfd27741aa2ca7d1b6e75e31854baafa672a628e07f436d6ec00ad347bfddc5`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 13.8 MB (13801472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4220e66a6bf35b34a3bb5baeb56f91170408b9ab942fd847656d2269db9b3d`  
		Last Modified: Thu, 28 Aug 2025 18:19:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a81d9c2a6514d42205201ffa10bd82e75e6afde82f6879c06a34389fdd35ad`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 14.5 MB (14506072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f805e0a1ecac6676d1958760954d8079c5012f082801852ed352b91fead4c6`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649f19a8e86e798e66b31ac499b953a5bc361deef04309a6be4455054e1cd34b`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0323412794631e0e5a6ee30ff4bf2c610a01b536eff6a8eff11e02dcf52c0642`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b650e102499a255a77af1c27412e31dc58585043eb876ec12784751cf1ab5b`  
		Last Modified: Thu, 28 Aug 2025 18:19:50 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10216e66091703f9a4e32e3e59ccdd1522b07d07df15b31f79b0941a0087d74f`  
		Last Modified: Thu, 28 Aug 2025 19:09:47 GMT  
		Size: 1.7 MB (1735863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfba4acdac903212708690c4a2f6eede334fe50b185dd11ec8a04a53c234ecc7`  
		Last Modified: Thu, 28 Aug 2025 19:09:46 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17e79a60ffc560bbd651bea1e16c1920dc0ba128d75842a872713c3d50a85b0`  
		Last Modified: Thu, 28 Aug 2025 19:09:46 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e573fb980324148e37c4ef53f203219936b9ea18bbf120ec920dbd38b4003ef`  
		Last Modified: Thu, 28 Aug 2025 19:09:47 GMT  
		Size: 751.2 KB (751222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7e53c5a6d5e16851485fc3af2449059b35d38de35b0aab7ac27370dc3ba95`  
		Last Modified: Thu, 28 Aug 2025 19:09:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497134f10f4878d10aa27435c2f51f580951a6c187728c43701dcacfae44b948`  
		Last Modified: Thu, 28 Aug 2025 19:09:49 GMT  
		Size: 20.5 MB (20534738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:89f2598b8d06b07971934d2b51e6c11cfd230ac1b41a8588fe487e6bf95312b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7365662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ae211938978a146b4fe590d199b330fd2891c8d3e3aa7b05cebb6d460a0160`

```dockerfile
```

-	Layers:
	-	`sha256:26997e9010813eb4be1e3d8aac03254d32fd7465666723f78112f4d704f41e8f`  
		Last Modified: Thu, 28 Aug 2025 23:05:13 GMT  
		Size: 7.3 MB (7316821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07c352a057ebbd114b58e6783f34f055bf9348a3028a1cc057d3b126dc1cf22`  
		Last Modified: Thu, 28 Aug 2025 23:05:14 GMT  
		Size: 48.8 KB (48841 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-trixie` - linux; ppc64le

```console
$ docker pull drupal@sha256:34c9102fa83f36c6344b81c4c7acd0beb43f4c66520b1f72417923098e8506e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199611363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c983835893a1812d27e54cfea1949a6b7af41d775d6bd36de57aa625621294`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe95aaa1875d4c50c764ba29c6f95cc470f62d9ac88ad9109e0cd4505d319b5`  
		Last Modified: Wed, 13 Aug 2025 05:31:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ffef807c2273a22858b85bf52a5cbb82101766a6dfce24ba2f8e3ca25f228`  
		Last Modified: Wed, 13 Aug 2025 08:03:15 GMT  
		Size: 109.6 MB (109595127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8a64ac10b73fd871320ade0ad956a6b2aeb6e2c3151d32095cad855bbccb`  
		Last Modified: Wed, 13 Aug 2025 05:32:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd42c19a20ac483aec1baacbb7b775bf9031104d0a0f064b9f0867d3ccc76220`  
		Last Modified: Wed, 13 Aug 2025 05:31:06 GMT  
		Size: 4.9 MB (4875422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcf6e5878ff7716cc38c54c9c5482a97442ddcdd8c0aabd868a7d11ed49b7e`  
		Last Modified: Wed, 13 Aug 2025 05:31:07 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983399591a61da466bb4e672cad02d507232883ed14732dd13f80ac851284879`  
		Last Modified: Wed, 13 Aug 2025 05:31:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f3b5c9dd55235c2707e50201e0fcb38ddd2c62fe1adf7f3fb0b4769c9b95ff`  
		Last Modified: Wed, 13 Aug 2025 08:43:55 GMT  
		Size: 13.8 MB (13797381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1484d464e8aaa1805cfe9dd3c8b3bf415740aec9463af3a6d2b0729c2248990d`  
		Last Modified: Wed, 13 Aug 2025 06:21:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db36b52d8fa42ab925d661822f72e29beb65c990af82e90ceedda9d5eaf6c05`  
		Last Modified: Wed, 13 Aug 2025 08:43:55 GMT  
		Size: 14.6 MB (14611810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127ac2e2121c6c111db630459faa25d794eb9c0be30d18da317f6496f93a481a`  
		Last Modified: Wed, 13 Aug 2025 06:21:07 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110bbcd9bdcdc0fdf0386642b5b0446f630d11197922e1b477ab17edb7dd5d78`  
		Last Modified: Wed, 13 Aug 2025 06:21:10 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d664fc0fb3fc831c5b9898719c0a53741870521b4f07653d3543ead13b4a8ee4`  
		Last Modified: Wed, 13 Aug 2025 06:21:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b366fcc85887d8f90a362808b538293275eb9ecc6abdb4ae8fc2d1fe36c39f3`  
		Last Modified: Wed, 13 Aug 2025 06:21:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf6fe03aa5623ac72c619a32cc0046282361bb11a7344ad938fb838d60bd129`  
		Last Modified: Thu, 21 Aug 2025 17:10:16 GMT  
		Size: 1.8 MB (1845155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341195d32af5d67167178606990d2ba44244316daadfd548dfe413583023443e`  
		Last Modified: Thu, 21 Aug 2025 17:10:15 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729b2c1d32e714fcdb3637b03f9f3789ce32430ade3698d9434003c94423b81a`  
		Last Modified: Thu, 21 Aug 2025 17:10:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2455ff58065e897b1c2f0e5b70a28b436280e6e3a80149023c8cf3a7a7f12b38`  
		Last Modified: Thu, 21 Aug 2025 17:10:17 GMT  
		Size: 751.2 KB (751223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67984f284d450596bf28b89c44faa1007e633298a725b8242e450b1586df3e1b`  
		Last Modified: Thu, 21 Aug 2025 17:10:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861f84d5cd2b11d1575aa1acd1045cf29e5bc6aae943dc3a300f4c3345a6ffa2`  
		Last Modified: Thu, 21 Aug 2025 17:10:19 GMT  
		Size: 20.5 MB (20534605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:d6ec06f1a4559f6bf00c8da8a681ccc02ee6e41e6e1942fde17778af7129eb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a887ce0b48089c06b9d8b2f4264b23c24d498203eb53981e7a14eabea1bcb6`

```dockerfile
```

-	Layers:
	-	`sha256:1c16e726f82ad26021a264c639f85d569d7172987e32195cae113c432025d8b1`  
		Last Modified: Thu, 21 Aug 2025 20:09:55 GMT  
		Size: 7.3 MB (7343014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03de2850fa8e23e1d4a68f9712a2685fac9bcf87ec4a32afda87de1c63f8e38`  
		Last Modified: Thu, 21 Aug 2025 20:09:56 GMT  
		Size: 49.2 KB (49166 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-trixie` - linux; riscv64

```console
$ docker pull drupal@sha256:11855fb0180d06d2f0c43dcbdd552cc1eefaa060f53399877de1cd3b3abb6ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229195318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c13da44d6fa0616319e930dab9f003aa01a4130c9250f356c0d2e8307f499c6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ee082f6fa69e7faad8700545098a6fe52d7039873614c52058e758703420b`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 4.0 MB (4025653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5398f81f2b0b9d166065f2794959e13fe5cef571690a888e526a297344cb648`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7320c702209633ef3bb6abda50aa7d4faab29f17f69247e387513e5af1004ed`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cddc700ba0cb108198a5a00e1def0c2af7bdbe4fe485ab8d91c640a321a73d`  
		Last Modified: Wed, 13 Aug 2025 17:05:11 GMT  
		Size: 13.8 MB (13810719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ec14e885eeb0d5b2317ab7a2c3d4e12796be0833b0f9585a694ab2ec3d706a`  
		Last Modified: Wed, 13 Aug 2025 16:16:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0e86774f6c6ec93e9bc7d2328a65a1a82bbe8267508a443c6e56d36776512`  
		Last Modified: Wed, 13 Aug 2025 17:05:17 GMT  
		Size: 13.6 MB (13644924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680b340ffb03bdc0b96c9aa4f464a5a3041272e42eeec4ae1b226daf8b3e1279`  
		Last Modified: Wed, 13 Aug 2025 16:16:16 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1560aeec2511b0a1fb912a9f9c4a378248f0b2d368d04192e3215e60f002eb8`  
		Last Modified: Wed, 13 Aug 2025 16:16:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f7b555c1e6beea9777086dd273c6d2bec21d788655edcd044cc34d74c0e80`  
		Last Modified: Wed, 13 Aug 2025 16:16:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9ae7b15094360374526a467b26cd186b321b527583245240db442766926703`  
		Last Modified: Wed, 13 Aug 2025 16:16:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433707c2d1f736bf65909f7c5fb0d8af814a6ca5e08b04e154b2a94d5b0dcef`  
		Last Modified: Sun, 17 Aug 2025 08:11:50 GMT  
		Size: 1.6 MB (1572061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba476d1de5bb0396323d34b39bb22768816748289bc9bc0fc8f22f01be32743`  
		Last Modified: Sun, 17 Aug 2025 08:11:50 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61df099c7596a5b5eba2535778b911667859e9c142e7f1f6ff3bead980e770ac`  
		Last Modified: Sun, 17 Aug 2025 08:11:50 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5900a6bce18d6e5df526f3e5aa3aaaae00f8941cf4027d630482e64d13e8fbf5`  
		Last Modified: Sun, 24 Aug 2025 21:38:38 GMT  
		Size: 751.2 KB (751233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847a3b73f4702ddd76a633cb8527d09d839e8302db4239eb22889cf32ec9c1a`  
		Last Modified: Sun, 24 Aug 2025 21:38:39 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386e746079b27ef1da8edc227de4a47aab6861017c4998cc521e5a8c5314c836`  
		Last Modified: Sun, 24 Aug 2025 21:38:42 GMT  
		Size: 20.5 MB (20534819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:e206284d422a16df3de4d7da6ae3908e0c19f4dc0a33429dbcea20223c09737b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7125f575500a0ab59a61dcd01f08fff73661e32aba3683f6428328038d750dc6`

```dockerfile
```

-	Layers:
	-	`sha256:41f20243d7dcf5a2593c87031d3b6b57fff684870e1fcbd1dde5da3b890be22e`  
		Last Modified: Sun, 24 Aug 2025 22:56:43 GMT  
		Size: 7.4 MB (7415011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5567f39109c1e0d3f0559a3b30f93936254784d35613d9f786e9b7af0422ac`  
		Last Modified: Sun, 24 Aug 2025 22:56:44 GMT  
		Size: 49.2 KB (49164 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache-trixie` - linux; s390x

```console
$ docker pull drupal@sha256:d45f84cac93ae325e2d087e809d91ec04f25ebf96a4a4c4d47d870f01e58db4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177764196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf08242a1173c67e385689f546af381ca7f5a09480d96327c172f68801b6f43`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.4.11
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
RUN { 		echo 'output_buffering=true'; 	} > /usr/local/etc/php/conf.d/docker-php-drupal-recommended.ini # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV DRUPAL_VERSION=11.2.3
# Wed, 13 Aug 2025 20:35:19 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 13 Aug 2025 20:35:19 GMT
WORKDIR /opt/drupal
# Wed, 13 Aug 2025 20:35:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 13 Aug 2025 20:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d672c8320b5c626e155e165336b2569c5c22cfbda44788e2e9dd0b175c8a1e`  
		Last Modified: Tue, 12 Aug 2025 23:44:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06790e9e58c7a87421168e1b912411e592f3adbcdce2412a5541e72fa8de3f1`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 92.6 MB (92562072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019838dc72213baa0c7fefd5773b69a921a755553c45ef473aea40f478c95cb3`  
		Last Modified: Tue, 12 Aug 2025 23:44:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7420b950475ba12842aacb09ab6fc12c17aed6a94e8f7425f2d9023a527d61d9`  
		Last Modified: Tue, 12 Aug 2025 23:51:06 GMT  
		Size: 4.3 MB (4320335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2286236b154642f4dfec098836badaf56b6f5891dfe3de1dd729e687339006a8`  
		Last Modified: Tue, 12 Aug 2025 23:51:05 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d32f90a36507f204f3058a0f5e737aa20705dbfb0fceb4bbcaba30b59ab9c8`  
		Last Modified: Tue, 12 Aug 2025 23:51:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f3942a5729b01ffcb5c4e1ce3a3a8bd31b3370437e6ac91a079d95d7db0609`  
		Last Modified: Wed, 13 Aug 2025 00:14:32 GMT  
		Size: 13.8 MB (13796770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5add4da810950fc0a80ddc3e57f5271372918589cbfa1d68d8373cf4f20fda`  
		Last Modified: Wed, 13 Aug 2025 00:14:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd5f26d2639aabd9abaf08bb8c49aedc411393a8e2912db4c5a0e00d1168812`  
		Last Modified: Wed, 13 Aug 2025 00:14:33 GMT  
		Size: 14.3 MB (14284789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7c7bb722cb1692f38f45a4df327de09c95d4de39af18ccdf80304370c4aa3`  
		Last Modified: Wed, 13 Aug 2025 00:14:30 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c06e3e780022cd99033155c66958bdf9398b9c7f8a117ab55cac84a5cde461`  
		Last Modified: Wed, 13 Aug 2025 00:14:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf7198e0179996c61f9092c94decfc749fd59dd9a62bcf41e6770a9d9306fdb`  
		Last Modified: Wed, 13 Aug 2025 00:14:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdef8b9fa477f528e1b72a2ff49108e67ef76a6d1937fc9c289fe9d4639ac64`  
		Last Modified: Wed, 13 Aug 2025 00:14:30 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4074831260b35b5d5467ed47ebe15f71ba1baebf3551bb698eda592f4186f1c`  
		Last Modified: Thu, 21 Aug 2025 17:11:48 GMT  
		Size: 1.7 MB (1674847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd1f41b53ed82bdae334906c9ae2add08ba2306a9f81c4dad436d2987bdd800`  
		Last Modified: Thu, 21 Aug 2025 17:11:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803272e639ffb3765de5ed263624804c89811908c1379cc69273b1a08f5a98b`  
		Last Modified: Thu, 21 Aug 2025 17:11:42 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6461d90303eba5bb882654be0fcfdaf70562d6916738e607e4c42d64d34e452`  
		Last Modified: Thu, 21 Aug 2025 17:11:45 GMT  
		Size: 751.2 KB (751222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5755b5779d66a55f0eed7c9aae400cb61a8f39116c31203b648d43a6e212ff`  
		Last Modified: Thu, 21 Aug 2025 17:11:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adfcc5d6f5e4a17affc31770f155f3f647700c2660e45dbd5e8459cdbee26f3`  
		Last Modified: Thu, 21 Aug 2025 17:11:45 GMT  
		Size: 20.5 MB (20534674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache-trixie` - unknown; unknown

```console
$ docker pull drupal@sha256:029b7144cd2dfed07f904eee5b6d67b8ad5dbf6fbbd88d190f42313a66b1d0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0164fb8af04afd985050592d956adbe075d38fb42658d8782e725f663ddd46dc`

```dockerfile
```

-	Layers:
	-	`sha256:ba6517f755188b24b7d6c80a128fa542342845f5b380eb0fcf5a6d0305b5ee03`  
		Last Modified: Thu, 21 Aug 2025 20:10:08 GMT  
		Size: 7.2 MB (7160319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9b8c33a590d61af48e1e06e1820fb86af52cd767ea5facd8b3d0fb58e329efb`  
		Last Modified: Thu, 21 Aug 2025 20:10:09 GMT  
		Size: 49.0 KB (48978 bytes)  
		MIME: application/vnd.in-toto+json
