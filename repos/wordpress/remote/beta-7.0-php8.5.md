## `wordpress:beta-7.0-php8.5`

```console
$ docker pull wordpress@sha256:4c9c50c7fe6e19edd76f51ea007b813559485c29cf31c7a215b7daf02cb8f361
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-7.0-php8.5` - linux; amd64

```console
$ docker pull wordpress@sha256:9c98e1401b6b6f88557217fdca6156336f83741ac77e672b563c43779adc0b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274182962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef369f69068d63f03579413406048713c213c07684a1afa895ba41e49bd1b74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:23:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:23:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:23:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:23:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:23:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:23:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:23:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:23:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:23:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:23:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:23:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:23:11 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:23:11 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:23:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:23:11 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:23:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:23:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:26:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:26:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:26:15 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:26:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:26:16 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:26:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:26:16 GMT
CMD ["apache2-foreground"]
# Thu, 14 May 2026 23:57:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:59:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:59:55 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:59:56 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:59:56 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 14 May 2026 23:59:57 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:59:58 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:59:58 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:59:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:59:58 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:59:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:59:58 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8417ea41e2c648f8c0706055fb594fffaf82b4ec7e81ea0f0ad75f4d3585f73d`  
		Last Modified: Fri, 08 May 2026 19:26:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252c0922e76bc7fe21fe1e4dd239aa6c57a1944e52fcc13ad6fd0a3ad3bf9955`  
		Last Modified: Fri, 08 May 2026 19:26:41 GMT  
		Size: 117.8 MB (117842422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abe97da0fe2a51136fc1763020b9954aae73d9a617577030a8f9ad81ed0e1a7`  
		Last Modified: Fri, 08 May 2026 19:26:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a07520e71327730b0fa453870e256ba71a5daf976df0786186b94bb94e3bd2`  
		Last Modified: Fri, 08 May 2026 19:26:38 GMT  
		Size: 4.2 MB (4228020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7de5184944781d4f8f3852b27a078c3db01b984234512ddd56bf8db84de47b2`  
		Last Modified: Fri, 08 May 2026 19:26:39 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb2139ce2b309b796e42b1c9a14606e434655dc16faa2568e090b6438d177d`  
		Last Modified: Fri, 08 May 2026 19:26:39 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a2e5b78463547594302050618d05428d5f8b717c66f97b181bbc56ec998d06`  
		Last Modified: Fri, 08 May 2026 19:26:40 GMT  
		Size: 14.6 MB (14559256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc162fef2efeb2831f298fe19561466fa042cb7804195bc738182796ad7d01b0`  
		Last Modified: Fri, 08 May 2026 19:26:41 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef594939b3e1bc658b7531ecda26cbde8f48861d074743899fbd2fc5b15e199`  
		Last Modified: Fri, 08 May 2026 19:26:41 GMT  
		Size: 15.2 MB (15158598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f66b28fc43d70afdf05a606d9a1dce3a2cc76b2f436e16f9a9f40a89014fd4a`  
		Last Modified: Fri, 08 May 2026 19:26:42 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e1ba1cf36a9ac3380bc861f039961a217f62bca4146923c4697f2d5b16c50c`  
		Last Modified: Fri, 08 May 2026 19:26:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db132eea48f8ccefce0ce4defd552a9233d5a0966056af2d8defc9c66cb6460`  
		Last Modified: Fri, 08 May 2026 19:26:43 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a4438c783b9689b1faa13f071a3fd9ec5f87c460f5897da86c4323925c2635`  
		Last Modified: Fri, 15 May 2026 00:00:25 GMT  
		Size: 33.0 MB (32956677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2be516b2e94c97082c34960e36a9b4bf65bfb68901d859d310a11d53651b86`  
		Last Modified: Fri, 15 May 2026 00:00:20 GMT  
		Size: 30.0 MB (29980355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab2b82c31939d83719816b7c10036215a6aad2362b087d58608cd3a9f5c92b`  
		Last Modified: Fri, 15 May 2026 00:00:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bee6530324f35c17c44fa44b783a64c2b540cf1715c1f57d333c447cfb1d97`  
		Last Modified: Fri, 15 May 2026 00:00:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a021622f9e406f2d53cc8d330bb0f0b9efc2f8b9ec88775afa320d4debb8d05a`  
		Last Modified: Fri, 15 May 2026 00:00:24 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc810c8f23f2d32a30f1906aa7cd4213b64bfac2195722ce7efe2f5a1366796`  
		Last Modified: Fri, 15 May 2026 00:00:25 GMT  
		Size: 29.6 MB (29648007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5564066f9a004e966b632c0b1b548f5cb4ec1ecb8a0a1b58aa3f2d0242d9a294`  
		Last Modified: Fri, 15 May 2026 00:00:24 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11acbda30396789d18d5588ecfc25d63f69b0262d318d086b6255890d2e2c982`  
		Last Modified: Fri, 15 May 2026 00:00:28 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d279909a4359abfe10a85ac1168960b02c35ce6f89d4a771ac6f52800d9b54`  
		Last Modified: Fri, 15 May 2026 00:00:26 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:6b4dc25d171c2e1978d079636683a99d1757285c58beb9dc3702301c0209b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8756773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca7185b2db228b0a025502624fe49fea4bc55a6addb5ff5abc1e1c1d2692687`

```dockerfile
```

-	Layers:
	-	`sha256:2c81e765dc55b813d398ff12cdbcaf5cd2d874fa693be7b7ae7c5c6da176685a`  
		Last Modified: Fri, 15 May 2026 00:00:17 GMT  
		Size: 8.7 MB (8692465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec387c7346224f5b94b262456fc00a574fb8876ebde67b3694a91b304f56bcb6`  
		Last Modified: Fri, 15 May 2026 00:00:19 GMT  
		Size: 64.3 KB (64308 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:a5b35040b1e374823d73f906118ec499e42eff8932ee406f2a6f018e3373d560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241881383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e9b6996c9f5166ea513884b3dc00753c079587919e1ef50e83f869846731ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:26:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:27:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:27:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:27:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:27:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:27:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 20:27:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 20:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 20:27:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 20:27:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 20:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 20:27:22 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 20:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 20:27:22 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 20:27:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 20:27:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:31:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:31:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:31:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:31:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:31:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 20:31:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:31:00 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:31:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:31:00 GMT
CMD ["apache2-foreground"]
# Thu, 14 May 2026 23:57:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 00:00:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 15 May 2026 00:00:01 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 15 May 2026 00:00:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 15 May 2026 00:00:01 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 15 May 2026 00:00:03 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 15 May 2026 00:00:03 GMT
VOLUME [/var/www/html]
# Fri, 15 May 2026 00:00:03 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 15 May 2026 00:00:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 00:00:03 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 15 May 2026 00:00:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 00:00:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2542369c28f4e51b174f2d95b25b25bb40506b39cc0096cb1dc030a6eb13bad`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebd24e297a0f4ad252934725da4fca2c93134ebd3c31955f3b894b82b0fd26a`  
		Last Modified: Fri, 08 May 2026 20:31:22 GMT  
		Size: 94.9 MB (94885405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b024ad8045732567913994e0bf4e4f270d45bc248a1ff1b0780f2d4f10c0c7b4`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f834a40f5d5fbb36b134d0c7b505a89774ced26b5663544cef918cb68f9316d2`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 4.1 MB (4090165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a00a5c2831ceefe48a7502a6f93f9e1ff67f9b7acf7b21e3a1f3fcabd25878`  
		Last Modified: Fri, 08 May 2026 20:31:20 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6da82bcd84ca804bda62f9e2d330b760d4cd8b15c9ccafbf173728e9402503`  
		Last Modified: Fri, 08 May 2026 20:31:21 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c8802583e54cf0e1a9398be6a2fe5510bbc500727afea51ba929467d7396aa`  
		Last Modified: Fri, 08 May 2026 20:31:22 GMT  
		Size: 14.6 MB (14556916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dd9f7ab943868aae660152a04082487a2fe7a39ca5321b2c6483732eb5bdc1`  
		Last Modified: Fri, 08 May 2026 20:31:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b8a0b761e91d0dda376a47978fb947225ecb17d66598426fe2fc4c409d3bd1`  
		Last Modified: Fri, 08 May 2026 20:31:23 GMT  
		Size: 13.2 MB (13235894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb2f47308487e998bdbdc2fb5f12a805f74d5ded33c0dc6a537bb936306bb24`  
		Last Modified: Fri, 08 May 2026 20:31:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74c8337c8b2757d583b8b24ae61ac7c3ea8f9503fa04e9773c2540cf3631682`  
		Last Modified: Fri, 08 May 2026 20:31:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747148f5aff5a94286802dc96e9a5ee7bdc93e2cb02b9483468162b641d7cc20`  
		Last Modified: Fri, 08 May 2026 20:31:25 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6713fe10f93bb5a097c94493f51d0aeb5c2f0faacd1a3a4f66512d5264fc9712`  
		Last Modified: Fri, 15 May 2026 00:00:22 GMT  
		Size: 30.1 MB (30142587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5646631b10fb936fbbd6aabe554e86f779ab0cc273e68239a13c48303f1068b`  
		Last Modified: Fri, 15 May 2026 00:00:23 GMT  
		Size: 27.3 MB (27344789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8273a191be96c3994b3ff3cbe81717a68ed31c91799221b3cdacf2f4d2f66dc`  
		Last Modified: Fri, 15 May 2026 00:00:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf55177d134d5e3da73cacf4b5d9768da952c808af9dbca03dd5ffd3785f52e`  
		Last Modified: Fri, 15 May 2026 00:00:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88f8d1ad3013637324365e26afd527e8034684b888782c1b703cc85509cb062`  
		Last Modified: Fri, 15 May 2026 00:00:25 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d0f242413abcd2dba6dbb927f4f566e407309680d198a1292263967c7a9a33`  
		Last Modified: Fri, 15 May 2026 00:00:25 GMT  
		Size: 29.6 MB (29648013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0dabd97dbf9380a0d38431ee7d9c2061818cdcdff7ac78cc28fce1c3354b90`  
		Last Modified: Fri, 15 May 2026 00:00:26 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24de713a7ea4cc8455e70d8027541d6d07a5581b2a69bf5a9389e912d26725d4`  
		Last Modified: Fri, 15 May 2026 00:00:26 GMT  
		Size: 1.8 KB (1774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4967bac0bde6b20f327201bd5aa1a260e19f1e0f6f5f008e125e6b058065591`  
		Last Modified: Fri, 15 May 2026 00:00:27 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:facbb6126c077807d51498c860c69be752badb85cba6119f5dc277affa3cb65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8550514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd64a74c886cd110471137e3f7bee294a7296252bb4107f7a99a083a2ac4024`

```dockerfile
```

-	Layers:
	-	`sha256:5e38608189071083607791226b5a59bb1c7bc1995b29b56402110840d94be555`  
		Last Modified: Fri, 15 May 2026 00:00:20 GMT  
		Size: 8.5 MB (8486026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840bef433b06dba7947ca3100af2f991d73864e215649dd61934df154d07f0f9`  
		Last Modified: Fri, 15 May 2026 00:00:21 GMT  
		Size: 64.5 KB (64488 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:f5cb1a3ec4920d4d1d3d498f03f487466c2b7b7b533ccbc1e6a0457814f96893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227887258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dd3112dce895ab208ac5a1d77a7792be2800aa06b022407eb9f37dac676f6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:16:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:16:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:16:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:16:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:16:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:16:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:16:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:16:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:16:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:16:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:16:48 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:16:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:16:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:19:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:19:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:19:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:19:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:19:54 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:19:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:19:54 GMT
CMD ["apache2-foreground"]
# Thu, 14 May 2026 23:58:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 00:00:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 15 May 2026 00:00:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 15 May 2026 00:00:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 15 May 2026 00:00:19 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 15 May 2026 00:00:21 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 15 May 2026 00:00:21 GMT
VOLUME [/var/www/html]
# Fri, 15 May 2026 00:00:21 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 15 May 2026 00:00:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 00:00:21 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 15 May 2026 00:00:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 00:00:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26f7004e87c4de58dc3edd5e2df9724991ee3e9915a880d58d3583cf4d5bf0`  
		Last Modified: Fri, 08 May 2026 19:20:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6393f0d48cd3aa2289517409694b46277da19241c5ceba80096538096ce6f10`  
		Last Modified: Fri, 08 May 2026 19:20:13 GMT  
		Size: 86.3 MB (86250382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0211bdd2a17cc65649476067f7e1008c707a83b1882863d0647ecc5e5f1c94ab`  
		Last Modified: Fri, 08 May 2026 19:20:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d9507ddb21ff84107c00222304cd79e0ef4c6770844aa8c324194eb02a51f7`  
		Last Modified: Fri, 08 May 2026 19:20:11 GMT  
		Size: 3.8 MB (3756682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4929a3d6f065048ce8114679154a8c1c1f68513b0b4651e66859f987a0ed1af6`  
		Last Modified: Fri, 08 May 2026 19:20:12 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840bd62807310f94d12b359008c3f4dcda31455d8822566333ce250370911957`  
		Last Modified: Fri, 08 May 2026 19:20:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8b0de1fd05903682d086fb5ca87f7f9d27ffe21af6225e8c77a821c6ef0b46`  
		Last Modified: Fri, 08 May 2026 19:20:13 GMT  
		Size: 14.6 MB (14557043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fbd1ebb38f910d23fc38392869d0e6caf94f56aa5552a1021426370ffd0c73`  
		Last Modified: Fri, 08 May 2026 19:20:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f949a73850d8bb0d1a2c96891eefd9f16f06c895de0add9bc387df9f0933deed`  
		Last Modified: Fri, 08 May 2026 19:20:14 GMT  
		Size: 12.6 MB (12616027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2375e40771eff2d7a9762c9836933effb47e9c5f790751bd9654a41e13639ef5`  
		Last Modified: Fri, 08 May 2026 19:20:14 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b8a744d1e153768f348bcb21f0c991395b66f8e2c185c764a5ec4906387284`  
		Last Modified: Fri, 08 May 2026 19:20:15 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ff52264cb8507bc717ac59a3a7ab92863247244b1f4441e5713050eeb39416`  
		Last Modified: Fri, 08 May 2026 19:20:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056c6aec9bf23040f863e6c4821baef1a3e16ebc22d5b9ec0d66b5a097e989b7`  
		Last Modified: Fri, 15 May 2026 00:00:42 GMT  
		Size: 29.0 MB (29041330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01780589d22636aa458389959998bef91ef6116e8b0d3858d03e0e01a77f749a`  
		Last Modified: Fri, 15 May 2026 00:00:42 GMT  
		Size: 25.8 MB (25773471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1371b9e629aaf3d0f6935c8cccec239e53e7542c65d32a641346a0e0b75db1b`  
		Last Modified: Fri, 15 May 2026 00:00:40 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1284e6c67c49ef0755969b6347c2e99608d913327d28d6ead22380d6821c946`  
		Last Modified: Fri, 15 May 2026 00:00:41 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2240b4f6dafa545c0a5ff946b8bdfb8cc284750f15b240401261ea7ca167d20`  
		Last Modified: Fri, 15 May 2026 00:00:42 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8366de768921b8b1375972c64c166bc0ca13b077970143b9c674eef97ac6ea48`  
		Last Modified: Fri, 15 May 2026 00:01:06 GMT  
		Size: 29.6 MB (29648016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc0b0525c0e0f44f5d046079adbdd063ff37b57c319313c5eb1fdc4546b00d1`  
		Last Modified: Fri, 15 May 2026 00:00:44 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8d6ab0f49764c1b7706e73dd67b60e84cd6a99448261b324fe953ba754373b`  
		Last Modified: Fri, 15 May 2026 00:00:44 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe9d7efc0b7b0f537e467173275369e3ba36cb9f42083999bd0926f447c5996`  
		Last Modified: Fri, 15 May 2026 00:00:45 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:d4dbf707f3ed370f2b6e0e46539cb9ede29f84cc97db98b37392f627eea38ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8555348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ec78998c3213bfb4cfcc7506fc7e2c2ceb452282d8619ce19a3207d6ca4d8a`

```dockerfile
```

-	Layers:
	-	`sha256:0c7c8398e6a4d451d7450ad31b5bf4ef831f1c6a52bc3fce9b548b90995ab55a`  
		Last Modified: Fri, 15 May 2026 00:00:41 GMT  
		Size: 8.5 MB (8490860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28c6ef5280e32d89d6656bad3671c81e51bb388f90fded92a05b49d8fab36d1`  
		Last Modified: Fri, 15 May 2026 00:00:43 GMT  
		Size: 64.5 KB (64488 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:a7f5c07496203b93075962b0c8bf58b937e7d7d2aa6eccea8c307f18324f45f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266350348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c19b6a8da529eb4b4fc2ee20daa2925cb73b63d72aa24133fd8275e3f4d369f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:22:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:22:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:22:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:22:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:22:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:22:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:22:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:22:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:22:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:22:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:22:17 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:22:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:22:17 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:22:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:22:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:25:48 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:25:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:48 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:25:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:25:48 GMT
CMD ["apache2-foreground"]
# Thu, 14 May 2026 23:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:56:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:56:02 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:56:02 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:56:03 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 14 May 2026 23:56:04 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:56:05 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:56:05 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:56:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:56:05 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:56:05 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839fbf070c8a8253ac6d1c8f6c9ea12bad1ecd40322affe8ea9a33e835917886`  
		Last Modified: Fri, 08 May 2026 19:26:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba04f9d377618a3731f55f7972bb9fbc8a4cb78391a46e88ededc6699af6a6d5`  
		Last Modified: Fri, 08 May 2026 19:26:12 GMT  
		Size: 110.2 MB (110165947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a56e8091661e47df4bb70ac904e0e28c26943dea545450dc023fe4cf6f935c`  
		Last Modified: Fri, 08 May 2026 19:26:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6957a5ca9a1d6108a85ef4e7c55ab6686e6dc409b3be4596fb27e5e1d56ce85e`  
		Last Modified: Fri, 08 May 2026 19:26:10 GMT  
		Size: 4.3 MB (4307802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26245f05b07982c7e84149579f69d47c1cbb06b3cd4d75d1f0e6b830f03c07a1`  
		Last Modified: Fri, 08 May 2026 19:26:10 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510440231ff68059aeff557712d950aec59d07dcc1dc89ec58a5af5e540f744a`  
		Last Modified: Fri, 08 May 2026 19:26:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3bdc6378ad36235558c8914d18e94e66a89040eefa967a9adeae79595ac95`  
		Last Modified: Fri, 08 May 2026 19:26:11 GMT  
		Size: 14.6 MB (14559097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ce2d325c660258ea061f01003c006695a597e693dbab79a07b0b0db93900b8`  
		Last Modified: Fri, 08 May 2026 19:26:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b92c4638a37fbaa4264e827363a8f834d4a1bc6b1839d2153041981def2c1f8`  
		Last Modified: Fri, 08 May 2026 19:26:12 GMT  
		Size: 14.7 MB (14727556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa03f078906c5fb3a4ae6c853dff19ff1b3fc5919e9911a20c296fbbc08cdac4`  
		Last Modified: Fri, 08 May 2026 19:26:13 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91e5beba54659ebb90429b41ea9ab685f312bf311aa34e86917bcd0e2a76b8`  
		Last Modified: Fri, 08 May 2026 19:26:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c393e8d120a6bac5369c4ade464607aa306abc21c939c0d46a6cdcf36bb527`  
		Last Modified: Fri, 08 May 2026 19:26:13 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482ee2d0d24bac0d41b20a4b646c7d031aa989194e082058b84ee6fed31d85fa`  
		Last Modified: Thu, 14 May 2026 23:56:23 GMT  
		Size: 34.5 MB (34468869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471df5998470b6c8970e9a6711e9859928f7f9302328c4073d16d47523085a7`  
		Last Modified: Thu, 14 May 2026 23:56:23 GMT  
		Size: 28.3 MB (28300004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19abd8a2b38fd7edd13815a7d04f0c6bca8bab1d037f9317a66285f11473a5b`  
		Last Modified: Thu, 14 May 2026 23:56:22 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5af4b622ca86dccd1890833705507d1fe3f1bc63327a64eec39dae48715353`  
		Last Modified: Thu, 14 May 2026 23:56:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9ddb8d191a01892885fb43184242d335a7d06eda44eab1bb7f570d7cd78303`  
		Last Modified: Thu, 14 May 2026 23:56:23 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f0a3519d2043f74136fca37773893ae28dd3c0ac7dc80bfebc7d8efb67aac`  
		Last Modified: Thu, 14 May 2026 23:56:24 GMT  
		Size: 29.6 MB (29648009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74255995181baf3d07d8261b66784be8cde0dc52b0569f2b910fe8f4a78d1b30`  
		Last Modified: Thu, 14 May 2026 23:56:24 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0252d354ec3db9c35a0454a0407ea5a299c54ab024c6b723cfaf39cc20b6c0`  
		Last Modified: Thu, 14 May 2026 23:56:24 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec5a3a2556ab091df2f101637363cc295287ab213f362ce9dd73434e0c3bbbd`  
		Last Modified: Thu, 14 May 2026 23:56:25 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:ff39f813076ce260827d41e9fda8e57fdc6414cbcd21768fe186317d3c4869c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8853535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeb3604202d3a05364f9bfe9f8fbc5a8d8221653786237e7d862c42be48c600`

```dockerfile
```

-	Layers:
	-	`sha256:71dc2bcf7c3cbbc0a6cbd4220a0f1d9fe4f28b19ce9a71e934a79933deb39aa1`  
		Last Modified: Thu, 14 May 2026 23:56:22 GMT  
		Size: 8.8 MB (8788985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92640630724d660d1626c465e712b14fc671af930a1a425a09c30798715c48e`  
		Last Modified: Thu, 14 May 2026 23:56:21 GMT  
		Size: 64.5 KB (64550 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; 386

```console
$ docker pull wordpress@sha256:991aa28245a0197079d1892887f28eabd4fcc9ee8c70167b02a0241e752ff940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272091873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411a7bed1e84aa28b28e7531c6ec669844404256ec01ce5e3e506da287fa6133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:17:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:17:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:17:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:17:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:17:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:17:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:18:02 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:18:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:18:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:18:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:18:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:18:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:18:02 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:18:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:18:02 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:18:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:18:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:21:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:21:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:21:46 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:21:46 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:21:46 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:21:46 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:21:46 GMT
CMD ["apache2-foreground"]
# Thu, 14 May 2026 23:56:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:58:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:58:01 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:58:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:58:01 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 14 May 2026 23:58:03 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:58:03 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:58:03 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:58:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:58:03 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:58:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:58:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5239d75dc5fa222e66fcee6b7d8a836e729c2e51ab518a21fbd76cee5d5edcd4`  
		Last Modified: Fri, 08 May 2026 19:22:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576c49032e42254b10dc96af319fa9e118eef73ca505814b51967e5feda6b9af`  
		Last Modified: Fri, 08 May 2026 19:22:11 GMT  
		Size: 116.1 MB (116144183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67735b713ac0ff9ea18e89ba69fab084a93729b4fffa8903bb8b86c95903d2`  
		Last Modified: Fri, 08 May 2026 19:22:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0caf85a94caeb4341498e1c236af6b7f240d5a13a8e8b88f8d3bcb8d9a1994`  
		Last Modified: Fri, 08 May 2026 19:22:08 GMT  
		Size: 4.5 MB (4459155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a34c8f33c27ec2224f287fa63240984f73a0836bbf79116ed29ad9ffb5a13`  
		Last Modified: Fri, 08 May 2026 19:22:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff20d59f22ab2da2688d9208370f3ba078e1ad04654609de265fb88bc63c90c`  
		Last Modified: Fri, 08 May 2026 19:22:09 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757aba349049486080def781a9f3c6bf33d96544a49e87515fdc5db91272a2d0`  
		Last Modified: Fri, 08 May 2026 19:22:10 GMT  
		Size: 14.6 MB (14558445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea4fb744e76c554cd936753a5287e04162c154938d4c1f8572b968451d7eae1`  
		Last Modified: Fri, 08 May 2026 19:22:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf80dac46faa8467f23f31315bfa58d85854b904aa22da6865cb4921e971a91`  
		Last Modified: Fri, 08 May 2026 19:22:11 GMT  
		Size: 15.5 MB (15508993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee6ea0ed94e28ff18e224855a47dcbfdc014a3e3bcacaa02f4e58d135ebcdac`  
		Last Modified: Fri, 08 May 2026 19:22:11 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4346dcaac36df989ed27fe367237fe9662bb4a626c9931db1962fb4007aeacc3`  
		Last Modified: Fri, 08 May 2026 19:22:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f5b14a6c8e81a483b3bc79eeb249cd752fee73c28b95020d2245d80763be2f`  
		Last Modified: Fri, 08 May 2026 19:22:12 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc5393cbb06603f973cbf222b356ee744671ec3b22927e73ebefe06875977ea`  
		Last Modified: Thu, 14 May 2026 23:58:20 GMT  
		Size: 32.4 MB (32404633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b4fa9e45c468a8c0e0e0f87d47563a827d1458bd9030e0ac4ce943cc3f705`  
		Last Modified: Thu, 14 May 2026 23:58:20 GMT  
		Size: 28.0 MB (28042656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d2aa6bca8747d138edc24b1a08e5b41e69438976e7af90d501714399e70378`  
		Last Modified: Thu, 14 May 2026 23:58:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab4039fc374103f39f5b579270cea3675135a6c17d1bdcd4a88b7eea8ddf668`  
		Last Modified: Thu, 14 May 2026 23:58:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa582cb94cc79164769f80ce455fb94b6d46e11e78509b59a197ca5643cf08b`  
		Last Modified: Thu, 14 May 2026 23:58:20 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23f179bb94c88cc4b73941c6c00666bdd3c7b89a60f8b8036114ed305bed6a6`  
		Last Modified: Thu, 14 May 2026 23:58:21 GMT  
		Size: 29.6 MB (29648007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf4153ff115f352c4a7e1674e588b02903f8c7466863a4cbd3bab82daa1e707`  
		Last Modified: Thu, 14 May 2026 23:58:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33592885dc57e6abfe0d9b799d2b9940602155ec7f0175407fcda0d330eaee08`  
		Last Modified: Thu, 14 May 2026 23:58:21 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfcba219825c5830f687bdd2e75007469515e2a1a366c393420b6dfdf05e99a`  
		Last Modified: Thu, 14 May 2026 23:58:21 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:2d484cab64024dc5ab4061d3e8928dc970caaa462834b6b3f40379b77100c010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8729713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc6c8c2e8cb3eee73af959f5ede49abd30c84437929cc04197420c51a036387`

```dockerfile
```

-	Layers:
	-	`sha256:de96d8982d96b78dcb75bde5f08f19bd171da7559b87758eae100db4ed8dbcf7`  
		Last Modified: Thu, 14 May 2026 23:58:19 GMT  
		Size: 8.7 MB (8665469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5211cb8524c0d993581566e9a484e4ce00e74d4864d97a0bc1eced527a0085`  
		Last Modified: Thu, 14 May 2026 23:58:18 GMT  
		Size: 64.2 KB (64244 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; ppc64le

```console
$ docker pull wordpress@sha256:3a5262f882c7542fbe2061b41fb6474391b5eaa8cccae8e994b07994c1d17590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269709760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee718f1a3027fa1c353634f300407ec170d414578e824d9d9ebab703c79a6929`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:49:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 20:50:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:50:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 20:50:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 20:50:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 20:50:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 20:52:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 20:52:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 20:52:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 20:52:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 20:52:17 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 20:52:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 20:52:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:56:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 20:56:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:56:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 20:56:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 20:56:48 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 20:56:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:56:48 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 20:56:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:56:48 GMT
CMD ["apache2-foreground"]
# Sat, 09 May 2026 03:12:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:16:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 09 May 2026 03:16:37 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 09 May 2026 03:16:38 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 09 May 2026 03:16:39 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 15 May 2026 00:05:28 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 15 May 2026 00:05:29 GMT
VOLUME [/var/www/html]
# Fri, 15 May 2026 00:05:29 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 15 May 2026 00:05:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 15 May 2026 00:05:29 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 15 May 2026 00:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2026 00:05:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec2632ee8119dd2f20ca1558eea30c9050dbe76cdeddfc47a82d2a99e3e922`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c7eeddeb286b4ad82e04422070cc9d0ea14c8385e61c160fdc6de15d44b838`  
		Last Modified: Fri, 08 May 2026 20:55:24 GMT  
		Size: 109.6 MB (109599289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9201651affe69dbeea0b40dd0a01797ab879ad276cbce7b1035fd2abbe6f32`  
		Last Modified: Fri, 08 May 2026 20:55:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e51c8a80d6a8bef8f0b2054c11688b31c933849cfa8969dad4e6902019fd92d`  
		Last Modified: Fri, 08 May 2026 20:57:14 GMT  
		Size: 4.9 MB (4883332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0f49e69dc9fe4788a52a9279ee2ccb8d494fe3d8ff41454f9fb3a16f8054d7`  
		Last Modified: Fri, 08 May 2026 20:57:13 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482f0abd8de4c23e09415b0ec42b86203a86547f87a68869616944382298375`  
		Last Modified: Fri, 08 May 2026 20:57:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8d52ddf887e4de3d2b4747e0e308899aacf14cf300e04af1a4f46f2ef85946`  
		Last Modified: Fri, 08 May 2026 20:57:14 GMT  
		Size: 14.6 MB (14558583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965d0797d0fde7684f37da295d79bce437a16d22d221e581472f099544d2b57`  
		Last Modified: Fri, 08 May 2026 20:57:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d05d0758148cd0cf0d75df63c97f0b879272014f3b4a57b15da910ef5367cbb`  
		Last Modified: Fri, 08 May 2026 20:57:15 GMT  
		Size: 15.2 MB (15153208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d54b0e8726764f3ccd88c5bb7d43e8d097952b80b238048aee8b7ee3faa7c05`  
		Last Modified: Fri, 08 May 2026 20:57:15 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957bb11b628901c9dfc5cc8d9fd83fd608e006aa159d0282274240fdec34bd14`  
		Last Modified: Fri, 08 May 2026 20:57:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bdd38206be1293c830cd6e68941b5ef74aab96b28563d93bfe049de216d70e`  
		Last Modified: Fri, 08 May 2026 20:57:15 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a684973d76ae7b15bdf82da3e9dc288aca0deee770ff4d922e46ae272d4ed0`  
		Last Modified: Sat, 09 May 2026 03:17:20 GMT  
		Size: 33.0 MB (32952150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f0bf3d102bfdae4e3303de82863ebe74d30654325551d725124c2b447038f7`  
		Last Modified: Sat, 09 May 2026 03:17:20 GMT  
		Size: 29.3 MB (29287671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef1bd6a067f4c0bf582920f0fe89df4df6d25a3ebcc38bbfab38ae2d9e6c63`  
		Last Modified: Sat, 09 May 2026 03:17:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5acb12c9ff12582d411e2e7f125cdcf71f029278a123214927a2fc7beedb74`  
		Last Modified: Sat, 09 May 2026 03:17:19 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d4d42a62eb07dc5673325b40d42f7911c240aa8acb6ace1608c5da787df6f9`  
		Last Modified: Sat, 09 May 2026 03:17:20 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7e61ec0073709c5c6b6807923659aba37be47a81f9f08afe73b7543f01bfa`  
		Last Modified: Fri, 15 May 2026 00:06:03 GMT  
		Size: 29.6 MB (29648023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef376737cbfa56cd468725151f1f2e3b571dba3954bdbca94a3994d9603f497a`  
		Last Modified: Fri, 15 May 2026 00:06:02 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba15389df9f8c3384ceed22a53ca9b58b0325f8e5446a1685d2c6c51fb59e033`  
		Last Modified: Fri, 15 May 2026 00:06:02 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c340d9df40f2b84fd6155826bf7a25fcff693f84c005f80b85c78a3355ad8617`  
		Last Modified: Fri, 15 May 2026 00:06:02 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:3dae8e15021995b222619f42b85e371a2d2bed3707715a339980dcfd36df0738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8757688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c314ba732eb77801503b9e4d17c1e5c4f4a62cae6df3ccfd799395f71e57e8`

```dockerfile
```

-	Layers:
	-	`sha256:cf69ffb955707117d29f3b13f952d186d9b9ce1746ea0085d5c2cc74e461c810`  
		Last Modified: Fri, 15 May 2026 00:06:02 GMT  
		Size: 8.7 MB (8693300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b742d35da5365fafb64d3bd00614f4a9c52b6bc7f1445b1097caaadb012c1f6`  
		Last Modified: Fri, 15 May 2026 00:06:01 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; riscv64

```console
$ docker pull wordpress@sha256:e218ce80e1fee7d00ca0eddcaea940d5006d9044b9b4a8065e5fd5180825f282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 MB (294282399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b131a25521f86f624ffd9a665d7b59f6d49873d7fc5719da34b0ab6a07d104a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 21:54:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 09 May 2026 21:56:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 09 May 2026 21:56:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 09 May 2026 23:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 09 May 2026 23:01:52 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 09 May 2026 23:01:53 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 09 May 2026 23:01:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_VERSION=8.5.6
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Sat, 09 May 2026 23:01:53 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Sat, 09 May 2026 23:02:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 09 May 2026 23:02:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 10 May 2026 00:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 10 May 2026 00:00:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 10 May 2026 00:00:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 10 May 2026 00:00:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 10 May 2026 00:00:11 GMT
STOPSIGNAL SIGWINCH
# Sun, 10 May 2026 00:00:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sun, 10 May 2026 00:00:11 GMT
WORKDIR /var/www/html
# Sun, 10 May 2026 00:00:11 GMT
EXPOSE map[80/tcp:{}]
# Sun, 10 May 2026 00:00:11 GMT
CMD ["apache2-foreground"]
# Mon, 11 May 2026 22:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 22:43:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 May 2026 22:43:42 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 11 May 2026 22:43:42 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 11 May 2026 22:43:44 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 May 2026 23:51:05 GMT
RUN set -eux; 	version='7.0-RC3'; 	sha1='ba6aad2a5d7e72d3e3bfe984780ff62983d38161'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 May 2026 23:51:06 GMT
VOLUME [/var/www/html]
# Mon, 11 May 2026 23:51:06 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 May 2026 23:51:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 23:51:06 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 11 May 2026 23:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 May 2026 23:51:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851920f3b2b9f32390e534dcffd1a0f98fdc6aa8d5199bfd378e81a327288ff`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0821c675bc014f36787754eae800bec2700775366123fdb7b93402865c4af1`  
		Last Modified: Sat, 09 May 2026 23:00:25 GMT  
		Size: 146.6 MB (146579482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b3119d655d94203c15aecf1cc2d93402f4523740a2527b967e186d7693c42`  
		Last Modified: Sat, 09 May 2026 22:59:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fef68a865e77649624e332fc135889fa3e311fd92fbd55efb9283eaf669560`  
		Last Modified: Sun, 10 May 2026 00:03:23 GMT  
		Size: 4.0 MB (4031575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b336a94a4c9567b8427e54f2733c24a8a5678559cf7b51711a20ec3f8d801d63`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110b6e8491a8e810371841937507898364acf2bcba097426fe8b034aea28f887`  
		Last Modified: Sun, 10 May 2026 00:03:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb2a6c6c00bad6bf70c7b384488768e8a60aafcf68c747c5cc8cb3ee2a03656`  
		Last Modified: Sun, 10 May 2026 00:03:26 GMT  
		Size: 14.6 MB (14558734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b6c7330076bf04bfd04c76b477f70b1a7471f7cc9186aea83c33ee117150f5`  
		Last Modified: Sun, 10 May 2026 00:03:23 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7498cae8d52088c42a2ea0679887d7d69b62183bef04c56d3ad8950269e8f87a`  
		Last Modified: Sun, 10 May 2026 00:03:26 GMT  
		Size: 14.1 MB (14081453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e804396fa5c253f5141f525cd077b5821add76af4482ab25ca6e3a52e31bfa`  
		Last Modified: Sun, 10 May 2026 00:03:25 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3b4bdd098920dc54b8c6012a432b5c4b148d01852f1406085059dc6a742797`  
		Last Modified: Sun, 10 May 2026 00:03:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e814fa66ed62ad8aa5225b39c6767650716990b4de97838ee4c504c577a067c`  
		Last Modified: Sun, 10 May 2026 00:03:26 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8badc00d193588d17e164e23692884065bfbcc52d9bf14e895689e5785609a47`  
		Last Modified: Mon, 11 May 2026 22:48:31 GMT  
		Size: 30.5 MB (30539309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38128995f144729b1b4e4daaa0a685daff93e698c44e4b4f98fa429176dc5846`  
		Last Modified: Mon, 11 May 2026 22:48:30 GMT  
		Size: 26.7 MB (26725834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3cad248b8275d8239b6218d7812f1cb34664834168d08bf008be0176840c4`  
		Last Modified: Mon, 11 May 2026 22:48:20 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d9172c3a98fc374acc639d377cc1552421f1bb821170cfe47062d37370effa`  
		Last Modified: Mon, 11 May 2026 22:48:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188d07424ea8109effec9492a495a65a5471386e180f692a937e69036b639fe7`  
		Last Modified: Mon, 11 May 2026 22:48:22 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed23edc5c112f79bf92c0d7b5a66298d1f1b9c80cf579ecfbea81ecb52edad6`  
		Last Modified: Mon, 11 May 2026 23:55:34 GMT  
		Size: 29.5 MB (29456323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5f5fe5b14c59069c075213769dd0e4fc4ffe9a03aa09495229aee5245dfdad`  
		Last Modified: Mon, 11 May 2026 23:55:29 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29687565290a0e9eebaa4ce766a51e5469a0bf0c0da6e37b21327b3b4cbbb189`  
		Last Modified: Mon, 11 May 2026 23:55:29 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc96d2c131981dea7c3d6c0d5000e72d17c7b6910c68e64b89733c0c611dad3e`  
		Last Modified: Mon, 11 May 2026 23:55:29 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:d2c5c8d67702cc29825c82484512c0c6673e4a6cca7229e397d777f944f6132f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdef587aa0e01ce90761b7bab89e183d3c34fc19fe6a3e09ce573e84c6cf0ab4`

```dockerfile
```

-	Layers:
	-	`sha256:49520bdd4cba0d56b93adee2d4eccaa87f8b5c08e2f3454fb4b270269506042e`  
		Last Modified: Mon, 11 May 2026 23:55:30 GMT  
		Size: 8.8 MB (8758203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36a3fca1bfb9adb2f2f2c6e0501bf50e0e668f961e1c33eb6bc1d96e6270a06`  
		Last Modified: Mon, 11 May 2026 23:55:28 GMT  
		Size: 64.4 KB (64388 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5` - linux; s390x

```console
$ docker pull wordpress@sha256:7f1b185ba5d87b419c7bf9de79bb60c218018464878880f6bf60169891a08d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244164604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007f93956a2b5cb358a5df520a9a94a52c808a6fb5146833b9de74702cf6a775`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 May 2026 19:20:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 May 2026 19:20:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 19:20:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 19:20:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 19:20:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 May 2026 19:20:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 May 2026 19:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 May 2026 19:22:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 May 2026 19:22:09 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 May 2026 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 19:22:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 19:22:09 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 19:22:09 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:22:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 May 2026 19:22:19 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:25:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:25:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:25:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 May 2026 19:25:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:25:54 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:25:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:25:54 GMT
CMD ["apache2-foreground"]
# Thu, 14 May 2026 23:54:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 23:56:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 14 May 2026 23:56:20 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 14 May 2026 23:56:20 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 14 May 2026 23:56:20 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 14 May 2026 23:56:21 GMT
RUN set -eux; 	version='7.0-RC4'; 	sha1='8bdbd1efa890b9ae2cd7b0f3c57c513a8139526d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 14 May 2026 23:56:22 GMT
VOLUME [/var/www/html]
# Thu, 14 May 2026 23:56:22 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 14 May 2026 23:56:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:56:22 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 14 May 2026 23:56:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:56:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30e2543e1ce26483b31ae0ac65719d9a5800e19da207c59f22603554a2b5f78`  
		Last Modified: Fri, 08 May 2026 19:23:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d2f428087efc8aa194b8a843faed3774a42d9ac843d1239581c5351a2bb2a2`  
		Last Modified: Fri, 08 May 2026 19:23:52 GMT  
		Size: 92.6 MB (92573061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3359c8aeeb1fbcf5e343e9841d059915fb9521599221a5914d1b3a47d375a7f2`  
		Last Modified: Fri, 08 May 2026 19:23:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77e80695f8e9db83e238538c37c3af75b475cd1fbf3614c86db4734dec733a2`  
		Last Modified: Fri, 08 May 2026 19:26:13 GMT  
		Size: 4.3 MB (4331263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d009eb6e21b03ad3d8232c01b14dc068704f8d6cdc985c19703dd5a9dd49b0`  
		Last Modified: Fri, 08 May 2026 19:26:13 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d40070ea56327d92d2b6b5e7f429fc4a8d18f636101f38ca6192db2b87b28`  
		Last Modified: Fri, 08 May 2026 19:26:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5169a3eaf058238abcd27f8548e2fdcfa9ff4f19f1f83295f3edd1d23f526f33`  
		Last Modified: Fri, 08 May 2026 19:26:14 GMT  
		Size: 14.6 MB (14557861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcc0b6e19048e5fceeb962b59871c4ecb20efe766a3c98e0f371973faffc4fd`  
		Last Modified: Fri, 08 May 2026 19:26:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b276b7f166f053d9546738d9b61f7863d48cc89bedd6a182e9d3bf48683f1`  
		Last Modified: Fri, 08 May 2026 19:26:14 GMT  
		Size: 14.4 MB (14438944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82cc3647d27f0ad15902202e6b4fc66009cdbe7b9cb2efc781c43de3cbd2e3`  
		Last Modified: Fri, 08 May 2026 19:26:14 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebd3b0dee27cc54253894b76e16275fb83e1b38f3b33ec2a283657bb80b4130`  
		Last Modified: Fri, 08 May 2026 19:26:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8bed782c34ee00cb7f877d5fbd290044f3bf92bfc0395d52ecef4e794ce8c1`  
		Last Modified: Fri, 08 May 2026 19:26:15 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52337d538c0928e189064c1fcdd776b83c2b8857d752b6bfc372a4fdd9bbdb46`  
		Last Modified: Thu, 14 May 2026 23:56:46 GMT  
		Size: 31.4 MB (31396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c6f79fc9ac516f558ff403e5e850e042c77e558d707dc152da2e9aad4aa4fb`  
		Last Modified: Thu, 14 May 2026 23:56:50 GMT  
		Size: 27.3 MB (27348782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a895ac89c5cb5ad235ad403ab0c04fac14a19b946abaacf7bd6f16db5fea9cc`  
		Last Modified: Thu, 14 May 2026 23:56:44 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd6aa4bd3c3bb6aeff67c8adb97fc8881547cabd02e4636f91b94e43df23ef`  
		Last Modified: Thu, 14 May 2026 23:56:44 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3044a5654cb639f5dbbf53c3710c1627a94bfe5ddae41a6218fe3f4e5ea8825a`  
		Last Modified: Thu, 14 May 2026 23:56:45 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26570a382a86a52d7e544a8781ef5b794ae5b2f1c41989a22eb38ceae5851d18`  
		Last Modified: Thu, 14 May 2026 23:56:46 GMT  
		Size: 29.6 MB (29648012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fc3b7a311544cb91c230064e04bf4e4ddd4738bb196c9402417be033dbc640`  
		Last Modified: Thu, 14 May 2026 23:56:46 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ba0125d1e4bfd612c00738f1a31821e1026916af97f3945ffd30556955617d`  
		Last Modified: Thu, 14 May 2026 23:56:47 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21345a3471577059e16e0efedbd78aee9163e4330a9dddd3a4a2f0510c0c168`  
		Last Modified: Thu, 14 May 2026 23:56:47 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5` - unknown; unknown

```console
$ docker pull wordpress@sha256:38008a49460bc63b55439c085a779cb3b975d11aee603ecd1ec5102c6b443ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8475899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c500cc740e19f7ce5a8799bcc33b0564ef51beb3209f1a3cb9d773cea092d55`

```dockerfile
```

-	Layers:
	-	`sha256:61a9033d5ac204e5ac525d8b1828172cad35ecb2b35ce6f20c9bceb3aab09c56`  
		Last Modified: Thu, 14 May 2026 23:56:44 GMT  
		Size: 8.4 MB (8411601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2257d820fcffb90a35602b98f7025bae22660c1388bcd324c2785ae6d15d4be`  
		Last Modified: Thu, 14 May 2026 23:56:44 GMT  
		Size: 64.3 KB (64298 bytes)  
		MIME: application/vnd.in-toto+json
