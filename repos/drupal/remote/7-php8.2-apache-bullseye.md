## `drupal:7-php8.2-apache-bullseye`

```console
$ docker pull drupal@sha256:d71332e15b04bf5121c57e93545cc373c2b5023ef828f3da8e0c87d3cb1239d8
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

### `drupal:7-php8.2-apache-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:628e33cba546ad5653585cf65b4ff2ca5cc71cf1adc3c290b0252f99502037a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171502917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45bed1651f24e3164fd150ebaec24346cb21ebc2f1c8892f70600473b9c646`
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
# Tue, 14 May 2024 13:25:31 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 13:25:31 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 13:25:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 13:25:31 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 13:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 13:25:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 13:28:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 13:28:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 13:28:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 13:28:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 13:28:50 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 13:28:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 13:28:50 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 13:28:50 GMT
EXPOSE 80
# Tue, 14 May 2024 13:28:50 GMT
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
	-	`sha256:26f09ba36f21b6efe6593fbc76e073d65e4accb3d1420a1a3bb8d919e0188ef8`  
		Last Modified: Tue, 14 May 2024 14:13:13 GMT  
		Size: 12.4 MB (12435902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bb64b5d1d53629f2d880c5ecb8d2ac4279b946087e04d2fe41c36f5d909a6a`  
		Last Modified: Tue, 14 May 2024 14:13:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d77c2a6cfd4e14d573c2d63fff64751f6476e452acec249b6bafcfa35c5ff5`  
		Last Modified: Tue, 14 May 2024 14:13:12 GMT  
		Size: 11.3 MB (11342435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a439dea666aec827e1eced75b0bcddb08a7426e3a350fa595405b29b7c7a73d5`  
		Last Modified: Tue, 14 May 2024 14:13:10 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b1682941759a341bb62793282d7a7fca5a20f1cc9af9a904fe00a989c12353`  
		Last Modified: Tue, 14 May 2024 14:13:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152251cf9d9c70d9fa853f6f4a475013370693bbd3718f1d0c297b874b50ffc7`  
		Last Modified: Tue, 14 May 2024 14:13:10 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8194c488a5583c20ecf8bc7f6531ae52a805b12f708a1af52b0b88457a8c9cab`  
		Last Modified: Thu, 06 Jun 2024 00:56:06 GMT  
		Size: 1.9 MB (1928567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cbec280ba71bf8e9895ebc592aabab72985de3095a92b3d2d264374109cabb`  
		Last Modified: Thu, 06 Jun 2024 00:56:06 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea435bb57f74dd4d3f32a92c3dc211a52173cb95def8783ccda46ea53393a82d`  
		Last Modified: Thu, 06 Jun 2024 00:56:06 GMT  
		Size: 3.4 MB (3427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7d20ef0393ccdeec3510c44bd40922b7b53721620ec415564964705cd21a9e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6932363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5aa5fab31d2e334b4ca6b87313a0003afe9224fb85a259f122b8599f8336383`

```dockerfile
```

