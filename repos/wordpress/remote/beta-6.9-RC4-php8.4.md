## `wordpress:beta-6.9-RC4-php8.4`

```console
$ docker pull wordpress@sha256:a0dbedbc912533293eeec6f42d161865f04aa6688e1694ed3580f1b61caecd50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.9-RC4-php8.4` - linux; amd64

```console
$ docker pull wordpress@sha256:92a54ab9ca4e0f3b14f25db81ab3e228f40e8ac1a3f9cbe7c8ea8f74cca6acf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266515811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4771f93f5aaeaf2aaf06a10a46e192df35bc708ef4498a1c72fa4b7e3b06a17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:46:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:46:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:46:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:46:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:46:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:46:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:46:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 19:46:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 19:46:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 19:46:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 19:46:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:46:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:46:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:46:34 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:46:34 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:46:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:46:34 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:51:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 19:51:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:54:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:54:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:54:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:54:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:54:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:54:45 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 19:54:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:54:45 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:54:45 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:54:45 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:17:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:54 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:54 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:54 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:17:56 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:56 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3976b59fc129db59b350a28790101d8951906fdd602638cd6832aac311e5c005`  
		Last Modified: Thu, 20 Nov 2025 19:51:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d807b4271c853d11f8129df1b8b84cf53f3082f360225cffc97407f4029a6c`  
		Last Modified: Thu, 20 Nov 2025 19:51:42 GMT  
		Size: 117.8 MB (117838302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8c6c805bade34546e78f6f9be60506d7ff85e28e1a551f5328ff25dbfff668`  
		Last Modified: Thu, 20 Nov 2025 19:51:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01157410134386957681082f289681d2a156492291aca25f69ac960551bda66b`  
		Last Modified: Thu, 20 Nov 2025 19:51:27 GMT  
		Size: 4.2 MB (4224537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baeb349142aefe488fa83cab7514cc493b43c03d1d6697352ec67080023412e`  
		Last Modified: Thu, 20 Nov 2025 19:51:26 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a688ee4a13ca4da980bbaab403712056318966c9f08ad807d1dc4324d17ff106`  
		Last Modified: Thu, 20 Nov 2025 19:51:26 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0ed0015fa0e23737a76054963e53ea0442ee248418a5ee1519de2b9423624f`  
		Last Modified: Thu, 20 Nov 2025 19:55:05 GMT  
		Size: 13.8 MB (13818919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f0a77084c8393306aae6846fb4fb6442a145d368979740bed5e3f25067543b`  
		Last Modified: Thu, 20 Nov 2025 19:55:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa53f291d2e2bb89ac6af7a4d39eb453ff7c56541f9935b14275c2dfeb7ded34`  
		Last Modified: Thu, 20 Nov 2025 19:55:05 GMT  
		Size: 13.5 MB (13533236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f355030c564457fc9d01baff9aad5c41600e5c6ec31452d8991e49c40359952e`  
		Last Modified: Thu, 20 Nov 2025 19:55:04 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928538a80131988f2ec1869f738ab175096ad14e4b7f9088c5254db954657fa1`  
		Last Modified: Thu, 20 Nov 2025 19:55:03 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f635124f423c72829e86870912e72487029368ca6e6376688fc6c30b2c6b0d4`  
		Last Modified: Thu, 20 Nov 2025 19:55:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148ff68d4dc9ba40c44bb2e5990782ee540b427e5b860bcc4f2ccfa21cbfe83`  
		Last Modified: Thu, 20 Nov 2025 19:55:03 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76541f89258f8bdddfe57c4d754331cd55dcdb1f641a06771b093075c3c899`  
		Last Modified: Tue, 02 Dec 2025 01:18:31 GMT  
		Size: 26.3 MB (26297246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681a8aaf3e955434a5cd2f6087072f3e8021e3db5b7c1d80888dadacc379271e`  
		Last Modified: Tue, 02 Dec 2025 01:18:31 GMT  
		Size: 34.0 MB (33972800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a93bab7cb6739290a2b0a2a76a2f9bf4dc80313228d226df005115b8ac3550`  
		Last Modified: Tue, 02 Dec 2025 01:18:26 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48f7173f68b0867d6a31c6ecb31a9950b352f2f0756994e714299247124aa85`  
		Last Modified: Tue, 02 Dec 2025 01:18:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fea1fbef7a614d3ffca35f4d341ad3f4c9d79da2bc472e7e58096734da48d15`  
		Last Modified: Tue, 02 Dec 2025 01:18:26 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c8ded225c6b5fbb37ce706ebe29b27f18773513f8f5c8f73a4deab32e4c41`  
		Last Modified: Tue, 02 Dec 2025 01:18:30 GMT  
		Size: 27.0 MB (27024636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b664467b114953b60adc3a7f888bfa41d4c4cfdd80333f280a796f5334339f57`  
		Last Modified: Tue, 02 Dec 2025 01:18:26 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2ea9f140c4fa5d52c49f80482b320fb2f089d9251cf2d25648020156022e2c`  
		Last Modified: Tue, 02 Dec 2025 01:18:26 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfc852ff812e5dd8d93b70bddb25fd1e191296f713fb985cb141b86e5b4fcf6`  
		Last Modified: Tue, 02 Dec 2025 01:18:27 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:29a9d5f2881ebddac9c79eb7da30c6aa3c6984b97680fb0f8ca7742951d8c593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8737041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b312b8017ba3be0f11719a093034ad8e77393783285865e6cd4318555b82b21`

```dockerfile
```

-	Layers:
	-	`sha256:09efb8147fc1b5e813c748a9e3bb7536e675a0bd5627174d1c4b6fba105f1775`  
		Last Modified: Tue, 02 Dec 2025 02:27:44 GMT  
		Size: 8.7 MB (8671614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238c1ad48afcb34c2483bfe5257b8755c85df39f08ca2404a39789f434036ab2`  
		Last Modified: Tue, 02 Dec 2025 02:27:45 GMT  
		Size: 65.4 KB (65427 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.4` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:1b47054032ecd38dc958aebf2a18eced629aa581afb3109da99c1b1f6cd80bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235784994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74e76c487bca75102de94ca749909f4e9e2de55cff2222f0fc6a466faa3120`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:53:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:54:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:54:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:54:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:54:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:54:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 19:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 19:54:10 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 19:54:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 19:54:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:54:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:54:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:54:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:54:10 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:54:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:54:10 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:54:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 19:54:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:57:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:57:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:57:32 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:57:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:57:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:57:32 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 19:57:32 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:57:32 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:57:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:57:32 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:18:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:18:09 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:18:09 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:18:10 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:18:11 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:18:11 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:18:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:18:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:18:11 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:18:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:18:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99edc103b321d05b3298598a9f40955765008f0d9acb10a070b4d6012d3a8c25`  
		Last Modified: Thu, 20 Nov 2025 19:59:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c8b58f8e0602feac83ef784ce0a4362fc037c0d55e5169f03bb7bf3af81c42`  
		Last Modified: Thu, 20 Nov 2025 19:59:24 GMT  
		Size: 94.9 MB (94874335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd0dd3de58bf8a9a2ce347561e608f4c657d003f54597282e05a6acb303ce5`  
		Last Modified: Thu, 20 Nov 2025 19:59:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3f8685be41f75b7df7345096d3aaa0cf117889ab86bb7b14af91680a4e49d7`  
		Last Modified: Thu, 20 Nov 2025 19:59:27 GMT  
		Size: 4.1 MB (4082065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62ef50f8c790af8bbad3e5e347a65ee5235b953eec76599bed57f652f93ba8d`  
		Last Modified: Thu, 20 Nov 2025 19:59:30 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c2ae0c6738c3fc956515075f5b8ef5ebcc85d65c412bbaa7d8d6a1e39121f`  
		Last Modified: Thu, 20 Nov 2025 19:59:35 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4a8caf2b6034f9cddccf97bf36be76e6cc136d94e28182b3a5591dd629bf55`  
		Last Modified: Thu, 20 Nov 2025 19:59:42 GMT  
		Size: 13.8 MB (13816397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae6129de1dd9943276ed868eb816527559bb2117850780b4d3ddb2e4d618841`  
		Last Modified: Thu, 20 Nov 2025 19:59:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e48717dd878b9465c10676bee2de44ff8a4162167b0c1d241e915679963288`  
		Last Modified: Thu, 20 Nov 2025 19:59:52 GMT  
		Size: 12.2 MB (12192227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15260f7d4bcb6ec296cb91c1d813c3922e8bb0200757cf0e7f26a812e64de2be`  
		Last Modified: Thu, 20 Nov 2025 19:59:55 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243459ef8def49932f1a34c3409718607ce09ede00fef910db2ebacb683ee656`  
		Last Modified: Thu, 20 Nov 2025 19:58:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712386e36178e9ba50c47044c7dc158112cde2cb1ce89a9cdc22c535a7bf9c7c`  
		Last Modified: Thu, 20 Nov 2025 19:58:01 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403dd00fec42ea7a18ab93a8ff761b50d2ed5521ab8c669a32223480f881d582`  
		Last Modified: Thu, 20 Nov 2025 19:58:01 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95731cd53502b3f52d2082aa13e6f023032b0642aaf89e934a205f5d77d859de`  
		Last Modified: Tue, 02 Dec 2025 01:18:43 GMT  
		Size: 25.7 MB (25728494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda3a804e50b6058bcb2f19b0ef52ce831cc6cd24f727c44beba500f5b4fbcd9`  
		Last Modified: Tue, 02 Dec 2025 01:18:41 GMT  
		Size: 30.1 MB (30093043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab28f9ac28169b55a38d1481663adb319d8f33854aca2970625dc8c48beb1ca`  
		Last Modified: Tue, 02 Dec 2025 01:18:37 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1756a446926d50a1cac574b1b16bd59667b8a8c814f8d0dcb46756d97a7c7bae`  
		Last Modified: Tue, 02 Dec 2025 01:18:38 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86283e6ddcab2875933fcbf6a1cb51d52bc757d055317b6b8fdbcaabe51fcc90`  
		Last Modified: Tue, 02 Dec 2025 01:18:38 GMT  
		Size: 18.8 KB (18808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83e961292c5665d5425a81dd8537695ed33ba70e3488207eb02949dc1779ccb`  
		Last Modified: Tue, 02 Dec 2025 01:18:40 GMT  
		Size: 27.0 MB (27024643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455fe4ba4808c9e37f88d4b9297eba5a3a9afbfb1efde2136d56c3b779adb6e2`  
		Last Modified: Tue, 02 Dec 2025 01:18:38 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11e8c570f3f1cea9afdc78d77c4eab8c8fd5f6be4ce610dc00d87b4c1698b04`  
		Last Modified: Tue, 02 Dec 2025 01:18:38 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f590bbed50b4ee497aee2dcd50a6f22bbd9ac8da8c835e0e926e46f7a94dd2b`  
		Last Modified: Tue, 02 Dec 2025 01:18:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:ff385a1bcd96acec1eec34eaa27ebf7fb88a418c700bfc0ffc0ca04b044aaefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8536254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bd77104f7ed40355e2b12d1a5bf2dc36c5a53d879adbba7bd6a84b0e78c3d9`

```dockerfile
```

-	Layers:
	-	`sha256:566a5b0100b5f20368e41053c5472be20e08f8ea32e1693093eb1b32f0e91aba`  
		Last Modified: Tue, 02 Dec 2025 02:27:53 GMT  
		Size: 8.5 MB (8470647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929531a6461c941b3b180efed000baa29caef572c9dd88284d047e1c0648b049`  
		Last Modified: Tue, 02 Dec 2025 02:27:53 GMT  
		Size: 65.6 KB (65607 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.4` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:b245fc1253ac242d6006163e55f87f8f44e9b99d42b73ec5e9a2add05414d55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221992687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adf60583dd31222d1ba4d0589a387c41429fccd8ec0054ed7e2883adafa98ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 20:06:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 20:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 20:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 20:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:06:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:06:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 20:06:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 20:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 20:07:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 20:07:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 20:07:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:07:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:07:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:07:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 20:07:01 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 20:07:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 20:07:01 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 20:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 20:07:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:09:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:09:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:09:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:09:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:09:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:09:58 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 20:09:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:09:58 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:09:58 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 20:09:58 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:20:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:22:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:22:10 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:22:10 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:22:10 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:22:12 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:22:12 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:22:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:22:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:22:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:22:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:22:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5e576ab306be26b46b78c13d1025d73ae4ad25367444a492464c3796c18faf`  
		Last Modified: Thu, 20 Nov 2025 20:19:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50460e7ebcf6c0966edcec39a86c805451c58b9f9fd7e159de66a94bb8320611`  
		Last Modified: Thu, 20 Nov 2025 20:19:40 GMT  
		Size: 86.2 MB (86246282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3449c2193a753b12966c23c9d12c12e5bc8ecf74969c886cb7a725490bfa32d`  
		Last Modified: Thu, 20 Nov 2025 20:19:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c403d163148670f4748a807a5d4a77a46b5a1323cc061c063984f1d6253af09`  
		Last Modified: Thu, 20 Nov 2025 20:19:37 GMT  
		Size: 3.8 MB (3752353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f5b913321f60fc85e691ab4ae96942e6418375f60a03ea043dbe8f85658abf`  
		Last Modified: Thu, 20 Nov 2025 20:19:31 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62d1091b79ace92dfc159216bd005d48c92fd00ee893484a86f96dd1fb8244b`  
		Last Modified: Thu, 20 Nov 2025 20:19:45 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b690b3715bf7105cc0d5e5dd17935e1ff829d958f116763e338b520e64c7bd`  
		Last Modified: Thu, 20 Nov 2025 20:19:45 GMT  
		Size: 13.8 MB (13816532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3300c799098cac0db640dcbfcc8cf0b930798a4f41c3f670d4a23763e78c9a2d`  
		Last Modified: Thu, 20 Nov 2025 20:19:46 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66ac97d2627ddf35622d0ab70fa5ba8f01d258edf08e0eaa4cf927695d7cd48`  
		Last Modified: Thu, 20 Nov 2025 20:19:41 GMT  
		Size: 11.6 MB (11609189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a229ae499c2cb97975c56064f80a3f8253fefdb7f32d88365e561fa256a4e5f3`  
		Last Modified: Thu, 20 Nov 2025 20:19:44 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05053ff75be2aa44b1749567a66bf057edae9fe582d52bee04bb94800aa4253d`  
		Last Modified: Thu, 20 Nov 2025 20:19:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b624122fb89cdf42482f5fb3673ab7642fee14ff405edbb73a58c85998c1f1`  
		Last Modified: Thu, 20 Nov 2025 20:19:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fffd20f3da35383abda7cd1bdaa4474b9a5099cde5997afd67d7028360ecae0`  
		Last Modified: Thu, 20 Nov 2025 20:19:38 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548ad48ccfea6f9b4523624ee3ba02d931c90fa4235cb7324f9457ca6e5b106a`  
		Last Modified: Tue, 02 Dec 2025 01:22:56 GMT  
		Size: 25.1 MB (25077629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d71f1f43c39fd03ee44a5ca06500ff9b9e5ddc606dec569da702f290989276e`  
		Last Modified: Tue, 02 Dec 2025 01:23:03 GMT  
		Size: 28.2 MB (28226476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873097a63683302895a0225b8f934560ff1665d801945d3d2ce276e7dee10fc2`  
		Last Modified: Tue, 02 Dec 2025 01:22:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31625bc4ad2babc05acb462fb05652cd2f28ea6580e85cd51738cc2c5ed56d28`  
		Last Modified: Tue, 02 Dec 2025 02:11:00 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7664c222688baba6079b26f6d86fe3e82bcf0bc7b955a66c5bc596e19eb59b6a`  
		Last Modified: Tue, 02 Dec 2025 02:11:00 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b3347e28b99f017758513a071557350cea8e82591592262ef8784a9b35f3bc`  
		Last Modified: Tue, 02 Dec 2025 01:22:30 GMT  
		Size: 27.0 MB (27024623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8e18af3f764dd79ecd61b0bf74e3ecaf459df33518705847ec987b886e27c2`  
		Last Modified: Tue, 02 Dec 2025 02:11:00 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debed717c7ebd486fd37f5d651c67a71574a44a39df584d7db956f67166f4f69`  
		Last Modified: Tue, 02 Dec 2025 02:11:10 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6caf3496e7771f2e8f7885637601eaee0a4dc55049afb47c50fed91fcdb1e6`  
		Last Modified: Tue, 02 Dec 2025 02:11:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:2ffd9ef9aa2983f90af8433e485518fcc25593255d5507d14f1db43bbe3ca943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8541081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1702e34e4827406827b789232bf43fcc7fc2a9e4188675a60b9aff0feb84f05`

```dockerfile
```

-	Layers:
	-	`sha256:a756edbf4720722a698b9a787d50091343d1e1fc6ff0bd96c35258688c3732ae`  
		Last Modified: Tue, 02 Dec 2025 02:28:02 GMT  
		Size: 8.5 MB (8475475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc2444a31b1bf3897c8535b63ac3d09fa7f05a827a9e489e3e94bb55a31df80c`  
		Last Modified: Tue, 02 Dec 2025 02:28:03 GMT  
		Size: 65.6 KB (65606 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.4` - linux; 386

```console
$ docker pull wordpress@sha256:b77f1da86a6c5e63f7cd41370ce119bbd01b8da3fe4569fa9042a2cdb0e3881a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265200707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ee865d7ff291e660c8f1e1bfbb99033ec4eef711fec8c202ba815221c2cbea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 19:46:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 20 Nov 2025 19:46:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Nov 2025 19:46:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 19:46:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:47:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:47:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 20 Nov 2025 19:47:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 20 Nov 2025 19:55:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 20 Nov 2025 19:55:55 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 20 Nov 2025 19:55:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 20 Nov 2025 19:55:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:55:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:55:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:55:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:55:55 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:55:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:55:55 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:56:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Nov 2025 19:56:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:59:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:59:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:59:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:59:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:59:07 GMT
STOPSIGNAL SIGWINCH
# Thu, 20 Nov 2025 19:59:07 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:59:07 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:59:07 GMT
EXPOSE map[80/tcp:{}]
# Thu, 20 Nov 2025 19:59:07 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:12:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:13:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:13:48 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:13:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:13:48 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:50 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:13:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff292d92bef83ffec9666e45f901f0d30bf38f82f60acab0ecb997e8f209816`  
		Last Modified: Thu, 20 Nov 2025 19:50:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18aa8726c9a92d3215ab9fa4618414426a4228b554cc4285bff1af82d490ab`  
		Last Modified: Thu, 20 Nov 2025 19:51:20 GMT  
		Size: 116.1 MB (116138506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1282098e4386452a38622edb95ad30bd5a0650ae0e7f35fd713393a703e20389`  
		Last Modified: Thu, 20 Nov 2025 19:51:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd8c81e8133d51511c512a3cda291eb9ae14748ae9774824ea64ad00ee2cd3`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 4.5 MB (4455943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2b0a34a60b16233175e2b652d704f4a74d74878f1278a4b64cc7f4c12bd97`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11df4a7067e926a81ac8c5deda145627d9bee9d040bfc8805bd36569b0f87fe9`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c9c3fc30618e1f78ff1297647bbd68a129da70a452b900c8ca5272a19ad72d`  
		Last Modified: Thu, 20 Nov 2025 19:59:27 GMT  
		Size: 13.8 MB (13817964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85e3900f492df89c074d395b5be188e341e1026d06d7e7a3245365b40e196b3`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b28288bc501c5120a5bf144eed0e8a9c124c602845d8620a473328823fec7e`  
		Last Modified: Thu, 20 Nov 2025 19:59:27 GMT  
		Size: 13.8 MB (13829422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4168ba293312cb3e070ce939ff820ef9c5d929e5bf103bd44422ee1513dd8d`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9044dfcbe2b198b93ed97680e9c47953a8877f6bf9a68ab4d2e4b6829f8a4b8e`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693d8c8bc661df7ce5c993dd89dd1e114cf14f7f65b0f6ce1f1972164fdc0d0c`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce3836f34efaafcea4c6faae55a2d3ae474f6edfb17607d19cbcd38f6ad46ce`  
		Last Modified: Thu, 20 Nov 2025 19:59:26 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f7734225517610c874edb27864f78de17a92174d0f30ebc4c3990a95b9bda9`  
		Last Modified: Tue, 02 Dec 2025 01:14:39 GMT  
		Size: 26.7 MB (26747450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b52c4cdeb107dd3c4d255a428ae84e628a8ff78b2d671f836d5d8d7c7b4bed`  
		Last Modified: Tue, 02 Dec 2025 01:14:35 GMT  
		Size: 31.9 MB (31864073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38ee5512c051c2722735c92a648de2865859ac67ff662ffdbc83723cebc9e2c`  
		Last Modified: Tue, 02 Dec 2025 01:14:32 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7010a333de8c574a88b2f9764b5374fa588a11fb5afdfe787733cb8d1f4b1adc`  
		Last Modified: Tue, 02 Dec 2025 01:14:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275bb3aa178a9aa98e720de26f28c735f2fd419cf03488b1b436513e2f8e849e`  
		Last Modified: Tue, 02 Dec 2025 01:14:33 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8258f4931beadab3d14a923780d27d7b6657057a3c92dedf5fe1c516ac4046`  
		Last Modified: Tue, 02 Dec 2025 01:14:36 GMT  
		Size: 27.0 MB (27024624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e4a8e5351758ae8a56a35d7443be555db3ee1739e38035b95eb40d8d3b25e9`  
		Last Modified: Tue, 02 Dec 2025 01:14:33 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b839094ae49152a12a0a71608a10fd2121d670728d52b79f8332a9babd4c87f0`  
		Last Modified: Tue, 02 Dec 2025 01:14:33 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e5d092bc2f4d9d9b34abcea6714b7499f543fe6faafb070ead9eb71fd53f44`  
		Last Modified: Tue, 02 Dec 2025 01:14:33 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:411c6fea10be33eae35e322008c22a0ceb47eacaf4da88e6cac935ee9b32d7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8709989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58bcdb0ec52556a36a121c3e800296e23ae023b9e40a24393b69fb0a1604106`

```dockerfile
```

-	Layers:
	-	`sha256:96591d227940a0575b50505d1d722fa9f99bce8c39bb9bbeffe02251479a58fc`  
		Last Modified: Tue, 02 Dec 2025 02:28:15 GMT  
		Size: 8.6 MB (8644626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:935918b1ec361daae48d2e406ac6ac238dc4ec1ff72ba8dd75aa9002f046a1cc`  
		Last Modified: Tue, 02 Dec 2025 02:28:16 GMT  
		Size: 65.4 KB (65363 bytes)  
		MIME: application/vnd.in-toto+json
