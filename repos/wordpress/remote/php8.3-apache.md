## `wordpress:php8.3-apache`

```console
$ docker pull wordpress@sha256:f2eb2bef5248eb6af43919d323d97d43e2e738182a0637c4fb74e8e137c96072
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `wordpress:php8.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:ca731f89fb94a4d840887215f309a989d374870829f9fd321d215ddfa1e85505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258289058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213902d7ce9ad3dfda52769b42025da0ef261b94ad2cb8ce40d3175f00a73e64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c386db9cb1d87e70bc4655a9f464379178e6faec37925b32f481121cd1fd6b5`  
		Last Modified: Tue, 13 Feb 2024 07:32:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef1b237c949fbfc49af0024af5189a1feefff253e445a7b19ab4327ce5a5909`  
		Last Modified: Tue, 13 Feb 2024 07:33:11 GMT  
		Size: 104.4 MB (104355255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c66cb68b0ffb6ab95a1aa748b4012b5da8077a4a4c14a3f9bebcf9bf02f351`  
		Last Modified: Tue, 13 Feb 2024 07:32:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c790c1c009dd7204cac7a35fd9151636c23f96ae965fec6263addd5d366c547`  
		Last Modified: Tue, 13 Feb 2024 07:33:38 GMT  
		Size: 20.3 MB (20303944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055748d0b38a426b2cef949d76f35fc04c5a9a9a66a2d40449219a4853635cf`  
		Last Modified: Tue, 13 Feb 2024 07:33:35 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d72b3b895bccef06314fe3a5818d977b5b695a9e1a698eab278c1138790f8`  
		Last Modified: Tue, 13 Feb 2024 07:33:35 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093e006a47483ceda4573d7de3ccbcb38aa62667a284b708662428d9efe4d9b`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 12.8 MB (12773077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2821a08332aa84def9fcf0ccd7cf2c90e2fcefd8fb3918848859e38ec4e86c`  
		Last Modified: Tue, 13 Feb 2024 07:36:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4588c42fab526da8b9cbe835fc3e7be6d76014ca7a9abf7bd08fc2d002fe3c`  
		Last Modified: Tue, 13 Feb 2024 07:36:30 GMT  
		Size: 11.6 MB (11633365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdf939f094eada0c10b20c929eb2a08c13e25d2d3b00e7a6c4c55f9f5d32099`  
		Last Modified: Tue, 13 Feb 2024 07:36:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438981ec14c9d99b230db98c8d16d898585846c65d2ca2cf9d78465bfa0b505`  
		Last Modified: Tue, 13 Feb 2024 07:36:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3a90424fc90e0fbb8526e43b4dbc0de3405d94a9c7694217553010a543cbbc`  
		Last Modified: Tue, 13 Feb 2024 07:36:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1767ae33f8c236854ed70c71d02502c73c82743b277b928a0591aff4c78bb9`  
		Last Modified: Tue, 13 Feb 2024 07:57:26 GMT  
		Size: 26.3 MB (26254072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b9bfa77d91eda21a26242dad627852bf6a50c61d40cf5773b9425c56174f0a`  
		Last Modified: Tue, 13 Feb 2024 07:57:26 GMT  
		Size: 29.5 MB (29501220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee73751103607d00b1ab3f18a8b094aa25164413570498a30ffc7b184b1bdd`  
		Last Modified: Tue, 13 Feb 2024 07:57:25 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e4b73873b8101bed77c22d6949709d4a169ae228683459d66962f713d78cb5`  
		Last Modified: Tue, 13 Feb 2024 07:57:25 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acb7aed29b3be02dbe07bf5ba1b4ecf11ec7140790f379d4fa6396831aa5f82`  
		Last Modified: Tue, 13 Feb 2024 07:57:26 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50d8e2ba626e926c0512d874ffb1747947b0f1be7dcccfe148f44e9289a5e3`  
		Last Modified: Tue, 13 Feb 2024 07:57:27 GMT  
		Size: 24.3 MB (24314491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5daec71a56a81e3535b3bf264fbe77d30261b27ae4f2ce9e3530f2d48082f7`  
		Last Modified: Tue, 13 Feb 2024 07:57:27 GMT  
		Size: 2.3 KB (2344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8557d7966e9b3920b67894beed2c2cb75ae476a73af268d5e265dd6218fb7dd4`  
		Last Modified: Tue, 13 Feb 2024 07:57:27 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:113fb8fdc245a3d246f5aab503254005337f37b0614bb5019639ce8ac3ec5bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7891109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0284fa9f102ad4eb8373a058e221e66520b9d700f3b04e6981591458f5d6d61`

```dockerfile
```

-	Layers:
	-	`sha256:56af2334d5ca447bc3cfc6e99cc20c8c002201ee061dc9e08f76eaf89e49ada5`  
		Last Modified: Tue, 13 Feb 2024 07:57:25 GMT  
		Size: 7.8 MB (7831532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629dde8777f6fc62a73385b40d398c6cacf2abd9e65b637fe2c54122c8125623`  
		Last Modified: Tue, 13 Feb 2024 07:57:24 GMT  
		Size: 59.6 KB (59577 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:8029985c6f38224c1f7b89aac01b4aad8219999a5e6a3748dd4cd804e3eb1a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228237010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b52fbbec5d49feb164e545419ff2ac4a9d22340752dc4b38fab9abe0a513f7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f40b458f7c293243effa9a1cbf7fd3d256ebbc7c885ff704daf63d435ffc3`  
		Last Modified: Tue, 13 Feb 2024 12:49:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8e895018d6862b371d9295a0d9d92eef8a6f5a8dffb4a82e39abac8f6d9b28`  
		Last Modified: Tue, 13 Feb 2024 12:49:47 GMT  
		Size: 82.0 MB (81999540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188a2589cb08b5b121e13881cfeea377bb20a0fd98f84991ab8741127a58efca`  
		Last Modified: Tue, 13 Feb 2024 12:49:24 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee225a49db0db9ebe2e4ca0b2e9e6ee790cf525bb7300b10e6a72fddfc8d07`  
		Last Modified: Tue, 13 Feb 2024 12:50:18 GMT  
		Size: 19.6 MB (19608448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059356789143839a10b3e1970a011879d190d495b19f9ba1079791ee724e517e`  
		Last Modified: Tue, 13 Feb 2024 12:50:13 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ae570e85310d6691597290db7efe3202d00b0fe0ae686830a0afe34a81d7a2`  
		Last Modified: Tue, 13 Feb 2024 12:50:13 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227daa52669ff0cb0d1edaa99b6aaa20399cdb20f02d45dbe8c24e21d8913462`  
		Last Modified: Tue, 13 Feb 2024 12:53:28 GMT  
		Size: 12.8 MB (12771272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0463b897266dcffdaa686b4810d538bc5e97d5882869f737307a34e543031381`  
		Last Modified: Tue, 13 Feb 2024 12:53:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672807d502cbd1725770e1272d21a34ff4994cf46a27b62f10539cdc5be478a`  
		Last Modified: Tue, 13 Feb 2024 12:53:28 GMT  
		Size: 10.6 MB (10600284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0772f4853cf097130bb7f869edc182c2de62f959fdeb2cdcd8970c4c49d51a9`  
		Last Modified: Tue, 13 Feb 2024 12:53:24 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b32b23f01505121347ca0d36f331a3e95469078dabe0359f2e40e916f6742a`  
		Last Modified: Tue, 13 Feb 2024 12:53:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd90e87faee7e4c0d5112506d52d66e526f6a09f6bfba0e0261f8394c99241d`  
		Last Modified: Tue, 13 Feb 2024 12:53:24 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9c09daedc3865900e344fdd27b4835ab53d2f05f3394002deeb3e44a83089d`  
		Last Modified: Wed, 14 Feb 2024 20:35:13 GMT  
		Size: 25.7 MB (25705689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1810698bf7be5eb60e2f39fca0740742fe41d89aba2183b652b707831d5dc5`  
		Last Modified: Wed, 14 Feb 2024 20:35:14 GMT  
		Size: 26.3 MB (26323820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aad513933931768f27679cb0e4da1079f13b178598150abdf9620be6c2fd367`  
		Last Modified: Wed, 14 Feb 2024 20:35:12 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d4d6751af554b7e419b29b61909efe72aa326f2f647b085dc90567b41dc7c4`  
		Last Modified: Wed, 14 Feb 2024 20:35:12 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289b14917918e7aea007e99ff308cb18f14ee16747d2423935fad417af22f3f8`  
		Last Modified: Wed, 14 Feb 2024 20:35:14 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6afd7d35e90652e4da70952e99092477a8c4ebc72831d58fae81a272d9cc6e6`  
		Last Modified: Wed, 14 Feb 2024 20:35:14 GMT  
		Size: 24.3 MB (24314485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c13a1953b8e54f22459c11c55267fd57138818e6dc41705ff8f333e9e2f157`  
		Last Modified: Wed, 14 Feb 2024 20:35:15 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813b407d8048a6e938ec9ea079d18e8875baee54b05ee755816dff8ec99c1a1b`  
		Last Modified: Wed, 14 Feb 2024 20:35:15 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:6a00d80f833e5838bbaf2473923d10cac3c1e59fa344683284d57bb161ebd08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7722658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e37544a2325262b4681a709ddaa99832973a77c444b30544fc34d46f08e161`

```dockerfile
```

-	Layers:
	-	`sha256:a9a5e5c0d45cb34dd8660623d01de8d3fa76dfa683ef3180d180fc8f08ec2022`  
		Last Modified: Wed, 14 Feb 2024 20:35:11 GMT  
		Size: 7.7 MB (7662923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140a53b08739cf62b3357ea29284ab932354e461d985a21794d7fc4dfc7d5fe3`  
		Last Modified: Wed, 14 Feb 2024 20:35:10 GMT  
		Size: 59.7 KB (59735 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:16f78e66ceededd254bc0ec88e6c98dd78731e915e07495553d514542bb733d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216955821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f163ab0bfde5af8ca284158f47d2b19b52c304dd7f8db221869e871a4ea647e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391138267e710c3afd1b13ba20349432d550fbb6ca24d5c03c761feae22b88ee`  
		Last Modified: Thu, 01 Feb 2024 04:24:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc30a445c6e4bf057f6d7fb3a4548be66cef938aca0884681b2602cf7807923`  
		Last Modified: Thu, 01 Feb 2024 04:25:04 GMT  
		Size: 76.2 MB (76169686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2abab10a7e661e57eca65741d4ee689ebb206370db90b4c05c93aa3b7afce10`  
		Last Modified: Thu, 01 Feb 2024 04:24:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c27433b27de38bd46689c5ab4ea8a423bc343feebaea73d1d20d2aa314da3e`  
		Last Modified: Thu, 01 Feb 2024 04:25:49 GMT  
		Size: 19.0 MB (19046603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1fd23f93df4e6bcc7adb049f7e12804c6313798f3ceec63da7db141eed10a8`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649568d520a69772a79a3e5c4ce6031b6f2f7e274993c07bb783e481941066ff`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef156575c717d6bb8b5dae31f558ff136bc74da241276af164c60db6628d24f`  
		Last Modified: Thu, 01 Feb 2024 04:25:46 GMT  
		Size: 12.8 MB (12772361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d2916f1a2e30ce54f2f20c46e16032a69459b026f2bc05c9a0e036e4f4d834`  
		Last Modified: Thu, 01 Feb 2024 04:25:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6dfef68d5dc9a7300bedd0504b737f66984211a8797084c6d535c2bd8601d9`  
		Last Modified: Thu, 01 Feb 2024 04:25:45 GMT  
		Size: 10.0 MB (10028974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4748959369b06975de070937b7296a36da99942df52df3c1d9d5b43c498fbc27`  
		Last Modified: Thu, 01 Feb 2024 04:25:43 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58488d4ec07e73c2eabd06186db1fa9ca6f3d1156336e929ce5fda92f1b3e9bd`  
		Last Modified: Thu, 01 Feb 2024 04:25:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bff761e5bb5763cd17b91c3c8567e5e4c15b96bfc9b03e531b9dd5ef84b1ff`  
		Last Modified: Thu, 01 Feb 2024 04:25:43 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375cdde8a721e5157062d5c3b9d67ebb1a0412088ed49c35130ee6d2835d4cfd`  
		Last Modified: Fri, 02 Feb 2024 13:53:13 GMT  
		Size: 25.1 MB (25079040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb72c714cf6465da51a216465174dbdf801cacae7e77cec25920c1e8d1649ce7`  
		Last Modified: Fri, 02 Feb 2024 13:53:12 GMT  
		Size: 24.8 MB (24773534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864748d7b0147c04261b9e55dac00865a00ed81df331a77ee5f04ca0f7a86966`  
		Last Modified: Fri, 02 Feb 2024 13:53:11 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d78505a8058c311decd6a7706d4ffceae25b61960979fe76cb34d89bf3a257`  
		Last Modified: Fri, 02 Feb 2024 13:53:11 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f2d4b7ce00f86fe24dbacb4391501f335f8f4f0d5f0da47cd5728a287de634`  
		Last Modified: Fri, 02 Feb 2024 13:53:13 GMT  
		Size: 19.2 KB (19174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad4083fef96358a7f88a87bc4918cf8098b270dd6b9bdae88ec73dafe0e9c2d`  
		Last Modified: Fri, 02 Feb 2024 13:53:14 GMT  
		Size: 24.3 MB (24314484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee3072d2fb5be4bce78410913cdd449c398125ec0c986267ca222d43ffc6cdf`  
		Last Modified: Fri, 02 Feb 2024 13:53:14 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3425646b7d57d062e216e92c6c20b39eb796c9859e764f7c202088d41774a1c`  
		Last Modified: Fri, 02 Feb 2024 13:53:14 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:830990e7214a903bcf993e7e5f4dcdcd3a7a19c6d25e161cde7ade38dba21df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7727340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad6335ecffac2bffbaf56cf35be2b51fc954986aa97a53e7c87ea65e66957ab`

```dockerfile
```

-	Layers:
	-	`sha256:5a640fe5dc3f0c8a9f779fdff0ca01ee46cdf08579f9d9faa0de0469dde72479`  
		Last Modified: Fri, 02 Feb 2024 13:53:11 GMT  
		Size: 7.7 MB (7667605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8afb134d46d1624952d58226e82d35cc4a09fc1f1d171334bc9d1d77f5eef6`  
		Last Modified: Fri, 02 Feb 2024 13:53:11 GMT  
		Size: 59.7 KB (59735 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:3910b266baecef763ecbb3a7c39f85034b2dfdbaf0e0684905d995dfed54bbe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249644954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c77595accb195f4925cbb9787415998f5acc83925c518e9c9f0e2d1b2719d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7a340515b48e1c129ae5f32a9749bddee1f8e8329b7598fcbf4d08bbd6fb1`  
		Last Modified: Tue, 13 Feb 2024 07:00:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290f914abd180febe4ca21f26e7dbd62a7d47b3e0c2bb607b502ef0420c26a39`  
		Last Modified: Tue, 13 Feb 2024 07:00:29 GMT  
		Size: 98.1 MB (98125913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa77fec9d8935ca4f47917fa1800499aeb09f491467b65b0914b9598f905ab`  
		Last Modified: Tue, 13 Feb 2024 07:00:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e32a81172311d82a21a8c59c44a19943264d56868424bc14043cf6100b2fd`  
		Last Modified: Tue, 13 Feb 2024 07:00:54 GMT  
		Size: 20.3 MB (20305132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4064de42914748cf75888bc76bce8469dc92ae858893c597ede2741b140c622`  
		Last Modified: Tue, 13 Feb 2024 07:00:52 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1ed550d4635090d82d30c08e1d408806bfba8c24fffe9004f3b0837df191b`  
		Last Modified: Tue, 13 Feb 2024 07:00:52 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386b601feb192f68b001dcc294c04609ab2204cfc10e5bb16c1def96e51c23bc`  
		Last Modified: Tue, 13 Feb 2024 07:03:41 GMT  
		Size: 12.8 MB (12772760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a803f43bb874b48ec53fe7e0ae2687a8fa6a77d8f0d581e7c811843e83252b`  
		Last Modified: Tue, 13 Feb 2024 07:03:39 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889843d853c3c34d1d264de99fc9ac6db1e44d05a670dcc1e6c71666b2279492`  
		Last Modified: Tue, 13 Feb 2024 07:03:40 GMT  
		Size: 11.6 MB (11627180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1595561ec290189d5085e95cfe28c198bd45463831cfab6395e2063a10b41a62`  
		Last Modified: Tue, 13 Feb 2024 07:03:39 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ef096bf616f8393809b5003f3df9d80c8b837fb2af77fb4c4ff8b5b412083f`  
		Last Modified: Tue, 13 Feb 2024 07:03:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e81334347996a88776dd3691bfa032cf0c4920f06973a11d5a4ded61129172`  
		Last Modified: Tue, 13 Feb 2024 07:03:39 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90745889eec4452f165c91a9d59db8c6a6fc3b31d28038330db005b25f65f4b8`  
		Last Modified: Wed, 14 Feb 2024 11:24:43 GMT  
		Size: 26.2 MB (26175737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1677e118c7d83341b7811b80ae158aff1a783123a6b1b84cfc9c83bcf0aa5b`  
		Last Modified: Wed, 14 Feb 2024 11:24:43 GMT  
		Size: 27.1 MB (27137795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df15a56021631d5d350b06c1ff71c215fe0528dcfe07b1053f386c8db83b7ce`  
		Last Modified: Wed, 14 Feb 2024 11:24:42 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e50dea63762d4b4b1f6526fa3cbbb318782c90ff0f7ec2f8f58216ce77c235b`  
		Last Modified: Wed, 14 Feb 2024 11:24:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f994c3964a639ffef7c0ab9ae1bf39db218937a36b5d2cf0852e2d2d0bb66`  
		Last Modified: Wed, 14 Feb 2024 11:24:43 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d96d25c065922f725317c51918744ecd676cdf2f84db4366531931a5b764761`  
		Last Modified: Wed, 14 Feb 2024 11:24:44 GMT  
		Size: 24.3 MB (24314515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4b0a5767cd45f27383f59ba7e2eacab27a018deac10fd932ff0709cd379010`  
		Last Modified: Wed, 14 Feb 2024 11:24:44 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbb3248c96c6819208845f7737e3e0139df95fddb94756ebaf3746cb6305f0c`  
		Last Modified: Wed, 14 Feb 2024 11:24:45 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:7a991c5112560df017d4d522c765ed9a8c54ae79d162ccdc17c674c83b9b1ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7914402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1c81c2eed3d5ab52afcc228c82e629b33634a784aa8f58467bbd1e28d9997b`

```dockerfile
```

-	Layers:
	-	`sha256:89fb60a6d8677e7037d1a57c63eb7e52c406ad954dc0ada65b8fecbe328fd243`  
		Last Modified: Wed, 14 Feb 2024 11:24:42 GMT  
		Size: 7.9 MB (7856924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927f9078c9ee6d1fbd4f09309e8565e114ba593951c71160fd9ab0b0cb93440c`  
		Last Modified: Wed, 14 Feb 2024 11:24:42 GMT  
		Size: 57.5 KB (57478 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:589c956ca3f070511234dfe896242e030f9f4e59f3132db4c231a872a710ffe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256999576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c02a7e853eab621e66012eb9885464c7dd1a287e2b4dfc4ea12647274d6f022`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfde49385a90835b9c1612c002c49650aa228e709c6bec76329576d154acf40`  
		Last Modified: Tue, 13 Feb 2024 09:08:55 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ed10d21879c841ec1dc9f3c51bfc996313547be9838dd0871e0c090e9db93`  
		Last Modified: Tue, 13 Feb 2024 09:09:19 GMT  
		Size: 101.5 MB (101519769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0108a981d683eb4695cf1efac3357088358d8bd27fafb095510dcdc689e9270f`  
		Last Modified: Tue, 13 Feb 2024 09:08:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa94a6b92707cb45a0ff3ab809cb18c5a53cfcaad6fb553c591ef3b376088a1e`  
		Last Modified: Tue, 13 Feb 2024 09:09:47 GMT  
		Size: 20.8 MB (20826088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ba0ea043787178dd74139db437ce2498a8d3bf85e4eed296ea8e55a598f5a`  
		Last Modified: Tue, 13 Feb 2024 09:09:42 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ec064cfc067a6de6b378be145b2249b472d81b6fbf511d5f614fdf9909cad5`  
		Last Modified: Tue, 13 Feb 2024 09:09:42 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e5e011db08875a622eba856434be56155e97ae3ff437fe172db2dc216577ac`  
		Last Modified: Tue, 13 Feb 2024 09:13:02 GMT  
		Size: 12.8 MB (12772195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d966e761afb2da61b31b0cb626adf2006bce7cfcf2f03ab98514a1de1be1dbfb`  
		Last Modified: Tue, 13 Feb 2024 09:12:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f8208c3a04b43ebb57f5622dde54b6bef4c9d251f98eb4859681efac6d999`  
		Last Modified: Tue, 13 Feb 2024 09:13:03 GMT  
		Size: 11.9 MB (11850254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52b72ad7780a5b0ad01d4511556b481021f3f7604bed5824d57019821cf4a6c`  
		Last Modified: Tue, 13 Feb 2024 09:12:59 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd121aea61fcd14d2dd1f83bad44e4e7f1e9d641d59b8d55d4817fded2b4fe2`  
		Last Modified: Tue, 13 Feb 2024 09:12:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555d413d1ca4ef1abe69e459b38efbc541de7f4221658d022523f81cb3a66c25`  
		Last Modified: Tue, 13 Feb 2024 09:12:59 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa4e9508a969f0d88612bff95aa4c4d3e23ceefac381d3e9a8f72f333091066`  
		Last Modified: Tue, 13 Feb 2024 10:58:49 GMT  
		Size: 26.7 MB (26700643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f4c3d81022bdc1515b8651d6f721ecb38c91100fd703cedd26bf4f16be39ce`  
		Last Modified: Tue, 13 Feb 2024 10:58:49 GMT  
		Size: 28.8 MB (28844808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df292429c193e5044bd154a54b4570f05dc6eeaa88d1c983f328380d4a382b17`  
		Last Modified: Tue, 13 Feb 2024 10:58:48 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77fac26b56a981863c480f976af0d330881d2e51666be91e9a6b7b28afc867a`  
		Last Modified: Tue, 13 Feb 2024 10:58:48 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad20168f470378053b05c4369341a019861c84a08d4b5a4787062e35ee60adea`  
		Last Modified: Tue, 13 Feb 2024 10:58:49 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6f6377516a2f9583c14b68555e6ebcb5d3baaf58957176c81ecdc88ecd5b3c`  
		Last Modified: Tue, 13 Feb 2024 10:58:50 GMT  
		Size: 24.3 MB (24314485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42613c1cf483063bfc80cd5e0ba94994a9e81e714803b1bf166dfb60218ecea`  
		Last Modified: Tue, 13 Feb 2024 10:58:50 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62b1b803cecd35440a11961558fd68521b63f23645041d960dd3650c2ef0873`  
		Last Modified: Tue, 13 Feb 2024 10:58:50 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:f349eca0db7f59c0c9476b0610bf0e11414d2f7505f22e93acbe1826f5689153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7872355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5063511c105d1bc8466657a544f8f020b7b19f91dbb64954d70657a40f437545`

```dockerfile
```

-	Layers:
	-	`sha256:f33f01e685cf957192897bee9593567f433a85cda660f6d3ddfcc79c28da28b7`  
		Last Modified: Tue, 13 Feb 2024 10:58:48 GMT  
		Size: 7.8 MB (7812837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7cd587d308a4a637b74bfd7a8b2fe11b3d79cd9173a0448caa9ffd2f51e403a`  
		Last Modified: Tue, 13 Feb 2024 10:58:48 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:05125d62344a88e71aff9120b1df59b801affc31fcaa1192e9af40f4e4b9c4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263920640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed2eb8182e6afb68f319b41da490f95496ad24280bf806d5cf0fd7341f78df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f1023e69b0297ca1b43f02b0de9f2700c16c9f3bc3cd4d532dce1fed98a82`  
		Last Modified: Tue, 13 Feb 2024 06:43:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c21152df6e3694f2bd61235e4c23ee7e24735cd91cfff9f6dca5abb307a801`  
		Last Modified: Tue, 13 Feb 2024 06:43:58 GMT  
		Size: 103.3 MB (103313095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0608cc469fd017def730be29629f988d7db21971cb60c627d4043f3f4ff24e3d`  
		Last Modified: Tue, 13 Feb 2024 06:43:40 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c86cd418ad9f36395f647795ce8a6ee67f8cc57ee87b45a13e843c0d2209c3f`  
		Last Modified: Tue, 13 Feb 2024 06:44:28 GMT  
		Size: 21.5 MB (21489555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82afa6fa26cbb0b105f3ff50f1bb25a7743b2fb1e1e56092bf210cfd7a63d9ae`  
		Last Modified: Tue, 13 Feb 2024 06:44:25 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20423759eec7201d4e061fab44ae4f2be21b3cf195ccf90ecac69aa7ff61e45`  
		Last Modified: Tue, 13 Feb 2024 06:44:25 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e67cdffd9e6ccb6da3ed323394494b8d15d9fcbaae840a3ad6b1c549bbef213`  
		Last Modified: Tue, 13 Feb 2024 06:47:43 GMT  
		Size: 12.8 MB (12772757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e473f81bb6ee8dfa1d6cd56fc76bd0c5e5424fb63cd2555cbbaffee6c5b708b3`  
		Last Modified: Tue, 13 Feb 2024 06:47:40 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea289a58b852515f12130218f91dad59b31729c4f84b51367a5253bf88626cb0`  
		Last Modified: Tue, 13 Feb 2024 06:47:42 GMT  
		Size: 12.0 MB (12043728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39d7f07c1343875efbd472dd8299f57f720b04beb552a93fa3b829b206a9892`  
		Last Modified: Tue, 13 Feb 2024 06:47:40 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a2bb243ba3c0a78c29807f26fbc3862d11e57acc1339f0f92b6e9513f15f19`  
		Last Modified: Tue, 13 Feb 2024 06:47:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0daea12ea22b18732a925c44e76659e56521b0b49c20539b6dcfb9a36ec8f53`  
		Last Modified: Tue, 13 Feb 2024 06:47:40 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0364583ef2408afa9b2b1756cff3c86ee15ff696ebed4151cb8737609f00b978`  
		Last Modified: Wed, 14 Feb 2024 06:29:37 GMT  
		Size: 27.3 MB (27340435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f37eccb3c44c925ca3fc183925f0d3f4ade92cad4803e21254b3263bc81bf5`  
		Last Modified: Wed, 14 Feb 2024 06:29:37 GMT  
		Size: 29.5 MB (29498107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30494b9667b1436ead55cffa2e7745377e5310aa4b24e5d9bd7011418d2bdf0`  
		Last Modified: Wed, 14 Feb 2024 06:29:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fcaea37fb7582ba5574b13255481635741bb52eb32a2d05bd847659fd1c23e`  
		Last Modified: Wed, 14 Feb 2024 06:29:35 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf27a740c861c504494b0523b81c481c12e617d681c14973c5d73abaf7c56f0`  
		Last Modified: Wed, 14 Feb 2024 06:29:37 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da27926b954fd640ccb87e827e82e1b77b63bb654cdefd4be1405c726e96e107`  
		Last Modified: Wed, 14 Feb 2024 06:29:38 GMT  
		Size: 24.3 MB (24314499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3953ae83ebc8b88685b70db8d93bb048c014842652258c833e8f8519f50a25d2`  
		Last Modified: Wed, 14 Feb 2024 06:29:38 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a837f28a205e5b00546d48fe4291ef603134deed839d3c603f89c45644b630a`  
		Last Modified: Wed, 14 Feb 2024 06:29:38 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:d32f896a0cd7dd01de5c9448ae6521d1305372fc1b85830ba4924d9cb638ea03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7872421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224e1842667f2411a4938e4a54d5fedcbd7ae5e946c8cc05fd15447f00f245ef`

```dockerfile
```

-	Layers:
	-	`sha256:e632ef5041f1467604849a2b331e9972f6b18b3371db3c93ddf89427fe3eede3`  
		Last Modified: Wed, 14 Feb 2024 06:29:36 GMT  
		Size: 7.8 MB (7814882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65af68e826d066f594aa2e621df4dbc1fd443dea93b9282f4aae2e53d0fa341`  
		Last Modified: Wed, 14 Feb 2024 06:29:35 GMT  
		Size: 57.5 KB (57539 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:cf3c728f13d2563812633c18b3d0e1f1bbdd2325d041fed21e97ed0319776ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228328629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207a50624ded4390662a88315e0fda8bdcecf6a3a40a966e366287cb5210df55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 31 Jan 2024 02:03:17 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 31 Jan 2024 02:03:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 31 Jan 2024 02:03:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_VERSION=8.3.2
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Wed, 31 Jan 2024 02:03:17 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 31 Jan 2024 02:03:17 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
RUN docker-php-ext-enable sodium
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 31 Jan 2024 02:03:17 GMT
STOPSIGNAL SIGWINCH
# Wed, 31 Jan 2024 02:03:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 31 Jan 2024 02:03:17 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 02:03:17 GMT
EXPOSE 80
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
RUN set -eux; 	version='6.4.3'; 	sha1='ee3bc3a73ab3cfa535c46f111eb641b3467fa44e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
VOLUME [/var/www/html]
# Wed, 31 Jan 2024 02:03:17 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 02:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 02:03:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db025363a3a1d7c6b99da4e14d1125b74c4b842740cab764d0f3f92123eda2ae`  
		Last Modified: Tue, 13 Feb 2024 08:11:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d7e20d739007df636f4e0bffb8c753fe34b5834c77a8560ad481209b713da9`  
		Last Modified: Tue, 13 Feb 2024 08:12:10 GMT  
		Size: 80.8 MB (80808538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231f09f66b39d784560a47b0a9a35c9ffc75c958ac6d714b931e2f10052eeccc`  
		Last Modified: Tue, 13 Feb 2024 08:11:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad9a7e236c2428d77411e290e407d3e563b97f82068a1a6f62ffd1c26dbd087`  
		Last Modified: Tue, 13 Feb 2024 08:12:35 GMT  
		Size: 20.1 MB (20083103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35a1a694219ffe08748ca3f8b465091ef91d33338469118ed8f6a3ba20e1b7a`  
		Last Modified: Tue, 13 Feb 2024 08:12:32 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad958effa4899374506d8ba746fcbf20d73ce55af4e9e5dae0e070db097fd91`  
		Last Modified: Tue, 13 Feb 2024 08:12:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c1e8e554dcb14898dfba23e70a1a1c4bb68947424e196b455f32e69aa4fc97`  
		Last Modified: Tue, 13 Feb 2024 08:14:44 GMT  
		Size: 12.8 MB (12771504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbea47df09964df260d28e5dc87d68270b9a934d2de901f43c233e558c434de1`  
		Last Modified: Tue, 13 Feb 2024 08:14:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2f277df75064b7df9b7bd581057b208c99f134115dc7a49e1992872554c4b8`  
		Last Modified: Tue, 13 Feb 2024 08:14:44 GMT  
		Size: 10.7 MB (10661719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3439af72c4840ef2c036d895c3cae701c44ee1ad29c6438d2f833fe781f6c3`  
		Last Modified: Tue, 13 Feb 2024 08:14:42 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f79cd8da68aacca9cbb90accd91025c260234ef4ae1cf830c4116171d450f7`  
		Last Modified: Tue, 13 Feb 2024 08:14:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9a1ed16d60ff8a99c3b8a183d7bb8182c7c5101f29a16750ba0dc63ed33d99`  
		Last Modified: Tue, 13 Feb 2024 08:14:42 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f2b9ee5f56874e239f579f08d0cb1420ee5ce4d8fa2411bfdda75f74484c26`  
		Last Modified: Thu, 15 Feb 2024 20:54:40 GMT  
		Size: 25.9 MB (25899714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3679a5fe4028055b02006208786f275115213a1cce21d9eb8964ec38642226ab`  
		Last Modified: Thu, 15 Feb 2024 20:54:40 GMT  
		Size: 26.3 MB (26271427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7ac9f03845685322c54a4f7859a1a1585660343da8e36123e7fea61354995f`  
		Last Modified: Thu, 15 Feb 2024 20:54:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7988f7bd0212b6869f8f0fa8193b22fdbd16c2c351fb94ebb65a6cef6c29ab4f`  
		Last Modified: Thu, 15 Feb 2024 20:54:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5e125bbbca7892720b4f8710e3a5cf44fd2113f79d4fa10206a612dc05d164`  
		Last Modified: Thu, 15 Feb 2024 20:54:40 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d427f10d13711d879669df32d3d4a0bbfb4829d2bd0d440ad5aa3d99d1cada`  
		Last Modified: Thu, 15 Feb 2024 20:54:41 GMT  
		Size: 24.3 MB (24314496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b831af19fa55b0dabf549e6d89420a223ae6d11021bed21dd968fecfb8dbe7d4`  
		Last Modified: Thu, 15 Feb 2024 20:54:41 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af1e188c194cb118123373dc556fa39ee11b80367a1ea1c1898f422ba129462`  
		Last Modified: Thu, 15 Feb 2024 20:54:41 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:1579c815600a87ebba34e9140948ac452b3e0db6f546d613f9f7aff3b149919d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7740341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d422beb26d60e4d831584ccf91bcc57250a5d19b69ca61a446f7b9dfb215363b`

```dockerfile
```

-	Layers:
	-	`sha256:91501d70e90fafe85745a3b3e53cbb9b8da62a335e74ba8cb5e99472d45136b8`  
		Last Modified: Thu, 15 Feb 2024 20:54:39 GMT  
		Size: 7.7 MB (7682881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fad0b121318950ece245368e611cd3ae0408b9c2f7481b123c24c31d00edb91`  
		Last Modified: Thu, 15 Feb 2024 20:54:38 GMT  
		Size: 57.5 KB (57460 bytes)  
		MIME: application/vnd.in-toto+json
