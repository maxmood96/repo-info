## `drupal:11-apache`

```console
$ docker pull drupal@sha256:203d8ecee548798abb6eb87f3b9babaa4e658b947181e939b48a54b70f23f5df
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

### `drupal:11-apache` - linux; amd64

```console
$ docker pull drupal@sha256:f11b3d905f4f1d5e3c834271c63c87ae34ab48a87624b1e13fa8c83f88c7158e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199916706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5bb580b35d102375dba987a5e165cf43fb720329b7ca700fd0831f01e76f7b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Nov 2024 22:37:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["apache2-foreground"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d111fc47c430ee2a0192d15719580b61457fd1a26cb45ec85aa406356c1b1ef`  
		Last Modified: Thu, 21 Nov 2024 17:59:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193b424feb9d5a2939e7bba165a3556a464b0e44697a8ac9a1347ab123df2090`  
		Last Modified: Thu, 21 Nov 2024 18:00:12 GMT  
		Size: 104.3 MB (104345665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0217fa02fd5fc5ac58d715e51f012bc438273113812bab2644e46525d2cf83e5`  
		Last Modified: Thu, 21 Nov 2024 17:59:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119202f2b3190b7bdf2b099905a2f5e643f3f66c1ce2ff32b55e0932b17d7542`  
		Last Modified: Thu, 21 Nov 2024 18:00:10 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41950bab19cdd2de76a484ab017f6f5476ec57b30466cec4aa531c3784f957f`  
		Last Modified: Thu, 21 Nov 2024 18:00:08 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d8d2e94654beb4e4d0fbabedf49c0786a19fabb3d120b053e7ff5d6dd415b3`  
		Last Modified: Thu, 21 Nov 2024 18:00:09 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78f6431083adccfcb48bfc93f6e87438833fb07f2b4be08e0293d5645e7555`  
		Last Modified: Thu, 21 Nov 2024 18:00:10 GMT  
		Size: 12.6 MB (12648310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967cc2bfc1081a7a907315564dbe7055197f7cbdb4d24d024d9fcbf2eb0ea630`  
		Last Modified: Thu, 21 Nov 2024 17:59:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0941d9a564d8cb1e7548b420a1f2bd7ded73a26f4d5171bdc914d97611983673`  
		Last Modified: Thu, 21 Nov 2024 18:00:11 GMT  
		Size: 11.6 MB (11649959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b04b7031fbdcaa2d91863c1d28d6e018b86462a39f65b24301d9f428ba497f`  
		Last Modified: Thu, 21 Nov 2024 18:00:11 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd375cf222d21ad2c772211c50813572ef4dd8975ce782d3cb3af5be5d8a7c0`  
		Last Modified: Thu, 21 Nov 2024 18:00:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d672bde1497b2c68e72b5bc6d81a952fc1a45670f5210a425599c08767c7c`  
		Last Modified: Thu, 21 Nov 2024 18:00:12 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617e467709d18419d819e2cd0843d6950e90de0a3f23f7953155992d0c06ff39`  
		Last Modified: Thu, 21 Nov 2024 19:28:50 GMT  
		Size: 2.0 MB (2000007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d93e3a1966843aa8c25e34db82d17861821ab62feab291c55c2815533c6f2b`  
		Last Modified: Thu, 21 Nov 2024 19:28:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204c2ef928a0e743733413c5cb2df46ae98281457da3addd9d3086d276b1238a`  
		Last Modified: Thu, 21 Nov 2024 19:28:50 GMT  
		Size: 739.9 KB (739895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e18fd157728886352393bac9500d58199f8aa16e39bc103c2b2585b88fb0d55`  
		Last Modified: Thu, 21 Nov 2024 19:28:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1522ab7c23402331a36d1c79a196086f3824f7bd665bd389a88ae0707a81057`  
		Last Modified: Thu, 21 Nov 2024 19:28:51 GMT  
		Size: 19.3 MB (19275155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:fc9f754d839f87c75c86f5e0ce249c45ef0b8a76593f7091d7ceabc71606e96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6907008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d7f613535fe892c26d5292615bb81c4a67bf735c6cf4129db3d6998acae0cb`

```dockerfile
```

-	Layers:
	-	`sha256:9c8a16f6eafbf81df111a4ee4b356016df43e53e4a579304246e1ae94ca76821`  
		Last Modified: Thu, 21 Nov 2024 19:28:50 GMT  
		Size: 6.9 MB (6864114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304acc48f8d92c1958dead88cbc89addd7690082406da4ef9113f350371e8757`  
		Last Modified: Thu, 21 Nov 2024 19:28:49 GMT  
		Size: 42.9 KB (42894 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; arm variant v7

```console
$ docker pull drupal@sha256:e1c21ba6ff18523381838f061d90729de50b5a02736d705a3038aa30a3d683cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163801103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2c18bdaf0e4fb4d8372ef9fe2d059d67fd99116d2385d0fec85947b2d3a79f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Nov 2024 22:37:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["apache2-foreground"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4297c5ae3c7e8e8915409622802213bf4512c2b4a0bf9a86ed680878ddc18a70`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b50adcb7cdffa12052ba1589718b3c06d474e40507177a93fc914de46e895`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 76.2 MB (76162385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681174cd466f54c52977f6c159c33d12bdd6aa108d2d06470ff258ce5d3fac19`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3956adc6ba757482684b1a409597f790541c714f71ba631eee7d291574e817e`  
		Last Modified: Tue, 12 Nov 2024 03:15:54 GMT  
		Size: 18.9 MB (18857501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e647e764fe2dcfbd101cd5fcaaec1c944c7cd89cd40a65dcd2442b62733654`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429807ca1f9d7d3c489deadada060b40a6d8bd76e76a48f0a9298d511be0304c`  
		Last Modified: Tue, 12 Nov 2024 03:15:53 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422974b0dd4b10270d4b45e7d7d79417adbd2f02e6a9ef87d991c7a02f519026`  
		Last Modified: Thu, 21 Nov 2024 18:51:59 GMT  
		Size: 12.6 MB (12646795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dcadf17699b85e6533a61d1704e90b7c3a3692da2634a771f4309ca2603104`  
		Last Modified: Thu, 21 Nov 2024 18:51:58 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6e4749653d19939519eeb08aaef4f7496cf2aee2913fa377e29233aa4c1c65`  
		Last Modified: Thu, 21 Nov 2024 18:51:59 GMT  
		Size: 10.0 MB (10039422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522c474c64e702a6246eb9bd570c3fe1369c662d3772ba53dbae3c5413c1536b`  
		Last Modified: Thu, 21 Nov 2024 18:51:58 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323cd2d3d77115ba94060ec89a913ad4a47c2419b629f55197bd0d8e8076379`  
		Last Modified: Thu, 21 Nov 2024 18:51:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f663d31c2e82179004a01feb5f621bb04b8dfb9aefb85c6d760d596e2757731`  
		Last Modified: Thu, 21 Nov 2024 18:51:59 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53671057a08bd33c62c5dce341c0e336acc6ff6415711d1c83a4435dbe314b94`  
		Last Modified: Fri, 22 Nov 2024 04:01:16 GMT  
		Size: 1.4 MB (1354978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6aa7bd59053f73b86e569043eeb6c30e7d61bdb3f4b1b8a6f05721527bb71c`  
		Last Modified: Fri, 22 Nov 2024 04:01:15 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff185faa55708da0dc64aeafa39fbbabadf7bb731fb45a1ae4ff5761cf0c1`  
		Last Modified: Fri, 22 Nov 2024 04:01:16 GMT  
		Size: 739.9 KB (739889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cff824afc8c8c74d88b605f4248fc6b5882aab28825ef95a2a4f490df02f0`  
		Last Modified: Fri, 22 Nov 2024 04:01:15 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1449cc462f52864fa728266fe029e2d21723c43c3f8ba2e7dda1d4cf144aa359`  
		Last Modified: Fri, 22 Nov 2024 04:01:17 GMT  
		Size: 19.3 MB (19275319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:420c171dc401336af42e83e3dfca71dd9bf86d8a2d3a3b2960a70742fb11bd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6722167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0406f8dadd9f2e34811b08226cbf740443395ee28413d908d53d42b2705f38f3`

```dockerfile
```

-	Layers:
	-	`sha256:68372d795f4d09219468b6708965e4b8525156af5e66f22554e1e96d7a731932`  
		Last Modified: Fri, 22 Nov 2024 04:01:15 GMT  
		Size: 6.7 MB (6678994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c834427a2b35c7d2f832c5707af11f4edc19fe27dea8d002f89eafa33c7215d`  
		Last Modified: Fri, 22 Nov 2024 04:01:15 GMT  
		Size: 43.2 KB (43173 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ff1849d66f7cabc6bfc55502a7346f9b63b59f0501f8f7598e823e040e1dfe81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193976244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc966fdf85e330713484a5df6b47054ea600f2d1679502a33a212b18d7ec870`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Nov 2024 22:37:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["apache2-foreground"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2c3efb5abbf8e94e4d66dc2330b25721feadd8a01a30c62c6a2d211e09fcf5`  
		Last Modified: Thu, 21 Nov 2024 17:57:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44629439c7e4c1ff8ecf41969075f175aeaa0d716e14846e8e273a98662ac50a`  
		Last Modified: Thu, 21 Nov 2024 17:57:38 GMT  
		Size: 98.1 MB (98130596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc85a62df490f0424a1d74531ad9dc6c9da15950f9cff18ffc5a1ec77331483`  
		Last Modified: Thu, 21 Nov 2024 17:57:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18100fadfd8a918109622c9df36831c0544276522dfadde8da6065286508704a`  
		Last Modified: Thu, 21 Nov 2024 18:01:25 GMT  
		Size: 20.1 MB (20120879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6835d6a09c304dec6de48a0b0f7777eaf1cb2c95cf3ab6c7e4fd023070581aff`  
		Last Modified: Thu, 21 Nov 2024 18:01:24 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f99f2d4839d254deaa59c2c3ec6f8e9913860995545ecc2a75c8b8e873ca532`  
		Last Modified: Thu, 21 Nov 2024 18:01:24 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15ee9357229ebdf4a177102a1e7915d5861e1da64b3bdf2c1286d01f7aebbe`  
		Last Modified: Thu, 21 Nov 2024 18:52:56 GMT  
		Size: 12.6 MB (12648130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d9a4f1cac140aeae99a8bec4d83f3838d29b763c500f44d2b8823ebdb9b8d`  
		Last Modified: Thu, 21 Nov 2024 18:52:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee73915e0007ea6cad9132521de10448ccfcbfe7c76a72dd43adb02204ee4ce`  
		Last Modified: Thu, 21 Nov 2024 18:52:56 GMT  
		Size: 11.6 MB (11640242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904796fd93498f887ff1083b34ce503943ba45ef472efa92e4c36629b21669a`  
		Last Modified: Thu, 21 Nov 2024 18:52:55 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad94d2ce62756d1180acbda70ca43cfea7190c70587b74ac8374b1c6cde9ce25`  
		Last Modified: Thu, 21 Nov 2024 18:52:56 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf017c5180176c7a0160e687c6f3564a5a94b238d78c066c700411db3006acf`  
		Last Modified: Thu, 21 Nov 2024 18:52:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bf71e125d4ed321a5d25d42c0d0c2f0f63b4d64345fab0a4adf759b3317493`  
		Last Modified: Fri, 22 Nov 2024 04:15:47 GMT  
		Size: 2.3 MB (2258160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326ef9b423286c47e5521d91a7e19ca39291ba663cb079bded99dae354ca4c32`  
		Last Modified: Fri, 22 Nov 2024 04:15:46 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cb66ad5752260e77b3afeaaf19711c73bb8d00ebe8bb70584b29cfb6d26072`  
		Last Modified: Fri, 22 Nov 2024 04:15:47 GMT  
		Size: 739.9 KB (739895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaadc152396574f211a8abcc3f5dc76ac0df07ae910840a4393deaa5ce511d1`  
		Last Modified: Fri, 22 Nov 2024 04:15:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b50551d4de61fa3ffded2ac42071b5864bd038d2974519c42d48c2f458cad1`  
		Last Modified: Fri, 22 Nov 2024 04:15:50 GMT  
		Size: 19.3 MB (19275084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:8d4ec40fa395d74159239c6850a6a5d793380d7dc6d1684e2eac4752bc1cd6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6936087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83decb24331262aad4dcc4ff4a22026404e7e1871c89ef3d5ffdb5ad7770ea0`

```dockerfile
```

-	Layers:
	-	`sha256:9f21098aaf7402d20e33753d81715ab20e7a80584bef9f266fc95ded232441a3`  
		Last Modified: Fri, 22 Nov 2024 04:15:47 GMT  
		Size: 6.9 MB (6892798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1596d8695e57ec48e05fb2f3cfdb8544a507a2591bb0e2951a2d72a4c7cd69b`  
		Last Modified: Fri, 22 Nov 2024 04:15:46 GMT  
		Size: 43.3 KB (43289 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; 386

```console
$ docker pull drupal@sha256:fb037dd6e424375c42db0c900f022d16e3fe9e67fe169cd0149fb26f7c7dca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198884908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c74c8505bf548656e6eaff18aede71614735f9ff60eb238627528f9960968d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Nov 2024 22:37:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["apache2-foreground"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6b21141c42b0db357a043cff5322268453b96b3a8ba6142cfb28e54509f560`  
		Last Modified: Thu, 21 Nov 2024 17:59:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a19236eaad5d9a59a25d6d44ce458afd1449c47176053cb1c2b07c656d4ea5`  
		Last Modified: Thu, 21 Nov 2024 18:01:04 GMT  
		Size: 101.5 MB (101514273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0217fa02fd5fc5ac58d715e51f012bc438273113812bab2644e46525d2cf83e5`  
		Last Modified: Thu, 21 Nov 2024 17:59:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea0c359a36058b6e7cc8805b3e046aeff6bb0459d7fbc18678ae7ffec61421e`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 20.6 MB (20638451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b4b4710be11a274365bd5a34277a41d6e55bd3b91851ce25304a4849697f3`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca8ffd1ca168207169751ae5439c152af206ae1d95e4c8c7b13eccccd79d6d8`  
		Last Modified: Thu, 21 Nov 2024 18:01:01 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b331e3735dcbee47811459a5ea93627bfa2f94a04b6f472eabf0433dd75e9a`  
		Last Modified: Thu, 21 Nov 2024 18:01:02 GMT  
		Size: 12.6 MB (12647617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537fcd756b3c1ebcb77ae837eccc085af0e8cc2a5ab8a579735d6a4dde557f4d`  
		Last Modified: Thu, 21 Nov 2024 18:01:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d889500d0c67f9b8384a472971a8b2578ae166b13224762ef89d369d4ef0849`  
		Last Modified: Thu, 21 Nov 2024 18:01:03 GMT  
		Size: 11.9 MB (11866123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7abc28024dcc02af6a333e99bd8396530a9be9dd4f403299cb98602e88af5`  
		Last Modified: Thu, 21 Nov 2024 18:01:03 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd24960ee298104edc0b13221a1e1a07140d877c06c73c8d5f0e47c8f16988dd`  
		Last Modified: Thu, 21 Nov 2024 18:01:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34755516292ad0719073f3685d2fe26966b827f670d7a732a9b937f8daa69662`  
		Last Modified: Thu, 21 Nov 2024 18:01:04 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e609f7ea2598ae71f415ea6eb9feab6a03f894cb37a11eb23d106370bf4913a`  
		Last Modified: Thu, 21 Nov 2024 19:28:33 GMT  
		Size: 2.1 MB (2052093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04442279243abb85f526b1256ee39b309106d748789f262cf0d83891cf9e462f`  
		Last Modified: Thu, 21 Nov 2024 19:28:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81affb1df2ebf3cf83cec60f576aaaec0328961f5ba2950a15b29cf1f93b7ad`  
		Last Modified: Thu, 21 Nov 2024 19:28:33 GMT  
		Size: 739.9 KB (739894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d95c20414b8e69a4c1554706f372128dfc615a0d2688214ce5a54bab8eaef38`  
		Last Modified: Thu, 21 Nov 2024 19:28:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19446164a25463176500897710ec5ee69e9e453f022d9095e41e71d265d2c66e`  
		Last Modified: Thu, 21 Nov 2024 19:28:34 GMT  
		Size: 19.3 MB (19275103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:d1201690a76f1d359500d3b4df400cd724e5ccbd165eb172d5a836d030b578fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6887025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9466d65c9d6f012f0abe8e0cef1d30a0cbdca668c0168832f508c4bbfdc4d`

```dockerfile
```

-	Layers:
	-	`sha256:1101f5759caa95ff8a93a3740131e1a01106a02163b937f7aecf9d52b0ead5e3`  
		Last Modified: Thu, 21 Nov 2024 19:28:33 GMT  
		Size: 6.8 MB (6844274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5131d48b6442dcc9575e0cce7a0d411329fecbfd22686a618fd6976e52edd000`  
		Last Modified: Thu, 21 Nov 2024 19:28:32 GMT  
		Size: 42.8 KB (42751 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; ppc64le

```console
$ docker pull drupal@sha256:3413f0b6da407eb061de112592383b501b2c57f9e0d95b930952875c1a2ae6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204346800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27aafe47175f9d7f3da8f552bad8ddc3c0edd959d468d948445be3a0f535222`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Nov 2024 22:37:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["apache2-foreground"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02cceb11c5f92ea5660ac6e0610c26c972c38dae66eeb9d41e3387390540062`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1d6ec9f7f7d2e7f8318e16194758fc58116d42583559cad4394fb117b2d735`  
		Last Modified: Tue, 12 Nov 2024 03:22:56 GMT  
		Size: 103.3 MB (103323960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e883340f45c1d0e36d2a728cca20410ca3254d93c803c062646dc430b8e41e7b`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2155f33ef158a9585945d382ada5e33cc0a6cb3faf942e6f840e0af8c0ef4e`  
		Last Modified: Tue, 12 Nov 2024 03:27:38 GMT  
		Size: 21.3 MB (21308382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7c3966720dc0d3b2f38f69d3927be83fe5fbd6d2d6ee5d45e6635cd22825b`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b76c10e03d21d789b97d145b294ce14e9afc78a7624eddb9a1e308056c07b3`  
		Last Modified: Tue, 12 Nov 2024 03:27:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c8bf88d92515be0c6db2fa150969358edd5ca05ac26bef18210332d7ef4c9a`  
		Last Modified: Thu, 21 Nov 2024 18:41:00 GMT  
		Size: 12.6 MB (12647979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d736e3dedbfad3b83771daf2c1ea3b092e51c9fb546ed8c77ce3211f82157a`  
		Last Modified: Thu, 21 Nov 2024 18:40:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e95626077cd230ebfe6d1a8f47494b65f9684fcdd081887a9cfaf3eb2e5a63`  
		Last Modified: Thu, 21 Nov 2024 18:41:02 GMT  
		Size: 12.1 MB (12064093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825937228ee4149b3fc0ee189180898268b20776d207d6e43939ff1cbd74f8d`  
		Last Modified: Thu, 21 Nov 2024 18:40:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c40b26f5cee1e119cdf8490ef1da513f84a2de7b09e378eff54e296090fdc19`  
		Last Modified: Thu, 21 Nov 2024 18:41:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355f1ad646b6545339f68d306c0e34eda957cc353a6af09c9e8744f8207301ae`  
		Last Modified: Thu, 21 Nov 2024 18:41:00 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e541b78086604cfca7cf57e74efe3861609bbb60ddadbf4a1926bb5a3570b06`  
		Last Modified: Fri, 22 Nov 2024 01:10:36 GMT  
		Size: 1.9 MB (1856028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b5f1ff310b736298cfb09a20722b0969bdfaba866d6c30339f8f71a1e11fab`  
		Last Modified: Fri, 22 Nov 2024 01:10:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c07731cee14dd9245a66599c4bb71974f1d47297238cb549c4ebda8e1e4b7ec`  
		Last Modified: Fri, 22 Nov 2024 01:10:36 GMT  
		Size: 739.9 KB (739896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543d15fe4ce4e46f62505000c21de0e559cd4f04857f10145dbcd75b76a264a0`  
		Last Modified: Fri, 22 Nov 2024 01:10:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02c16afc0b4480725ffaf56de618c02c2d9474e724093a4d3b7de2573625fe`  
		Last Modified: Fri, 22 Nov 2024 01:10:38 GMT  
		Size: 19.3 MB (19275197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:e05a8b0268d6717730f867457bf1f053d13c8f5dbcf65a816c650906f9b11f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6884251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4e150231bfb35cf9c7bc8aab45c9714fc087d80e56a276d1d7d404dea5ef0c`

```dockerfile
```

-	Layers:
	-	`sha256:b2a2e3804d424fe3dffe2741d98c7b9bae92419667185c29ffeef97525e9d2dc`  
		Last Modified: Fri, 22 Nov 2024 01:10:36 GMT  
		Size: 6.8 MB (6841178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddc0119fd4332b11d42fb8dc69d34a8162163a1a22320d4d036780f0b6dc7e0`  
		Last Modified: Fri, 22 Nov 2024 01:10:35 GMT  
		Size: 43.1 KB (43073 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-apache` - linux; s390x

```console
$ docker pull drupal@sha256:7bedbfdb39598d0a89c01f2d60011c798e92b7a14ddfb3da2ab40c9417c1c48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173292823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f1f19fcc949ebfa1f11ca96f377d0af89e9bb3c6ae0c39aedc037508fb29c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 20 Nov 2024 22:37:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGWINCH
# Wed, 20 Nov 2024 22:37:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["apache2-foreground"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557ec8c9288f91e0e914bc88a84e7f99c5caf8f6d9840288a739773c38a7c07a`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26af4e0d7a3fb552ad3968a1cee38ccd36f353e2162832fca3623342e7ab8a`  
		Last Modified: Tue, 12 Nov 2024 03:15:07 GMT  
		Size: 80.8 MB (80817024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36392fa6e835e08d294727ebd2c1c3a2bb6f80d6dc6273a5056d2f6ed2c1ffed`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e67acbced0cb69e2dc640f712d45dcfa623c348b09bd75ae63c1818f0129f`  
		Last Modified: Tue, 12 Nov 2024 03:20:14 GMT  
		Size: 19.9 MB (19895214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5427c8084a617f516431588d36205b585b6e003a7c6f3326454cc9e4e520946`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd0bc1eddda7a2174cecf32a39f30306b749d6521c2b41823a1b05b41eef6f9`  
		Last Modified: Tue, 12 Nov 2024 03:20:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d2fb57742759ef7169aec807238b1d30df5ba2dec0b875bc04cee986672763`  
		Last Modified: Thu, 21 Nov 2024 19:04:25 GMT  
		Size: 12.6 MB (12647112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb707621ec909054da5deb10eb01f5454e19281952e315de4069f5f2083ef78`  
		Last Modified: Thu, 21 Nov 2024 19:04:25 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6e9afe3c421e9a7e9991b6ee4ab4ead4f1b5ddd641db1c116944be883cb532`  
		Last Modified: Thu, 21 Nov 2024 19:04:25 GMT  
		Size: 10.9 MB (10867147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ff594922b8bf3f94e8d21ba6e40bea0107780922cc53996ff7558271c7cde4`  
		Last Modified: Thu, 21 Nov 2024 19:04:25 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97a1b83fa4d40c5005aa7ce99e37fd1f7d89a96924057c75eaca56fe942ccf5`  
		Last Modified: Thu, 21 Nov 2024 19:04:25 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f5c85fedeba9e13b3645789b767b7ce6ee97113461c8c76fa3278ce013a9b6`  
		Last Modified: Thu, 21 Nov 2024 19:04:25 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24563122e8661b6ae1e446c0d3eee5b5aa44e15eb102430c806f33744f4bfa2`  
		Last Modified: Fri, 22 Nov 2024 02:18:59 GMT  
		Size: 1.6 MB (1553614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f3b34799f791cd53d7a66bb6bc1acf2a68e4136bee29bbefda116139c592f8`  
		Last Modified: Fri, 22 Nov 2024 02:18:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e515adeec4aacc53f6e62fac2d1bcf6f9762f0d4c00b61cd74998362b2bad2f0`  
		Last Modified: Fri, 22 Nov 2024 02:18:59 GMT  
		Size: 739.9 KB (739890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1a845e0e33a24efac7a623d4f44c5b898856b010a492681a3576bb2e1b0898`  
		Last Modified: Fri, 22 Nov 2024 02:18:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7e2d5d00acc735e218d7d7c4457e3b6faaf38c77edf4859cb23adf440f3762`  
		Last Modified: Fri, 22 Nov 2024 02:19:00 GMT  
		Size: 19.3 MB (19275274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-apache` - unknown; unknown

```console
$ docker pull drupal@sha256:c9277ce9420cd6a8a0f6bda66b6ca207e3042508267810108774c5e776bf10a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6748217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793de36edcec1aa5d20f4d87fe768cc0ded2daf3987136402ac45abebf596984`

```dockerfile
```

-	Layers:
	-	`sha256:767f3fac61d6f8241aef8d05ecc87885558754f64368834de4c4d1f4cf017261`  
		Last Modified: Fri, 22 Nov 2024 02:18:59 GMT  
		Size: 6.7 MB (6705328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fb8ae630369150d4a21edc6787d7b9396a6dd520c1dd53398e0ace5594c49b`  
		Last Modified: Fri, 22 Nov 2024 02:18:58 GMT  
		Size: 42.9 KB (42889 bytes)  
		MIME: application/vnd.in-toto+json
