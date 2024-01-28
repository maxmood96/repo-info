## `drupal:php8.3-apache`

```console
$ docker pull drupal@sha256:c86f857f146666e8a93ba84ef0e4366f5b4cf6949a1bc619e80680e218457e30
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

### `drupal:php8.3-apache` - linux; amd64

```console
$ docker pull drupal@sha256:9d7257c8f519bc30aad4c046f0c480b66c1f866d3245b28382bf46205327ebe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200119086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcc5335c441f23735419b530cabbfcd407042ef04ce4548960460b5faa69303`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:13:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 06:13:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 06:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:13:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 06:13:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 06:17:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 06:17:52 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 06:18:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 06:18:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 06:18:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 06:18:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:18:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:18:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 06:18:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.3.2
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 80
# Wed, 17 Jan 2024 22:53:51 GMT
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
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a95dcec60350663284915f66e96b2d216179ebe405663a818c81de0f22f45e1`  
		Last Modified: Thu, 11 Jan 2024 08:44:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22afa33f327082e95c674a5bdf3b6d25760aca5abce3b032de2c444ba4864ed`  
		Last Modified: Thu, 11 Jan 2024 08:45:06 GMT  
		Size: 104.4 MB (104352766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa61ea11ee8a864fd6b368bd09be18de3692f7ada24f03df32e585107432160`  
		Last Modified: Thu, 11 Jan 2024 08:44:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67ae2bde3303f6e68d4e0f2e641771894224010749cd780d5b602f500d3c81`  
		Last Modified: Thu, 11 Jan 2024 08:45:32 GMT  
		Size: 20.3 MB (20303737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5356c6468fd18c3e8b9c7b77f02d4387bc52f207263ad1766a141711da8b02`  
		Last Modified: Thu, 11 Jan 2024 08:45:29 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91cb51e8865de77fe278c43f87cd11246e5a71d43047c7be581b1475e1cd31`  
		Last Modified: Thu, 11 Jan 2024 08:45:29 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905dfad1f5ebddc097c64a7e1af99e2e8ceb0d2683d3f5962ed72c153d7be07`  
		Last Modified: Sat, 20 Jan 2024 00:29:43 GMT  
		Size: 12.8 MB (12772926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dd1d2ea0c984a8ee5dd29d42e30211fb4c5ca7428a99247d9f96cc64506a89`  
		Last Modified: Sat, 20 Jan 2024 00:29:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd76059c95e8adc33cc5ef3e1f8d3e14a35ba2be8e5718da47644d271da407b`  
		Last Modified: Sat, 20 Jan 2024 00:29:41 GMT  
		Size: 11.6 MB (11633204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742bf19f28dcc7c5fe3a5d72972e78610b42b0c7bdec6b84f53436faf6f0df2c`  
		Last Modified: Sat, 20 Jan 2024 00:29:40 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d14c1366f7b57f9ee3095992451497cd3351ac8d9166f433d168bdd86aff42`  
		Last Modified: Sat, 20 Jan 2024 00:29:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e8dd0183e74671c6db54e1ea9ee9b39bba748045b830cb053e84c16084343e`  
		Last Modified: Sat, 20 Jan 2024 00:29:39 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376a32789ebc2f1bad007ccfd6de9e8b6d74aac9ab793853fe1f02b341646152`  
		Last Modified: Sat, 27 Jan 2024 11:54:48 GMT  
		Size: 2.0 MB (1999214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6c601f9e5c994b37e2a8a73f95d74bf40beb480e0932c5508c1cdaff68bcf1`  
		Last Modified: Sat, 27 Jan 2024 11:54:47 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3dae81b3e943c1aa1e1aa2decd5ed80214bf8a9a334830d232dfc44621c67`  
		Last Modified: Sat, 27 Jan 2024 11:54:48 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4bbea4520e71710fbabe80712eda122768ec3cb98f4ca3c55b50b7fee8d7db`  
		Last Modified: Sat, 27 Jan 2024 11:54:44 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c25027c89f9de906df7994f4bc8b028b0751fc88c9882baef2c93e56bd1eb4`  
		Last Modified: Sat, 27 Jan 2024 11:54:49 GMT  
		Size: 19.2 MB (19220108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:df194835903cb73f7220b4538491c6ddabe3e2c855d3f36e9df9889e44b4d7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5957414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae1c37b7be0968283b8ff6b9ad81106a61791fefe5c63824d238582ddd746b7`

```dockerfile
```

-	Layers:
	-	`sha256:cdb78a5562f4a284166efc68900613cadf667cbc51f242b5819163bbc2cbb5a3`  
		Last Modified: Sat, 27 Jan 2024 11:54:47 GMT  
		Size: 5.9 MB (5915508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:634ef70bb2e19b5c78b180a689bcaba7ddea01a50a05aa7027468c389f55eceb`  
		Last Modified: Sat, 27 Jan 2024 11:54:47 GMT  
		Size: 41.9 KB (41906 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:1776b1c4d1acf74109d0c38fc328fff1ed8a791154f6439e6234a478abdb8ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164014843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f44f223dbafe7a75f32b04a9098b5f4d71ddc400e6f0c442d554389cc5d6c4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:01:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 07:01:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 07:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 07:01:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 07:01:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 07:09:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 07:09:03 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 07:09:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 07:09:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 07:09:21 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 07:09:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 07:09:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 07:09:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 07:09:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.3.2
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 80
# Wed, 17 Jan 2024 22:53:51 GMT
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
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78480f120d1bf6d4d635fb5b3b6c319e732dd057429d1179f5e8a7c8435599bf`  
		Last Modified: Thu, 11 Jan 2024 11:11:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49b281e927e3ce40bca6838ab4b25427cc76d3bc1fe6d5d47703c2197862df8`  
		Last Modified: Thu, 11 Jan 2024 11:12:06 GMT  
		Size: 76.2 MB (76167092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b9c5e142ab0229e1d7a3ed2041f80a73142bf9108777851a45069945807a61`  
		Last Modified: Thu, 11 Jan 2024 11:11:47 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3215df082d33bfb0e065272d32ebc4ac5c259a7eadd2ebaf94aecda99376df`  
		Last Modified: Thu, 11 Jan 2024 11:12:36 GMT  
		Size: 19.0 MB (19045474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3fad5523f42cc20308e3a32d188b65108487b3dcb81737770d47b702d3ac18`  
		Last Modified: Thu, 11 Jan 2024 11:12:32 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e567489660f9bf784e38c5220f927cda797a42f1a5e3574f25251089ec466e`  
		Last Modified: Thu, 11 Jan 2024 11:12:32 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7244b81d31250cafc45a94794658e3067848cdc0e410d4e666042e7ff605cbd`  
		Last Modified: Sat, 20 Jan 2024 01:04:37 GMT  
		Size: 12.8 MB (12771057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e7d67d28fb4270aee99acd2daf77167293f2d8e739f27225dd44e3be8e222c`  
		Last Modified: Sat, 20 Jan 2024 01:04:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c4e0e70f1f2d2f15219d10e6c0bf0e33772b1a30264d6845ec52d2a7c54664`  
		Last Modified: Sat, 20 Jan 2024 01:04:38 GMT  
		Size: 10.0 MB (10026287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493e8a034142aab6226855e68aaec3253e82ca68f7bb8bdeab55694757aec850`  
		Last Modified: Sat, 20 Jan 2024 01:04:34 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27488e1e56628d8e1f1168133d2197f00fb21d46345134f87e807ce32ec1bf4`  
		Last Modified: Sat, 20 Jan 2024 01:04:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af8fba4fd2b175adbb930c2bc80b6b862d4fd3a5ef17eb1b9d2253f655e9f4`  
		Last Modified: Sat, 20 Jan 2024 01:04:34 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf351943097446940de9dfa2026e3bb93e1d7311e95ce9134ce622032454190`  
		Last Modified: Sat, 20 Jan 2024 06:49:09 GMT  
		Size: 1.4 MB (1355500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dddb3c0ed46e2d052c18e41f2a58d7ecf3de4dcb21ee116d73ba48a4b2d2be1`  
		Last Modified: Sat, 20 Jan 2024 06:49:09 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e01a5923c222003009bad9e3093ae1577640ca4a610264223751cb32bb1492f`  
		Last Modified: Sat, 20 Jan 2024 06:49:09 GMT  
		Size: 705.2 KB (705210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0168bc6ae7967cb9060e56a2741cf16163cdc024dec30fe41b0d44163038e1`  
		Last Modified: Sat, 20 Jan 2024 06:49:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3135fd075c452f0d48c789457cd57020143467a2cec7da0d9c1220ea1f48e35`  
		Last Modified: Sat, 20 Jan 2024 06:49:10 GMT  
		Size: 19.2 MB (19220088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:eaca210d978cbd1a4b2dc1c29caccbfb4b71e684dc2e5a2aa896051f91224b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bb9e3179087c76ec40c7c56a79e03b6c6e55e11d9e4ab7cff70a0cf5fa7610`

```dockerfile
```

-	Layers:
	-	`sha256:f107613a84e226d285ea5d92d0e926975cf9f8ff25932ff9e857032e4853ee53`  
		Last Modified: Sat, 27 Jan 2024 20:47:20 GMT  
		Size: 5.8 MB (5755175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d1fc12469ff3156056a03c4c0275d7ac3f9557e17430e17dc3ad9578ac2bda`  
		Last Modified: Sat, 27 Jan 2024 20:47:19 GMT  
		Size: 40.0 KB (39967 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:537ea97060026d7861975c6ac8cf5fa9394a3231d92449ee22ddbc46296abfd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194181151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496954d40f6f69e4117d08f10c97979070dd8d3d85e0e6f9d43fafa71d3c093d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:30:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 03:30:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 03:30:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:30:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 03:30:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 03:34:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 03:34:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 03:34:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 03:34:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 03:34:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 03:34:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 03:34:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 03:34:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 03:34:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.3.2
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 80
# Wed, 17 Jan 2024 22:53:51 GMT
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
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451161081bb50dfa3757568668f099cf58479733644abdbc5c2f79d7c4d9cade`  
		Last Modified: Thu, 11 Jan 2024 05:46:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e283d29837ef0a320a5446924b58fe28a48bdb544e3b65cc753b44483e58aa4`  
		Last Modified: Thu, 11 Jan 2024 05:46:13 GMT  
		Size: 98.1 MB (98128972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99cfb51d5dc36e05dbed790e970497125214a08a60c68ef185661b1a6638e4a`  
		Last Modified: Thu, 11 Jan 2024 05:46:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762abba6396b86cd8ac66ebd05371dfddd5a4be381c99d663cfd880c4c32c5c`  
		Last Modified: Thu, 11 Jan 2024 05:46:40 GMT  
		Size: 20.3 MB (20305032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b269b42eeb2e3e56c31a41df02e0fd99dda0c92189c542f90f69f5aef4b538b5`  
		Last Modified: Thu, 11 Jan 2024 05:46:38 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612f169f08b23d156c839c07adbdf6aeede1e477b8a1745a92f0e501405d955f`  
		Last Modified: Thu, 11 Jan 2024 05:46:38 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add1ee637363b159ba72c61ffde546afc4c3ff203f5070e2524838209fee24a9`  
		Last Modified: Sat, 20 Jan 2024 00:37:26 GMT  
		Size: 12.8 MB (12772672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bb7e6f2fff0d743bd99eded5f57d66c6fd972b49a6ab59596922b85ca57dfa`  
		Last Modified: Sat, 20 Jan 2024 00:37:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa0a19d110189ebeab21334c563ba46dcdaaeb8a431d9f7b628204a1fce0c89`  
		Last Modified: Sat, 20 Jan 2024 00:37:25 GMT  
		Size: 11.6 MB (11627216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2afb8ec37bfcecc0af3c32d1773db2c9cef86e7965440d90e6415d9dbe36a0`  
		Last Modified: Sat, 20 Jan 2024 00:37:24 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf658c5f144f497fb12115006d4f254766b045dc4761661f5097d26bc863d77a`  
		Last Modified: Sat, 20 Jan 2024 00:37:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c7adceb69e2e215090832cd57ea2fc1977a7cab2211e3793716407cdecaa5`  
		Last Modified: Sat, 20 Jan 2024 00:37:23 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff280536cbd97a988ad2af1ae5cd8cb770dd1e35526af7f9096936c032e5891`  
		Last Modified: Sat, 27 Jan 2024 18:05:12 GMT  
		Size: 2.3 MB (2258595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ef9dd5e42d2691debef4939fd3d8a33d90a9c5362660252948dc83a415232`  
		Last Modified: Sat, 27 Jan 2024 18:05:12 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4538df908ac8cffc609a20d0522f305ead8c2ae9b7ec0249b580c864d6820`  
		Last Modified: Sat, 27 Jan 2024 18:05:12 GMT  
		Size: 705.2 KB (705212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8a5a54d998e8a668f313f3d7e627c54d889ae04cd6e863ad929fca7b9ae166`  
		Last Modified: Sat, 27 Jan 2024 18:05:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1101a26df1f61ce6bfd2e70d1ed6b6bebff691d513f7411181bbdf9cc6e88f8f`  
		Last Modified: Sat, 27 Jan 2024 18:05:13 GMT  
		Size: 19.2 MB (19220114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:1573ee0d5860336ecdfc61a249a23cc48ef733dbe846a3454ae108abd2d3cb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5982456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0c3697402d8ec674c15e6db33ae565c8ccaf55e4b09a058267f7f07f7e1ea8`

```dockerfile
```

-	Layers:
	-	`sha256:37db9519c4ded8deda88a4abc4a4fc07a5d89aa2902dcc5aeeaa7f4624ffb8c9`  
		Last Modified: Sat, 27 Jan 2024 18:05:12 GMT  
		Size: 5.9 MB (5940531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:176ee26f10e3c92ddfd026fa7739da921491604a17d9f22a38e2da9ccf6b4e1c`  
		Last Modified: Sat, 27 Jan 2024 18:05:11 GMT  
		Size: 41.9 KB (41925 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache` - linux; 386

```console
$ docker pull drupal@sha256:74824812059dd4b4e3b0dd10179644fa14823e9aa4dd0a6ac79f6f903d4d4f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199111756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1e449b773e6553a6c54fe06c542fe3050df8d25b3cfc43d48c0c29cc93ffba`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:48689786b7812032adc0d36643501f16ddee15750a8f0f8b614dba58e5037b2b in / 
# Thu, 11 Jan 2024 02:38:40 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:58:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 04:58:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 04:58:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:58:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 04:58:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 05:05:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 05:05:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 05:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 05:05:36 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 05:05:37 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 05:05:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 05:05:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 05:05:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 05:05:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.3.2
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 80
# Wed, 17 Jan 2024 22:53:51 GMT
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
	-	`sha256:de2bfe459016bec412fddc313b793adc6d47c8a4540608a6f3e217998027f073`  
		Last Modified: Thu, 11 Jan 2024 02:43:20 GMT  
		Size: 30.1 MB (30143875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946df82896e7966597c6491529e0230dd6f4ba0b305c589840bc9133f0535fa4`  
		Last Modified: Thu, 11 Jan 2024 09:11:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76d33e770c7aaf9e80071255e0e21cfc96139d4398eeda332ed50d769a3e6b0`  
		Last Modified: Thu, 11 Jan 2024 09:11:46 GMT  
		Size: 101.5 MB (101534598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97c877b297ab5b95038cd30ec523bacef9b483ba3674f3ddf56597062ef9955`  
		Last Modified: Thu, 11 Jan 2024 09:11:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a0b6736627858a695eb9b48b55ce6ef151a47aae0f60810d77efb68928bc15`  
		Last Modified: Thu, 11 Jan 2024 09:12:15 GMT  
		Size: 20.8 MB (20825996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c39c6532ba583bb00f0f880fa1ec094d1dd2e8e9a00e933b12731b486b3db7`  
		Last Modified: Thu, 11 Jan 2024 09:12:11 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9ecb92d7ef9c250277fa01c18fa30461213a07d580f494d2e70daaf794d7a`  
		Last Modified: Thu, 11 Jan 2024 09:12:11 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3f757954e92997ce8c2257f503d969f9d0558bd29299275aba286068397b6`  
		Last Modified: Sat, 20 Jan 2024 01:44:04 GMT  
		Size: 12.8 MB (12772099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9068b34b8fe2c9ffaf9d01fbe9a3c647214329396ed106a5424711969f441387`  
		Last Modified: Sat, 20 Jan 2024 01:44:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bed5d604238637693d9985c4545078df7484f0e8281b878d7eae575f34d80fc`  
		Last Modified: Sat, 20 Jan 2024 01:44:05 GMT  
		Size: 11.9 MB (11850215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3b06cfaab0fe5db5e5028806a15ab2f936f528bb681bb0b453fea7e25f4f6d`  
		Last Modified: Sat, 20 Jan 2024 01:44:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea6b567de69b9e9ca1353c752e568bb5d261ca2671987be6e8f58393ba97cf6`  
		Last Modified: Sat, 20 Jan 2024 01:44:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0181e0a30864ee660ecc38aa85321422d5a2d7c2af82485e203beab9f7f0706c`  
		Last Modified: Sat, 20 Jan 2024 01:44:01 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7899bb00d96d3b9a716972c53a3df430a7aba96ea2231b44912820520fbfb261`  
		Last Modified: Sat, 27 Jan 2024 09:55:07 GMT  
		Size: 2.1 MB (2053180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a65df278b9e124f3e593cc82a6211727f86bc7783ec7bc3a267ec04ed14e5`  
		Last Modified: Sat, 27 Jan 2024 09:55:06 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0fabf0e7e4ea14ee6c2837f258ad7d2382bfe83eff249b7b6b5a22cb48e7ed`  
		Last Modified: Sat, 27 Jan 2024 09:55:07 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6732b737424db8d904c158273193eccad15ab441c803f31cae6f89631a42deb3`  
		Last Modified: Sat, 27 Jan 2024 09:55:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19df72a8129b8e37777568fc3544860abc5f3dd023617e5043c96dd7454758`  
		Last Modified: Sat, 27 Jan 2024 09:55:08 GMT  
		Size: 19.2 MB (19220598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:a25089090b2da9f8522e37a0349d862587bb87ce5a898ef3d0f649384624b8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5939433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ca78cb7021cb083d317e2b916e757621a78141243cbaf216ab7d6c2e3cbcf5`

```dockerfile
```

-	Layers:
	-	`sha256:b3c7e1a13b2d2a030544493dd445d42ee2770964b53786b61583f27718470cfd`  
		Last Modified: Sat, 27 Jan 2024 09:55:06 GMT  
		Size: 5.9 MB (5897604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2b90dfb48361d6cc269ee67e8c8c472334fde60f09acbf271ad95ffce0fde9`  
		Last Modified: Sat, 27 Jan 2024 09:55:06 GMT  
		Size: 41.8 KB (41829 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:1d92d127876aa246b8ec83f77745a13e0a9d745752a88e4c872013d5764d8760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204534833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bdfb3f0d5b1a07eb038b2fe50f2c473142ac5e525aee6adbe95eea7ba9ee87`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:27 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Thu, 11 Jan 2024 02:34:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:20:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 04:20:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 04:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:21:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 04:21:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 04:25:15 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 04:25:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 04:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 04:25:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 04:25:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 04:25:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:25:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 04:25:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 04:25:51 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.3.2
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 80
# Wed, 17 Jan 2024 22:53:51 GMT
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
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deccbdb3118a70cea029f0aa9a00e20f50a0f9e7ee48c0b2e47e908baa1aa9`  
		Last Modified: Thu, 11 Jan 2024 06:47:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b1fe163bf5146471d387e12d2994c0200954be8c29360da9b7d6645856db5d`  
		Last Modified: Thu, 11 Jan 2024 06:47:21 GMT  
		Size: 103.3 MB (103321106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21810f5c2e4eb5e038fb75e5935cd7ee106a1f1c2af8465b5b414700d1cbc42`  
		Last Modified: Thu, 11 Jan 2024 06:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db359f0198220811583d45f054d34f3c7eece5487a08c02682858796dd467dcc`  
		Last Modified: Thu, 11 Jan 2024 06:47:51 GMT  
		Size: 21.5 MB (21489342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153b50b7700af076c4027ca4685d067048893bbd5b852047f87dbaeb97568c66`  
		Last Modified: Thu, 11 Jan 2024 06:47:48 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e9665480e2e5dd3d7d2c11091468a75255d8bdaec9cc796844f121e83048f`  
		Last Modified: Thu, 11 Jan 2024 06:47:48 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649ec3f0fb60f5eddd2047ea8abd9e5a04e73ef4d7e24733df3ea9c327c73a09`  
		Last Modified: Sat, 20 Jan 2024 00:01:34 GMT  
		Size: 12.8 MB (12772437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2009dd14ba3ce6f074d91bd1c40122d5124334c6cfc53da7511626193268b85f`  
		Last Modified: Sat, 20 Jan 2024 00:01:31 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e46b47697e0062eafff0caebafc2aedba8f3cb1fadb30883c720d4843a616a`  
		Last Modified: Sat, 20 Jan 2024 00:01:33 GMT  
		Size: 12.0 MB (12043352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df11c6e6411798f996f396c246ce0cc352ac93962ffc32513574a4a20d6aa05a`  
		Last Modified: Sat, 20 Jan 2024 00:01:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3b3834e017cbf197e4384201e7da3dc5010ac548416eac3f228dd2a0201a5`  
		Last Modified: Sat, 20 Jan 2024 00:01:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23629c3638596b5b6553024c23ad2677addd445671fbac88876a952159aadb92`  
		Last Modified: Sat, 20 Jan 2024 00:01:31 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536ea6b0462bcccea6fc3a483df2b9cf68b2a486ecb23fc190da27e40b6d1552`  
		Last Modified: Sat, 20 Jan 2024 04:33:29 GMT  
		Size: 1.9 MB (1856258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738d0e1aadaace0346e65171e37be3c570c5cbd56ba5c94172517327038f569c`  
		Last Modified: Sat, 20 Jan 2024 04:33:29 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dae6a0ebee515857d9517be77c74e5fae3c0285ea06e32b53dd1ca20202f65`  
		Last Modified: Sat, 20 Jan 2024 04:33:29 GMT  
		Size: 705.2 KB (705209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130107e7c93c31ac689500e48db6cba384f3f3406576a5d01885d9df0090c1c3`  
		Last Modified: Sat, 20 Jan 2024 04:33:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8581e53565ef7caf720d13119f8892b5c8955f67bb55cb20b2c88a7fa85dd369`  
		Last Modified: Sat, 20 Jan 2024 04:33:31 GMT  
		Size: 19.2 MB (19220576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:6a7c593c4f02cc36fb2e209c01be64ae61e995dedfb55c414f40c105e1093dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb244a7a404093e602f4133264b34a44cfbf93d26a17c33274629c3873a439a3`

```dockerfile
```

-	Layers:
	-	`sha256:e97032b1dccd98787f5c6df4bae653a0e421c6a0ff69067fbe0c01530e3cd2c4`  
		Last Modified: Sat, 27 Jan 2024 11:41:06 GMT  
		Size: 5.9 MB (5896883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6ad4a105250aedc09ce52ef3721ab22518bafe907999e30724c46d2fc4358a`  
		Last Modified: Sat, 27 Jan 2024 11:41:05 GMT  
		Size: 39.9 KB (39891 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-apache` - linux; s390x

```console
$ docker pull drupal@sha256:897f07f87fc24fd3a8b52c7fd62b284c44648655b3eb25c668c7fd2d5283e427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173309448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712170815b5a7f38c1c7511ab7dde57699a12f5b238a50b6f3738f8800ac1fc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:22:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 11 Jan 2024 06:22:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Jan 2024 06:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:22:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jan 2024 06:22:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 11 Jan 2024 06:25:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 11 Jan 2024 06:25:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 11 Jan 2024 06:25:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Thu, 11 Jan 2024 06:25:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Thu, 11 Jan 2024 06:25:58 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Thu, 11 Jan 2024 06:25:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:25:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jan 2024 06:25:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jan 2024 06:25:59 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.3.2
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 80
# Wed, 17 Jan 2024 22:53:51 GMT
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
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970b99384646b14a68f58b4d5f20aa7646bcdb273987830ab94a7d0c52118696`  
		Last Modified: Thu, 11 Jan 2024 08:18:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5937e142a80962f22503718b83e94f9fcb8d1c62fac80dcce04bb7b4061486ba`  
		Last Modified: Thu, 11 Jan 2024 08:18:23 GMT  
		Size: 80.8 MB (80814132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ae514a5d8229351dc8ed615a4b5ab3427359d88b93956cdc894c5a4a652bd`  
		Last Modified: Thu, 11 Jan 2024 08:18:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b8e435e581d3dc2f630e33354f40c1595733614e874fe5325c916b9c05987b`  
		Last Modified: Thu, 11 Jan 2024 08:18:40 GMT  
		Size: 20.1 MB (20083203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77340e1ba61c24de6634913db72d5a424d3864312ac9e0f791c0d19940f708`  
		Last Modified: Thu, 11 Jan 2024 08:18:37 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d4aaa5dad250c12a0dcca6b3b73e0d7c6e5bb321be4a2c64e9a50fa7f9bcda`  
		Last Modified: Thu, 11 Jan 2024 08:18:37 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b51c87141fd0b63d502565d89b2abbc18230f1e89570873ce6f978e8ff366`  
		Last Modified: Sat, 20 Jan 2024 01:56:24 GMT  
		Size: 12.8 MB (12771227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ba672bbf3ef509af06d72aa5816d796f9a71547a045ea26d5e128b1158ec1e`  
		Last Modified: Sat, 20 Jan 2024 01:56:23 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9dfde922e09a9fb80b06d05faac5b15ae4f3f66745d7241f66273a28c9c08c`  
		Last Modified: Sat, 20 Jan 2024 01:56:24 GMT  
		Size: 10.7 MB (10661522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cdd5594c152279463f24ec8099a55dc8201fca31b58a4a04d9d88db4b2894c`  
		Last Modified: Sat, 20 Jan 2024 01:56:22 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bece06a95c55a4de406b363fc081492611d350b84faa6d7ebb021624d59f260`  
		Last Modified: Sat, 20 Jan 2024 01:56:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1a88ab9801a2134dedf32a242f2b8df90334bc49830c015c585688bfb7626c`  
		Last Modified: Sat, 20 Jan 2024 01:56:22 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f648295bb80314871a55419f862d1c6ac8a3021e9511ad1a3483575d96a4d52e`  
		Last Modified: Sat, 20 Jan 2024 19:14:29 GMT  
		Size: 1.6 MB (1555130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25294fcca0ee0ee04fbf7f13e264ef0e9c1d071ea3098ccd4e5881831813f8df`  
		Last Modified: Sat, 20 Jan 2024 19:14:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab394d64c031defe7fd1149f3c87aec2c70466951b3d7f317851f864bef7a8`  
		Last Modified: Sat, 20 Jan 2024 19:14:30 GMT  
		Size: 705.2 KB (705211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c30a66c1f0e82cc845ce1aca98126da71e0c8a443d91170a311476b0f0c6a7`  
		Last Modified: Sat, 20 Jan 2024 19:14:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcdd5fedc128b0ccb95845c3258d8d36c9c908e5953540bd246f256adf7e9e8`  
		Last Modified: Sat, 20 Jan 2024 19:14:31 GMT  
		Size: 19.2 MB (19221170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:b204cc9043470c8dba807f16b117092dfcdb18ab785ce631cb0f22c16fa37858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5816801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e4f06dca47bd83c1928ba695f3aa1783fa5bd0f50a97228fdc88a4c09be070`

```dockerfile
```

-	Layers:
	-	`sha256:8c2f406141ad9e2291952ed421bcd5222d4f5a2ef96ca52562a05086c25c2d1c`  
		Last Modified: Sat, 27 Jan 2024 22:17:29 GMT  
		Size: 5.8 MB (5777010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a32ac135d0a7c46fb7069f3723fd2d0a425bbe347a2771bc808dac516fa69b`  
		Last Modified: Sat, 27 Jan 2024 22:17:29 GMT  
		Size: 39.8 KB (39791 bytes)  
		MIME: application/vnd.in-toto+json
