## `drupal:7-apache-bullseye`

```console
$ docker pull drupal@sha256:de90ab5f9f35390a5fca7f468b7ac403c0f608821fbf6842dc6ef6f13e368a38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:7-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:dc9cbaeec850c18e6a3d604855d2044c4ecc17ca5d2f15751c40bfe5bcdc0f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170998438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575294af986deaa0dc4e06b43e1a0545c3a617be68b48839563586afcbaf29c5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:51:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 12:51:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 12:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 12:51:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 12:51:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 12:56:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 12:56:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 12:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 12:56:13 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 12:56:13 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 12:56:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 12:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 12:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 13:55:13 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 14 May 2024 13:55:13 GMT
ENV PHP_VERSION=8.1.28
# Tue, 14 May 2024 13:55:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Tue, 14 May 2024 13:55:14 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Tue, 14 May 2024 13:55:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 13:55:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 13:58:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 13:58:37 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 13:58:37 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 13:58:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 13:58:37 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 13:58:37 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 13:58:38 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 13:58:38 GMT
EXPOSE 80
# Tue, 14 May 2024 13:58:38 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42384b2e40755c8835bac1e8a80bcf7705b651b682e295b474aa2eb8dacc67f`  
		Last Modified: Tue, 14 May 2024 14:09:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edafe777f0df7412759a4528b5a09abb9ecb8ed5ea6b3fe4390ce4274ce52f6`  
		Last Modified: Tue, 14 May 2024 14:09:57 GMT  
		Size: 91.7 MB (91651595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d174440dfd58b85adb34f55a3daa0c72f18275045621f3031b4144bd03020ea4`  
		Last Modified: Tue, 14 May 2024 14:09:44 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef97632441472f9a7056d7f37539f8e4b327ae94f0aa12ba1bd2ad34fcdd26`  
		Last Modified: Tue, 14 May 2024 14:10:25 GMT  
		Size: 19.3 MB (19276883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d3609832af175b20845b3bebdd5f037ea79b6d9426caaefeee5eb214dc9344`  
		Last Modified: Tue, 14 May 2024 14:10:21 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c64fe3ac3a07c758b9467a289146bd76cf7c34fef4ec2979faabc5ce3db99a`  
		Last Modified: Tue, 14 May 2024 14:10:21 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554df5e52b83cd6f05bb6394b694a51e61ccc1b351251d751cfe402fa07b9c7f`  
		Last Modified: Tue, 14 May 2024 14:15:40 GMT  
		Size: 12.2 MB (12190658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d58db902fe7c2d7949f913f1e12e8b98c219391cac337aa02b6e5e5e53117ea`  
		Last Modified: Tue, 14 May 2024 14:15:37 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a1c030a1553ee3dfefd268a4babe8ea919d88187d40a2e940023dc6c911bd`  
		Last Modified: Tue, 14 May 2024 14:15:40 GMT  
		Size: 11.1 MB (11087352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793af84fb08424d5bfad31acef3ac804df182a9030a2e387964e1ba2bdca3f5`  
		Last Modified: Tue, 14 May 2024 14:15:38 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0e300e0a43b86652d4ef1158027de14f390e39d999256996411fc798dd74c2`  
		Last Modified: Tue, 14 May 2024 14:15:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a43f1b3447392f483b4eadc0e008d009e9e849f174141885ad187183b36e382`  
		Last Modified: Tue, 14 May 2024 14:15:37 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb2ff9d3f2383bd3033d7b48de87e9ea0cc03e6600e10717a440a4a196539ad`  
		Last Modified: Thu, 06 Jun 2024 00:56:15 GMT  
		Size: 1.9 MB (1924405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c348416b202d9d0312657ff6b804520608154f0724588c66b222d38453574f2`  
		Last Modified: Thu, 06 Jun 2024 00:56:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45783d137722579076526950f412af88ddd8beeb78488adc0cb49699b225131`  
		Last Modified: Thu, 06 Jun 2024 00:56:15 GMT  
		Size: 3.4 MB (3427726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:a7e605e5b94b9c3e0dfec2512f9cfad0858a4450b5cab63500a6c15bc8406638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6933659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf0a95233da9db3229a1e8a8f55b923d15f83e2e3d9cb7bcfb1b9a901242294`

```dockerfile
```

-	Layers:
	-	`sha256:acb087121d200e690af2b26f0bc72798465699fc34bac8a43d763a789b9a0f43`  
		Last Modified: Thu, 06 Jun 2024 00:56:15 GMT  
		Size: 6.9 MB (6908232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16b1fda15be85a5a305415b61b10d1e560d661223ccfecfb92b2362a328c53a`  
		Last Modified: Thu, 06 Jun 2024 00:56:15 GMT  
		Size: 25.4 KB (25427 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; arm variant v5

```console
$ docker pull drupal@sha256:a3905c120449c4c4f95fc8f41fe4a50ab85d2f188db63742150a5978de964e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148353907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d432831c14229ee0e9cbf92aeec5073085521238be0b89b26b290c175cc922af`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.1.28
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=7.100
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5254867beca08309dd265dc965ae6a45917711e6ab265247a35bc70002203c4`  
		Last Modified: Tue, 14 May 2024 07:35:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f0b52fdd6780a9a7bc8f69c8f4fd6e5b17e40bb2edaf1aab319712aac4247`  
		Last Modified: Tue, 14 May 2024 07:35:35 GMT  
		Size: 73.7 MB (73699404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e889983969fef452a702ac36c006bfa3cd58df33304ee140d9da004d401934c8`  
		Last Modified: Tue, 14 May 2024 07:35:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd94103e02c67cda82605a17143c840ee71a818d380ebe14bbded97fe0ab1db7`  
		Last Modified: Tue, 14 May 2024 07:36:02 GMT  
		Size: 18.6 MB (18581002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2aab7a245566120232f38b86e7d198e39ca70206d4c46f3265add1bd0ae9c`  
		Last Modified: Tue, 14 May 2024 07:35:59 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f15f92c0df288635171bc23082f9640c047af14101d225e643e7b525f9ba2d`  
		Last Modified: Tue, 14 May 2024 07:35:59 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0855b1159201698a091e2836fe340963f9cce6d13b76538f682c129b250ed79`  
		Last Modified: Tue, 14 May 2024 07:41:09 GMT  
		Size: 12.2 MB (12188987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385d8852dc750dbbfe49336f07390a6038cd75425ad6a5d8f61126381ed1f160`  
		Last Modified: Tue, 14 May 2024 07:41:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359ebefa02ed53c92ac3ddd2c4976875debd311041df0eb1b3c9b764527a801b`  
		Last Modified: Tue, 14 May 2024 07:41:09 GMT  
		Size: 10.1 MB (10105094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d68648d3bf4f10edc4d40a5247005e5c08ca2bd90c56b3c9e5ba5f58c0cc1c0`  
		Last Modified: Tue, 14 May 2024 07:41:07 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbe11bce04de3df0bf14f03c2fbf85235479eead9ff9f05d992aa6a84440ea6`  
		Last Modified: Tue, 14 May 2024 07:41:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732caa9cf45879d971862e4a9e1aad0149ec6d2dde31e134aac78f775088c6ff`  
		Last Modified: Tue, 14 May 2024 07:41:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ed779d1c5a760b650f83e924a70583a7a0d737628334b84d9cbe98ddcb401c`  
		Last Modified: Tue, 14 May 2024 22:07:22 GMT  
		Size: 1.4 MB (1410878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7075e5d78958fd60b8be8aee61673b614ffd8f2b3f53a7d22fda0e6bb5e8216d`  
		Last Modified: Tue, 14 May 2024 22:07:22 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11761637d84dfe92035cc1da06caf498a0b4be7bb949cb19925ec737e43ce317`  
		Last Modified: Tue, 14 May 2024 22:07:23 GMT  
		Size: 3.4 MB (3425927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:22f20d40d0e7f3a4a53bb6f6d13437745cd2e2ddec31a65996e39aa62082521d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f448f82219e495838ffdf622d79f54fe2d058076d3d8e66d27c687d34cb39e84`

```dockerfile
```

-	Layers:
	-	`sha256:392e0f4032caa5bb842ac9cff30295fcd3102b174e00dca9ae9fa50a5e6feb37`  
		Last Modified: Tue, 14 May 2024 22:07:20 GMT  
		Size: 6.7 MB (6713977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b76ccd7b9ca63eaba753a90dd0791f8f97b036723aaa9a61a762028a144bd774`  
		Last Modified: Tue, 14 May 2024 22:07:20 GMT  
		Size: 27.6 KB (27582 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:7d54b96a98244c6b880c17298aeecf01b7465b453d5dd36a367bfe2a7920d482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140437369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5aa82e4dc88d4887007f092f8150d68d861bc461c4f06eaf034637435f30875`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.1.28
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=7.100
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc05c17fa2e8a7259d0f0b9a9ea374677de4ac1ba6e6ad81dc15efbee63b709`  
		Last Modified: Tue, 14 May 2024 05:13:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd171ab1151439b2197fbcb9ab871b837749f7e4a1e4edafa401e1e3926bad9`  
		Last Modified: Tue, 14 May 2024 05:13:27 GMT  
		Size: 69.3 MB (69329838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d371af7d2ac5d293924b8d6645812e55afce249f1fed3719a72568ded90e5`  
		Last Modified: Tue, 14 May 2024 05:13:15 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed6bf1ce0b26af0b14343cd55a854d70c0fe6b68e3af3799cbeb28bf702705`  
		Last Modified: Tue, 14 May 2024 05:13:54 GMT  
		Size: 18.0 MB (18022703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6af76741dc3579f16c546179dcb4aee04d109a5ac1eef79e1c528e34472eab`  
		Last Modified: Tue, 14 May 2024 05:13:51 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11059d205725cbea02893b2033bb7cf9890ffcee76d7cec4842a418614c73be8`  
		Last Modified: Tue, 14 May 2024 05:13:50 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65977f5ea80127eddbd30eea4f260245695425dcd2571e6261c806b41b31c3b4`  
		Last Modified: Tue, 14 May 2024 05:19:11 GMT  
		Size: 12.2 MB (12188958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91de6066901b00b796c6961a6d0979ca1a8ecbf1d4fa216745f0f49b9ab3ed3`  
		Last Modified: Tue, 14 May 2024 05:19:09 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfde2c6e3ac642e5fd887ed18bdd61cf3d4ce509aa204a51336f2679b74f1e5`  
		Last Modified: Tue, 14 May 2024 05:19:11 GMT  
		Size: 9.6 MB (9570536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6424a5d728fc03cb8bc197af52468aa0ae7ed93ea902fb01cb691112072ba4b5`  
		Last Modified: Tue, 14 May 2024 05:19:09 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667d5d78397f0e1edba598668174da0e1852c5e4645562dcd9fd81f5074c64bb`  
		Last Modified: Tue, 14 May 2024 05:19:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6cb8048a50140431fa4e45ba9d99a1db2e37900ee02f00ff66a09f42cda90b`  
		Last Modified: Tue, 14 May 2024 05:19:09 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9e7b0bb826d9d31f76c966432ff968a4b64c6be435bc833d8d0a77876c85fc`  
		Last Modified: Tue, 14 May 2024 21:10:17 GMT  
		Size: 1.3 MB (1299029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed93b75e07fe1dc0d4a2147034b9d34b168f1135db5395723faa7538b4fe0894`  
		Last Modified: Tue, 14 May 2024 21:10:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85849f6c4cf6f5880bc4af9e43b259f7e9caae909353da156531e016dcdef24b`  
		Last Modified: Tue, 14 May 2024 21:16:03 GMT  
		Size: 3.4 MB (3425928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:24e72e9b4ed30a14c448dcbda0dfe1554da0cc2b1a11b9b85990e0e3c1a8cfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6743365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087b40d9ddefb32cf7f802f145fde3da56238e306c7b6929053d8cbe0a53ad20`

```dockerfile
```

-	Layers:
	-	`sha256:f913e6e6cf584f54279ea2e0fecfc6c9d0ff5d864cf20158a90ca955bc638bce`  
		Last Modified: Tue, 14 May 2024 21:16:02 GMT  
		Size: 6.7 MB (6717895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfabb938a265cf1e31af7f4aa36c6c3226e86b16f73b1c71b08298f1f082ac67`  
		Last Modified: Tue, 14 May 2024 21:16:02 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d91a7e5211b0a672474b43b0bd1dd3a4cf74bc39b3913f25b851eb2947c1115a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165180667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1ff2ef2eec14452a7bd64ab0245cc4cb5724f5e31834aadfe35835535592b5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.1.28
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=7.100
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b28d5ff525366de7bc2d606257dc27f5b0e6adebb1a1c5a15170baa7cf734`  
		Last Modified: Tue, 14 May 2024 04:46:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc83af822564e6b97596c5376f64e10e44a15e638d26d1dccba0a300a1ef5c6`  
		Last Modified: Tue, 14 May 2024 04:47:00 GMT  
		Size: 86.9 MB (86940379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef548a71e6eb619804a740361b4c74d6bd6cf98aed9eb2e52ea18ba9810208d`  
		Last Modified: Tue, 14 May 2024 04:46:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9a81e5f58429a5d71dde8f1852a1c5208c267912bc1a7eed68faebb587351d`  
		Last Modified: Tue, 14 May 2024 04:47:24 GMT  
		Size: 19.2 MB (19192587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30700c97ac4ababac88619a3d09dbb08d5ca8144c867ffa6a7ba4f4d182543f9`  
		Last Modified: Tue, 14 May 2024 04:47:22 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3670334f1080ea95dea7daf00d49b4e2093332b336c37175480d2dbf439c135c`  
		Last Modified: Tue, 14 May 2024 04:47:22 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86dafa80080ed59c604dcad980f6764dd12afee16d049bad2503c2192ff20d79`  
		Last Modified: Tue, 14 May 2024 04:51:59 GMT  
		Size: 12.2 MB (12189848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b534f8b7f3457e799133ce768cdc8fb4efd274ff3d610b01d29faa8d2dfa70`  
		Last Modified: Tue, 14 May 2024 04:51:56 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f7977a9b408225777509e37725edc78c42ac05bca900274dd970b3fa5628`  
		Last Modified: Tue, 14 May 2024 04:51:58 GMT  
		Size: 11.2 MB (11153092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c1d451b1f4a11e49da017217505747841d4349afb78c083fedec0ff7d54791`  
		Last Modified: Tue, 14 May 2024 04:51:57 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e683d1ad8812640a8f091def53b37d524aa288491fc0552822257b9003b637e4`  
		Last Modified: Tue, 14 May 2024 04:51:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080ed3dbf3866bd31e60601d1428f94d5b3a636f8f13a57abbcf1e9abe43e1fd`  
		Last Modified: Tue, 14 May 2024 04:51:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a5f7e136577e880a98aaceaafa21ab3cb64cc5c24bbfac02a4634d5e133e76`  
		Last Modified: Wed, 15 May 2024 01:21:37 GMT  
		Size: 2.2 MB (2186048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ade2c5e0d5fb33f79f2c09b0701de04f3d9ce4df7bc1db85e98a933fc909bd`  
		Last Modified: Wed, 15 May 2024 01:21:38 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120c838319977ebb37bac50e4bcd4552ba3d985fdd5e0d5981a11af12f391426`  
		Last Modified: Wed, 15 May 2024 01:27:25 GMT  
		Size: 3.4 MB (3425931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b4a210ab6e2c9cc3cbe2f9084b1ea17b5a041bd7a321aa149b8e34a68a536fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6936625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061d739ebe7c7c6f04c83f606452b1dd8c22e54479b895a84950100664b1ae65`

```dockerfile
```

-	Layers:
	-	`sha256:f2be39206153e5d2d3cb69f7bf49a2b6cbb2f79b1bf613f63d46dc7a2f3dfe40`  
		Last Modified: Wed, 15 May 2024 01:27:25 GMT  
		Size: 6.9 MB (6911237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22ff96320fcd592beb95bfa11ea4468b3a5a16c4be1d58628e15190def01fc1`  
		Last Modified: Wed, 15 May 2024 01:27:24 GMT  
		Size: 25.4 KB (25388 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:a51f2a3a2b1d363b36186e04ce3f9f7a2312266c7e3d7aab78dc43e69fb70f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173843888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b0f23d1e7a4286bb8fe8f2d84d701345dd552c1aa3341c6118c2424000fc36`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 00:47:34 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Tue, 14 May 2024 00:47:34 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:23:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 03:23:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 03:23:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:23:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 03:23:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 03:29:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 03:29:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 03:30:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 03:30:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 03:30:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 03:30:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 03:30:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 03:30:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 05:09:42 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 14 May 2024 05:09:42 GMT
ENV PHP_VERSION=8.1.28
# Tue, 14 May 2024 05:09:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Tue, 14 May 2024 05:09:42 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Tue, 14 May 2024 05:09:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 05:09:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 05:15:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 05:15:13 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 05:15:14 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 05:15:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 05:15:14 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 05:15:14 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 05:15:14 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 05:15:14 GMT
EXPOSE 80
# Tue, 14 May 2024 05:15:15 GMT
CMD ["apache2-foreground"]
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_VERSION=7.101
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.101.tar.gz
# Wed, 05 Jun 2024 22:17:43 GMT
ENV DRUPAL_MD5=ddcd8cb4e885ae865a3d1a8b06707a67
# Wed, 05 Jun 2024 22:17:43 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddf9fd35283eb25ec0ef16228354456ab08998fb0a17cc37ebb5b807eba2733`  
		Last Modified: Tue, 14 May 2024 05:30:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ce25874fbfc1a8c7598ac13b3f1442d82f74b0fa671a791ebeb9fcc4092ea`  
		Last Modified: Tue, 14 May 2024 05:31:03 GMT  
		Size: 92.7 MB (92721090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20da8d4cca7fab299f2a4227321205c6828eb67210482a17471aa2ea928a1f00`  
		Last Modified: Tue, 14 May 2024 05:30:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6554b49d94dc7f4eef55ed0531aa1fcee7260a13cc2b01009c7c0e0bffb8eb`  
		Last Modified: Tue, 14 May 2024 05:31:32 GMT  
		Size: 19.8 MB (19764835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf98d0caf36f4eef4e41c9827e7ead2835df3a96d37b8e519b463c3677e74db`  
		Last Modified: Tue, 14 May 2024 05:31:28 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35741ffe8bdbc6d557cc071205b09e98df571002fa3f498f9dcf469ee660ff40`  
		Last Modified: Tue, 14 May 2024 05:31:28 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2d2bf43251b8f00a8c3a80b228b1d1d6b04003cd3b535b4ebb995f411f2109`  
		Last Modified: Tue, 14 May 2024 05:37:20 GMT  
		Size: 12.2 MB (12189953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85669b6daef3024ee9acba9ac1f324a91ac72b3a2882717dc2106808aa328ed`  
		Last Modified: Tue, 14 May 2024 05:37:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145195d610a9c4fff1da778822e58f1e730d2a32d46a241f41a6d5ac6c165c36`  
		Last Modified: Tue, 14 May 2024 05:37:21 GMT  
		Size: 11.3 MB (11318921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144fd77fc5fc198dafa15fc7e566e44decca3765dad0456bb67be3ba0d71855`  
		Last Modified: Tue, 14 May 2024 05:37:17 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30f3fbd145d5c12a2a27806d7b7d9621f4d569e08df2c521a7dacd6efbfcb82`  
		Last Modified: Tue, 14 May 2024 05:37:17 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5843ad85856d7d3c6141c0059d8d83fb70e0914854deab992fe61b478591a7`  
		Last Modified: Tue, 14 May 2024 05:37:17 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7e7ed9363671a1d747d04df1acbed69b1304042c1242619d4d594b0b3d23c3`  
		Last Modified: Thu, 06 Jun 2024 00:56:13 GMT  
		Size: 2.0 MB (1991452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab243178bde1b021d54354973d9fdda67a30af037d9473f097195ececc3e3f7`  
		Last Modified: Thu, 06 Jun 2024 00:56:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1689aa592b23e644b04b7756907b69e4de303cba68ee0241339fd9c92ec351`  
		Last Modified: Thu, 06 Jun 2024 00:56:12 GMT  
		Size: 3.4 MB (3427720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:90f1659f01d80d18958b021b9403564852ebeabf91dab7bc6344fb3ef7f98af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6924728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3572a3cf10e60dfaebcdd36091c33fb5f30dfa3a8b5accc3646118563be2c11d`

```dockerfile
```

-	Layers:
	-	`sha256:399adf72a8ab33b9991b504f8d2b28fdb145ffaa1b2989af3f8c5cbbf69ff061`  
		Last Modified: Thu, 06 Jun 2024 00:56:12 GMT  
		Size: 6.9 MB (6899334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c977455ed4b05208cfd6ec7b5a6bc62f2416c98948ec9a459d1d564d315880e`  
		Last Modified: Thu, 06 Jun 2024 00:56:12 GMT  
		Size: 25.4 KB (25394 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; mips64le

```console
$ docker pull drupal@sha256:354969c5f5448205dcf1dbcb3db6c5f8a0d613a2154f71aea4cb2fc54486a18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147576584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9781db318f08bf300fe6c107954fbae75b952d21e4250e516afc7259b919ebfa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.1.28
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=7.100
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709bd420a171b4c831eab5b1e14a72230265bbe04b9205d95c1a099be17a3bf`  
		Last Modified: Tue, 14 May 2024 10:47:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d14cd9bfda93699c74b4aea7ff746b998decece84e891925b4ca3e6b53b0ea`  
		Last Modified: Tue, 14 May 2024 10:48:35 GMT  
		Size: 71.8 MB (71817635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9873051262b566d610c7d2218a5c16a67069022d0b67a57a212f761a74318bde`  
		Last Modified: Tue, 14 May 2024 10:47:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ad57ebda66e1e7a4656a2dcbc9bec26ba066f5186fed60eb2e547cb252741d`  
		Last Modified: Tue, 14 May 2024 10:49:15 GMT  
		Size: 19.0 MB (18959739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec786dafcbadcea2163d346fbb0d6677ed0755ff181adf3afe0f16e0d664843`  
		Last Modified: Tue, 14 May 2024 10:49:03 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b55fdfdeb4a728ca355deabd139cecd8f489d773f4b6a2c3ef0dd1968cde6`  
		Last Modified: Tue, 14 May 2024 10:49:03 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad213d91e8f1e092ff4c1f9f94e3e4d9431aac48beeddf9e19588cb80c74162`  
		Last Modified: Wed, 22 May 2024 23:28:48 GMT  
		Size: 12.0 MB (11972600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718c4ea7b7a51cf647991aba1edae52636fabdc36b7c598ae97fd5af3872b32`  
		Last Modified: Wed, 22 May 2024 23:28:43 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dec7231d921fc3f2d0f9e7eac7bab9227d028b81a3d1fa6a7dcd9b4d966161`  
		Last Modified: Wed, 22 May 2024 23:28:51 GMT  
		Size: 10.2 MB (10231458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f80aeea2f8909d32cc8b6b600980da20d05fc3c5a9b8a7518d6937da48e6cf`  
		Last Modified: Wed, 22 May 2024 23:28:43 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bd3f26ed72b7d50b90fa726aed4c86baff5a26aaf126150a6b6e756416809`  
		Last Modified: Wed, 22 May 2024 23:28:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e5345d14104c6e4f73624121af19ee17398171cffdea44457b05596a1f894b`  
		Last Modified: Wed, 22 May 2024 23:28:43 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274cb7f2118eb66db8da22af9c9ede83807af99c21f970f0bee09026c1d586f`  
		Last Modified: Thu, 23 May 2024 02:00:55 GMT  
		Size: 1.5 MB (1511562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22796e9a061bb0199a251fa51b6e68d5d4c314052469604c1d53819940072b1f`  
		Last Modified: Thu, 23 May 2024 02:00:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd9b3540ce0b44b013feb8a1f4abc6b3118c460809ad9e26a50d0b3203484f0`  
		Last Modified: Thu, 23 May 2024 02:00:55 GMT  
		Size: 3.4 MB (3425930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:36c619b2e7de21a1269ab388ee229ee3e08312fdb0519c9f723343b4000c6008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015abe844d952c3d8db58d65411b06c761c9495af667b380fdce03f61d2396e5`

```dockerfile
```

-	Layers:
	-	`sha256:119d62d344de6e04d65161cf2d42075307c6686cc72a7d82842f95122f42824d`  
		Last Modified: Thu, 23 May 2024 02:00:52 GMT  
		Size: 27.3 KB (27330 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:e7b98725c972689ec47f334a01f064de91c909e7304475dc0639aa7545420740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171347715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3387ae47217d91b1e811051956016c051ce42c9d2eb3f14103a8ee4a3ba4c8f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.1.28
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=7.100
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78d8c927887dd52e63a5293e85b78b81e421fe974b4b82b151cbf8e69724324`  
		Last Modified: Tue, 14 May 2024 06:09:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4451d0364dcef4cb15db808bb03f5021ab39e88b9bac6086c97a98d6c22e54ef`  
		Last Modified: Tue, 14 May 2024 06:09:27 GMT  
		Size: 86.6 MB (86649174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4d88438080249f84852a32b9ff5adb579bbf163912af81f701470209204c2d`  
		Last Modified: Tue, 14 May 2024 06:09:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c47f0216e727bed9b414e5c6b22df7502b658686393ac7490d93d42b61baf19`  
		Last Modified: Tue, 14 May 2024 06:09:55 GMT  
		Size: 20.5 MB (20492223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d212e4ccc501d35db656447e8d91aad76ecc30ff827906c7d1203f5f00ec19`  
		Last Modified: Tue, 14 May 2024 06:09:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95f5a024058146f633b79f805ef5365f60ac688fa2a51e9dc5fabab9dc7059d`  
		Last Modified: Tue, 14 May 2024 06:09:51 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d110aa5b43e4970aab1ec9cf5090e65900872e4d2220ec3c60fa4b5d72e858`  
		Last Modified: Tue, 14 May 2024 06:15:19 GMT  
		Size: 12.2 MB (12190427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9bf4caf8653a2e6e69fee705d01acb1123ba0da97de36cc19aa5b82e5530f2`  
		Last Modified: Tue, 14 May 2024 06:15:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76142fe338333f9c02d7dc683d92342e4c6783ad53215a13a70f2a2cf401894f`  
		Last Modified: Tue, 14 May 2024 06:15:19 GMT  
		Size: 11.5 MB (11485915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c0d0a86888eac76d4a342bea8101b2819c983a99feda888b61698c0d2fa561`  
		Last Modified: Tue, 14 May 2024 06:15:16 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9765f81807b1e1318f506027f598e64fc270891e54da4fba4889bf5d3bc1214c`  
		Last Modified: Tue, 14 May 2024 06:15:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691e5f6ad302793a1fa08a44f0ffce1e55914f6f8582f6aecf7098ae33d9294`  
		Last Modified: Tue, 14 May 2024 06:15:16 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19f610450891be7b493da43bb0dc9acd4266ea07ea52dfa4fd978649fc539b`  
		Last Modified: Tue, 14 May 2024 17:20:14 GMT  
		Size: 1.8 MB (1787001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdce69ada2a3bf8cdfab69d593d835561b8bb8b995bebc4920d981c0e5392bc`  
		Last Modified: Tue, 14 May 2024 17:20:14 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ab6c190b3546ed8e98476994e63094499580f1b7f12d959aae7fb211e8d3b9`  
		Last Modified: Tue, 14 May 2024 17:26:29 GMT  
		Size: 3.4 MB (3425930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b9b0f976bbe529262f5dd568b7de1f6b2834194a00acfa582f69bbb847056697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6899592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28b16030a45629d981b1e1880e9368aae960532c710dcca1aa63940259de719`

```dockerfile
```

-	Layers:
	-	`sha256:53b78ac017b244a9bf0af58289ebfcb64405f973d41865bc817408060c3a6e3a`  
		Last Modified: Tue, 14 May 2024 17:26:29 GMT  
		Size: 6.9 MB (6874172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e33c7180bc47d70e5a60288f553b700c13a30d53acc9573d56c5190272b661`  
		Last Modified: Tue, 14 May 2024 17:26:28 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:c26842b54b9285fee6c63c49c10a5aefd787861767433c01d9803d97b14e70fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147765569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7daf034887f441c43d89b26cbecd01e931994b46ea7b0fa3b4b0b571ff32ae`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:55:18 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 05 Apr 2024 21:55:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Fri, 05 Apr 2024 21:55:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Apr 2024 21:55:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.1.28
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.28.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=95d0b2e9466108fd750dab5c30a09e5c67f5ad2cb3b1ffb3625a038a755ad080
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 05 Apr 2024 21:55:18 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN docker-php-ext-enable sodium
# Fri, 05 Apr 2024 21:55:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Apr 2024 21:55:18 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
WORKDIR /var/www/html
# Fri, 05 Apr 2024 21:55:18 GMT
EXPOSE 80
# Fri, 05 Apr 2024 21:55:18 GMT
CMD ["apache2-foreground"]
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_VERSION=7.100
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Fri, 05 Apr 2024 21:55:18 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9383ecd0cdb7004ae94014a462d321d45dfff89d96fcc459c574a56c95e76b88`  
		Last Modified: Tue, 14 May 2024 02:42:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa02b0fa1d10e88d7e6b96f9ca05ccd7a11dfc2cad7434a074235b5da1178848`  
		Last Modified: Tue, 14 May 2024 02:42:47 GMT  
		Size: 71.6 MB (71643141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3264a0ddf17e7d4173c491af8551cb2ff25e13b763031b48d65ded20bac6bae`  
		Last Modified: Tue, 14 May 2024 02:42:37 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3642873d30e5ffdd519eab2e0d2259e69bd581ad31af507301a8ee7ba908ad`  
		Last Modified: Tue, 14 May 2024 02:43:06 GMT  
		Size: 19.1 MB (19097642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68045d6b08b0cb8123dfe4a74f980807cc95ecf11736e234a1bf433ab8ad4a1a`  
		Last Modified: Tue, 14 May 2024 02:43:04 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19105d47ab2ddd363fbebecf208150407701effe202512f94f9e932dbc2dd189`  
		Last Modified: Tue, 14 May 2024 02:43:04 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7bf5d76b4334bc28b8dc24b018f5d6058284f17c1e7b9986651b20a4ff3f19`  
		Last Modified: Tue, 14 May 2024 02:47:11 GMT  
		Size: 12.2 MB (12189493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782959d963b013bb14ce03963b473185db271ca83298500e58d0629d24f88b49`  
		Last Modified: Tue, 14 May 2024 02:47:09 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3690868b828cb26e6a0087bfb9f0720fd02ed3706a9ab9666a092a9a249ec33`  
		Last Modified: Tue, 14 May 2024 02:47:11 GMT  
		Size: 10.2 MB (10216731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fa3e78d39a5db0b2e2df467f0ce6582c6121957e71468a5770db57de7948b9`  
		Last Modified: Tue, 14 May 2024 02:47:09 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10129e40224e963b2abf554dc9f3a277d8c04406e2fd4a18dda92328fe16294`  
		Last Modified: Tue, 14 May 2024 02:47:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47f22f89efdeee80232756707e1e56c378c92dcd4790d80f0685c378245c7c5`  
		Last Modified: Tue, 14 May 2024 02:47:09 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fbb5eff848fb1b09b903fb3d4f10a4e584e2eb777b0181efe1aba6ec0fd3bd`  
		Last Modified: Wed, 15 May 2024 01:30:53 GMT  
		Size: 1.5 MB (1513094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaf659031388a3a6a2ffd2f01abd0bdb584107909efaab03adb603b7f5358a2`  
		Last Modified: Wed, 15 May 2024 01:30:53 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5730ed6096ad429092ada37e3c80e78ab8fce69cf0b0932f48ca78e6a0fd4f`  
		Last Modified: Wed, 15 May 2024 01:36:51 GMT  
		Size: 3.4 MB (3425929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:2d2f721bcadfac1f93836f1213f8a28420d51c9167de006ad2c780bc4b13e76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6764532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d10340e595d5c1db45c15cf855970e39c4f856412713c3e6127d9125c456e59a`

```dockerfile
```

-	Layers:
	-	`sha256:c5b773bb3bea2fb8f95de007bff07b1e6a8a1519aeaa00035d509993b3a09fa2`  
		Last Modified: Wed, 15 May 2024 01:36:51 GMT  
		Size: 6.7 MB (6739154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6d57c61f2391780aa743f12329d7b5ec0a9d5d2247f9057cbb5ceb2a1f835d`  
		Last Modified: Wed, 15 May 2024 01:36:51 GMT  
		Size: 25.4 KB (25378 bytes)  
		MIME: application/vnd.in-toto+json
