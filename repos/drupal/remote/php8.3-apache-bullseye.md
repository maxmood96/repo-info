## `drupal:php8.3-apache-bullseye`

```console
$ docker pull drupal@sha256:c1af9d217684f6059de6b8476d9d8d91aa053a041c633ed9a0054a2c8a933cb2
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
$ docker pull drupal@sha256:2c9c322f366e47df38280a2d6060c02025d5e723f79d70c1dec0a715ab7b3f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188604741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2513a04c37011ff6f5cc4bf32e52d702a553621cb884e70b07df2e67b01a242d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 10:27:16 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Wed, 06 Mar 2024 10:27:16 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 10:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 10:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 10:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 10:27:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_VERSION=8.3.3
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 10:27:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 10:27:16 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 10:27:16 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 10:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 10:27:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 10:27:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 10:27:16 GMT
EXPOSE 80
# Wed, 06 Mar 2024 10:27:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV DRUPAL_VERSION=10.2.4
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /opt/drupal
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a110dcb6d2f3bea8c7f86c44dda941c22c88034e199a40fa904ec2e203a23dee`  
		Last Modified: Tue, 12 Mar 2024 05:26:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a676cd3cc4aa867242bce97f4a71ef07fbe9d401ce8f56bef633008f42c9b07`  
		Last Modified: Tue, 12 Mar 2024 05:27:05 GMT  
		Size: 91.6 MB (91639971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0074f28e265cef1b2a0480f04003205964be45768281d74af416ccdda13de198`  
		Last Modified: Tue, 12 Mar 2024 05:26:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a771575b0adf58ab44dcc6e2e209a780f11062dcff563ac25cb3914d972059c`  
		Last Modified: Tue, 12 Mar 2024 05:27:22 GMT  
		Size: 19.3 MB (19258343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbf0ec1c723fd5bce2954a37ce4a0a3b1d0e17cc1d0743fbd5d370bc9f4d632`  
		Last Modified: Tue, 12 Mar 2024 05:27:19 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fc7c6855ebd1cace15ba25870174eb7225a7f2f0f9ac764a9907fb4a572030`  
		Last Modified: Tue, 12 Mar 2024 05:27:19 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7307591b079494e0f26c497f8295cf1b24de2b11ec8e2a68f3b135d886cfe9cd`  
		Last Modified: Tue, 12 Mar 2024 05:30:28 GMT  
		Size: 12.8 MB (12805100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652ce3316d51368d296e942acc4f45d83688d52f3292bcbdd711a9e363bdf1a7`  
		Last Modified: Tue, 12 Mar 2024 05:30:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94ac79ba956965bcdac377bd01d6920d18fb517495091f06835f0bcef0bc6ee`  
		Last Modified: Tue, 12 Mar 2024 05:30:27 GMT  
		Size: 11.6 MB (11570291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d50556caca2e20e4519350bcba54c6b8712e649a2e2c552ac0b53056da5f80c`  
		Last Modified: Tue, 12 Mar 2024 05:30:25 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9836e8d15e03430447dbf9c9654155d89c52728f86ccb002f5d9b777bd61d63`  
		Last Modified: Tue, 12 Mar 2024 05:30:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1eed37601bba408825e63f3bd9771f25ab6a5bd6332c77297bafd535c7c764`  
		Last Modified: Tue, 12 Mar 2024 05:30:25 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a72fcde4c66778fc264d3edca53050e94be5d20a4781841e219a2e414511db8`  
		Last Modified: Tue, 12 Mar 2024 06:57:03 GMT  
		Size: 1.9 MB (1930266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1208ca74efdf5ee9d232f00c0ddd18b7d5e9f787c6cadc09fc9c32fdd64dc636`  
		Last Modified: Tue, 12 Mar 2024 06:57:03 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4ea47fdd1b48870b3c47e2a045210065e810dcd97f83651d718b589ec2c503`  
		Last Modified: Tue, 12 Mar 2024 06:57:05 GMT  
		Size: 721.6 KB (721587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ed077917301e591de2151a68344581ca69d01addce7b12343046d02bdc9a04`  
		Last Modified: Tue, 12 Mar 2024 06:57:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3048ea413d463c5f5e685304f02be70c787c9880578f2876e25c0f3820cb349`  
		Last Modified: Tue, 12 Mar 2024 06:57:04 GMT  
		Size: 19.3 MB (19250696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:4986eb57d800c2f70b104edb5f53a2288018d589e16738ceb99a79b52c6e2d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b488976de5d7e2ea092a46cc5c13365b76a768875111fc0319cf1195ddae0a48`

```dockerfile
```

-	Layers:
	-	`sha256:59207cc589517285857185470fabc1aa469ee3ec1b3eb76fecf2fa86733c6c29`  
		Last Modified: Tue, 12 Mar 2024 06:57:02 GMT  
		Size: 7.5 MB (7481423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea3af94f772aadaf0e35d14d2f34875ed01b69ccfd95c9e1725733f26aeb02e`  
		Last Modified: Tue, 12 Mar 2024 06:57:02 GMT  
		Size: 39.4 KB (39399 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f7f652ea0e0b376e17c5f69501002c4cab70d223e75ec55a73d3e9c8afc03ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158023921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e5298c95ad7a4cf18f062445194ef45e1eefccfd72d55aeb95372967a6b4fa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:39 GMT
ADD file:8904abb8948cc1601202f5f3dd63ae52e3b980ac6acafff765b9424bfd5defef in / 
# Tue, 13 Feb 2024 01:20:40 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 10:35:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 10:35:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 10:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:35:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 10:35:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 10:43:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 10:43:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 10:43:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 10:43:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 10:43:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 10:43:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 10:43:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 10:43:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 10:43:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 20:28:47 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 20:28:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 20:28:47 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 20:29:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 20:29:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:33:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 20:33:24 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:33:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 20:33:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 20:33:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 20:33:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:33:26 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 20:33:26 GMT
EXPOSE 80
# Fri, 16 Feb 2024 20:33:26 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV DRUPAL_VERSION=10.2.4
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /opt/drupal
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7c57dc7cd6a5cd2a6636e8cbb774969d6394ce3ef35cb0d229f5cfbcd8ada61a`  
		Last Modified: Tue, 13 Feb 2024 01:27:40 GMT  
		Size: 26.6 MB (26582672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cb48d46564242eb666ef2709f5c44f0268233c3ef7fbc6904fbd4780ab3b3c`  
		Last Modified: Tue, 13 Feb 2024 14:20:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6fae91b417277015175919e07494b0db59e171855d2b0b54c9b886c3e2e78b`  
		Last Modified: Tue, 13 Feb 2024 14:20:46 GMT  
		Size: 69.3 MB (69323367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df4cc65cfede2b85f3ef5e84b76776014fefc210389af238133ff41e86ea4c8`  
		Last Modified: Tue, 13 Feb 2024 14:20:28 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6254f888fb1d2ef44fd0c1c8f8259a0887a54dc57f3bad7fb37a69b87f681f75`  
		Last Modified: Tue, 13 Feb 2024 14:21:06 GMT  
		Size: 18.0 MB (18017607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc89abf5bded7d8ca0d80361243746da14c2bc1979e4405ed718ed0c8e83cf6`  
		Last Modified: Tue, 13 Feb 2024 14:21:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e63482801e5af3952c943ec3e3a6d655300a1544238380ac6e283a2e95bc9e1`  
		Last Modified: Tue, 13 Feb 2024 14:21:02 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233f991a6e765e10ffff6af7ac3bf3d7a1cd82d065e027b07f93354f2cecf83`  
		Last Modified: Fri, 16 Feb 2024 21:55:50 GMT  
		Size: 12.8 MB (12803491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fcbbd131f16522ad121347ecb999c72f078e79f14980cfd2b8703df607a21`  
		Last Modified: Fri, 16 Feb 2024 21:55:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f1585a5a22368450fcef2c9f581e9d7df4bdbf504316be9415271c48151e7b`  
		Last Modified: Fri, 16 Feb 2024 21:55:49 GMT  
		Size: 10.0 MB (10007647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ad08b07d1e5a41129f77576840c67c5b39f6472fca381493ec6a2bde2e6c27`  
		Last Modified: Fri, 16 Feb 2024 21:55:47 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f287971bc36862c0e443ab56a94b09e7eb529205a93b9c8cd5d39696c5a2fdf3`  
		Last Modified: Fri, 16 Feb 2024 21:55:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5139794af0998841143d8890312239a72cc9d65e35cc9256748948cbe61626`  
		Last Modified: Fri, 16 Feb 2024 21:55:47 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32e04b78c6d07ba721b1b439cd02afa15d26502ff786b31dfe96c4dee9f3a92`  
		Last Modified: Sat, 17 Feb 2024 06:04:39 GMT  
		Size: 1.3 MB (1311045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0f45d9f18069571bc96864b49d75e7be3aa8996f0063a078b19c200ce80055`  
		Last Modified: Sat, 17 Feb 2024 06:04:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee398802bd54553db01032902a0e06994ca1872ce31bc86f632c969f1d18af4`  
		Last Modified: Sat, 17 Feb 2024 06:04:40 GMT  
		Size: 721.6 KB (721586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b42ac37ff0ec14a71467a86d6fd16fb250e250798830e12c2263238d379565`  
		Last Modified: Sat, 17 Feb 2024 06:04:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3235080a30c5099b7348202778a8964764712e8faf9610c1220d282d66c3c68`  
		Last Modified: Wed, 06 Mar 2024 22:50:20 GMT  
		Size: 19.3 MB (19250497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:198c2012ba29a188a870654b19096effd5b00745852256f044b79811dc459d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c230ab359a70765b896916a79225a259e65cc957e6230aac94ef48033d320038`

```dockerfile
```

-	Layers:
	-	`sha256:e23a7e9c09142779292064f40f1c24ae09e16964554c121dd676adc31cbfd4f0`  
		Last Modified: Wed, 06 Mar 2024 22:50:19 GMT  
		Size: 7.3 MB (7291087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d691cdb226f49bb1108a8afdf2d5c709b605dc6c039e215fe2360e5aece12043`  
		Last Modified: Wed, 06 Mar 2024 22:50:19 GMT  
		Size: 35.1 KB (35129 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6f27f81cfbe110dff77d13e3f1f9c6c1ebb01e404c43308add2141c9ec9616c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182796594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53df5089a931441269692c1f2927ae26ef7df203c995a84711efcc34133b205d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:53:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 04:53:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 04:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:54:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 04:54:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 04:57:49 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 04:57:49 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 04:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 04:57:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 04:57:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 04:57:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:57:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:57:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 04:57:58 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 23:04:00 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 23:04:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 23:04:00 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 23:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 23:04:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:07:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 23:07:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:07:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 23:07:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 23:07:17 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 23:07:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:07:18 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 23:07:18 GMT
EXPOSE 80
# Fri, 16 Feb 2024 23:07:18 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV DRUPAL_VERSION=10.2.4
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /opt/drupal
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e6761f5309e7053d74e42ca6e73ff3d4654fcb94eafe53927cd9f968ded5d9`  
		Last Modified: Tue, 13 Feb 2024 07:01:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d087a9a699e52864665689cf4ab9b86b9acb06b2c89742057e48e0f4dc6000e`  
		Last Modified: Tue, 13 Feb 2024 07:01:57 GMT  
		Size: 86.9 MB (86934155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868526445d4e7ba5e3298454a4c65450b2a0f6a038cbee0c148f97ebfe8d4e3d`  
		Last Modified: Tue, 13 Feb 2024 07:01:47 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2276c26b0f4da1fd855a8649aea179034b500774e7f08e8d3e32fae64a304b14`  
		Last Modified: Tue, 13 Feb 2024 07:02:15 GMT  
		Size: 19.2 MB (19176578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a095931c77ad3dedd0a6e47e57f6bc9db20a00d7c6af376bdf642df2f555c1ca`  
		Last Modified: Tue, 13 Feb 2024 07:02:12 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf008538fd7034c23254a2744bd0cbf794b9dc88170908ae563c2946db5e27c`  
		Last Modified: Tue, 13 Feb 2024 07:02:12 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7d5db6fcf285281d211655914cbeb94a4a55b0d6b69162598663aa1399bec8`  
		Last Modified: Sat, 17 Feb 2024 00:37:22 GMT  
		Size: 12.8 MB (12804344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c160059a738863c72d9f62e6d1361487e7f1d60701959c47b2668feb077a7d39`  
		Last Modified: Sat, 17 Feb 2024 00:37:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d60ee276e648302994be6f47bef0952b49c49e592e0fe4086f2541fc495d99`  
		Last Modified: Sat, 17 Feb 2024 00:37:20 GMT  
		Size: 11.6 MB (11638299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54629e9a5744231b1139064426b4ae6234a4578d0608e5ee5f09b9a628d2b864`  
		Last Modified: Sat, 17 Feb 2024 00:37:18 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d91a2c8762be44327d037bdd7b8891f1eb2cbae9629aa455630495ca017fa5`  
		Last Modified: Sat, 17 Feb 2024 00:37:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b733f21938bfc9338a86f4655ca55303712d9f6a90bd8b900bf5600f53f70c7`  
		Last Modified: Sat, 17 Feb 2024 00:37:18 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8c3d44c831e1b856f3e9cdc8b796c31ab57d3cac5bfa7a6c58586900bb546c`  
		Last Modified: Sun, 18 Feb 2024 04:00:13 GMT  
		Size: 2.2 MB (2194044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69176c8c506f152299789b3e00d58b0c0cb88e219ce8bc99197a3b87f028e03b`  
		Last Modified: Sun, 18 Feb 2024 04:00:13 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e625463a98c171018346bcb6e6f16b6d59f4f4df545f399020919a343488a02a`  
		Last Modified: Sun, 18 Feb 2024 04:00:13 GMT  
		Size: 721.6 KB (721586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df136d8e7647adff1d3b60de4e86ad21f9aaffd82b9a6347ba87125e4436a4ce`  
		Last Modified: Sun, 18 Feb 2024 04:00:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be84bb271310494ef9f35714fbdf2fce59d990c5cf7421dfef427c2d553f5049`  
		Last Modified: Wed, 06 Mar 2024 22:06:56 GMT  
		Size: 19.3 MB (19250515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:627bb3b009e0d4ccbeaf522ec60f21944d34e6252e722bd86b1793fe1499e89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2e66f2fa430b3dcb933995e69e723d3c9c6c648cb2c11a55376bf8eb003a01`

```dockerfile
```

-	Layers:
	-	`sha256:2245c998915f2015b9defe6e7d7eac57274d558afe25806bcb78527b9a1b3ee2`  
		Last Modified: Wed, 06 Mar 2024 22:06:56 GMT  
		Size: 7.5 MB (7484429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10c31b81a28afa0aeabd7caa94084ceec46c3791fc0115d826b825132b89d6b`  
		Last Modified: Wed, 06 Mar 2024 22:06:55 GMT  
		Size: 35.0 KB (35028 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:c4369db0aceb8c37ff4f41ae99c93258f8fe95f0b54688233eb385fb22ec32c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191442653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7909ab1d4b8eb8851c633b8b54bb6cc56b848ef73ae3a6b6d2480d6faae682`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 10:27:16 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Wed, 06 Mar 2024 10:27:16 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 10:27:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 10:27:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 10:27:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 10:27:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_VERSION=8.3.3
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 10:27:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 10:27:16 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 10:27:16 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 10:27:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 10:27:16 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 10:27:16 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 10:27:16 GMT
EXPOSE 80
# Wed, 06 Mar 2024 10:27:16 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV DRUPAL_VERSION=10.2.4
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /opt/drupal
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defbe26c351336c8405b50dd81b0ce898a2954212bcd4566c5725d81b71f6c67`  
		Last Modified: Tue, 12 Mar 2024 05:54:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d04d58f5de19f3515ba4c5a32bafaff0f783c662531fc7e823967ceb91042`  
		Last Modified: Tue, 12 Mar 2024 05:55:20 GMT  
		Size: 92.7 MB (92721578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952cb4e8013927fe1576fd535359e0b85695f2ee328a271fbf5f7d88904d183d`  
		Last Modified: Tue, 12 Mar 2024 05:54:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a82c37dffcfe58e8511d6df8fd4b394d8115c36f4841725a954dc6921346562`  
		Last Modified: Tue, 12 Mar 2024 05:55:38 GMT  
		Size: 19.7 MB (19744121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a123efd000f9fab5ee7fb38d715bda069291ec1809df6051deae6d9f6911204`  
		Last Modified: Tue, 12 Mar 2024 05:55:34 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d201f8fdb47c4fc661c8093efdc3d39d7396f704bbac169fbaf12c9b5a92c5`  
		Last Modified: Tue, 12 Mar 2024 05:55:34 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777e19f8bba220cde2c3369f26f6c976e7a94218939b24e3055799b94c314043`  
		Last Modified: Tue, 12 Mar 2024 05:59:05 GMT  
		Size: 12.8 MB (12804339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730344dd26390b13d9fc570d083d94c17ce96b4e5c82190c1912dd810f934cdd`  
		Last Modified: Tue, 12 Mar 2024 05:59:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77c391c301e7b2eb5808edf3485e4a5c3d2685ebdc18a39e7e4d488afa7fa40`  
		Last Modified: Tue, 12 Mar 2024 05:59:06 GMT  
		Size: 11.8 MB (11790031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469ab36f52089488a1041e44cc58dc2343b7dce4a6ec8cc585cf98b9829fe0d`  
		Last Modified: Tue, 12 Mar 2024 05:59:02 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650bd1f7a16eff89e7257d4bdb8477790d1ac567522d7550cf370ba56734da70`  
		Last Modified: Tue, 12 Mar 2024 05:59:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab120b094520a36e9c000a1dd889ac5829ae736a2aff1af2b587bf5b1ac416e2`  
		Last Modified: Tue, 12 Mar 2024 05:59:02 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01c08fd3ed30a75ecfc035ad4c8c1b4f06b4e192e23230b452e2e17d52e333`  
		Last Modified: Tue, 12 Mar 2024 06:56:59 GMT  
		Size: 2.0 MB (1996851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf2fb8775ccfce9d2498f8409279b385476c3dcdc8990dc8232b26a619b574e`  
		Last Modified: Tue, 12 Mar 2024 06:56:59 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8efd80118f354ba9bb42cc8d85bf14ca8b4c2e95e5018ce0feffb249ab691a`  
		Last Modified: Tue, 12 Mar 2024 06:56:59 GMT  
		Size: 721.6 KB (721587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed8334ef54be324a22a4db9d9477194b541fbeaf314385018d13022a4c77292`  
		Last Modified: Tue, 12 Mar 2024 06:56:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7febba52eff5a73510e06e74ccf13be4ebd7488bdf4defadc6c730ecc195d1`  
		Last Modified: Tue, 12 Mar 2024 06:57:01 GMT  
		Size: 19.3 MB (19250562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:33b6652ddd79b094f2240eeb7c488162331e132b57179eb87e7435b3c14f391e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764a0393f1d89facd4fad2954dcdf849b592b827da273adab7c6c34007d7e046`

```dockerfile
```

-	Layers:
	-	`sha256:54cb0fc89f84d8650dee90d378d9764c9b906621a52e84a91aed6cab714b7091`  
		Last Modified: Tue, 12 Mar 2024 06:56:58 GMT  
		Size: 7.5 MB (7472527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66068d2f544eafb659372250281a097b0acfb37a6a85b8a2cd00a6350d741ee4`  
		Last Modified: Tue, 12 Mar 2024 06:56:57 GMT  
		Size: 39.4 KB (39362 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:f7f83ffc5c6e092b13ad5642a9c76600d3a77bc7eb67aa9494524eacd20c5292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (189015775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795250cdc43d9c743efa1dc2ae45cb4718c4f165c632c74a7cf942bfbc9423e6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:35:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 04:35:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 04:36:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:36:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 04:36:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 04:39:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 04:39:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 04:40:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 04:40:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 04:40:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 04:40:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:40:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:40:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 04:40:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 20:43:48 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 20:43:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 20:43:49 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 20:44:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 20:44:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:47:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 20:47:23 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:47:24 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 20:47:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 20:47:26 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 20:47:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:47:27 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 20:47:27 GMT
EXPOSE 80
# Fri, 16 Feb 2024 20:47:28 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV DRUPAL_VERSION=10.2.4
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /opt/drupal
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60a2e07f944badb5933cd05a85dffeb9381d92a5d4aa9ec6c8734107ed8d100`  
		Last Modified: Tue, 13 Feb 2024 06:45:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e8a4ec517f6c888244a9425d7fffe86960f5f7b9d094d7a27ad6bf7cd71a3e`  
		Last Modified: Tue, 13 Feb 2024 06:45:41 GMT  
		Size: 86.7 MB (86652532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4206748c9c84f95b69bb7c840742125b8415508600486e0ff2cec15cd13ffd91`  
		Last Modified: Tue, 13 Feb 2024 06:45:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81e5f2fddceea149588f87c0d00867093aafa3f283ca8f04f00c41283ae8e59`  
		Last Modified: Tue, 13 Feb 2024 06:46:03 GMT  
		Size: 20.5 MB (20473704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f82b010e5ca369ca0decf6af1e8a6cf09f38ad5579f8817a98f67215402314`  
		Last Modified: Tue, 13 Feb 2024 06:45:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca96e1fee8e98446fac7666999d944fb9f650128be7ff50d6bc7bc5c28cb4f1d`  
		Last Modified: Tue, 13 Feb 2024 06:45:59 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54a84aad08ecf2b8688e3eaa4287c1090afe384db404b2b2c390167ae86c0d3`  
		Last Modified: Fri, 16 Feb 2024 22:04:38 GMT  
		Size: 12.8 MB (12805025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3985b9377c2543062c1a82d76796ff9d5cbce6ecd7eae5f86d202d7bac4586`  
		Last Modified: Fri, 16 Feb 2024 22:04:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb70cf84f48a8fdf710b2819987812367a5dcbd958fe4f68cfed6c9ea6f05e1`  
		Last Modified: Fri, 16 Feb 2024 22:04:37 GMT  
		Size: 12.0 MB (12014038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebde012a04f3b3a1f06f93f7c13fb690c0f6139a98f23dd9514c84640858f67`  
		Last Modified: Fri, 16 Feb 2024 22:04:34 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc9ace09556d50ad55da145159b25b8d90c971603508c1599dfd8a84a498ace`  
		Last Modified: Fri, 16 Feb 2024 22:04:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3d7fb40ea54df50741fd71d70b5053292f5d5e49a5ef922814f5d97452c6c`  
		Last Modified: Fri, 16 Feb 2024 22:04:34 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4241b6a1204c3af351bb3cd89ada50a9d872146a48369e04dbca20c6d376f9cb`  
		Last Modified: Sat, 17 Feb 2024 03:32:15 GMT  
		Size: 1.8 MB (1794892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5861b15e3eceff7c4d17372820c2cf9a996135816ecd351da753818c1ee69d1`  
		Last Modified: Sat, 17 Feb 2024 03:32:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db0f645b3db6399e093679bb39808e3bf6675d0461b61e4fbb43342529477b0`  
		Last Modified: Sat, 17 Feb 2024 03:32:16 GMT  
		Size: 721.6 KB (721582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce54ac104385b1b5e7ecd2dfc278d236df0f7041d3915af9c8c55199620de8d1`  
		Last Modified: Sat, 17 Feb 2024 03:32:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02aadcdcbcea9c4743fed2d01e47378dd85ae6f0d2ecda7b42c74fe155005475`  
		Last Modified: Wed, 06 Mar 2024 22:15:04 GMT  
		Size: 19.3 MB (19250192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:9153490f6ec123d6a3f3ca480a3f91d3ed7feafdd3be9f2cce478a8e40fab84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c31cf2e9cc49c78e5c23b94835f9fbf82523e792d569f77e2221fa5ac328ad`

```dockerfile
```

-	Layers:
	-	`sha256:e6fb6f65d2dd903bfc10054957f0e2837c56a2801e235f9086bdac9b6294e7c9`  
		Last Modified: Wed, 06 Mar 2024 22:15:02 GMT  
		Size: 7.4 MB (7447364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e18597b9de07578921a3334706bf17c283987f1c2c87553fbfc6d0f81977e5f`  
		Last Modified: Wed, 06 Mar 2024 22:15:01 GMT  
		Size: 35.1 KB (35064 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:cca0d6071e6683f9f95f04ce4603c43a94f8473f915e35dd425f57fb51d91a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165348464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16d059968c2665e5503eb5317e8392580421e133c1ca950c62d66b57e441fc1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 01:06:13 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Tue, 13 Feb 2024 01:06:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 05:24:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 05:24:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 05:25:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 05:25:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 05:25:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 05:28:52 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 05:28:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 05:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 05:29:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 05:29:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 05:29:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:29:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:29:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 05:29:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 21:31:49 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 21:31:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 21:31:49 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 21:31:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 21:31:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:34:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 21:34:05 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:34:05 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 21:34:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 21:34:06 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 21:34:06 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:34:06 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 21:34:06 GMT
EXPOSE 80
# Fri, 16 Feb 2024 21:34:06 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV DRUPAL_VERSION=10.2.4
# Wed, 06 Mar 2024 10:27:16 GMT
WORKDIR /opt/drupal
# Wed, 06 Mar 2024 10:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 06 Mar 2024 10:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f92a6bea080f413e99319dd0b739411c3eeea639a77a8ef3450ac276bcdd574`  
		Last Modified: Tue, 13 Feb 2024 08:13:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621233f2aa9f390b199ed1bb99dfec061caa63a41b5d758fc4979621f73ea20b`  
		Last Modified: Tue, 13 Feb 2024 08:13:19 GMT  
		Size: 71.6 MB (71639070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d1f9f7f563e462ff0471e75ab1b5554a6c01668a3744f1064441e03f0fd9fd`  
		Last Modified: Tue, 13 Feb 2024 08:13:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b3a59c0ec3a114f34ce4aeddd84e42479633a475029d4c53f3fbcbf2599cd5`  
		Last Modified: Tue, 13 Feb 2024 08:13:35 GMT  
		Size: 19.1 MB (19080244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f1dbbfdc6deeb9b39b5ff6e215edc51f042178b9e87b1c1612f7b9276db9b9`  
		Last Modified: Tue, 13 Feb 2024 08:13:32 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f039ac6444697d4500659a76e65ab1886d94ab4b9c950ef4c37d8ed7d9f3c62c`  
		Last Modified: Tue, 13 Feb 2024 08:13:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ecfcde54f1bdd924249b8dca22f88e9fcf3a43d3b5fdf971e64a9815611ab9`  
		Last Modified: Fri, 16 Feb 2024 23:19:31 GMT  
		Size: 12.8 MB (12803895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7180be60b8c85b8ddf581c24217197f057307bedfd79a8269db0b44a0d77d6`  
		Last Modified: Fri, 16 Feb 2024 23:19:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49545a3258cb9ffb3389d498ab303f9b2db6171b73f1059ab1c4fef56651cbf`  
		Last Modified: Fri, 16 Feb 2024 23:19:31 GMT  
		Size: 10.7 MB (10663741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fef99d1d6a397446744a8a9a601cd501a8ad6257da18f61426276de3cdaa89a`  
		Last Modified: Fri, 16 Feb 2024 23:19:29 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248f580c2e2cb071d979ead320f546a33b86daa44fe797e3a08be374835f27c3`  
		Last Modified: Fri, 16 Feb 2024 23:19:29 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911ac6573eff1eddc40ec311263c3d8c148182a720fead34319d183466b8bad1`  
		Last Modified: Fri, 16 Feb 2024 23:19:29 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabb0fe52be9eb6b745fb6da8b998a1baff987bef2cecd8e48e699484a9e8dfa`  
		Last Modified: Sun, 18 Feb 2024 04:19:47 GMT  
		Size: 1.5 MB (1523380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaf336a3e68fe43637d658a8847a65985a8ac7f6c70c1cfbe9df7e40c8e52ce`  
		Last Modified: Sun, 18 Feb 2024 04:19:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2af201b644168096ed80f05ca1de344ec01cb05b3b7c48740368f7d88a3a6`  
		Last Modified: Sun, 18 Feb 2024 04:19:48 GMT  
		Size: 721.6 KB (721587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c9919f2a065dd0ebd2325d9b6fd3135b3fa062b2421be2be2da897e47e383d`  
		Last Modified: Sun, 18 Feb 2024 04:19:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa321553a6f5a885bd9205be9f05350ea659e6380649a927fbb26479172a30ec`  
		Last Modified: Wed, 06 Mar 2024 23:16:16 GMT  
		Size: 19.3 MB (19250391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:887695d8e8e7c03925f8cd0ab0897efd871ab034776042477815a65ceb12319e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e47e5275fcd0e192c52d1faafcccfb6974bfc4d320bdc82a13f41e19b1e8df8`

```dockerfile
```

-	Layers:
	-	`sha256:95760d8dc5b5e608ebca25a59260e06904b1ccc4855090edf69b999253ec7745`  
		Last Modified: Wed, 06 Mar 2024 23:16:15 GMT  
		Size: 7.3 MB (7312346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17c843a61e9d635a71971c7ae3362f1604b01a9882b1a428eb7efa86263105fa`  
		Last Modified: Wed, 06 Mar 2024 23:16:15 GMT  
		Size: 35.0 KB (35018 bytes)  
		MIME: application/vnd.in-toto+json
