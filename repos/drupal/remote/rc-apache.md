## `drupal:rc-apache`

```console
$ docker pull drupal@sha256:c6455b1f6d1b714572da22e8e4366141900d5337c5dc7a6b1336792539319481
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

### `drupal:rc-apache` - linux; amd64

```console
$ docker pull drupal@sha256:e36c0afda92dafd63be74289539f05219b4c46e0a556f273c47bbcd528fce7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199586062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f7fcd89aa9a188da319d3b9ef75e8aef8a4c32d94dd7a0db90e4c8a34c4119`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:09:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:09:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:09:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:09:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:13:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 02:13:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 02:13:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 02:13:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 02:13:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 02:13:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:13:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:13:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:12:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 06 Jul 2024 01:33:04 GMT
ENV PHP_VERSION=8.2.21
# Sat, 06 Jul 2024 01:33:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Sat, 06 Jul 2024 01:33:04 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Sat, 06 Jul 2024 01:33:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Jul 2024 01:33:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:36:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:36:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:36:44 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:36:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:36:44 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jul 2024 01:36:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:36:44 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:36:45 GMT
EXPOSE 80
# Sat, 06 Jul 2024 01:36:45 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c1fd48de30b16f5766e6ac96a6fe3c0b3241c34c93fe82ddc8a8536729dd53`  
		Last Modified: Tue, 02 Jul 2024 04:36:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b3bda7c6d1ae6620633030596609872e7f2b102e3f274f02c71ee92e136cb7`  
		Last Modified: Tue, 02 Jul 2024 04:36:44 GMT  
		Size: 104.3 MB (104349018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a68eb681dd3cc5f145cf854bf049843298d6ee06c3259ddff5bf4793710a80`  
		Last Modified: Tue, 02 Jul 2024 04:36:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35406f9afc7f771a49890b78aa21515eb9a55078c04c935db2eccebfa0ee09e1`  
		Last Modified: Tue, 02 Jul 2024 04:37:07 GMT  
		Size: 20.3 MB (20328149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d29e3575095485f641778e00db76200a84450e66c56ade92952177c80038fd`  
		Last Modified: Tue, 02 Jul 2024 04:37:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497b137ced83d700feeac177251b0552c63749019adf459aeb89db255825ee2`  
		Last Modified: Tue, 02 Jul 2024 04:37:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabbc6b5ab09e04935c68a7659c2e80b0b2b41e59d634fdc50b6ec8608a52411`  
		Last Modified: Sat, 06 Jul 2024 02:30:02 GMT  
		Size: 12.4 MB (12439918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ebbd004593003f179658b2562d67a3d42c3c5527763d67d96c142ba25f35c0`  
		Last Modified: Sat, 06 Jul 2024 02:30:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8437f303b6df59ec330d4364e06b4cef7626f22a38b9ecf85d44c5acdc54070`  
		Last Modified: Sat, 06 Jul 2024 02:30:02 GMT  
		Size: 11.4 MB (11404425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb7786e3600f7bb48cd9717d74657073a0f862b1903523e5d41cea499dc284e`  
		Last Modified: Sat, 06 Jul 2024 02:30:00 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f109a68b308f37eae8e4f942024ca0d202bc7964a7468af4261838fb73ae342`  
		Last Modified: Sat, 06 Jul 2024 02:30:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fae4e1410c68bd81131febbe6f042369a95c60b240228299aafa48de444cb33`  
		Last Modified: Sat, 06 Jul 2024 02:30:00 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed40dd9757807f55154a58cccf34bcf528d47af777a53797d2094a05f2796ad3`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 2.0 MB (1996843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1345e85c5920c0c674237ef39e310082e5c2ccc29fce556dfd9e76122aa84ee3`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445fb91d9e40bf0aab0ebd27136b49732f218cfd8c3286d0f238d0a13dc8d7eb`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32fc6a410c3a5ca3f952ad7085df486bb1617287e73c102787e1f5472354e5`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88656cf747a2afd5c1640cb5d9d5842b4ca6b39e3d5779ad55e48d18a0f2d1e`  
		Last Modified: Fri, 12 Jul 2024 21:57:55 GMT  
		Size: 19.2 MB (19209193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:a23558a5c0ffa6383bc302b559bd381e3ca4459decb50ebb9b99b80e669c68bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6829257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b55acdb756fdb3a4ee82ec8129730743c8d4a16212358879d67a660f023ce35`

```dockerfile
```

-	Layers:
	-	`sha256:7be9f959d88da4faca65011379281a3ebc8aa72b5ed5db2a677ced94bc74cb57`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 6.8 MB (6789040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8909d117119408804d1c4279d58882f34c9653b2013e7999c6ff0e365c0a22`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 40.2 KB (40217 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:1ea2acea295ba7c8910f3df193017fead871c19de5a17b31cc88423abc91ea5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163496132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5203093cb6bbc0cb8f71ecca357705fd9218cab9834a3b6e0ff144ef0729fc8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:47:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:47:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:51:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:51:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:51:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:51:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:51:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:51:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:51:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:42:11 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 06 Jul 2024 02:01:50 GMT
ENV PHP_VERSION=8.2.21
# Sat, 06 Jul 2024 02:01:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Sat, 06 Jul 2024 02:01:50 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Sat, 06 Jul 2024 02:02:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Jul 2024 02:02:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 02:05:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 02:05:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 06 Jul 2024 02:05:19 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 02:05:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 02:05:19 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jul 2024 02:05:19 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Jul 2024 02:05:19 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 02:05:19 GMT
EXPOSE 80
# Sat, 06 Jul 2024 02:05:19 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98f2ea35903ab22a64a0b9429586e5ebf253d8f30160f658c9a3e91506b6b4f`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed99c1553b06b60dc38f501a723427469be3c7f305f660c2d3f5c4826636db6`  
		Last Modified: Tue, 02 Jul 2024 03:57:17 GMT  
		Size: 76.2 MB (76166316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff1c809dc06de95648d78a0490826dc9afc53a05c01d001be86b39ec6903ec`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751f0125442586c37682f7ec34b710b4ab71ddc530c91fea2cf2af4901d2a1a4`  
		Last Modified: Tue, 02 Jul 2024 03:57:42 GMT  
		Size: 19.1 MB (19057874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016198828fa6032df9c10ec2e792db92c6a8b19d35a884387328ccb4cb68f19d`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b6f3e158190277e0f0f214b0dc62c26057875ebd2af19ac0a15534c73fb171`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67d49f7b73697acdf6bcc1a9e3eb1ea63a9b27042b8d33b439b997dfdb56d66`  
		Last Modified: Sat, 06 Jul 2024 02:49:47 GMT  
		Size: 12.4 MB (12438316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f12e978cd19aadd065b12b683bac7203a182884f3e58fa2e41db8edfa21088`  
		Last Modified: Sat, 06 Jul 2024 02:49:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a9576c4547f5c978525a2f3440a9fd17b1ec77497b1311d4c482dfece1d1e7`  
		Last Modified: Sat, 06 Jul 2024 02:49:47 GMT  
		Size: 9.8 MB (9820446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80242c861919a2697b121a12df1e45106624a31aa546aa4d30d5daec84ed48a4`  
		Last Modified: Sat, 06 Jul 2024 02:49:44 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7686fa419e0c8029f71848b669c980e438f2370b2c59f1de1be736fd7199be`  
		Last Modified: Sat, 06 Jul 2024 02:49:44 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96c2ebf5f9dd5a35ce959322f3f204130e2ab16a428874e07d047258a15bc09`  
		Last Modified: Sat, 06 Jul 2024 02:49:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf1e1f63381770eb449717cd1b8a9a9d9c9de0a5d67acaeb6a2d6252365ebc2`  
		Last Modified: Sat, 06 Jul 2024 05:24:29 GMT  
		Size: 1.4 MB (1352891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c410e5a24d79d0566478ea9ab9ac9cd635f4a1a878e47029c741c930e09bceb9`  
		Last Modified: Sat, 06 Jul 2024 05:24:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0873b45732dae38618bde4f969c2993576ff2140232a0cf9b9bfd7cbd98a6`  
		Last Modified: Sat, 06 Jul 2024 06:02:47 GMT  
		Size: 726.3 KB (726336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84632445b601a6167af500b6f84e9fc59e65b7c2f5de28080d1078a3d68c68b6`  
		Last Modified: Sat, 06 Jul 2024 06:02:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543cb2824ed69898e6839261f95b2b11f2e4de5170953dfe0e068bb5485e02a`  
		Last Modified: Fri, 12 Jul 2024 22:02:16 GMT  
		Size: 19.2 MB (19209895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:4d50b74e198856f28338199b27c26f86f80f2cc7529f960fda168cbc2d386c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960bb8a3f0e1d5cf729ee60aaa738b7b2109c070a58163f28ad28dafa4f8922`

```dockerfile
```

-	Layers:
	-	`sha256:a74a4e0cdd9711fa17d4b429cbb01ce0dff0041f7586432cd4e3983df628e674`  
		Last Modified: Fri, 12 Jul 2024 22:02:15 GMT  
		Size: 6.6 MB (6605223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1157a908371629541fec4fb6c74dc58a490eef1d5a6050311258818a77e6982`  
		Last Modified: Fri, 12 Jul 2024 22:02:14 GMT  
		Size: 40.5 KB (40489 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:f980666ba5324a24efe12319a8ddfe731be4a0416ffb73f7a68814ac0ab42a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193658283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec1116882d4997f4782e279181dde12635b129b5c57b62441bd4ce10abf45dc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:18:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:18:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:18:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:22:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:22:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:22:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:22:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:19:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 06 Jul 2024 01:39:35 GMT
ENV PHP_VERSION=8.2.21
# Sat, 06 Jul 2024 01:39:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Sat, 06 Jul 2024 01:39:35 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Sat, 06 Jul 2024 01:39:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Jul 2024 01:39:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:43:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:43:01 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:43:01 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:43:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:43:01 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jul 2024 01:43:02 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:43:02 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:43:02 GMT
EXPOSE 80
# Sat, 06 Jul 2024 01:43:02 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d168c82669385a88cb2d49927f5d97a9fd361459c5ba221ade1b4833b14530`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be59d5943ae49be3e4ff309c07ef79eacf2bf161b53590db30e1227422f98601`  
		Last Modified: Tue, 02 Jul 2024 03:36:42 GMT  
		Size: 98.1 MB (98131121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702846940aedcd56970bc052b4e64fa8ff21b12b0a6ba8ca8273f4e256aaedc2`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8911daeb05e620d4f86e6e1800ae61553a08eaf29667c22d5a6bdae9461cada3`  
		Last Modified: Tue, 02 Jul 2024 03:37:07 GMT  
		Size: 20.3 MB (20321495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4028ee2076616a6cf681ab5e49658e589a2d0b1918e9213d61a41938d6b4299b`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4d03e54d8a1108c589658f102c0afa22f96cd422f05ace79e1ae3b68741d06`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf9d317db705ec6b9bdce9b577d6482aa035267167983e339d3163780063495`  
		Last Modified: Sat, 06 Jul 2024 02:34:16 GMT  
		Size: 12.4 MB (12439656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a762a6b11b69ade205e4b57cfeefba812cd226ed91aaaafe1fe7fa3dcdf028c4`  
		Last Modified: Sat, 06 Jul 2024 02:34:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edaecdb14cb165c98dfabd3cff48b04a078f9b6a59d65c5e4c3eb17c1d21914`  
		Last Modified: Sat, 06 Jul 2024 02:34:15 GMT  
		Size: 11.4 MB (11413248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0758b025013d58c22243411654051ac6ef75d2e3b73e8d1c02de38cdf383591`  
		Last Modified: Sat, 06 Jul 2024 02:34:13 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a45469237f099855b690a9bbe620bd1f471bbd7f8f91376b1054771800bfed`  
		Last Modified: Sat, 06 Jul 2024 02:34:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c461d9ba4cf54844c82817ca5707ae134df828bb03b3ab55fc43bbf8c6646e5d`  
		Last Modified: Sat, 06 Jul 2024 02:34:13 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724d25c0b983f99d086fda2096254f1a9b57e3c26d13caee9883461353527cf4`  
		Last Modified: Sat, 06 Jul 2024 05:08:40 GMT  
		Size: 2.3 MB (2253620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382b1dd9eba7c6cee7682d581bcd87012f97b34aa822bd842de03ef1f152d59`  
		Last Modified: Sat, 06 Jul 2024 05:08:40 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391e5e87f4d39019a5aa0871fc3a6aa3546af5cf5709e27f29cd7fd5d669954`  
		Last Modified: Sat, 06 Jul 2024 06:06:10 GMT  
		Size: 726.3 KB (726337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291a1b459516c7145ff970aa9ee4460663176201daa90b7bc0a150ea08a457c`  
		Last Modified: Sat, 06 Jul 2024 06:06:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab23a56d7aed5bbacc36cd629d862370e7e3ad46bff450c2fe0fcbf79711e33`  
		Last Modified: Fri, 12 Jul 2024 22:00:38 GMT  
		Size: 19.2 MB (19210351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:e0c982e68720e34579493e47126a05890cd18dd2a0a4a45dc4150ab986f1dd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6858717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099c368398f065ea891595b4f78e884024f668e928901e40391a86010563f5e6`

```dockerfile
```

-	Layers:
	-	`sha256:387a631ce36b8789f7ea42fda0f38b15d7c2beb331cd9545236164f8da259af5`  
		Last Modified: Fri, 12 Jul 2024 22:00:38 GMT  
		Size: 6.8 MB (6817652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d365307c18ed4edb1d7143413facd9c3c55993b6efc2fe17b4f43cd2eec094f`  
		Last Modified: Fri, 12 Jul 2024 22:00:37 GMT  
		Size: 41.1 KB (41065 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-apache` - linux; 386

```console
$ docker pull drupal@sha256:533fd815b22b51cfdb000c4cee3a525bcf188854d56d125f0bed8dc7950ed5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198573128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6312d951549ab09b1d3d3d914c1b57c4044e00920915d0142523ee0ae1754f6a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:42:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:42:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:42:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:42:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:49:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:49:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:49:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:49:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:49:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:49:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:49:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:49:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:23:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 06 Jul 2024 02:14:37 GMT
ENV PHP_VERSION=8.2.21
# Sat, 06 Jul 2024 02:14:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Sat, 06 Jul 2024 02:14:38 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Sat, 06 Jul 2024 02:14:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Jul 2024 02:14:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 02:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 02:20:43 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 06 Jul 2024 02:20:44 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 02:20:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 02:20:44 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jul 2024 02:20:44 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Jul 2024 02:20:45 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 02:20:45 GMT
EXPOSE 80
# Sat, 06 Jul 2024 02:20:45 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daa048202ff5a552b6eacd27b84297ac780821f0730574f9bb61ed3a6996e20`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d876e28acd3b5f3038bdfb0fb8fe720824179dc347e25e6d745ae512376fa6`  
		Last Modified: Tue, 02 Jul 2024 05:39:40 GMT  
		Size: 101.5 MB (101516977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe24ff1fc83352bac36eafb7daa5d32e7ea2232fe6fef612107fdbd1f81e7c8`  
		Last Modified: Tue, 02 Jul 2024 05:39:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087987d024f8b2145282ca5bfbb784c34ed054bbc454fc96a25334882be4e1fe`  
		Last Modified: Tue, 02 Jul 2024 05:40:06 GMT  
		Size: 20.8 MB (20843476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723ec10434fcdc00676902f705fe56081a8fb0a774cb1a3a00894a4be83d8bf`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f856f33b11561e423f77df5f979a60b6dd4042c3f53df3d21647a29b671248`  
		Last Modified: Tue, 02 Jul 2024 05:40:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a32b0bc789af643a1e48825380f7c44f1cd48a491a96a75de9dc87796431a`  
		Last Modified: Sat, 06 Jul 2024 03:44:04 GMT  
		Size: 12.4 MB (12439213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b8ee9b8256477781c0732be62796031309a5dc12e850600e8c346aa7a2913`  
		Last Modified: Sat, 06 Jul 2024 03:44:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2867cf41d88fcae0343cc6935912e7c85fdd1ec8bc3ceedeadcf325cc9d325f`  
		Last Modified: Sat, 06 Jul 2024 03:44:04 GMT  
		Size: 11.6 MB (11638453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f280e5f3486331123f72b88d0f2c823a694da9f981597fb3c6161b50ba5cbd1`  
		Last Modified: Sat, 06 Jul 2024 03:44:01 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c25865ebe8277f3aa6e3b4ccc1d0430fe6749fecce3ee9c21ed162f66a562d`  
		Last Modified: Sat, 06 Jul 2024 03:44:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd6ad4e6d546308b8936bf7ffcd99e9312bf0257b6e9e41be53353462871dca`  
		Last Modified: Sat, 06 Jul 2024 03:44:01 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6fc4e10f8493daf8f9dd0fc659e6ca349f0e2ff8465001cb42f41b689d892e`  
		Last Modified: Fri, 12 Jul 2024 21:57:56 GMT  
		Size: 2.0 MB (2048372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799b1f3cc915e9c308a4ed97c7eea727ef933a2849804fb01096aa814bd818c`  
		Last Modified: Fri, 12 Jul 2024 21:57:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86fefae5381cf3f225403af060814f3af7920dbf3c6db57c248b307c693283`  
		Last Modified: Fri, 12 Jul 2024 21:57:56 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32fc6a410c3a5ca3f952ad7085df486bb1617287e73c102787e1f5472354e5`  
		Last Modified: Fri, 12 Jul 2024 21:57:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335f40077d670aa547f43fc4390bdce725ddfa4cdb6471141943e14eb3e6b6f4`  
		Last Modified: Fri, 12 Jul 2024 21:57:57 GMT  
		Size: 19.2 MB (19210119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:ca2c7f81fcaf1a4b2273d8c837e77995ebb246d50eaacb8a9350aea2d1baf182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6809835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261656e91726305b9fc6fae5e0a74dbbec2761f35c13ac47e11ff756451bc522`

```dockerfile
```

-	Layers:
	-	`sha256:0f7528e21ba6807918b5724d637724f422fce55b72726cbd2110977f74cc38e5`  
		Last Modified: Fri, 12 Jul 2024 21:57:56 GMT  
		Size: 6.8 MB (6769728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dff5928c404769d3e0756dc2637cca6d09f1f1425f5ec3c328b4d66370f32fd`  
		Last Modified: Fri, 12 Jul 2024 21:57:56 GMT  
		Size: 40.1 KB (40107 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:49f273c900f738f7842d7126ceb75834230c5ce64c7cd05b1665229d5c94147e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204008344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f3a5d7b166fc3bb511f38528e4e95670daaa5f51d5d2e77adfa0179cda32b2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:35 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 02 Jul 2024 01:17:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:10:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:11:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:11:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:14:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 02:14:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 02:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 02:14:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 02:14:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 02:14:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:14:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:14:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:04:27 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 06 Jul 2024 01:01:02 GMT
ENV PHP_VERSION=8.2.21
# Sat, 06 Jul 2024 01:01:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Sat, 06 Jul 2024 01:01:03 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Sat, 06 Jul 2024 01:01:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Jul 2024 01:01:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:04:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:04:07 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:04:08 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:04:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:04:08 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jul 2024 01:04:09 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:04:09 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:04:09 GMT
EXPOSE 80
# Sat, 06 Jul 2024 01:04:09 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609eb2596342a8a7f536a9dbbffcfccaaadff4bcd99626d15c588274979eaf2a`  
		Last Modified: Tue, 02 Jul 2024 04:14:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9e2e6a6e6ca971bb68e9cd39a2e7d46e2bacfa5a93def5ea728e84f1553a4`  
		Last Modified: Tue, 02 Jul 2024 04:15:02 GMT  
		Size: 103.3 MB (103317721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8703185de8bbe987d67d7808f74a14a5bcb767eadd604f0096503f998496675`  
		Last Modified: Tue, 02 Jul 2024 04:14:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bfa1030b231350ace419a1b1cb2251a16babac7f828c4850f38366b1a7319a`  
		Last Modified: Tue, 02 Jul 2024 04:15:27 GMT  
		Size: 21.5 MB (21511668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ed004f3d7d188c082021564296cd592b4b41057f3e2a33679c35c3e7bb1a2c`  
		Last Modified: Tue, 02 Jul 2024 04:15:25 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacb72cfc9dd2acb981ca25b9f1f57e62d7bf82694d0a3219b604b104ba52cab`  
		Last Modified: Tue, 02 Jul 2024 04:15:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c37e3fee8da6c8d21970de5c02ed3f83088406872117358a730ce3b264a2ad`  
		Last Modified: Sat, 06 Jul 2024 01:46:38 GMT  
		Size: 12.4 MB (12439509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc0a4b4e3e06702c136c1d97237f9c1650835af4e11ba3f613196324b925cc8`  
		Last Modified: Sat, 06 Jul 2024 01:46:36 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5982a12ee93d50a939e877fc37f3cba6e8ea9f3029ede48d951bd35e18d77173`  
		Last Modified: Sat, 06 Jul 2024 01:46:38 GMT  
		Size: 11.8 MB (11819519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c9c97bb3b3217eedb4a9bf736fc4c0d28823eb4d9f089fd4cfcf060b182a93`  
		Last Modified: Sat, 06 Jul 2024 01:46:36 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e002c025d9adde2ffb74ce95ad091c4a764ae161b4ec2f0babf2ff3f669c7e`  
		Last Modified: Sat, 06 Jul 2024 01:46:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecab8709ae8c39d000df88457cc106a8a9f8ad2d46d9eee62fb488617679d7df`  
		Last Modified: Sat, 06 Jul 2024 01:46:36 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49e667d456cc3fb6e36143b310bf9310dc5e45f7c14513909e83792bd7413d4`  
		Last Modified: Sat, 06 Jul 2024 04:44:50 GMT  
		Size: 1.9 MB (1854973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe25c025bff08fa0d79703b8b2d774f2b675b8c5eb63af5ea84983e578f73597`  
		Last Modified: Sat, 06 Jul 2024 04:44:50 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da9665b6fdb5547a36f2623c59d77f4ce9dd3e7156fb4780cc71f7b908ec16`  
		Last Modified: Sat, 06 Jul 2024 08:46:08 GMT  
		Size: 726.3 KB (726337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e4b7a78cfe9768adb51226b8fadbbcdcc05d97a45f92adac4acc4230d1a026`  
		Last Modified: Sat, 06 Jul 2024 08:46:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b578533adcb7488c589e19158a5dc9808c38d76aec68f88f555d81e6c2953a`  
		Last Modified: Fri, 12 Jul 2024 22:04:48 GMT  
		Size: 19.2 MB (19210441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:4c67ae92bf88434a7728a05169645939b34696c85d3b16d8070e0ddede58688e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6806830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4052e0f89fd1509b88d547e85fd757237faeafc3308bafe905c22b1cc5d570e`

```dockerfile
```

-	Layers:
	-	`sha256:c4e088ff4b34726cf914e442562e0ef85533280b9ddcf9597fa866e0c67b56d8`  
		Last Modified: Fri, 12 Jul 2024 22:04:47 GMT  
		Size: 6.8 MB (6766423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004cd04b19593f75c2252bc7eaf6f344e84fa88181c2761385705788aeb6e79e`  
		Last Modified: Fri, 12 Jul 2024 22:04:47 GMT  
		Size: 40.4 KB (40407 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-apache` - linux; s390x

```console
$ docker pull drupal@sha256:23232a1eb712fbddddfd3b9fde55ba83c9fb9015445e18b4f8329e1eb057f6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172982378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf1d0de36db7f2547c69f9d695e344219cd9fa6012f4aa99c13941833baa62b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:14:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:14:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:14:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:14:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:17:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:17:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:17:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:17:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:17:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:01:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 06 Jul 2024 01:27:03 GMT
ENV PHP_VERSION=8.2.21
# Sat, 06 Jul 2024 01:27:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Sat, 06 Jul 2024 01:27:04 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Sat, 06 Jul 2024 01:27:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 06 Jul 2024 01:27:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:29:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:29:40 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:29:41 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:29:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:29:41 GMT
STOPSIGNAL SIGWINCH
# Sat, 06 Jul 2024 01:29:41 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:29:41 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:29:41 GMT
EXPOSE 80
# Sat, 06 Jul 2024 01:29:41 GMT
CMD ["apache2-foreground"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9251ecd224e15bee1af8e5d8ed06b4583727d21c25571b0841308fa40637020`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de732a471a32b9581046aa3735f5891fa36c8dc024c7c7a007087dd77b0bd3a`  
		Last Modified: Tue, 02 Jul 2024 03:05:16 GMT  
		Size: 80.8 MB (80817736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f9b6de1c71adae007cab6934b2b7dfe2155be5d6b7fecfea770f4dca1aa159`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac393ffa46cdbdd309e76835caefc39b9a5f28208a5117719850422e50cd1830`  
		Last Modified: Tue, 02 Jul 2024 03:05:34 GMT  
		Size: 20.1 MB (20101995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b9ac198003d25e1ae488b290fbd759f674d87fea5692596dc85177b0ad0014`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe10d7b17a1f1937efded756698b3791c41a781a95ad1f5b3436f29993e08d6`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001ad0031776cbc1c59cfaf531fe968adce5eff9708b472f2dbb5cd8a1c02ce`  
		Last Modified: Sat, 06 Jul 2024 02:10:56 GMT  
		Size: 12.4 MB (12438606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf5e77c6cb140e611f1f6567bf9bdeca69265c27cc6fa26b3c50d26f57cda09`  
		Last Modified: Sat, 06 Jul 2024 02:10:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7b6da7c5dc47a3dfb96ed238f0b6fe3acc401319d03b2706f32bdbb517499`  
		Last Modified: Sat, 06 Jul 2024 02:10:56 GMT  
		Size: 10.6 MB (10639966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889019a4ca3263ec74e7d1fe32492e1f96d294f96a989b42980c8d29179a1d39`  
		Last Modified: Sat, 06 Jul 2024 02:10:54 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8d2423ebcab089af2116f17627bccb5d50b59cdeeee5dd4efe464d99bb9c9`  
		Last Modified: Sat, 06 Jul 2024 02:10:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2361c891e9824c97c5c4fcf8f8d9ab03c3c7460f2b604b4ad7bf36d0f1b67737`  
		Last Modified: Sat, 06 Jul 2024 02:10:54 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db174be96f7694b155b633d5861a74ec23ea3c03847c991e894f68a9dbffddd`  
		Last Modified: Sat, 06 Jul 2024 04:13:44 GMT  
		Size: 1.6 MB (1552343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31993fc5730f51de9783f2ebdcc50e1d498bf304d00e67f18cc3a50aff133a87`  
		Last Modified: Sat, 06 Jul 2024 04:13:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f9b11478355e7743502d0cce1194572aacc3e60bf614a96c415ee40c15441`  
		Last Modified: Sat, 06 Jul 2024 06:01:54 GMT  
		Size: 726.3 KB (726343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec8151025d89d3233a186956ce8a8318662704ce2d8c3dbab9a0b5a80a193a`  
		Last Modified: Sat, 06 Jul 2024 06:01:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596e2d99cd9d9d7cf696cfb85770f054bc37b0ec17967b6d53134e2ef83bfbc1`  
		Last Modified: Fri, 12 Jul 2024 22:04:43 GMT  
		Size: 19.2 MB (19209406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:abbc5334f066e311543a093d6a52ac422ad563da8e9aa8fbbd071b80852748e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218f00c4032ebfdb62f3491056c5f43edd2c3531406db2b4c91e0b81e7f36f49`

```dockerfile
```

-	Layers:
	-	`sha256:2654eff91cdf112eebcfaa5dbb0774ba18f7ecc45db7e1f56bdb2a2f945d48b9`  
		Last Modified: Fri, 12 Jul 2024 22:04:43 GMT  
		Size: 6.6 MB (6631462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19f29ff4c2e558a0dc5dc656313af1f708897528e03732b58cc4d96e7a4f7e2f`  
		Last Modified: Fri, 12 Jul 2024 22:04:42 GMT  
		Size: 40.3 KB (40265 bytes)  
		MIME: application/vnd.in-toto+json
