## `drupal:apache-bullseye`

```console
$ docker pull drupal@sha256:f1f761cb706b5689bdf27d91df83c2547b830986859e548a2db6c2ab5261a9ef
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

### `drupal:apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:3af6857a6064c834c3b76daa6915961a1f8e8e5f89e6a1140ca491f2e58326e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188077312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8397059de8d428aaa5ea1c3338d9ccdc1d9a16f9172e3d2ea0054a368b8a8bda`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Wed, 29 May 2024 22:34:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 29 May 2024 22:34:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 29 May 2024 22:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 May 2024 22:35:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:35:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:38:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 29 May 2024 22:38:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 29 May 2024 22:39:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 29 May 2024 22:39:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 29 May 2024 22:39:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 29 May 2024 22:39:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:39:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:39:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 02:32:00 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 80
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["apache2-foreground"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6f7a35042495eb772e67d34515d94aba1d3b255a8723ca526b85400d418b6`  
		Last Modified: Wed, 29 May 2024 23:19:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3967c95942e791bb3423c9101608556e6c0e5b7793b441d5819965227d98a0`  
		Last Modified: Wed, 29 May 2024 23:20:02 GMT  
		Size: 91.7 MB (91651332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a12ef0702bde7f65e33a9421341f3c062ebf741ab9e183fe96d18318adf32f`  
		Last Modified: Wed, 29 May 2024 23:19:49 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24887d144abc52d2022e90f2fed4ddd0782218d5f5cb3082d13925a2e166c4f1`  
		Last Modified: Wed, 29 May 2024 23:20:20 GMT  
		Size: 19.3 MB (19276883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d17ed3fb79cb17f6d19efee1d14d27821d66d6f12b194623963b9caf1a4e43`  
		Last Modified: Wed, 29 May 2024 23:20:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15aa7ea646d5009a177c63063c11eeb506014b786b0d993ed11ad6c1dc30a3ea`  
		Last Modified: Wed, 29 May 2024 23:20:17 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db52f7fbccbe562c13c09ff542a1c26c83dca2e8281bc806ef585ba37d4487d5`  
		Last Modified: Thu, 06 Jun 2024 22:17:54 GMT  
		Size: 12.4 MB (12440197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e5a195734026364c3d31f5aec538134ed43a8d242be70f4cbbeb8d6eb1b944`  
		Last Modified: Thu, 06 Jun 2024 22:17:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb7bc7d36bcf7edc445fc7bfd81c093357d4cae4add896681daa5a85d78bf8`  
		Last Modified: Thu, 06 Jun 2024 22:17:54 GMT  
		Size: 11.3 MB (11343137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73339e09c7b935ad8552b51b7f7bf45aae9c1ee3f5bf96ed55cf5e2efe08095e`  
		Last Modified: Thu, 06 Jun 2024 22:17:52 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1358a2fa5ab472605fe5fef972fec21ebbb436bfb0c2eeb0e77ecc10e738e8a4`  
		Last Modified: Thu, 06 Jun 2024 22:17:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a8b4ddcb3c863510955e150418ae14587c00ec15cae9de9146860abce1224c`  
		Last Modified: Thu, 06 Jun 2024 22:17:52 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24abc344bfdcfd7fff03fe469e9f324c18d82d34cef76d70c44319cbdbe3e614`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 1.9 MB (1928514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a68aee9ad35148abd65561bddbbba7a9d82f06d6b9d16a3000b80bdb853b4d`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8969c9812f6c985b755ca3484912ff86dc2a6ba2b239a50961c6ab13ade607d`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab55843d68393b62ae02d3e050f6f7e43510dd2230ba6d951322617b183e9ff`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f66b545319477ccb7784c4c300faa0ee0fab1d059d547672e145ef8c8fedee9`  
		Last Modified: Tue, 11 Jun 2024 21:28:32 GMT  
		Size: 19.3 MB (19270959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:6c7be5e9ee58904858017de212fc55e441cd0bcc1e2de308ad41e467ed971fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2fac98251d553c5fe30414b33384460e86be0a1c38e4855b29d6f35beda5c0`

```dockerfile
```

-	Layers:
	-	`sha256:a21da289605693f46c8c658531c919f72e195af4414c415ae78d0b36e29e42b1`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 7.0 MB (6969446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01153d84581dec6020b76289a5b60cfe20b92dedd8147582c63b6b4c03114d9e`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 36.9 KB (36914 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f1e4b7caa9ca5172e3e4b419d9dec24757ef34d017fc794efa23c08f9ad515ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157505086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058b5fcc628a73fd17b525efc22d61eda2784cbd9af88626d2b05442afb8074b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Wed, 29 May 2024 22:31:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 29 May 2024 22:31:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 29 May 2024 22:31:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 May 2024 22:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:31:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:34:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 29 May 2024 22:34:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 29 May 2024 22:35:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 29 May 2024 22:35:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 29 May 2024 22:35:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 29 May 2024 22:35:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:35:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:35:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 03:08:13 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 80
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["apache2-foreground"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783c0efb0e0053728f3dc715352c794db52befb8a96a9d36e381a2e878d332e5`  
		Last Modified: Wed, 29 May 2024 23:36:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9f33c9ef8240f2ad0b16f166848beeccb6fa495b52f95027c7356497ce753a`  
		Last Modified: Wed, 29 May 2024 23:36:27 GMT  
		Size: 69.3 MB (69330096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a19f46b099bfc8c077ba78448fc56ff7b206058a99fe9c1922276e1e3ecbcee`  
		Last Modified: Wed, 29 May 2024 23:36:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bbd01e08a585f81e9e485fc902a23b98c9140d389d55baf3d8b6817b26418b`  
		Last Modified: Wed, 29 May 2024 23:36:46 GMT  
		Size: 18.0 MB (18022775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f461608f26a3ac754b2acc73496f6e36f3d31fab57124d0a6207762ebd8397`  
		Last Modified: Wed, 29 May 2024 23:36:43 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5292b9590e7156637faca885fdce4cb095964dca24a7fec0426601a68e0fde0`  
		Last Modified: Wed, 29 May 2024 23:36:43 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188acc2405648a1c6c8b015e572b4f1db11e354847060574f946bbd82a18234c`  
		Last Modified: Thu, 06 Jun 2024 21:44:23 GMT  
		Size: 12.4 MB (12438704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4626f73044374b3b0b6e70d31a67e486761cb40424836276ab0166b77996f3`  
		Last Modified: Thu, 06 Jun 2024 21:44:20 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02c8ed7e4bb1896b6c204bb13af949cb1e0df89af67e07f0055a477401f03e5`  
		Last Modified: Thu, 06 Jun 2024 21:44:23 GMT  
		Size: 9.8 MB (9806253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06226ffac0fcd1cca4aeede9c5c3fd401d9af8a66b37cd943b1c872a35f1237`  
		Last Modified: Thu, 06 Jun 2024 21:44:20 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff1c307b2444d51597db632f321fdbbb4c2962354f8a363dfb04f62cdfae2a`  
		Last Modified: Thu, 06 Jun 2024 21:44:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e86be5d8016a59fbb5827196ba392cb92cfff2ac132184b10e2920d99fe3a1`  
		Last Modified: Thu, 06 Jun 2024 21:44:20 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8672d252c6f76d97faf46e9156498618116592f6b178ad970a7e461c77eba6b4`  
		Last Modified: Fri, 07 Jun 2024 02:47:07 GMT  
		Size: 1.3 MB (1309518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e119f22e01c83848059f9040ad122dc077b6510a2fba27f968401794c37c234e`  
		Last Modified: Fri, 07 Jun 2024 02:47:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e1329ad21662efb439823d376c2e8352d986c5068b6ab60e07e47f6f47111f`  
		Last Modified: Tue, 11 Jun 2024 20:31:30 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1326f610536c9b46a7a4c78bc3699902a5506e0017ee404aba6502e4d7449f29`  
		Last Modified: Tue, 11 Jun 2024 20:31:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a354d3d9c7a865ed8a622fbb72a778c9eabbce96535c644b000127c22b5e710`  
		Last Modified: Tue, 11 Jun 2024 20:50:46 GMT  
		Size: 19.3 MB (19270906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:eb4f3a149e0b7adaecb15b3b43f27d9617b9fe024838e104016f256f69f324d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6816190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaff445641767707f17279c56ddd87f06a6c5480ebbcd8435ce809144c123ff1`

```dockerfile
```

-	Layers:
	-	`sha256:1c1f6e28cd50754af5585917c7b0b4fd266a9ac2e26799c3996cd4e6c305f2da`  
		Last Modified: Tue, 11 Jun 2024 20:50:45 GMT  
		Size: 6.8 MB (6779140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23259d54d3986b6122fa6c17d03038c1d3a6fbadf98f25c9bc6f384c29ada9da`  
		Last Modified: Tue, 11 Jun 2024 20:50:44 GMT  
		Size: 37.0 KB (37050 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:647f96c67b2ab6dd9504603153039688365e9050ee343ff6ba005b76a005c597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182275538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f80f12eceb821cca36027ea97c728c79b58d16cc58eb2f99cec2d2a2c7975fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 29 May 2024 22:11:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 29 May 2024 22:11:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 29 May 2024 22:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 May 2024 22:11:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:11:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:14:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 29 May 2024 22:14:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 29 May 2024 22:15:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 29 May 2024 22:15:04 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 29 May 2024 22:15:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 29 May 2024 22:15:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:15:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:15:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 02:45:06 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 80
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["apache2-foreground"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69820fd5190812978fef2cc491c2f8c06ac3033d3a4c5f56a80d6ae159fe721`  
		Last Modified: Wed, 29 May 2024 22:55:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e1819d6521b2eddfd40f5d97089a600f5439c4ddebdb8c31cc4aa9ca7753`  
		Last Modified: Wed, 29 May 2024 22:55:20 GMT  
		Size: 86.9 MB (86940388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792d78ea2ad6c5b68426f2a9c4056f8a82155f13648b7e649e4ed356a5b60441`  
		Last Modified: Wed, 29 May 2024 22:55:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0c08d97689d48f510730d6787145a671c0e3e5da8b0470aa4ca8b8cb960f4`  
		Last Modified: Wed, 29 May 2024 22:55:37 GMT  
		Size: 19.2 MB (19192484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec052db23f8955ad45f93c882a35a2307bcd28293331c3d862c6eee2d3bbf44`  
		Last Modified: Wed, 29 May 2024 22:55:35 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cc20ed957bb3054108a7529d37bc66682a52526a924d640f0edc74043c62e5`  
		Last Modified: Wed, 29 May 2024 22:55:35 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc162ecdceb68fd7ccfc73aaf665f189c15ebaa543b7e7ecf1bcc97d8f4e00a`  
		Last Modified: Thu, 06 Jun 2024 22:24:57 GMT  
		Size: 12.4 MB (12439413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4d5412ff77b832113b64e3e472ae6a0d7095f5048ee38f7bfb7c22e8b09b3e`  
		Last Modified: Thu, 06 Jun 2024 22:24:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af7cd7d2a780035b9c15d6435204677bff134081380d3be5441613596c3b4f2`  
		Last Modified: Thu, 06 Jun 2024 22:24:56 GMT  
		Size: 11.4 MB (11418650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9497dd257230c0315670727db9766fecee2a856b0892f3d7e4f31c8b0a1820e0`  
		Last Modified: Thu, 06 Jun 2024 22:24:54 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5cf0d5de366376e4a59daeaaea2e74910598203287ad398e06b7641194ae57`  
		Last Modified: Thu, 06 Jun 2024 22:24:54 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06f8a79a2ee15ff6e9c3535835c61fa73727302ef54f3d67f63c6f6112adc5`  
		Last Modified: Thu, 06 Jun 2024 22:24:54 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5cfea38256d8a41107d0826d562265f9ab5349e5968ff8a1e531c0bda693e`  
		Last Modified: Fri, 07 Jun 2024 04:32:05 GMT  
		Size: 2.2 MB (2194723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7a564ee9f3b2be3e3de75d4ecfb5fcd6effe73251aa87dbb73eb8002a96f5`  
		Last Modified: Fri, 07 Jun 2024 04:32:05 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639439b1cd5454e004f036e13728c126edf48a3e45f7e3f466bb48d1295ce919`  
		Last Modified: Tue, 11 Jun 2024 20:31:55 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c4e64d4bad7a8a98deab35aa2f52f6900478c1a8912f305071aa397641ef5`  
		Last Modified: Tue, 11 Jun 2024 20:31:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f8c6c8ecf2dfa1f4cce6dea110b9e28aa22254cf627cc635648e7d08d55971`  
		Last Modified: Tue, 11 Jun 2024 20:48:20 GMT  
		Size: 19.3 MB (19270637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:d2dbb0aff99247a23eb73a5a02c492975e0e99d9698a0f0a57da6dbe861a4748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7007770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426f4efe6aa62894199c1982836b9e602224c1ad40a07a7e19df9eb6b0d33057`

```dockerfile
```

-	Layers:
	-	`sha256:79ddd38c1fcde5640ecffdaf3393d800b03e8f8701f4e21c6277e3ab8ffcbca2`  
		Last Modified: Tue, 11 Jun 2024 20:48:19 GMT  
		Size: 7.0 MB (6972543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7aa8d5fa24052e1b90989eafcb85a4a2c03a099da3a14129d708cddd292a616`  
		Last Modified: Tue, 11 Jun 2024 20:48:19 GMT  
		Size: 35.2 KB (35227 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:7f4751be9a5f399471fd4c72a3db173fc04e88f36688e66fedab77b3824dcc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190935646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa4f0274069cb6e7a9ab1a21d0a158548763924fe1f0135fbfecfdce7bfdf61`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Wed, 29 May 2024 22:04:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 29 May 2024 22:04:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 29 May 2024 22:05:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 May 2024 22:05:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:05:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:10:56 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 29 May 2024 22:10:56 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 29 May 2024 22:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 29 May 2024 22:11:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 29 May 2024 22:11:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 29 May 2024 22:11:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:11:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:11:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 04:01:42 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 80
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["apache2-foreground"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473b05e0d1eb51876fcbb7a148d721b1ff42ec2c145ff422a18940d5b5b0e6ff`  
		Last Modified: Thu, 30 May 2024 00:13:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29af9525f2910675085a82f8276034f0ccb853831e92d0167f11078766d3c08`  
		Last Modified: Thu, 30 May 2024 00:13:39 GMT  
		Size: 92.7 MB (92720969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4bfcd2ba0acf379a7ddca2344dcd54aab9c8fb8f5a06ab790be17253d6a60b`  
		Last Modified: Thu, 30 May 2024 00:13:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2382cc2aa3a8d80ebabe475d974e815946e8178ddbbd9761e614130662aa208`  
		Last Modified: Thu, 30 May 2024 00:13:59 GMT  
		Size: 19.8 MB (19764646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf83b9ef186cb996cd3a8f3de05a1fba0d589df5a86c3fbca55b26f6151ea8c`  
		Last Modified: Thu, 30 May 2024 00:13:55 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e1f2672632a4a5ac4658b0a421484d3aef04663ba839ba1aab62a7bae16210`  
		Last Modified: Thu, 30 May 2024 00:13:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78da1fb603c14644f966b77d97cee895d18d90a0eabdea2e29abfc627825770c`  
		Last Modified: Fri, 07 Jun 2024 00:13:39 GMT  
		Size: 12.4 MB (12439530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f1e49dbb83ece6a9c8d99e85dd18a0a356f2526d6b7e63a01318f91a1dc9f1`  
		Last Modified: Fri, 07 Jun 2024 00:13:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a091ee3a6cc74eabde9799093dbf468d4cecf9b764691b9203782f8c38da3bd7`  
		Last Modified: Fri, 07 Jun 2024 00:13:39 GMT  
		Size: 11.6 MB (11586980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811574ecb81a57ffced6628820aa4df7c7570e0b213ca5dba4760e027a6d3240`  
		Last Modified: Fri, 07 Jun 2024 00:13:36 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ddbe2d4210a0d712d5fa7fa8b3102a0c905f3eb4e2f5b13a3fc3266968b6b`  
		Last Modified: Fri, 07 Jun 2024 00:13:36 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb6b586050910a672af2059547ae37adfe94beacf83e5f5e879030ec3d594f4`  
		Last Modified: Fri, 07 Jun 2024 00:13:36 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8edba4ced1eea3a42bc93b0ff25b4e4665a47673779608fe3c11cd0ae7eacf7`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 2.0 MB (1996279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ca16068fcddbdb955d2ec7b4974c7c4671dd0b0dcec48a1229221cfe5dacd`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fe87bf622a15749ddea1be6a9ef4000c5157d488deef71a93a78fd45d4236f`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab55843d68393b62ae02d3e050f6f7e43510dd2230ba6d951322617b183e9ff`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ef8db5bc5614c23646b50101720fd797eba957544c750c740561cb4c5406a6`  
		Last Modified: Tue, 11 Jun 2024 21:28:32 GMT  
		Size: 19.3 MB (19270965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:81ef305248eb56a9a54e78162c36aec394f2ddf86f34d9e2a4161c3e67d87b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6997385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6168d09f8b12728c26bb4435741b976157f05d2c8cec62f7957c26726cefc431`

```dockerfile
```

-	Layers:
	-	`sha256:0f5040b3079d9e920b18ab4ec93c1c4b26c7c2ad98c3414e54daae1bd404d210`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 7.0 MB (6960528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce5a905c02407d3079c515a8e464ca3f2fcdb1c266d7a9605f2eec4a195dfd2`  
		Last Modified: Tue, 11 Jun 2024 21:28:31 GMT  
		Size: 36.9 KB (36857 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:797e43d0689e009f6a56ae16201b584bc32ac0949bb555de8f7e9bd5e4cabb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.5 MB (188491196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8fdf078efc2017295038541234a70a747dbad73491a0bd91824fe1930ec81c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Wed, 29 May 2024 22:48:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 29 May 2024 22:48:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 29 May 2024 22:49:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 May 2024 22:49:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:49:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:52:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 29 May 2024 22:52:37 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 29 May 2024 22:52:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 29 May 2024 22:52:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 29 May 2024 22:52:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 29 May 2024 22:52:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:52:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:53:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 01:59:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 80
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["apache2-foreground"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870ecaba6f0dcf3aec9686524cdde6574efabcb0918d3c0fb7651f07aea89899`  
		Last Modified: Wed, 29 May 2024 23:49:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0778ba542c959742944633ae4bbd1f5d35c0646f169143ef3ec0846d514913a`  
		Last Modified: Wed, 29 May 2024 23:49:35 GMT  
		Size: 86.6 MB (86649195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e023ef0a7a410242e59c2299be274dcf59fef32e150586fe4ec17a6fe6af92`  
		Last Modified: Wed, 29 May 2024 23:49:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8ed135cc75b44be54a73302c0fefac8cfa59112b02082cc479938bf49777ca`  
		Last Modified: Wed, 29 May 2024 23:49:55 GMT  
		Size: 20.5 MB (20492212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad04683574feaf17f529969f55ba92b90d97554cc15383574ecb46d1c1858e85`  
		Last Modified: Wed, 29 May 2024 23:49:52 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6863c4abd0177f57cce4e9c3972bb5cdf5f791b05d7dcd8ed57004480e224d0`  
		Last Modified: Wed, 29 May 2024 23:49:51 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffd611cccf62c98344421b61576c2db19a29a9ad48532a15286740a56739111`  
		Last Modified: Thu, 06 Jun 2024 21:33:42 GMT  
		Size: 12.4 MB (12440001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7ddabdb659264d7faece214b38aba1a08d6576edf41113d634ad8361a2a1d2`  
		Last Modified: Thu, 06 Jun 2024 21:33:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95783f53681c369251aed0014a4a3e06a337303bf7e4b1f33045f5cfa86658d3`  
		Last Modified: Thu, 06 Jun 2024 21:33:42 GMT  
		Size: 11.8 MB (11800997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26807952f8c0b13e4235b3bf1772fa6e8f2892d2a591012f752a279b0adc17`  
		Last Modified: Thu, 06 Jun 2024 21:33:39 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914453899ef044b5e9af297116b3033a107d90ae66c9fd4918e71f16984a96b`  
		Last Modified: Thu, 06 Jun 2024 21:33:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3338fc19124a907bc874ade5fceae3cc2df7c70c4e1af2740b2992ff04e70`  
		Last Modified: Thu, 06 Jun 2024 21:33:39 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cbeffdfe108e43475489f788bfde60420ecba03f6e1e7a8881150a74228d45`  
		Last Modified: Fri, 07 Jun 2024 03:16:50 GMT  
		Size: 1.8 MB (1794327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab695dec382d04b601b87b66e9ef8737a84018873495cf90d8f15bb91150af`  
		Last Modified: Fri, 07 Jun 2024 03:16:50 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90e0483dfd0a9735aa6e96b71a7fc4a94a4f866be8bce8849fcd5e417b348cf`  
		Last Modified: Tue, 11 Jun 2024 20:34:14 GMT  
		Size: 726.3 KB (726348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57492e3054048d5e88cb9a31d00a2c060f427f10a68179bb8cac0b89543bcada`  
		Last Modified: Tue, 11 Jun 2024 20:34:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6b7000aa8007d1fdfa0c121771d85fb4b2fedfc70ebcc893f471b2397803b`  
		Last Modified: Tue, 11 Jun 2024 20:58:35 GMT  
		Size: 19.3 MB (19270941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:71e82bd852a39b8100afec4a8074c50aa0d6420ddbcacba20cab68f3ac9f7d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6970108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76d238beeffd3093ddc4dddb05e55322745265f219e2ea1727ab5ec709f0e57`

```dockerfile
```

-	Layers:
	-	`sha256:f14e98843dc1038624e7abb7820706b62ea89aeb31f7ee4cc76141c8bf5ba8a5`  
		Last Modified: Tue, 11 Jun 2024 20:58:34 GMT  
		Size: 6.9 MB (6935409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfdf90849416c998310b9bc9d8a702a80d94ad7d78d97e83a24d53a015c470c`  
		Last Modified: Tue, 11 Jun 2024 20:58:33 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:00ceb88556deb2e537aed6b14020e20afc3b9fb94668214dbdabdb9f41e3c45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (165030248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eedf5b6b3d88cbc1343f3fec8294333c40506e34626a2bdcc2749675b4782c0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Wed, 29 May 2024 22:01:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 29 May 2024 22:01:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 29 May 2024 22:01:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 May 2024 22:01:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:01:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:05:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 29 May 2024 22:05:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 29 May 2024 22:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 29 May 2024 22:05:21 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 29 May 2024 22:05:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 29 May 2024 22:05:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:05:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:05:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 02:18:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 80
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["apache2-foreground"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898a29f76d4d0e07149c20f50185095d79e6f1159218f74b2d0d08e71cf8ab5`  
		Last Modified: Wed, 29 May 2024 22:43:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7c33406ca7ffd9c4d66dea27b031782b5c4db026f8b9b385eae74c1d7b283`  
		Last Modified: Wed, 29 May 2024 22:43:51 GMT  
		Size: 71.6 MB (71643670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef26c588806de548cb7114b376ceb441832d4daef29f42a66cb35e17f3101c`  
		Last Modified: Wed, 29 May 2024 22:43:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2c9a723c95ac8d4eed1daada684e0dd26883050f765d2fa1eeec59f756fea8`  
		Last Modified: Wed, 29 May 2024 22:44:04 GMT  
		Size: 19.1 MB (19097637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb148aff00dd92d172ffdadcdacef4f5dbf5c734592fb924c854784c9f3a0d9`  
		Last Modified: Wed, 29 May 2024 22:44:02 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030ed7bf8bc6a9db476cc964a9fc5b179ca38f6b19afd59d08da936f618185bd`  
		Last Modified: Wed, 29 May 2024 22:44:02 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743d08425d36eaa939a796874a6e0b0445f003e696431939fd93f26c1a58d79`  
		Last Modified: Thu, 06 Jun 2024 22:04:39 GMT  
		Size: 12.4 MB (12439182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07b03bf321f99669e3b9e067b407d22dbc5e74f8bb128c99e1a6e1a7b79216a`  
		Last Modified: Thu, 06 Jun 2024 22:04:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861a5db73dda7e5ba4b1863e18a789a350b1482d7149555b9298bca3477481af`  
		Last Modified: Thu, 06 Jun 2024 22:04:40 GMT  
		Size: 10.7 MB (10650552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad1c209310d330f6f54d61f4a0074e710f4d5864107cefc9beb7015566a67f3`  
		Last Modified: Thu, 06 Jun 2024 22:04:37 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a9e27ab1184896220dc47076627b254a7f4035d77cb34261b3282f2bef40e7`  
		Last Modified: Thu, 06 Jun 2024 22:04:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1893a781350754389dd696191df50bb0183b819498552eca87b74715852a19ae`  
		Last Modified: Thu, 06 Jun 2024 22:04:37 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec838925d3d315f976b94e9dc4216f129291077ebbab08dbfed108df8fe27228`  
		Last Modified: Fri, 07 Jun 2024 02:36:55 GMT  
		Size: 1.5 MB (1522463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aef9920471600bcea052b3a63f9e3a75e616a13c6a283466bb370976b38bdb`  
		Last Modified: Fri, 07 Jun 2024 02:36:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfefae9290b2bef91ea06edc8956d8c3ea358d433672e4794a12da14f5e3c0e2`  
		Last Modified: Tue, 11 Jun 2024 20:32:58 GMT  
		Size: 726.3 KB (726346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5186d00ccddab0866278978b135eceea7cfbac3c6988811137770eac0cc5228c`  
		Last Modified: Tue, 11 Jun 2024 20:32:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdc16e41e3775bbe35b129b75d7437dc6e0ce33533dcea6dd0b9b34e0b70fda`  
		Last Modified: Tue, 11 Jun 2024 20:57:35 GMT  
		Size: 19.3 MB (19270742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:8a2e48d5e8d9d6d4b6a348d6fa138b907762f55ba22479c69a3a3d761b3c4df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6834998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303600fa6644e0bbdae9cf13f391a3e689d32e9c2b6b1df9661a4cdf77bfa84c`

```dockerfile
```

-	Layers:
	-	`sha256:2f06ef68daba65c2030895f146565704059f2322489a832b7c4cca4a0e826b52`  
		Last Modified: Tue, 11 Jun 2024 20:57:34 GMT  
		Size: 6.8 MB (6800367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574015c2486a50ceecbd65828ca3f8834192883bdd85d91ad12575016bfd1a23`  
		Last Modified: Tue, 11 Jun 2024 20:57:34 GMT  
		Size: 34.6 KB (34631 bytes)  
		MIME: application/vnd.in-toto+json
