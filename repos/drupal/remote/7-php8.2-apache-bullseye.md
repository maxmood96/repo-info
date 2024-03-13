## `drupal:7-php8.2-apache-bullseye`

```console
$ docker pull drupal@sha256:1449dc7336d04132c4f5453be1517d0f2ffc2a634ecc18e8c2dc56a5a1d09863
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
$ docker pull drupal@sha256:81af92225f65e12c7e1b6922d5b454b564c185d967d2da1229ee740e6c94ba01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171443299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5cf65b76126b3fdc969e86ac69450ba018997ccafc31e6fada8b90291a34eb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 16:28:12 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 16:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.16
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 80
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:9c2efc19334a964858d7a16e2d09a13035fb6305be8ad80b48f13947ef0c78d6`  
		Last Modified: Tue, 12 Mar 2024 05:35:16 GMT  
		Size: 12.4 MB (12426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4e72dac5d90fa095a8ceca85541647f14eefd9c6c91c5e4d442433677d99a9`  
		Last Modified: Tue, 12 Mar 2024 05:35:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3d53e714a13425f140740f8f10c09423ccba34c3f8314cff0768628bf15a70`  
		Last Modified: Tue, 12 Mar 2024 05:35:15 GMT  
		Size: 11.3 MB (11336105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a8765dafb48e6e88a10ff51707d6f9aa618a2c5d390454778f29a6a403b723`  
		Last Modified: Tue, 12 Mar 2024 05:35:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cac7c109793ccdb25713fc1ea2d3f637b370d3ff7b77aeab4e1464fd125e85`  
		Last Modified: Tue, 12 Mar 2024 05:35:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c64a8d6b0e17344b9ddb051f9de945fddafb7bbbf36896110b918f046e42a8a`  
		Last Modified: Tue, 12 Mar 2024 05:35:13 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878afa9f0be6dcfb35af99c989019423376991d6c8ec0d391bd04449504303c3`  
		Last Modified: Tue, 12 Mar 2024 06:56:59 GMT  
		Size: 1.9 MB (1928204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6b4cebcb62ddfefa3e8517665fae31fa31ec203eb7e30cf099dee816dfee97`  
		Last Modified: Tue, 12 Mar 2024 06:56:58 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827a8bfe447cf6c854ed2f4dbf3905a74e1938d6fb158362b5e7c91a08971651`  
		Last Modified: Tue, 12 Mar 2024 06:56:59 GMT  
		Size: 3.4 MB (3425933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:47370852cf38a269fb654aca24352eecb5634128c7d2f578b2a0deab7ce50389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6934118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e2b829f51b63f4ed55205b70ea233b2f9275dd27504d74a4cead4ccea2d8ad`

```dockerfile
```

-	Layers:
	-	`sha256:374d97acd3c217e5182a987ffc50e67dd1dc2b1421a1e261bb255f137a51c18a`  
		Last Modified: Tue, 12 Mar 2024 06:56:58 GMT  
		Size: 6.9 MB (6907309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8770de5538c42f28ae0666b68acb670f22bd2f9ebeed4c669422d61a1b2b7dd`  
		Last Modified: Tue, 12 Mar 2024 06:56:58 GMT  
		Size: 26.8 KB (26809 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v5

```console
$ docker pull drupal@sha256:88c463acdcfc56815286101e3b6d9f16446f8c2903b5f7688226bd666d6b7d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148816789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c91c8ca2449c4d85a530847473edbb4bb075d9c9052c25df92931509a47bb5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 16:28:12 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 16:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.16
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 80
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba57b16e604e5717ec580b73cd6a9df4feb74a61417087025b25f7f7201368`  
		Last Modified: Tue, 12 Mar 2024 03:52:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8541f2a8dab19f5796c7f598eda1579dcc5cceecd00e5ddd885c72253a98ed6`  
		Last Modified: Tue, 12 Mar 2024 03:53:02 GMT  
		Size: 73.7 MB (73694966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcd4ab94da51a16d224bf5f56430c8a93c8dce6f1d6354acbaf0c92f698a2a0`  
		Last Modified: Tue, 12 Mar 2024 03:52:43 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7964f81b9a897e233918b966074e2e48a7d3f071c2ae3294b618451eae42716`  
		Last Modified: Tue, 12 Mar 2024 03:53:24 GMT  
		Size: 18.6 MB (18557757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3a3c5cf0fbf1f136fe0395cc1d188903eef0c10d9a6b981a7c5986c26ecd85`  
		Last Modified: Tue, 12 Mar 2024 03:53:19 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d0785c0c8ead7cda0153efe29cc816715a73c2d839050eaa1fc51412cf537`  
		Last Modified: Tue, 12 Mar 2024 03:53:19 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe572773f3148bda0cbd94c25a97e3c4983538bd7e9569bed8642b34bf67a1ef`  
		Last Modified: Tue, 12 Mar 2024 04:01:19 GMT  
		Size: 12.4 MB (12424950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f1343303e612ae16bc5c1431c88616bba6c677768c5a8a468b12f9467b729`  
		Last Modified: Tue, 12 Mar 2024 04:01:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2310d423ac063f5eb1e4131b8e0f38a4ed004d13443a70b1105df93ef19a2115`  
		Last Modified: Tue, 12 Mar 2024 04:01:18 GMT  
		Size: 10.4 MB (10363699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c533dce409543b9b7864bb06cac2749593238dc6a546bf63d00d39f324140c4f`  
		Last Modified: Tue, 12 Mar 2024 04:01:16 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f07419ab79e01f19e9bc767b3da7119bf29b7ce74a7e25b31e53b3b4ba89c8`  
		Last Modified: Tue, 12 Mar 2024 04:01:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdea7e61a2cf2e9a9a118d1aa31ec942a8cfb7e65419db69bd4c9c788b55458`  
		Last Modified: Tue, 12 Mar 2024 04:01:16 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba4eaf8bf039eb463c9d8d4b129beddef04c71b57fe46e1028d265bd8b1fec9`  
		Last Modified: Tue, 12 Mar 2024 10:22:34 GMT  
		Size: 1.4 MB (1419035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa3cba67a1773537b780be2486f05b5281cf188211ea2316a4a36eccdcbc883`  
		Last Modified: Tue, 12 Mar 2024 10:22:34 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58675f5a37e18b89f3521e094cd9f7570a9bea68dd489d85622602c134156638`  
		Last Modified: Tue, 12 Mar 2024 10:22:34 GMT  
		Size: 3.4 MB (3425932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:ead00b1b41fada1c8f7d8141523fbca15ec78b94d9ecfb38fb49a21a1ed421fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6739928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c424dc71c2885fd3ebb1a7f374976ec10dd1db6022982c7f331e4c633060287`

```dockerfile
```

-	Layers:
	-	`sha256:3df51a11a7be3e7bee82a58c1a431738dc50db02b30e7d750cabdc3467321715`  
		Last Modified: Tue, 12 Mar 2024 10:22:30 GMT  
		Size: 6.7 MB (6713039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee40819de3d4420c81b055ba9e1809bc56007e636a21e009c2928f2575666154`  
		Last Modified: Tue, 12 Mar 2024 10:22:29 GMT  
		Size: 26.9 KB (26889 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:bccf478fc2844170d948cad2d4e27b82c462679df0eef0056dde8c9983f17f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140891586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a4759a0f08b70deb79c9da7c3568f2511918cfdfa21ff831eb70be1fd06555`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 16:28:12 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 16:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.16
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 80
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f87b16e5fcb62e87351e595cf38c491acdcd0bdfb7bb303f8627347a17597e8`  
		Last Modified: Tue, 12 Mar 2024 09:25:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365740a2d4d855bbcfa6ab7f879e136f8176a1fcf9684965898d32dad4cec163`  
		Last Modified: Tue, 12 Mar 2024 09:26:09 GMT  
		Size: 69.3 MB (69322871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc3ad1d06c5095049b3ad5080d5164ed5ba69a85e7501a564e764c88500cc6a`  
		Last Modified: Tue, 12 Mar 2024 09:25:57 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5485de947ea9af5c3266f0ec8740e4912a0075d82e8ae593497b91389c628ac1`  
		Last Modified: Tue, 12 Mar 2024 09:26:27 GMT  
		Size: 18.0 MB (18017550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8363e13348c3bcc642540c3d7e3afa540d49bc6a6cfb12f417c8003226a899a1`  
		Last Modified: Tue, 12 Mar 2024 09:26:24 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1ba5f9e3d7110b1412e948075607ee3a2356484346e450b1158efcea38de27`  
		Last Modified: Tue, 12 Mar 2024 09:26:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c745318d669ab827d3508c5dc2ee6eb79cd63a129498df8630576b3135a36e7`  
		Last Modified: Tue, 12 Mar 2024 09:34:30 GMT  
		Size: 12.4 MB (12424954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdf4bee417720e51e66458969e7fbab71bb49bb7d05be13e5a8a0a34052ade1`  
		Last Modified: Tue, 12 Mar 2024 09:34:27 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28170f9451be971617bc20728a5c208cd7978c391568f0c232b1dbcc07757dc`  
		Last Modified: Tue, 12 Mar 2024 09:34:30 GMT  
		Size: 9.8 MB (9802550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12607b36fefedc89dcff8ac5b34c4603017c09c153cf6cf31cb4a7b12b0c45b5`  
		Last Modified: Tue, 12 Mar 2024 09:34:27 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c24b6093f17af45d195f323e843d9b87fe815a32cd81ae6edfd5b2bd5cef36`  
		Last Modified: Tue, 12 Mar 2024 09:34:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0f9592dacc048b7f47b1178bae8e768f6c51fc8ec82700acbc86040def70ad`  
		Last Modified: Tue, 12 Mar 2024 09:34:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51388940915796b54ccbe0adcc350f170453b3c9acdeb722b47749881e3da561`  
		Last Modified: Tue, 12 Mar 2024 14:31:46 GMT  
		Size: 1.3 MB (1309135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eacbcac50f8c2f24a3b60616bc27e575e7c8b72b3137668327e57bcf7e89508`  
		Last Modified: Tue, 12 Mar 2024 14:31:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e02ef487ab1a4c32c64be38b5521dfe5d79d41d9795c3a26456bf7fde739672`  
		Last Modified: Tue, 12 Mar 2024 14:46:55 GMT  
		Size: 3.4 MB (3425926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:483f862c69f94b88398c4729400391f2540041f0d7b39ac789bfd4870f0b353a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288c01904612b54b0eb97bd045989937709b800785fa8d5f4eb866c88ce9d4fa`

```dockerfile
```

-	Layers:
	-	`sha256:ce76b7f63571f1d5c10940900cd32a1cdf2461ab73d2f48e0a2dbee9b322c314`  
		Last Modified: Tue, 12 Mar 2024 14:46:55 GMT  
		Size: 6.7 MB (6716957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e0701a2f442f482744b35bf6210d3c7cec4fb2dde65ec4234264b92797c0c4`  
		Last Modified: Tue, 12 Mar 2024 14:46:55 GMT  
		Size: 24.8 KB (24777 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:d1c6b142d3ced294509a3089174153aeb8e39044d8f90f5d6574f865053376a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165648841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61d1b7e52d5fe3f9105a214a97484a6e1b8f116c5dc54588a511e0b040b21e2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 16:28:12 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 16:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.16
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 80
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95434312c87bbfb0c1c0428101ecb9ad5da0f27b23e0bab2cfa9aef467e4d9e`  
		Last Modified: Tue, 12 Mar 2024 06:58:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465e10561b205308476d133ec1a862daf9138d09b954ce86d35fd888baaa8727`  
		Last Modified: Tue, 12 Mar 2024 06:58:46 GMT  
		Size: 86.9 MB (86934539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3beb929c6bc3ebeb0fbc6e8e3ce3ecda6ee33da58ad63dafdead658eed3e34`  
		Last Modified: Tue, 12 Mar 2024 06:58:37 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a6c16a4e68dfed4936e63fc18b9545de7b4e641bd4b3648a257cfb671a56ef`  
		Last Modified: Tue, 12 Mar 2024 06:59:02 GMT  
		Size: 19.2 MB (19176429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54357b7213684526c87de7cf652881acb8c47f5cd91d21da3eeec2b1fb354cd3`  
		Last Modified: Tue, 12 Mar 2024 06:59:00 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a668dd352ed32bd7e0c3e6b0ee6806e46212fa1d91b50f98a6fdf0c4c8175`  
		Last Modified: Tue, 12 Mar 2024 06:59:00 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1046c35a77bbfdd2d92d2ea318c75bc908f4f82acc11e9b795cfc2fcc0b4d955`  
		Last Modified: Tue, 12 Mar 2024 07:06:35 GMT  
		Size: 12.4 MB (12425535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d20b1de8592740a2f134a37e1dae2b463df33ee4a3ef832a608ad8e51330038`  
		Last Modified: Tue, 12 Mar 2024 07:06:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993d602938526bbf51dbf4d46eb29e8d4c002050088541f8ce89db81c97b2b4a`  
		Last Modified: Tue, 12 Mar 2024 07:06:34 GMT  
		Size: 11.4 MB (11415208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4084fe1b35934c10c33912134ae18e6fa4f550d56b0fdaad8f6740be478912`  
		Last Modified: Tue, 12 Mar 2024 07:06:33 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557afbeb9fd71abbf98b1dbfdefbb6c95f3fb1020fb75dea0972e09997860645`  
		Last Modified: Tue, 12 Mar 2024 07:06:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672d1e800183c650e3b886b46cc525953a53443b313f6c49f36b91c803c505dd`  
		Last Modified: Tue, 12 Mar 2024 07:06:33 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab021871ac960971de82cf158ed26db3e7afdb42942e5892754eea70c8612991`  
		Last Modified: Tue, 12 Mar 2024 15:02:05 GMT  
		Size: 2.2 MB (2194200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0851933bc01867889afdb705cbe7542037d70f1fc5e3c8adde67409f5495349`  
		Last Modified: Tue, 12 Mar 2024 15:02:05 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a5a3ac8dbbf5bed0d65409a159c19060df3315a960c488c2ab7a82b4f0c6e1`  
		Last Modified: Tue, 12 Mar 2024 15:15:15 GMT  
		Size: 3.4 MB (3425929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:dc4ac11db0c3fe3035ab0bb00526933d2e9eb9cb195ebf9f83d71b2f3d402d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6935018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a07c480f1c4b508d33763804258dc7d169af3d394c1a6e257c1857fa1762ee`

```dockerfile
```

-	Layers:
	-	`sha256:9413e5648ca0d4123f84173ccc01d9d44067736c961219655557829f843b1d4c`  
		Last Modified: Tue, 12 Mar 2024 15:15:15 GMT  
		Size: 6.9 MB (6910311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093c2c0e115dbbca220f686ff29a4cbf993868f93770c1c879001291069517cc`  
		Last Modified: Tue, 12 Mar 2024 15:15:15 GMT  
		Size: 24.7 KB (24707 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:e03b0bdee598a0f9d3a768556bd036f64b9c3d20ed291418ab58b57c1f76b4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174305164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6326f9a7abb56ae9b85a8cbdd04d4b8c17cf06cd99bc8f5d0f54b8b0772a303`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 16:28:12 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 16:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.16
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 80
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:a4ac62e0c088321f09d39e0818a9e438345338fd85939945d97111159db854cd`  
		Last Modified: Tue, 12 Mar 2024 06:04:47 GMT  
		Size: 12.4 MB (12425629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55f8751986a098c6a29c1ca91f9e44c108bdf6b2cec1fdcacafcad9b6bb715`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3962e640ed5cd84fda248b19076ff327dd68115614a7c38f86feee415467b4c9`  
		Last Modified: Tue, 12 Mar 2024 06:04:47 GMT  
		Size: 11.6 MB (11578482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a75f798cd46d6a128078f583826dae3ab6f905da4e0f8caaa9887148bf70b2`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a87fd6ee3ca3ac4d5b2313f3f9908cb8acabd214138d6b236cf1cf61f08bac3`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0877322669b053756e3938f59234ca2460789735f11f1090e1a48529cebc3c74`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ea144b1afe14f453d39172b4c922bd8498a04f8525bb9bb41207922ccab58c`  
		Last Modified: Tue, 12 Mar 2024 06:56:51 GMT  
		Size: 2.0 MB (1995945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95147907326f12428576e32f311de637f6328ce53cac28ba7b23dc52b28415a3`  
		Last Modified: Tue, 12 Mar 2024 06:56:51 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98e9707d87f7ce413708a38da496c892cfea73e07b45a451df2d6bf005b54b4`  
		Last Modified: Tue, 12 Mar 2024 06:56:51 GMT  
		Size: 3.4 MB (3425931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:1c03e29a6d775729213d71bf7e9abc4a17a5ec7a38cb2a6f0178a921aba6321c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96bb7ebc412724ba396883048e1eff8334893d91e1ec658d8dcd18177a4f03`

```dockerfile
```

-	Layers:
	-	`sha256:958e4f5a269ac8232bb55017562a179b6feb1049de697fd4c8bbedb53a09d05a`  
		Last Modified: Tue, 12 Mar 2024 06:56:50 GMT  
		Size: 6.9 MB (6898423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704ce8149be041b373dcb6bf27616d4b96489ac9c6b41e8dc0f5f0e8fe962aac`  
		Last Modified: Tue, 12 Mar 2024 06:56:50 GMT  
		Size: 26.8 KB (26786 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; mips64le

```console
$ docker pull drupal@sha256:f317f4042aa27154dd8f73269a6f146ce03295fa543e3a6248d7c9481f35be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148242090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66547f7bac4b6daf629addabe7a6b17151e6792b71f2b23fa6e16ab3db0fa081`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 02:05:30 GMT
ADD file:aec249f679ecc1ccad460833afd79f8f10ccd9378d1275ed1f23fa98cf3f99b6 in / 
# Tue, 13 Feb 2024 02:05:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 08:56:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 08:56:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 08:58:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 08:58:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 08:58:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 09:13:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 09:13:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 09:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 09:14:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 09:15:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 09:15:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 09:15:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 09:15:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 13:21:40 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 23:39:17 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 23:39:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 23:39:25 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 23:40:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 23:40:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 23:54:09 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:54:15 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 23:54:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 23:54:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 23:54:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 23:54:29 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 23:54:32 GMT
EXPOSE 80
# Fri, 16 Feb 2024 23:54:36 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c99d8d33768bdc2aba62f6b3cc956b807c30b43339ac2ffa3db52a47112dd416`  
		Last Modified: Tue, 13 Feb 2024 02:16:36 GMT  
		Size: 29.6 MB (29640432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190bb31c5c2cc4118146a50d54fb930bb92cb5f142d8921682384a36f74bb5ff`  
		Last Modified: Tue, 13 Feb 2024 18:14:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376fbbe3c612f5997b431972f1ca50b9f0d13299ec0e3df2619733a74e6fe68b`  
		Last Modified: Tue, 13 Feb 2024 18:15:03 GMT  
		Size: 72.0 MB (72019538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7832bf6851fe254235c0da62fc44394adb06731c39e8814fd2a5e5d97405c10`  
		Last Modified: Tue, 13 Feb 2024 18:14:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cac0a08c2d78f26703ac8ff397543d45b130bb58748627df7364d4d4a165989`  
		Last Modified: Tue, 13 Feb 2024 18:15:35 GMT  
		Size: 19.0 MB (18955433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d055b942e538c8381bb91a917e9ac94add20ce699ce73a8c64e4c0285c9a2a3`  
		Last Modified: Tue, 13 Feb 2024 18:15:22 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5272d51f434c3ee8bb877822d65ddb5fb4ac94926ac8505f89e01fe2ab7c24`  
		Last Modified: Tue, 13 Feb 2024 18:15:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18a08bd5685f15182753cc1513e2659c6e9723467a39a73c8a202eb48a6408b`  
		Last Modified: Sat, 17 Feb 2024 00:33:45 GMT  
		Size: 12.2 MB (12208094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9dc25c823a42694bc009cc3caf972f9feb247a247c0dfca1b08da8a987b26`  
		Last Modified: Sat, 17 Feb 2024 00:33:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb886f5c4df66d061b7d4f4737081d86e461fee534ed9ea613c7758b9a7585b1`  
		Last Modified: Sat, 17 Feb 2024 00:33:47 GMT  
		Size: 10.5 MB (10469204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19a8a9ba5289748cd5cb3942e64047401dd2cc96d184a555fc7335be8aec8e5`  
		Last Modified: Sat, 17 Feb 2024 00:33:39 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02a4b90d1f55fc94735892a071abcbca2561354925b6fc120d334172510a275`  
		Last Modified: Sat, 17 Feb 2024 00:33:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf680a8a2600644cf22b17daead033547a9ef91e6c47b45dc8e8ce3c279d706`  
		Last Modified: Sat, 17 Feb 2024 00:33:39 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e24396109a672098db1685a35b9449a534782ca37b1d2aee8197b247c591f7`  
		Last Modified: Wed, 06 Mar 2024 23:26:00 GMT  
		Size: 1.5 MB (1517667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348bacaf66befc11d60bcc2d5fb4a9d3528b2d4150f6518c912344c6fd09e075`  
		Last Modified: Wed, 06 Mar 2024 23:25:59 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a3a3b7c90241ef40b3caa0ddbc4521d5d53f95fd94bbae95baa4e9208a472`  
		Last Modified: Wed, 06 Mar 2024 23:26:00 GMT  
		Size: 3.4 MB (3425930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:9ed55a66779078cf74277a0341bb8f4eeeb3fb018226fea2ca1d8d46c28a3c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c79085332b09f2fd88426509f0b62f258402d6dc3b91306f1b4a17b780188be`

```dockerfile
```

-	Layers:
	-	`sha256:790746597f83eb53dc3d0e10ad8c643f981d11d37c9b8ef125360ca0ed5d7326`  
		Last Modified: Wed, 06 Mar 2024 23:25:58 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:b90877b6e4d9dbdcfef60e40ac2330ba9f1f94799b25b0f46a44895a7136c611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171877988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664b666f864d6a1599d8a1c8b61b0c70368df1eaac49e0a2c51fe43177eb4c61`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 06 Mar 2024 16:28:12 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["bash"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 06 Mar 2024 16:28:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 06 Mar 2024 16:28:12 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.16
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGWINCH
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 80
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9819e7f16eeb590503b7316e9fb3cee2dd1a0ccd07915c19a8c43b4926b6a7bd`  
		Last Modified: Tue, 12 Mar 2024 08:10:21 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3742d5f892c8ae918501b4593107b28f0388e280be87d383e05b91c1eada4f3f`  
		Last Modified: Tue, 12 Mar 2024 08:10:36 GMT  
		Size: 86.7 MB (86653305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb123743606f50f2969d2fb7d79741fbda8e5bd5208e34c2f91f7e4f057a4554`  
		Last Modified: Tue, 12 Mar 2024 08:10:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119ae7de40f6520f3bda4ab2f60c77ca3ec44daf06c6931597b87ab5e1a8db6e`  
		Last Modified: Tue, 12 Mar 2024 08:11:01 GMT  
		Size: 20.5 MB (20474199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57db5f5d72723db2e3e283d5467b153a15f6a7e6b26d82eee8c4f05f45ae5ee`  
		Last Modified: Tue, 12 Mar 2024 08:10:57 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57901357393cfe03b5555ccbcb9644e4a336e255bb316f21027911a43766a65`  
		Last Modified: Tue, 12 Mar 2024 08:10:57 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2904c4eb2e846427c5150b25452849e028ddfc72f029051a5d1195af3a82d44`  
		Last Modified: Tue, 12 Mar 2024 08:20:29 GMT  
		Size: 12.4 MB (12426945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ff40c04e51b562fb6062c8668d48e56cbbbc9050a739d9bf320345baeaa888`  
		Last Modified: Tue, 12 Mar 2024 08:20:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d6f6664771d9efbfd8f346df81220ca96bb702377dc57e2f8c76f57f7fcc1`  
		Last Modified: Tue, 12 Mar 2024 08:20:28 GMT  
		Size: 11.8 MB (11798348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a715b6fcaa49a8f9f14acf679f1fd38cbff81705b5644ff153bc0acdad55232`  
		Last Modified: Tue, 12 Mar 2024 08:20:25 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce5ccca993c860b8cacc9d299e93585598980973dd9b7b83e5ea0588ac7ea8`  
		Last Modified: Tue, 12 Mar 2024 08:20:25 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28c2e9063313dd288d049edf7eb869514c6db64f28fd21b9694919b72ee4b10`  
		Last Modified: Tue, 12 Mar 2024 08:20:25 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba55dc6d9d80b240853446db9c88bf30c5fa45f6067232049e941cb9c92c70`  
		Last Modified: Tue, 12 Mar 2024 20:02:57 GMT  
		Size: 1.8 MB (1795354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcde3965c0ff3ee6018459550099c17f9b291976f4dcd75e3a16cf5e60cf486`  
		Last Modified: Tue, 12 Mar 2024 20:02:57 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df95c1595e5191a668019f05fd0728b6011fd5d1c155f4fc00c56e9e83eeba7`  
		Last Modified: Tue, 12 Mar 2024 20:02:57 GMT  
		Size: 3.4 MB (3425929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f4053bc67d307f77824eb4b33b06d06464a30d581d7c2265b40c8cc1fc5d5ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d407940f4fcac8aaa451d0b1d3220b58a5d615401787d9ff7e5b4b3a7d83c071`

```dockerfile
```

-	Layers:
	-	`sha256:7f10760f20eaf93a4ce2c7fad76c47e87599f369485bd7f5ff78e7667ac573bf`  
		Last Modified: Tue, 12 Mar 2024 20:02:53 GMT  
		Size: 6.9 MB (6873238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664a616b42ea86fcfef3d9ac95c3432dba3239fe26ddc7f320f5a52455ad94e4`  
		Last Modified: Tue, 12 Mar 2024 20:02:53 GMT  
		Size: 24.7 KB (24731 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-apache-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:b20ffcf7c249946c2566defc2b7c58082eaf724d09edb6888153de539da38a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148216527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8de0738d22d0af5576ed4d76e29aafc701bef052666aab9b23b1f78346a0abc`
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
# Tue, 13 Feb 2024 06:40:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 22:25:33 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 22:25:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 22:25:33 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 22:25:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 22:25:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:27:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 22:27:49 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:27:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 22:27:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 22:27:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 22:27:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:27:50 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 22:27:50 GMT
EXPOSE 80
# Fri, 16 Feb 2024 22:27:50 GMT
CMD ["apache2-foreground"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
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
	-	`sha256:a4d7528b8ed7df09d50f2fd50a91ec6ee1b39c1c9b4467693660b1a0a4c637d7`  
		Last Modified: Fri, 16 Feb 2024 23:22:58 GMT  
		Size: 12.4 MB (12425336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b00fea78d72fb2376fcea2b9278fa3bca97a7e40e7dfd3a9794b610ff03c187`  
		Last Modified: Fri, 16 Feb 2024 23:22:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb40740bfcd51c76ec94e7930b38d4a5df75df35ceafca58646dd7ff1c2cae73`  
		Last Modified: Fri, 16 Feb 2024 23:22:59 GMT  
		Size: 10.5 MB (10457639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029367869d3921b8bcabb52bc1612e32688ffe695f03d25537257ed744ec6533`  
		Last Modified: Fri, 16 Feb 2024 23:22:57 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d844fcf309449d7d6c44ea9e1583690da2772c94a3136a49b0e7b6f913c3b58f`  
		Last Modified: Fri, 16 Feb 2024 23:22:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7f216b8dcc222ed5922768a9576936045ed4e6daf6dc646211f2f6851392b4`  
		Last Modified: Fri, 16 Feb 2024 23:22:57 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f642b9ab91c35fae57ec1416b919c842e34f2a10302cfe70beb7e7b39f8adb`  
		Last Modified: Sun, 18 Feb 2024 05:06:22 GMT  
		Size: 1.5 MB (1522271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3b1d22677bdc49305f11a1bc795993c78b1fbacc83fdef7c9cb27a15435992`  
		Last Modified: Sun, 18 Feb 2024 05:06:22 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac396585962612985a9d920e1e8a720d513ce1ac69305c53f9f4372d059ddc1`  
		Last Modified: Thu, 07 Mar 2024 00:58:07 GMT  
		Size: 3.4 MB (3425929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-apache-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:5a05d48f3ad0d33ad8398b111bae7d3cd5f69971ff766d915d9fa9d058811e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6762933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef46ab8ff135c6732b35cd1d2d60f2010bffef1c032a9530cacc2aa373129ff`

```dockerfile
```

-	Layers:
	-	`sha256:d3d5950b48c4e1d63b089ffda9b981699b0edd2b87542e33954eb14b40a7f078`  
		Last Modified: Thu, 07 Mar 2024 00:58:07 GMT  
		Size: 6.7 MB (6738232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583f7d781500ed20a10156b2ac1384c1a374199f720920b8f547bac117624aa2`  
		Last Modified: Thu, 07 Mar 2024 00:58:07 GMT  
		Size: 24.7 KB (24701 bytes)  
		MIME: application/vnd.in-toto+json