-	Layers:
	-	`sha256:46474e4661cf9bbe839bba64c84fb7bf8be441836102d87d03a530797cb91fbf`  
		Last Modified: Thu, 06 Jun 2024 00:56:06 GMT  
		Size: 6.9 MB (6907584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e61a4814529890bfdc8b76963d168f970430bd233123d11661604992cd9661`  
		Last Modified: Thu, 06 Jun 2024 00:56:06 GMT  
		Size: 24.8 KB (24779 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v5

```console
$ docker pull drupal@sha256:df31104dc54f4d7749e0411948645e2b93e3626ffcff2be8d2f6d16310c54ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148867459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fb5e02438301c8bcb86fef71f986c4751dac207d50fe4f96c2178f3608ce8e`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.2.19
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:ea8f9497d112a0fd9bfb36b5f5f09db03b58da89dd66365ba2cd291a073e9201`  
		Last Modified: Tue, 14 May 2024 07:38:29 GMT  
		Size: 12.4 MB (12434249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4ca0aa9fb77f7c97fcf579c8b34ccdee6c2b96482ef31752b193b4b3d87806`  
		Last Modified: Tue, 14 May 2024 07:38:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa3949970fdc8f1cd7be2f80f90c49c427cb4b5f1c1f12a53870a6cc1c6a99`  
		Last Modified: Tue, 14 May 2024 07:38:29 GMT  
		Size: 10.4 MB (10365146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87459f36d8cd65a3c37f9bef2dd12beeb325c391b57b543832078264ed50338e`  
		Last Modified: Tue, 14 May 2024 07:38:25 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51007143e68c5d5e991397754349bf38b3d1471fa66f1a09674c9ede4a1986b0`  
		Last Modified: Tue, 14 May 2024 07:38:26 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e8340a60e987a6e179691f01ab26f7baae0ab3ba0023980e2f4f87f98ce0c2`  
		Last Modified: Tue, 14 May 2024 07:38:25 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1b345c56a06783c6a36b6e8f60a9036e09cfe362932fba95e72758bc2addfa`  
		Last Modified: Tue, 14 May 2024 21:55:49 GMT  
		Size: 1.4 MB (1419116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ed2660502240fc97d79ed5f4c628fb28947644321c2378524b1580a6a98860`  
		Last Modified: Tue, 14 May 2024 21:55:48 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325865275f19e67e1f1b37d52bd40433d0e0f9f838fa1a4c8467eaee9ea9f8ed`  
		Last Modified: Tue, 14 May 2024 21:55:49 GMT  
		Size: 3.4 MB (3425929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f210581173e0ad0399e5bf93053e9c591d7fea19457c96d5597d37d816e57dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6740231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abd3dee6fc47c0e27d7c985b7e6682133e517193541318acbc93ddbff488b6f`

```dockerfile
```

-	Layers:
	-	`sha256:a5387ee1ab5ecf5f0eda54a4a2d63175ae9ebdf1236e52d454312fb49555f0ba`  
		Last Modified: Tue, 14 May 2024 21:55:45 GMT  
		Size: 6.7 MB (6713313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12cbcb589cf102d691280f3c343335d8ffdaf85c1ce40ceb3880455ce5321a70`  
		Last Modified: Tue, 14 May 2024 21:55:44 GMT  
		Size: 26.9 KB (26918 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5698ddbefccc547ba52a0d1f53d09e2881fbd9600179bf6d38a0670083d7b874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140928720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fddec0c3074f8a08ac5151618ad903b0ed78fc87b4f498281801ccf72b5ca9`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.2.19
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:c5ba66df7e5e7ac6556090d57116ce823e82a3a6421b861a30b9573dad88fc83`  
		Last Modified: Tue, 14 May 2024 05:16:48 GMT  
		Size: 12.4 MB (12434210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424100eac67ba274ffd9cbb09d95c531dcbb0f6e8019767c9c6334eca2210a4c`  
		Last Modified: Tue, 14 May 2024 05:16:45 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5b518ebeb4b145e6fecdde06b91cfa4bc7a4a5bcba5c948f2c9f99ddfd69b8`  
		Last Modified: Tue, 14 May 2024 05:16:47 GMT  
		Size: 9.8 MB (9806376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a2d7f913aea683d255f6ed5a72eee9e84730e712268f2438950710d25014e6`  
		Last Modified: Tue, 14 May 2024 05:16:45 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6789cb17744b51a81cd862bfbdafc71755618b12eb709beab3b27d20cf33ead`  
		Last Modified: Tue, 14 May 2024 05:16:45 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dfc351167ff6342dc871acd98713d3a8f20b7bebcbebb43addc4e9fa994ad9`  
		Last Modified: Tue, 14 May 2024 05:16:45 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bedebee37c66b18d83b8e36f50afcc3c06b0ec5a5353b10c3b0c545819812`  
		Last Modified: Tue, 14 May 2024 20:47:44 GMT  
		Size: 1.3 MB (1309299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0838a1362e68fde92f5583e0768d2fc5a7ea877c040974a66370aebfa5bf3831`  
		Last Modified: Tue, 14 May 2024 20:47:44 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c0c4a61cb02cb4daab169ae4ee02cbe0d2853e25c37330f8d085dd286c6791`  
		Last Modified: Tue, 14 May 2024 21:13:40 GMT  
		Size: 3.4 MB (3425929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:433bec7422bdf244b02eaec84a05dd4684288563f38357a629f810df5aa56170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6742037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e835dcff9bd48897de411590fe48dbe049fbdd8173f3cd971d2be5f0487b75`

```dockerfile
```

-	Layers:
	-	`sha256:7d26bdab126d5ee9cfbc0c4b3d81900bfda67abd25ec83a4aeaa91d1f6f9d209`  
		Last Modified: Tue, 14 May 2024 21:13:40 GMT  
		Size: 6.7 MB (6717231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a75533836c9ede5182cd90f1cdec28232d15a406ba79e6e8f5bd4b9363b48b32`  
		Last Modified: Tue, 14 May 2024 21:13:39 GMT  
		Size: 24.8 KB (24806 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:662e536d8a505fd95ea96275c81b1828748c14ee1fdad3718ae8d85ca6684344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165698524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da09822a8507f9a79ed2abd5d0b1a08c93862bfb4d9eff6c37d0566979c7e7`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.2.19
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:62d3ef98c52772f96b4d8c57959e8316fef71065b13cdb53a79490b2de659f3a`  
		Last Modified: Tue, 14 May 2024 04:49:50 GMT  
		Size: 12.4 MB (12435111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4417342d52cf883914a2cdb59125a4e678998542c0358d57465d4d3cd18fbb`  
		Last Modified: Tue, 14 May 2024 04:49:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23432ef6800739532104eeb9c5ea09dd2af06ff936772afa23863c0d5ac3d618`  
		Last Modified: Tue, 14 May 2024 04:49:49 GMT  
		Size: 11.4 MB (11417444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661a49f1c46b8c35576da486c4ef37851e15f27d7edf14af1c787dfda7110569`  
		Last Modified: Tue, 14 May 2024 04:49:48 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a963a4a499453f296abbb76ea05a5f51b9fc44aa84c8f350bd1d2204b143b1`  
		Last Modified: Tue, 14 May 2024 04:49:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49d6ae26043f1ba6b1f226951c2af439552bf3f7bec8d38ce98af692485be72`  
		Last Modified: Tue, 14 May 2024 04:49:48 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2a065805667bd11759e6d8c905e8557ec0b41413372dc186d250263ad79bb7`  
		Last Modified: Wed, 15 May 2024 00:43:14 GMT  
		Size: 2.2 MB (2194287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23725e88e29d4bdf6294dcb3846da63951fb6fb9d1859751a69a89bc8092e07b`  
		Last Modified: Wed, 15 May 2024 00:43:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92896f1863590794dfca5fc0ebed8108ebb1814199c3d8826b212f1a8ef708c6`  
		Last Modified: Wed, 15 May 2024 01:25:45 GMT  
		Size: 3.4 MB (3425933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b7ccd104655d5c423d5d1874bdc122e822460eaa878ffc21bfe7593ec75b7b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6935321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6bcb78a4e0c82833ef6fa731874c823b4f61471ce9e76980d45f6294fe5ae6`

```dockerfile
```

-	Layers:
	-	`sha256:af0896333ef13bfbe14232775adda3ff712b6070d68cc4d3b4e4f79cdfbc18af`  
		Last Modified: Wed, 15 May 2024 01:25:44 GMT  
		Size: 6.9 MB (6910585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de3436fe09a74cbd93abd37cc05bca62596dc41e2c660344f940064e14853af`  
		Last Modified: Wed, 15 May 2024 01:25:44 GMT  
		Size: 24.7 KB (24736 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:bbcb822650b583ab30a7b2539b79215d3d908c81b27f42901b5da73d6196d85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174358569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921b0ed045c357bd0409e21be2a3adc412b0b117feb4889c2aa9ec2f365f50e6`
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
# Tue, 14 May 2024 04:19:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 04:19:54 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 04:19:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 04:19:55 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 04:20:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 04:20:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 04:25:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 04:25:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 04:25:26 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 04:25:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 04:25:26 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 04:25:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 04:25:26 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 04:25:26 GMT
EXPOSE 80
# Tue, 14 May 2024 04:25:26 GMT
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
	-	`sha256:20ae68f3342493d170cb6d769712eabe04774896028bdc7e0d07c0645a49a136`  
		Last Modified: Tue, 14 May 2024 05:34:35 GMT  
		Size: 12.4 MB (12435204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78731a58a6cb5049a27a341c988eacc972fcd93bf716fb1a0e80aaafab69b6e2`  
		Last Modified: Tue, 14 May 2024 05:34:32 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6801bb65e16b4d3f62ba45b49c0521db76757005cc6cbf1dd20f725ed76d4475`  
		Last Modified: Tue, 14 May 2024 05:34:35 GMT  
		Size: 11.6 MB (11583531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa3b3263709efff18240e46bd075846c0ef247e71f7dc50cf10102b78cced2b`  
		Last Modified: Tue, 14 May 2024 05:34:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b37e2a7a8942fed177ab9b899886d9b12ae4fc147dbc3e60dadd4170c399945`  
		Last Modified: Tue, 14 May 2024 05:34:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879e398f4dcc40dc588580f2b91500064f50911a9a4011d595ed0dd1e1f93374`  
		Last Modified: Tue, 14 May 2024 05:34:32 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecd4c853b117674b6881cd9a10d8746115c808506000484a1603bea0d3b4275`  
		Last Modified: Thu, 06 Jun 2024 00:56:22 GMT  
		Size: 2.0 MB (1996254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf53b62b395535e769fa94b779fcab41259c81f273223fa958a7f6497dae31bc`  
		Last Modified: Thu, 06 Jun 2024 00:56:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0e6784a46178eb9107770e39d745a611071e96f352bd508a0d75968e40374f`  
		Last Modified: Thu, 06 Jun 2024 00:56:22 GMT  
		Size: 3.4 MB (3427731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:b94587d4532c10a1210f088f740b33fa3da8b4448347c22682c0851b45dae832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6923452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f343224547b32b8990bd1ec4710795c39fd2fab2a29c4891814345532782c397`

```dockerfile
```

-	Layers:
	-	`sha256:b95588d3760e08b5659ee91b6e543fde156525acf711d2f1008d95ab6e1f955d`  
		Last Modified: Thu, 06 Jun 2024 00:56:21 GMT  
		Size: 6.9 MB (6898696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c317f699719ef335182b6591719a503d00b70b2e17aeb4135d871f7f78a773`  
		Last Modified: Thu, 06 Jun 2024 00:56:21 GMT  
		Size: 24.8 KB (24756 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; mips64le

```console
$ docker pull drupal@sha256:adeac307588ad08647c3fb16f14bfa9e582f166b75ba6daa9cb9f2deae3e7085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148072046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5414905ab20e4054e05d2fbb7aa8b52ab32ea75cf0d3273aed2889d20a025`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 14 May 2024 01:12:23 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Tue, 14 May 2024 01:12:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 05:48:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 14 May 2024 05:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 14 May 2024 05:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 05:50:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 May 2024 05:50:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 14 May 2024 06:05:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 14 May 2024 06:05:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 14 May 2024 06:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 14 May 2024 06:06:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 14 May 2024 06:06:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 14 May 2024 06:06:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 06:06:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 May 2024 06:06:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 May 2024 08:10:15 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 14 May 2024 08:10:19 GMT
ENV PHP_VERSION=8.2.19
# Tue, 14 May 2024 08:10:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Tue, 14 May 2024 08:10:26 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Tue, 14 May 2024 08:11:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 14 May 2024 08:11:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 14 May 2024 08:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 14 May 2024 08:25:25 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 14 May 2024 08:25:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 14 May 2024 08:25:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 May 2024 08:25:39 GMT
STOPSIGNAL SIGWINCH
# Tue, 14 May 2024 08:25:42 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 14 May 2024 08:25:45 GMT
WORKDIR /var/www/html
# Tue, 14 May 2024 08:25:49 GMT
EXPOSE 80
# Tue, 14 May 2024 08:25:53 GMT
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
	-	`sha256:9f64bf8dd186218a637a9508ea4ce1fe56bef6d2cac9f35d8042ec643955728a`  
		Last Modified: Tue, 14 May 2024 10:53:40 GMT  
		Size: 12.2 MB (12217984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab46c3ad01485a2d0044f21bbaf306671ff08650a04cb9d25dad7951482bd7a`  
		Last Modified: Tue, 14 May 2024 10:53:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b75302ee5aeb8c2bcd69c01e12df58364e083c396b35540d4576f907be557b`  
		Last Modified: Tue, 14 May 2024 10:53:42 GMT  
		Size: 10.5 MB (10473380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f252a868caea81f9ebcae141912f55868d7bcd35d57910022ae108e439e8843`  
		Last Modified: Tue, 14 May 2024 10:53:34 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070e3b5c4e77e3157c85b932af0e750219303d7109d49ec266083a7ecbb1456f`  
		Last Modified: Tue, 14 May 2024 10:53:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2dd64dd2b4c6b1390111afab992b9feab73a941037ab70ad9e8ea44e3d6015`  
		Last Modified: Tue, 14 May 2024 10:53:34 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6f2639862fec24adf1dfce1248d2ca055834443c5280b73091d470565f6724`  
		Last Modified: Thu, 06 Jun 2024 01:07:06 GMT  
		Size: 1.5 MB (1517916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587bf48c86f8e164af70bb621558e6579483289c58b6d1f5ad2acf7e43065baf`  
		Last Modified: Thu, 06 Jun 2024 01:07:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87917415023ebc57528cc2d04c42a13f73a5a54445894ea772215afc2b04a842`  
		Last Modified: Thu, 06 Jun 2024 01:07:06 GMT  
		Size: 3.4 MB (3427726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:0dabbd641ec0728a6716ca6903507430412881af8966d6293f4a0970a6a0d152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 KB (24605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f52241b30c8bb319afee07e694928e06061ddf287a5b8d468eb52d45abe65b`

```dockerfile
```

-	Layers:
	-	`sha256:369024af59504a0485026a47673c2a490c92b7597a2066cb3d530a36853de2d1`  
		Last Modified: Thu, 06 Jun 2024 01:07:05 GMT  
		Size: 24.6 KB (24605 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:bebd169c17001e07092ac78a18b6060ca1b74fb3ec698120f5d5e7f38cb7b7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171914962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26425c963fd84e3ab560292d504abd38846a22c88214c8885576f4f8f53e736`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.2.19
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:4b5c7ada496af68e0a2d0b07c84d6456985952ce370048fcdab4fb5b80ed2626`  
		Last Modified: Tue, 14 May 2024 06:12:48 GMT  
		Size: 12.4 MB (12435662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f9bb0eb00be5c6f0e1d797ce5836b986af8677a337817f9027fc5911edf567`  
		Last Modified: Tue, 14 May 2024 06:12:44 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308b1db6af89afd3bd68fd1decbc5af6de62ede31e3c3abfa72f13ffb18b9c24`  
		Last Modified: Tue, 14 May 2024 06:12:46 GMT  
		Size: 11.8 MB (11800647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c4d716cf5ba7e3b8abcf648beb863def11927d252b9be9d3eeb18e38ab9429`  
		Last Modified: Tue, 14 May 2024 06:12:44 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef26d8744b28040d944aff41ae7ac667b98ce842bfc640ede533edd641a7173`  
		Last Modified: Tue, 14 May 2024 06:12:44 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf58e42bda1060e6a2e7ddc2a054155519b9551e2e623ab26572886717531eb`  
		Last Modified: Tue, 14 May 2024 06:12:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006ef9ace75bdfb3f7ff2ca2b620bb7a69f3c461271df99e5d3841c21354ddf7`  
		Last Modified: Tue, 14 May 2024 17:08:24 GMT  
		Size: 1.8 MB (1794280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d5e0ce3de8a0181e5170f679fd896d5c9f227455fd792a635d80fd5da22f5a`  
		Last Modified: Tue, 14 May 2024 17:08:25 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b3c6e0b8c5ce46245aa59ea4da078f0e1d3176f0a20d47b8bc92781246c0b3`  
		Last Modified: Tue, 14 May 2024 17:24:03 GMT  
		Size: 3.4 MB (3425932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:73e698658962ed3fe9e99376a4a5e724f112b22c7a6fdfece800e5ae28a30c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6898271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e8ce35255dedd2055bb03c61dfb6ce3b0bdca9ed61860de21486ca94d97e21`

```dockerfile
```

-	Layers:
	-	`sha256:5740bab3a7d9da1e0b0dc80495b918d9439791c46891c9cb62e0d7c61a631ea8`  
		Last Modified: Tue, 14 May 2024 17:24:03 GMT  
		Size: 6.9 MB (6873512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2bb7f692bd343f57fa5bcefec65b22ea1578f114b7964eedb67fc733f6c1d9`  
		Last Modified: Tue, 14 May 2024 17:24:02 GMT  
		Size: 24.8 KB (24759 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:65d60a743041d28d1fe4605297cd77db0100acb46c1b81bfe63a366f6776dc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148267248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa8ea494a9eff123751c39376474949c8b37eedfabfed1e920b6df81b213cd`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_VERSION=8.2.19
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Fri, 05 Apr 2024 21:55:18 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 05 Apr 2024 21:55:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 05 Apr 2024 21:55:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:1dd89ef5a0cd75f3e9425e57d50bbb0d0a8918004a23628c5f4898c193c41805`  
		Last Modified: Tue, 14 May 2024 02:45:17 GMT  
		Size: 12.4 MB (12434697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa4806e58197a8b6c50a2bf2d3dc26b4342ef7de70a1f53478e5474d33104ae`  
		Last Modified: Tue, 14 May 2024 02:45:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2d7327f1693db161c2686b5e05706d972e99909800b2441d48c38ce3b309a0`  
		Last Modified: Tue, 14 May 2024 02:45:17 GMT  
		Size: 10.5 MB (10464171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1f3dd041cd66f24c2f81b83b6781d1c7a2431656fa641539df558baa03c55a`  
		Last Modified: Tue, 14 May 2024 02:45:16 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0342c451f0521418027128e33db91b71ab161363243016a8d618a45aa6995329`  
		Last Modified: Tue, 14 May 2024 02:45:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4fc4275db9fe252804940bfc29c3faa7f40aa85568fbe62129e0b644c12754`  
		Last Modified: Tue, 14 May 2024 02:45:16 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e76e696a47bf57c5da0b1bf266afb975ce525a15d2f2ab50346b01f9fe539a`  
		Last Modified: Wed, 15 May 2024 01:17:16 GMT  
		Size: 1.5 MB (1522129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986788af57c75e8f3df684a6e47ec0ec8b490d10dfa49bcd05067aa79d7f8709`  
		Last Modified: Wed, 15 May 2024 01:17:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b405a069c9200dbf991dba3e78b46e79290850a8bd7e7ed785fe042ca7d0fdbd`  
		Last Modified: Wed, 15 May 2024 01:34:14 GMT  
		Size: 3.4 MB (3425926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:d2241852d4d96fc1815c94cd3244bbca19e2ee45ea352c251d3ef814527718ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7582400eca6bac97c3fc5e709e900967e6686dfbd61318e10e84dae581a57e`

```dockerfile
```

-	Layers:
	-	`sha256:679815cb189409bfce00357ca94adfe5c8c5f6f5225b345223d236c68583d83d`  
		Last Modified: Wed, 15 May 2024 01:34:14 GMT  
		Size: 6.7 MB (6738506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc20117fe4ac2442c9cbc137876f749a98e65e35851167819684d873fd530402`  
		Last Modified: Wed, 15 May 2024 01:34:14 GMT  
		Size: 24.7 KB (24730 bytes)  
		MIME: application/vnd.in-toto+json
