## `drupal:php8.3-apache-bullseye`

```console
$ docker pull drupal@sha256:49207e8c882ca34855e9187316f9241054c32639a95bb2ac72cf8f838ff10dac
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

### `drupal:php8.3-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:9904a1b2903b77dad613424c9e82d4a5f7ead955b18a187bb2fd92efd2ebb74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188561906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba30a7210cb35e30ac6030664c4453209a3f1675d474751b823b034089847ea`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:29:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 06:29:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 06:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:30:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 06:30:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 06:33:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 06:33:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 06:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 06:33:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 06:33:52 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 06:33:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:33:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:33:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 06:33:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jan 2024 07:04:07 GMT
ENV PHP_VERSION=8.3.1
# Thu, 11 Jan 2024 07:04:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Thu, 11 Jan 2024 07:04:07 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Thu, 11 Jan 2024 07:04:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 07:04:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:07:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 07:07:32 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:07:32 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 07:07:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 07:07:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jan 2024 07:07:32 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jan 2024 07:07:33 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 07:07:33 GMT
EXPOSE 80
# Thu, 11 Jan 2024 07:07:33 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff5e264c0172e546465321c8e7e18d28917d577b9ba9e6683a5ffe99b6aa9b5`  
		Last Modified: Thu, 11 Jan 2024 08:46:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30198f3cbc20934e9ef32fdefef02e3f1003c53e190223e260e5e595a3776298`  
		Last Modified: Thu, 11 Jan 2024 08:46:37 GMT  
		Size: 91.6 MB (91635933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028e119b7673aba33f88294bb94929751a3b1e8a7ab4b84dad067d4358a4b7db`  
		Last Modified: Thu, 11 Jan 2024 08:46:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eaf98ab48938fe76599776001808aeab007ee05867ae3c9c0ec61fc9a9fa51`  
		Last Modified: Thu, 11 Jan 2024 08:46:55 GMT  
		Size: 19.3 MB (19259231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f012fec9a3400565cd26117aba1583f3fef4201593561f44761cebabbebe0d`  
		Last Modified: Thu, 11 Jan 2024 08:46:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4671d4cdd77de421d143743f5140fa3702c1941a83c9829e0851a56f9ba65a9`  
		Last Modified: Thu, 11 Jan 2024 08:46:52 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877d26d50def4a139ca3927cff653886d0371ed3906c4b66309bea62b33e3acb`  
		Last Modified: Thu, 11 Jan 2024 08:50:10 GMT  
		Size: 12.8 MB (12786458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33ea56466d6b7c40f013fef2acbd7621da4e545380b87651ba9b53978e9adcf`  
		Last Modified: Thu, 11 Jan 2024 08:50:07 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84b98b18e143649edb2fd02a251c4dbb0ca62f68794e8d847f36540c1986b48`  
		Last Modified: Thu, 11 Jan 2024 08:50:09 GMT  
		Size: 11.6 MB (11601021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6708f9a581680b53aa4c57e0e9ff7747d7629bfabd11018ae4d974754bdfd8b6`  
		Last Modified: Thu, 11 Jan 2024 08:50:07 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f2d5d1566d6de8c849ec23d9a59bc90607f4572ca82ab4db27c875905b2160`  
		Last Modified: Thu, 11 Jan 2024 08:50:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca32b0ad6b0746e161e25b897daf89e30a7d42a8262b48be47d7fc0d10f452f`  
		Last Modified: Thu, 11 Jan 2024 08:50:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab9b02137fc5139d473fa0cb8d6612c86e6a791811934ab7b099a8b76744ad0`  
		Last Modified: Thu, 18 Jan 2024 01:00:29 GMT  
		Size: 1.9 MB (1930067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5355905da4aec91532f9cab4cc8b7ffcac57de7aca9f505ca5090144b3d372`  
		Last Modified: Thu, 18 Jan 2024 01:00:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7beeb994adc5ebac185f7d6bb7528c76677c5e7030897135db7a93db21e7fb`  
		Last Modified: Thu, 18 Jan 2024 01:00:29 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11284a9d1642c834fe71213d9bf19dfd4a92cb1d28c845e0edd588011a9bec2a`  
		Last Modified: Thu, 18 Jan 2024 01:00:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ada687022237bf798ffaf0d12b9456655891d83468957d23f7147269df677`  
		Last Modified: Thu, 18 Jan 2024 01:00:30 GMT  
		Size: 19.2 MB (19220034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7ab7406fb4e1a476ff7d262b9eaaedc61ea58dadd2821d92143156930cbe11fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6007898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13ad42f57c98a183f78e542b26bf5749c2db0ffebf4edf2680733e4e83d78df`

```dockerfile
```

-	Layers:
	-	`sha256:488d2164fe564a1fc17295a1d3f369a8e4ece2f9c2f054d068fd8e3274a191df`  
		Last Modified: Thu, 18 Jan 2024 01:00:29 GMT  
		Size: 6.0 MB (5968499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0418fde7f844c65a8b44c7ee90746637bf5917cab27782f43a3ef3a4c7921d2`  
		Last Modified: Thu, 18 Jan 2024 01:00:29 GMT  
		Size: 39.4 KB (39399 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a0d090714bde00b086a27bb70e649ad1789a20c2d6ceb3e18d2fb4e2acae5e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157985922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8563b010862f7815971e6338bddb38194f9ad0695512773d58461f9d6fe9e504`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Jan 2024 10:27:22 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Fri, 05 Jan 2024 10:27:22 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Jan 2024 10:27:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jan 2024 10:27:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Jan 2024 10:27:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jan 2024 10:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_VERSION=8.3.1
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Jan 2024 10:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Jan 2024 10:27:22 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Jan 2024 10:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jan 2024 10:27:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jan 2024 10:27:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /var/www/html
# Fri, 05 Jan 2024 10:27:22 GMT
EXPOSE 80
# Fri, 05 Jan 2024 10:27:22 GMT
CMD ["apache2-foreground"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4701722b879f62d8acba3f8f3e1112876a738a749abfbde91ff32668b97cf48`  
		Last Modified: Thu, 11 Jan 2024 11:13:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27838f64e10b5768426c27a39253117c59cb617ecc2fc587aa0bece98752be1`  
		Last Modified: Thu, 11 Jan 2024 11:13:53 GMT  
		Size: 69.3 MB (69323950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810c0b57076bb8a1f72f3f179e7a2e4f0279044a8c0a4db6cef528ffa6f409b`  
		Last Modified: Thu, 11 Jan 2024 11:13:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecc7baa51643afebc5e0413f8d05d0acbf14de84e8c9803df60cd1d9c933b16`  
		Last Modified: Thu, 11 Jan 2024 11:14:14 GMT  
		Size: 18.0 MB (18017964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374cc8ec493398d012ceb45f0bde0f1cefd2293900779585b332fdc7b7e31cc9`  
		Last Modified: Thu, 11 Jan 2024 11:14:09 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b22b3e63f59f773e3514cf66caf552a14afac7d05be7aae1a18debdc685226`  
		Last Modified: Thu, 11 Jan 2024 11:14:09 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d8d907d319b30b10a9de1a385a527611e871bbe35fe1814d6cdef7b4cdd024`  
		Last Modified: Thu, 11 Jan 2024 11:17:55 GMT  
		Size: 12.8 MB (12785237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0350ca48c70a40f4a9ade7accaa31f5267ad33accd9da9c0df040ad4421b7ef6`  
		Last Modified: Thu, 11 Jan 2024 11:17:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0560d7d335fa2ef59c2ad68b595b2ff56f63880e57a96988f083ed7931753`  
		Last Modified: Thu, 11 Jan 2024 11:17:55 GMT  
		Size: 10.0 MB (10037748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9918f6755d135b413b94dbd83483f43b352d66ddbd3912dc7d2946553b54cd`  
		Last Modified: Thu, 11 Jan 2024 11:17:51 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff05e0da909e0be153ff9e26e1587f50cad7209ca815ed6a8925d68813e4f4b`  
		Last Modified: Thu, 11 Jan 2024 11:17:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a8e9b0fb3bbf1a870d8dbe461dac7b8f06814c6e7f6bdd236d141c3d4c2018`  
		Last Modified: Thu, 11 Jan 2024 11:17:51 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d74c31e64846dcf788f7a8c0a2337ae9f588b167b7503dceed2d725fff52e0`  
		Last Modified: Fri, 12 Jan 2024 02:17:14 GMT  
		Size: 1.3 MB (1311102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b57130d7fd574470132c41bdbb0ba99ab4d86314418942f3798604938a6f79`  
		Last Modified: Fri, 12 Jan 2024 02:17:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6af96ef6cd84a77be4a2682ec80222c7a64df34b635405b3fd05632dcc0713`  
		Last Modified: Fri, 12 Jan 2024 02:17:15 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd1a93a62f1e1ee4c762a888baccebdd2c76075e31934c3edb30eb12abbc53a`  
		Last Modified: Fri, 12 Jan 2024 02:17:15 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f42b407512eceb434b91605fffb976ea6347bc7b9dab8b51c34462364f53aed`  
		Last Modified: Fri, 12 Jan 2024 02:17:17 GMT  
		Size: 19.2 MB (19219737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:2e396fee80d6364c886b64debf08103d6b2f8e561874fc5b2d6e167a1cdfe603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5839344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b1054beef26e101d7e72d49e7db7b21a0f1bedd6b77621ae0e0ad94076d1d`

```dockerfile
```

-	Layers:
	-	`sha256:c4e53ca98420d4700b4f3e82d06d812ce2ad09f076811c849ba718a85d453c99`  
		Last Modified: Fri, 12 Jan 2024 02:17:11 GMT  
		Size: 5.8 MB (5802107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb73ee4735d8a51435ce891ff184eb22630c13369fb1036a9d11ab7e9456600`  
		Last Modified: Fri, 12 Jan 2024 02:17:10 GMT  
		Size: 37.2 KB (37237 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:60d44b5527c2c24c79cafd03b97f86b2656104dc6e4f22f367dd94f98dfb0a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182759309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc900a849861f3f5e7230556a6ef88823b7f0ed9cf3c123c10523e32b544f1be`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Jan 2024 10:27:22 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Fri, 05 Jan 2024 10:27:22 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Jan 2024 10:27:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jan 2024 10:27:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Jan 2024 10:27:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jan 2024 10:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_VERSION=8.3.1
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Jan 2024 10:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Jan 2024 10:27:22 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Jan 2024 10:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jan 2024 10:27:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jan 2024 10:27:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /var/www/html
# Fri, 05 Jan 2024 10:27:22 GMT
EXPOSE 80
# Fri, 05 Jan 2024 10:27:22 GMT
CMD ["apache2-foreground"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b5325d41b2385184a6306452d88092af1b9bbfba4f3b0eee422401e32a046f`  
		Last Modified: Thu, 11 Jan 2024 05:47:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4a656112423f6afce0d53ff1563ed8e9094e719e9590770f0eab9c6a89695`  
		Last Modified: Thu, 11 Jan 2024 05:47:48 GMT  
		Size: 86.9 MB (86934767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ace44d987c8de3ac442ad478520d128bad0094fa80c8ac8d7dc5e10d3239209`  
		Last Modified: Thu, 11 Jan 2024 05:47:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963881fd5d9f54e5ca1b0d73c4c96df373b8b4c68a1cdd61d3af11ab9792ef6`  
		Last Modified: Thu, 11 Jan 2024 05:48:05 GMT  
		Size: 19.2 MB (19177584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91087cec2aa1b213cd5a3068f27281814a5b3e676eb2f6bbfec477b4fa373e1d`  
		Last Modified: Thu, 11 Jan 2024 05:48:03 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83e4e1be1e626e407783ca667d5cb594fdeee2ae6018ccb2754dc1aaf8cc8a`  
		Last Modified: Thu, 11 Jan 2024 05:48:03 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166fd22ddabae0b5996a8ff9c3f7ca7097bc4aac060b7c1becac680f5cfdaf08`  
		Last Modified: Thu, 11 Jan 2024 05:51:10 GMT  
		Size: 12.8 MB (12785865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15f64d9faebe7201086ea1327cc8e3b82e0a7d7acc9fba524d974122959210`  
		Last Modified: Thu, 11 Jan 2024 05:51:07 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48544ff6b4176d350252e3497a7b2097a8baf13d1463fc772b1edffe8e294e8`  
		Last Modified: Thu, 11 Jan 2024 05:51:09 GMT  
		Size: 11.7 MB (11672015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37d66a0db13a06a6d83348792653802f7ab4195c12c77e47b017c66282248dc`  
		Last Modified: Thu, 11 Jan 2024 05:51:07 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52c24e5d137a2622e5a651b3c6b493809ba1952ce2b5b36220b07b3f9cbb4d2`  
		Last Modified: Thu, 11 Jan 2024 05:51:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec9f6e036dbd12ddd2922e0d2b154002262526416ed7f7355108fcfd338cc4`  
		Last Modified: Thu, 11 Jan 2024 05:51:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14785b3ffd3d48d9b8c87712202024398b2e982e9945ea575c91e49099ff16be`  
		Last Modified: Fri, 12 Jan 2024 00:46:49 GMT  
		Size: 2.2 MB (2194097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7519f453fb8fde26260a1c19f8c3f16e78c4caf2297d76c799308bb8bea47ae7`  
		Last Modified: Fri, 12 Jan 2024 00:46:49 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae49ec19106166fc58c06ff3992977da3eeda2b6545a0ee692f6cf54d4675a21`  
		Last Modified: Fri, 12 Jan 2024 00:46:50 GMT  
		Size: 705.2 KB (705214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7730775c8fbf458b5297f3b63f39bfc7dd43c16c341cf4395cf4dfe167221b54`  
		Last Modified: Fri, 12 Jan 2024 00:46:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e359bf0e5d03067c29d2224a36a825e7c195030dd546259d6f1a08ae861b9af1`  
		Last Modified: Fri, 12 Jan 2024 00:46:51 GMT  
		Size: 19.2 MB (19219758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7d4073d97962b219343797ed28df5f847cd36641093505de5e770b59f41691e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6007463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1584c92a476befd2069db79322ce64eb1fcf83927480cd5e0b29dd8e3a53690b`

```dockerfile
```

-	Layers:
	-	`sha256:2f89d5899b6707c42b84b018e46fabaf231d0f8939d0a28e5706e86d39ab9339`  
		Last Modified: Fri, 12 Jan 2024 00:46:45 GMT  
		Size: 6.0 MB (5970327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1889a15a9a6ce83b97d03eb564ac8e6b4f088d5ff1e1fbd4fbb14dd08f5fffd`  
		Last Modified: Fri, 12 Jan 2024 00:46:45 GMT  
		Size: 37.1 KB (37136 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:95c93083fef315d0980f175d51fcf4134a934c929f5299ed427255a81d1f7e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191408289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad87efdf0c0ae53f113cce3f1764efdbf25ef3eedde0521c675deee215c8e3c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:39:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Thu, 11 Jan 2024 02:39:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:26:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 05:26:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 05:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:26:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 05:26:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 05:32:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 05:32:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 05:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 05:32:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 05:32:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 05:32:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 05:32:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 05:32:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 05:32:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jan 2024 06:22:42 GMT
ENV PHP_VERSION=8.3.1
# Thu, 11 Jan 2024 06:22:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Thu, 11 Jan 2024 06:22:43 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Thu, 11 Jan 2024 06:22:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 06:22:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:28:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 06:28:22 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:28:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 06:28:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 06:28:23 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jan 2024 06:28:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:28:23 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 06:28:24 GMT
EXPOSE 80
# Thu, 11 Jan 2024 06:28:24 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587efb275ebb74b2c5c7e4487c410281d4aeed19ced5f2582a504c4c690060bc`  
		Last Modified: Thu, 11 Jan 2024 09:13:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66518b377d9afc7d2be5fb2882f5697822432b0fc3141b67a6f49e93efb7801d`  
		Last Modified: Thu, 11 Jan 2024 09:13:39 GMT  
		Size: 92.7 MB (92726316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949f2dd63a58425c29e2f92e53dca3ef43798194a0922ff21cdd4383c4ff57a7`  
		Last Modified: Thu, 11 Jan 2024 09:13:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f817f39508cea3046138ff5d0a4918da094553d27b0656f48184542f292d79c`  
		Last Modified: Thu, 11 Jan 2024 09:13:58 GMT  
		Size: 19.7 MB (19745310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8046853bb5590cea852148e7ab1821fb87a76a5ccd13bbeecaa41d45cdc351e`  
		Last Modified: Thu, 11 Jan 2024 09:13:54 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bf9f1473e891db44de5b90280734858a003ef4764a59a8c500f7557e22166c`  
		Last Modified: Thu, 11 Jan 2024 09:13:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc5c6ee42ec53d9ff841474c566fd7311ae5728adee5ab7bc5e129bfb09830f`  
		Last Modified: Thu, 11 Jan 2024 09:17:45 GMT  
		Size: 12.8 MB (12785869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe30ee33b21fc57cd97d28680a6723ffdf36beda7133aaeeada05686d42a868`  
		Last Modified: Thu, 11 Jan 2024 09:17:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a6c92d4901b75d8ccd89a732b3111ccb1451e5b9ed52fbd7d27d632827e7f`  
		Last Modified: Thu, 11 Jan 2024 09:17:46 GMT  
		Size: 11.8 MB (11819313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2885939ab4460ccce2705ae24dd2ab27cd8e41eaeaa7fc2b2ecc8071ec945d98`  
		Last Modified: Thu, 11 Jan 2024 09:17:42 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d6daa9e8bb27426a656ec98e193bb5c641ff941c00d9b484973783d6f8066a`  
		Last Modified: Thu, 11 Jan 2024 09:17:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7212042ae1497da74c96138e6ac5064b0691de0353fcf6a6876e4672693bd04d`  
		Last Modified: Thu, 11 Jan 2024 09:17:42 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b828c9058bdb59965c6f512c525a649d81293621176de07bf6c7666d637be8a7`  
		Last Modified: Thu, 18 Jan 2024 01:00:31 GMT  
		Size: 2.0 MB (1996862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e246167c63d1bad99fa2e7481b12e37d9240db469f6faecd742bdb775f8c27c`  
		Last Modified: Thu, 18 Jan 2024 01:00:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b91741f059e9ad295cd7675a12213cb93f8884581e927e7c10dc85531fd5640`  
		Last Modified: Thu, 18 Jan 2024 01:00:32 GMT  
		Size: 705.2 KB (705213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c375f45848c14d57e6054f3d3e90527b44ec493c1628613d0c29eb60e878e52`  
		Last Modified: Thu, 18 Jan 2024 01:00:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c95572a991e72619830bbb06df848140f807f85fcf200664a7aeae16bc9bbb`  
		Last Modified: Thu, 18 Jan 2024 01:00:33 GMT  
		Size: 19.2 MB (19220720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a19fcdd6c6086d8d3703cdc3c0ed61f423d28ca4939625e2b148c7649c624bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2d3114a62e6eebc68a81d3222425acd5a762258d870b4ef3f11834c392677e`

```dockerfile
```

-	Layers:
	-	`sha256:c86db5ed00f7a23eee08c86bc3dfb829fcdf10126fb6ae46f1e34cd19b310f37`  
		Last Modified: Thu, 18 Jan 2024 01:00:31 GMT  
		Size: 6.0 MB (5959603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9b578c3c258bd6a6259a599bddad616ac7862b9f856f4970fa834c168533bc`  
		Last Modified: Thu, 18 Jan 2024 01:00:31 GMT  
		Size: 39.4 KB (39362 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:f6dffc0343e1d5a9309b85cb67c156760284684aa80c33488fe46889c1c1e693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188980480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d993179cc391441de7304680310f599920736ceafbe66baf19496a27a83eaf`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 04:36:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 04:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:37:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 04:37:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 04:41:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 04:41:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 04:41:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 04:41:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 04:41:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 04:41:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:41:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:41:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 04:41:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Jan 2024 05:08:50 GMT
ENV PHP_VERSION=8.3.1
# Thu, 11 Jan 2024 05:08:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Thu, 11 Jan 2024 05:08:51 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Thu, 11 Jan 2024 05:09:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 11 Jan 2024 05:09:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:12:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Jan 2024 05:12:15 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:12:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Jan 2024 05:12:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jan 2024 05:12:17 GMT
STOPSIGNAL SIGWINCH
# Thu, 11 Jan 2024 05:12:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:12:18 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 05:12:18 GMT
EXPOSE 80
# Thu, 11 Jan 2024 05:12:18 GMT
CMD ["apache2-foreground"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7190f696a06c78ee7b8deeea3a247e10855f7dd84a61900697e3359f2b9ae3`  
		Last Modified: Thu, 11 Jan 2024 06:48:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a066abb8a86243926ebf74c3212ff59c1482a22c4c7d15cd7405284de0862f8e`  
		Last Modified: Thu, 11 Jan 2024 06:49:06 GMT  
		Size: 86.6 MB (86644384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24429c3ab51c9b2d86867d99d49ce1421723a0d5b783b3a1fdc35ee37c3e1bb7`  
		Last Modified: Thu, 11 Jan 2024 06:48:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab235fcee54ef75691b605c36f973ae4ef670c60c51fc322797a934ed7ccf853`  
		Last Modified: Thu, 11 Jan 2024 06:49:27 GMT  
		Size: 20.5 MB (20475113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d51d2ce52ac2db42ded5f9cc92ab63f93b2ccaa74ad82fc73eec61b31d5586e`  
		Last Modified: Thu, 11 Jan 2024 06:49:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2486e5eebed1eee65cc5d5a20f26fd74b8bc4ba08d1903dc7d10deb2df3a5786`  
		Last Modified: Thu, 11 Jan 2024 06:49:23 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f653422c23afa2a13471c43cbb872cf45991a8927a94412d6b8caae526edea9e`  
		Last Modified: Thu, 11 Jan 2024 06:53:01 GMT  
		Size: 12.8 MB (12786586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb47cc19e0a8fe011d517faf56653d2f5edc6e78fa946bd472d1d1cda7df1b58`  
		Last Modified: Thu, 11 Jan 2024 06:52:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6409f18185e4a6f110973c4cc039cf7016ff0da33367a6096ae54af885427b`  
		Last Modified: Thu, 11 Jan 2024 06:53:00 GMT  
		Size: 12.1 MB (12053615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602961a223de9e9695ca311b4b0cb0a85e379dec9e191c39c6caf16a240621fb`  
		Last Modified: Thu, 11 Jan 2024 06:52:58 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd588e3679537822a332e1bb45331df4a99526fa041a18d32e5d4e14efdf78a0`  
		Last Modified: Thu, 11 Jan 2024 06:52:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f8ae65747bf6c6c5d2423e57a72a3d82dd27e7d3f7dacec8988345d3efa65e`  
		Last Modified: Thu, 11 Jan 2024 06:52:58 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8169e2b469ff7258b6c737935f7357714cdb3c6f30dceefb276858f97fb151`  
		Last Modified: Fri, 12 Jan 2024 00:47:59 GMT  
		Size: 1.8 MB (1794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77189246a21e9de84185ece395100f91a4ac119c800994ebe99263a247ecb97b`  
		Last Modified: Fri, 12 Jan 2024 00:48:00 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c741652419af89fd592281f8bd3e4c008b370eb5222b0814fedb1a70cf447f`  
		Last Modified: Fri, 12 Jan 2024 00:48:00 GMT  
		Size: 705.2 KB (705214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836142bab806ef37e333894bc8fb4e3ddff459fa25e8dc0ca19c3ddb1a9c1f93`  
		Last Modified: Fri, 12 Jan 2024 00:48:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac043d8a8c0fa050b0aa33e9ef9aedf5c9ffb1597d688689149f963c2e8f84`  
		Last Modified: Thu, 18 Jan 2024 01:23:07 GMT  
		Size: 19.2 MB (19220816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ebbd40d878cc7b8fcfd0f4af26b0299efd7c9af409733c046ce215edf0d1ec62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5973155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9bfdfb0516d0599458d55e2a06b9509543a08c66661d57a33d51dcc6fc3d07`

```dockerfile
```

-	Layers:
	-	`sha256:c51cc2b1d3c866653227c18cd41d6c9621d5d7e38a8f86f568ec2644f12b52f4`  
		Last Modified: Thu, 18 Jan 2024 01:23:05 GMT  
		Size: 5.9 MB (5940376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5335d59c8a1fdf726779051b5b9414477d9b060156643ccce2364ec06858dc1`  
		Last Modified: Thu, 18 Jan 2024 01:23:04 GMT  
		Size: 32.8 KB (32779 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:dfb67376f5550ae78ee5a73a4d1ebfe62f7255daaa3b21e90c62e8bd1b708a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165313164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f625f28aceec56e6e17a536d12e7b4348dc91a1abb94a06e5e841d1d7ca49e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Jan 2024 10:27:22 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Fri, 05 Jan 2024 10:27:22 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Jan 2024 10:27:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Jan 2024 10:27:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Jan 2024 10:27:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jan 2024 10:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_VERSION=8.3.1
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.1.tar.xz.asc
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PHP_SHA256=56445b1771b2ba5b7573453f9e8a9451e2d810b1741a352fa05259733b1e9758
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Jan 2024 10:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Jan 2024 10:27:22 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Jan 2024 10:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jan 2024 10:27:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Jan 2024 10:27:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /var/www/html
# Fri, 05 Jan 2024 10:27:22 GMT
EXPOSE 80
# Fri, 05 Jan 2024 10:27:22 GMT
CMD ["apache2-foreground"]
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV DRUPAL_VERSION=10.2.1
# Fri, 05 Jan 2024 10:27:22 GMT
WORKDIR /opt/drupal
# Fri, 05 Jan 2024 10:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 05 Jan 2024 10:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6dbf1cfe3c4cbdeae3c718a8017076eaafaeaa7f851fffee6a65e9b3a26d7`  
		Last Modified: Thu, 11 Jan 2024 08:19:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3af4afd42fce7a72940da0adb8f8d962357fc71a6c302548a904593f830d59`  
		Last Modified: Thu, 11 Jan 2024 08:19:23 GMT  
		Size: 71.6 MB (71635317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9001eb8694075797a2cc406e1174b64701ccf7f9c01a8ebd52c43e3108cf9b2b`  
		Last Modified: Thu, 11 Jan 2024 08:19:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20074705c6c3399f6d059ea4033c3b4c509a462a323e1b81e94b72c7b241988d`  
		Last Modified: Thu, 11 Jan 2024 08:19:35 GMT  
		Size: 19.1 MB (19080566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799aafb91517df33d3bd9f07c130983ba18da3c7fe16743aa414c6bc3548a8d7`  
		Last Modified: Thu, 11 Jan 2024 08:19:33 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cbd41d6d814e4c7ec5edc8871e5e77fec52715281b3073d1a32ab1e4c649d`  
		Last Modified: Thu, 11 Jan 2024 08:19:33 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe5aa54d53bc81eeb6cfff74f6653174e231c3a9fbe4c68ebab1107a17845fd`  
		Last Modified: Thu, 11 Jan 2024 08:21:49 GMT  
		Size: 12.8 MB (12785626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b89510d277f883c5c77ef555e8ca47caed04dc1a5f78a636d24ccaf5eeac19e`  
		Last Modified: Thu, 11 Jan 2024 08:21:47 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc14b7e3058187f29699a0fcfdd250b80316bf8632da2b8f2eaf8c194806add`  
		Last Modified: Thu, 11 Jan 2024 08:21:49 GMT  
		Size: 10.7 MB (10700536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b617fb75dae5754332e30521f2454c07a9d96ba978a8947f60de81b5ddc788f6`  
		Last Modified: Thu, 11 Jan 2024 08:21:47 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0788107b00c160e230bf9efff2001018b70b36ed552ba125ba729d4ba2953`  
		Last Modified: Thu, 11 Jan 2024 08:21:47 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710c1c72fdd9a36b00d9cebd360e3a7243a7c2f1b97e0217d4604350ccfc4545`  
		Last Modified: Thu, 11 Jan 2024 08:21:47 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f9876de6f1e24e4d1dbfe821c131b0cdaac9473c33d242bc0e37db45733f24`  
		Last Modified: Fri, 12 Jan 2024 00:32:46 GMT  
		Size: 1.5 MB (1523327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81b8f70f348b07315b3121f9fcaed53241be1e17c8b63d7e831a89a28d92801`  
		Last Modified: Fri, 12 Jan 2024 00:32:46 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d74c78c5c82c2c2bb9e4063a09ff7829042b821aaa77893dead7c07ce7c257c`  
		Last Modified: Fri, 12 Jan 2024 00:32:46 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b44fef240269b2a0a2356ee42671d68aebc2665e13953e825f1ecdd2511604`  
		Last Modified: Fri, 12 Jan 2024 00:32:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dd859b910c217f694adfb3402ef3556fd6fe8a38c2ecdd79cb50149f679353`  
		Last Modified: Fri, 12 Jan 2024 00:32:47 GMT  
		Size: 19.2 MB (19219706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:0608efd95115b1435bc74a4bc75c9960dc10796e7c854ef32aa621d3b8b79b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350a814fa3c01ac2d95f8652de67f62b292a733d831372e52ce0c79682152245`

```dockerfile
```

-	Layers:
	-	`sha256:19d08425344280f1d6ede7a774256dbfc8a36f92fa2f79969205f710738d1ec7`  
		Last Modified: Fri, 12 Jan 2024 00:32:43 GMT  
		Size: 5.8 MB (5819762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42f592f1fb024b7853df127fa415a99bc3011c1634469c7d0b5c79bda1704a0`  
		Last Modified: Fri, 12 Jan 2024 00:32:42 GMT  
		Size: 37.1 KB (37125 bytes)  
		MIME: application/vnd.in-toto+json
