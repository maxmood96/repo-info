## `wordpress:6-php8.3-apache`

```console
$ docker pull wordpress@sha256:68db5f699d3dbc8b34037bf1106c62cc09f7d52194816d6f09bb9b9d5d3ec970
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

### `wordpress:6-php8.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:feda947251b81f08d18018ee7980d145a31d3bf483830ab256a76bf723c6d84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241440652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e2ff56535569217e2610fd8a1eaddac352616e2fc5ba46797fdb0b90289965`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e881592e808c901299c28181782f4352df25f3d05fb65aad76e6c9d10c6c27`  
		Last Modified: Wed, 29 May 2024 23:18:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a4c251f36c9a7cd5c6b279c62fe1009f9ae4960e681bef0697387ef94388df`  
		Last Modified: Wed, 29 May 2024 23:18:30 GMT  
		Size: 104.4 MB (104357409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433084d93d648338100d955c81e31a60256909b24864a2a676fc7578e2916400`  
		Last Modified: Wed, 29 May 2024 23:18:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dd3deb295ab1153694603036220a84ca81e850cdfa5bb68800306ede0a2214`  
		Last Modified: Wed, 29 May 2024 23:18:57 GMT  
		Size: 20.3 MB (20329767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284035b533c8cef4086b6c39f8737757b407c77e4424d6501415be8d72dd204a`  
		Last Modified: Wed, 29 May 2024 23:18:54 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a4ba92ab72133d58060ca181f0d4114031110754da57aede725bceaa29a8c3`  
		Last Modified: Wed, 29 May 2024 23:18:54 GMT  
		Size: 514.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f8c869faae8fb82ab46cfc7d02f72823f326565ecd484ee5d1db9c848c20db`  
		Last Modified: Thu, 06 Jun 2024 04:10:59 GMT  
		Size: 12.8 MB (12790481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a9f1c074b610c479257c6e01af4da97ddf7d9784c296129da8b06ac405d35f`  
		Last Modified: Thu, 06 Jun 2024 04:10:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a51185a3c6f525b5afa92d50b1a04cbe1c305108f58a57586081039d71e74`  
		Last Modified: Thu, 06 Jun 2024 04:10:58 GMT  
		Size: 11.6 MB (11638065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace36dbcb9805cd5db51339f7bff272e4bce087d5653e23f7a006dc148a20f9`  
		Last Modified: Thu, 06 Jun 2024 04:10:56 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c57ddc214859016431f2003f4c82f105b1c4167739d958ec8fafd1429117f6e`  
		Last Modified: Thu, 06 Jun 2024 04:10:56 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3a9e36b231a77b2476808f9a5827dde67a3c6d1b78dba1315a07d8041ff5c7`  
		Last Modified: Thu, 06 Jun 2024 04:10:56 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca77a87060d064d17ab3b105a2c64ef80111356b3ba13b75b9cd165615b1b586`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 26.3 MB (26258037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb577f0088c04141cbdec407fa7e65a163b2c01d160a0149deea06fa5f5f95d`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 12.4 MB (12358849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2c96cfc31adde757a6d225f91ccd89c64d12a594692a4d7315897b1ea3c37c`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a0eda0f452b09232295be9b929833ff878487b21255347a3438ac0a6f0b150`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1957e0b34b6ec01ceaaef624b9ec7ac886ba50ecb1b0745fe4132b993c18095`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 19.1 KB (19146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ff23d7627c0eadf60e0e0fd7db8b4684d50a49a50fe50089e02fd4766fb8ba`  
		Last Modified: Thu, 06 Jun 2024 04:58:59 GMT  
		Size: 24.5 MB (24528080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd18a8102f998598e92d0f19cfeb385621db476a608bc95cf77e11c0c6c05279`  
		Last Modified: Thu, 06 Jun 2024 04:58:59 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b13ddee5f3a5e4d6209514d2c872f0378382c743dc4cd73344c45a50461314c`  
		Last Modified: Thu, 06 Jun 2024 04:58:59 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:cdfa9f796f44c88b41d43d7fb1033f91d5cf62dee8c8c14c3c7fe8bbb7909a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8016321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8364bf7177b63ba59f90eb6d24253004c1e281cdb07f5299705d38c31ab27320`

```dockerfile
```

-	Layers:
	-	`sha256:5c6a7e23094313340414aaf6517964af93b0626ab59262c47cee3aca36a0c663`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 8.0 MB (7956715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e9c1832ce6b8d77577cc1ace14f4db8bda1474f2714dc52dd600f086c2fc1e`  
		Last Modified: Thu, 06 Jun 2024 04:58:58 GMT  
		Size: 59.6 KB (59606 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:257f2971c7e9326e556916ab7f35c735626c4264e71f6739de1645d7e7f46f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212152257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c21d7696bc1ab2d0710c3b3184beb0a0d4021f6388a4ae4bc4c2e5e59e80e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9145292b7a7b35c827a769eac94a5446df79958907822cbcf127a5f0ee7195f7`  
		Last Modified: Wed, 29 May 2024 22:25:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fa9377b1a44bcf9ba188d37995fdcdea4dbdccef35b73110ceeffd33a9f2c3`  
		Last Modified: Wed, 29 May 2024 22:25:24 GMT  
		Size: 82.0 MB (82002515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd872800fe92d45c4213854b4e7fadc2e19c9b5e8774ab9d889521c61f825327`  
		Last Modified: Wed, 29 May 2024 22:25:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be63283c8893f4474b1ef29b56f4e321f58afee48fec8b0e5c60ea12454f0f`  
		Last Modified: Wed, 29 May 2024 22:25:53 GMT  
		Size: 19.6 MB (19622277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c1b86de3e64b47da78434469ccd9d2823904df230982161830db0b5a40c3ab`  
		Last Modified: Wed, 29 May 2024 22:25:49 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8443d55710be37614ca87fa85e5f627630114be32581210228324d66fe3a1d0d`  
		Last Modified: Wed, 29 May 2024 22:25:49 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0724d46b5add389ae4ab0d29cccecaa05a2f8375bd08cc2c14ecfae92dd6dd`  
		Last Modified: Thu, 06 Jun 2024 02:57:09 GMT  
		Size: 12.8 MB (12788604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848e0e8a172879abec57adca049c30972f72ca7c0f5399164ae99338a429a879`  
		Last Modified: Thu, 06 Jun 2024 02:57:06 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9744ed6226f2a25dc8655d9b3acc29b6a1bf60d57ad32e4a33c1a6916fdb415`  
		Last Modified: Thu, 06 Jun 2024 02:57:09 GMT  
		Size: 10.6 MB (10608737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de564d38c2cfe31e3be2f704993a9b5bc9baff4238598763b335ca9b3c3877ba`  
		Last Modified: Thu, 06 Jun 2024 02:57:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6c832417d3ad32b9b0c53c44f8fb592f7d705e542cb4c856599ae2b7049697`  
		Last Modified: Thu, 06 Jun 2024 02:57:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee8ce73d8ace1443990fdd3fd1226b9a9faa3ca3e841562fea4bb1bcb63539`  
		Last Modified: Thu, 06 Jun 2024 02:57:06 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9592e1aa15393bf250fe929a208f7ac161f2fa37684483940fb00ad1e0d070c`  
		Last Modified: Thu, 06 Jun 2024 06:09:02 GMT  
		Size: 25.7 MB (25710848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaac24e96442379a125f5418091cc2070c4b9b0607b60f069a4c90a5b817e57`  
		Last Modified: Thu, 06 Jun 2024 06:09:02 GMT  
		Size: 10.0 MB (9951709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39d6efd4d6f81fa5785acf70153e8ac508504805ec223f623baaa50c1a4d133`  
		Last Modified: Thu, 06 Jun 2024 06:09:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4427303684a42feacb6ca23e518a33c1d647e88557887386db9ac8308826ec99`  
		Last Modified: Thu, 06 Jun 2024 06:09:02 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145987b7c5b2e4ce4679ae5c820c3a0aae6bcf0c7e3fe2fc143c4614141aa4c5`  
		Last Modified: Thu, 06 Jun 2024 06:09:03 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcc4e8c846abf4f8d868436ae109aff169b3e9657c041debf68c0529f7a62be`  
		Last Modified: Thu, 06 Jun 2024 06:09:04 GMT  
		Size: 24.5 MB (24528083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a02ffe913c0d6c39b98be0a24b22655a3cc7c9138fbb89cc413024951d76463`  
		Last Modified: Thu, 06 Jun 2024 06:09:03 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb10616bee747a022020e7b84b8db7dcb33105c7807f0be445c86b5183e3cfb`  
		Last Modified: Thu, 06 Jun 2024 06:09:04 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:7f91b6364d7482e1efba48ec87703d9552f778c43409666ac0c5f3935d6c61bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7824028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6195ae3ac580e8192cc8255bbe0baef5c3c18a070c9f63be1dc2b1803be6dc`

```dockerfile
```

-	Layers:
	-	`sha256:108683d87a6f360930225bcb49fe5540b2f635fb669112a77c50e8a1cf4a236d`  
		Last Modified: Thu, 06 Jun 2024 06:09:00 GMT  
		Size: 7.8 MB (7764271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caef37e6e88d965efa3a0aa0e9cd5080bc6c077393c1519837af17fa7f4fbbbf`  
		Last Modified: Thu, 06 Jun 2024 06:09:00 GMT  
		Size: 59.8 KB (59757 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:9f291e949a7ea4b3f37df571cafcdfa4da7bac0acaf2e94d563b61c021a1445f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201411639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47842392533ce779348b845a2ca8ebdc3ce90a850c117efa058d9a38b36efe12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0669aad48e5535f7a37a1db4ef7adc3041b27d6401be481d96b2f1caec7135`  
		Last Modified: Wed, 29 May 2024 23:34:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1889970113df85d42205d7749e42d9479aafae8a28ee304a252b39596d9d15`  
		Last Modified: Wed, 29 May 2024 23:34:54 GMT  
		Size: 76.2 MB (76173127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ba193271322395ee1837a5096cc8266945252cf87c1611520b9a9d37d64eb`  
		Last Modified: Wed, 29 May 2024 23:34:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d33951c91ee28e636edb2b5850837fe9e62c97fa9d2e88285cba9616eb9d824`  
		Last Modified: Wed, 29 May 2024 23:35:22 GMT  
		Size: 19.1 MB (19059226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6d87663eef938c7674a652d4347c95fefdc897c587bf528132bef7d9a56e3`  
		Last Modified: Wed, 29 May 2024 23:35:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4068b53ee3ba83cfa63eb0ea57d530f2654bf19ecbc2ef98e1271cfc0d7d4`  
		Last Modified: Wed, 29 May 2024 23:35:20 GMT  
		Size: 515.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c31652c6f6783e8e4f71626befe537b691ae3e1cf7d3c2cadc71a8de8a8a6f`  
		Last Modified: Thu, 06 Jun 2024 04:22:08 GMT  
		Size: 12.8 MB (12788530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2502c6381a9d192097a1607b21db7858c4b87243903708d6c6961b6fe2e7efe`  
		Last Modified: Thu, 06 Jun 2024 04:22:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f8dd2457db5e14624ffa7932656f8bf2db7336398d7b64afa859c1b6afa1e4`  
		Last Modified: Thu, 06 Jun 2024 04:22:08 GMT  
		Size: 10.0 MB (10031293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5838a66e86d7c17ab3a99f61f733ea7c9693651d5a91bb7e2b83b0ace7afdec8`  
		Last Modified: Thu, 06 Jun 2024 04:22:06 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7480893b0a745e7643627519820b6d95d2ee38db924397f914cebe92de88752d`  
		Last Modified: Thu, 06 Jun 2024 04:22:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e851c26e227b0e551764fe6ac77f68d970cb9452cacd2fa8a7f1a5871992f25`  
		Last Modified: Thu, 06 Jun 2024 04:22:05 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721febd59d7c37c82874c223012bb66f5c1ed7454dc89fa1fcd73c31a5f1e174`  
		Last Modified: Thu, 06 Jun 2024 07:50:15 GMT  
		Size: 25.1 MB (25078288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83db2baf048146f41f3456c8525cf46f08b4e4bb13c4dff08f6bf8557446efb5`  
		Last Modified: Thu, 06 Jun 2024 07:50:15 GMT  
		Size: 9.0 MB (8983327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411ddc854609e36bc0159d43ca3e25e663674502ce41590c81ab60b053e3a141`  
		Last Modified: Thu, 06 Jun 2024 07:50:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8532199afb4e901c55a54a42248bb13b984cf407579c937363a86aa562c23baa`  
		Last Modified: Thu, 06 Jun 2024 07:50:15 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a36beac2b04ce1c54edb6e2bb735741aaa5bad7bf853face22357a76e33e3b`  
		Last Modified: Thu, 06 Jun 2024 07:50:16 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8c5f91dea442bc0e9c7bbe6be25b66c6e2773b2bc70f471134f9fb5265fb5`  
		Last Modified: Thu, 06 Jun 2024 07:50:17 GMT  
		Size: 24.5 MB (24528069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480a21e3a2cdc04e42eddafd78d4c848f8a755f05b754daab2fcbb159289fa2b`  
		Last Modified: Thu, 06 Jun 2024 07:50:16 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5222d438a94c400957e0f096f67024347a8d36d074414f46e7f425c93ded1b`  
		Last Modified: Thu, 06 Jun 2024 07:50:17 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:c3c03fe8425383dfc5f0d1566c2a8a24182444aa575ea831c7bb64fbe5e656ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7828584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ca9be4cb96c77dc635955182f8e03130ec4381bc0a704438402d1e03bfd8ff`

```dockerfile
```

-	Layers:
	-	`sha256:636dc3c045a8518bee870ea37c7d0a4b535be08a3c1996ca545f1c74a471a3ed`  
		Last Modified: Thu, 06 Jun 2024 07:50:13 GMT  
		Size: 7.8 MB (7768827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c56baba557dc855d8dc21a8e34c84f43770d7f65e1075b85c42d125387b2f9`  
		Last Modified: Thu, 06 Jun 2024 07:50:12 GMT  
		Size: 59.8 KB (59757 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:38f46db398eecd37e7bc7a45206d7f13e387731fa95c453edca6080392076173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232767028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126c57602214b42bd20ad1ae226181671befb8ef909bc0d182884c43282a1be3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08227a7cdd1d3214d11329cf01f5114df7343b00fb37373161db1e32fd1cb35`  
		Last Modified: Wed, 29 May 2024 22:53:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea103f4ff29331e870d8e27667d0726fc38087fb5545660758eaa86427458d8`  
		Last Modified: Wed, 29 May 2024 22:53:54 GMT  
		Size: 98.1 MB (98133034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f43600df16ccc688ffc47123b84c497ed1483c88ad36a6eb39e2fb5c11e055`  
		Last Modified: Wed, 29 May 2024 22:53:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129678900e7c64daa2310d7ff9b1a0dc73b00801ef0f7e4e1768c5105596084b`  
		Last Modified: Wed, 29 May 2024 22:54:20 GMT  
		Size: 20.3 MB (20322371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98747e6ac719e4992f35f8955f73db52551189a346dd48ca1a70ff43e127ff16`  
		Last Modified: Wed, 29 May 2024 22:54:18 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0cd77750715b16a02e23863f0ac2e8a2f9c2eda9900b065715b81a8a35797`  
		Last Modified: Wed, 29 May 2024 22:54:17 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b00bdc5269be4be9f5637e5306a101d82b443426ec2f8b4bf3976838a01c2d`  
		Last Modified: Thu, 06 Jun 2024 04:16:25 GMT  
		Size: 12.8 MB (12790200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff0f0d9710ff473ffcbb5c36a076f6b3fe416b3b6c30991b97f8ffeec522f13`  
		Last Modified: Thu, 06 Jun 2024 04:16:22 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4aed29e6a68e5740bfda865b2d95ebb927ef3cf79d56153e50c9823da494a7`  
		Last Modified: Thu, 06 Jun 2024 04:16:26 GMT  
		Size: 11.6 MB (11635281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9579281aa6980bed5d7bc68cd69a0d02be393b12a82b5cd25c0865c840f118b`  
		Last Modified: Thu, 06 Jun 2024 04:16:22 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db68b158d059254f691b27ff54b7f272e29d32e053e27c32bcf7916a2e5be5e`  
		Last Modified: Thu, 06 Jun 2024 04:16:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba556f27485b7d95f7d5bec2eb5d216066908bb9a4fd13d0f74c5145af9543b`  
		Last Modified: Thu, 06 Jun 2024 04:16:22 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26c5c527dd71ead75dbfb4895af21421a14a40f24508be68c20005c4b5fe9e3`  
		Last Modified: Thu, 06 Jun 2024 09:29:32 GMT  
		Size: 26.2 MB (26179643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435bada782ee6e5e2626000d9917aadad8cc941d6b0262c6d80cc31bdde1c9c`  
		Last Modified: Thu, 06 Jun 2024 09:29:31 GMT  
		Size: 10.0 MB (9969349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5803028b7be5052e1634819c5037b1bae6cebb5553d44184f5bc89f3d232fc`  
		Last Modified: Thu, 06 Jun 2024 09:29:31 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80241ced36ef5ac469866a471a1ddbe4e706abf3a10da414bd5561af351bf4f4`  
		Last Modified: Thu, 06 Jun 2024 09:29:31 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6551661cd976b8f1eaf7a0977bb766b017d64a883906115a015b43d03053008`  
		Last Modified: Thu, 06 Jun 2024 09:29:32 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32a98b51870c6275592917587f2d69fe8a2426c65e663d9188db3327754654`  
		Last Modified: Thu, 06 Jun 2024 09:29:33 GMT  
		Size: 24.5 MB (24528085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd688925eae349606b9d9d1efe788a7fcdd4d0cd1fa14cb1cf78aa8f949334a`  
		Last Modified: Thu, 06 Jun 2024 09:29:32 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df46c8fff2457be2818893716d6d9bb6fc388ccb1f6e2fe540c7d49a4e842c2a`  
		Last Modified: Thu, 06 Jun 2024 09:29:33 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:6421dfa17eb8aefbbe0025876819e2b6d2ac1512b2b5f942a983e30ee544a63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8045434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eac2bf40b671990e6fc6abdce306aea3b335e29a386e17a8518ab0d6e5bc378`

```dockerfile
```

-	Layers:
	-	`sha256:e9b69598ec219705ea7cf3bf5dbefeae6d3d867261fa1d37d242dcad551583ff`  
		Last Modified: Thu, 06 Jun 2024 09:29:31 GMT  
		Size: 8.0 MB (7985493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cef0fecb2767cf82be63363d3eddbfbeadfed8d15c46d8754bbd64535a43d09`  
		Last Modified: Thu, 06 Jun 2024 09:29:31 GMT  
		Size: 59.9 KB (59941 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:7451f49b98a165e84717687306c36a55e5aa85cadabcfddd4fd7e5998d807096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239875754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a6acb4bfac8b5a43b010c51abd8026915177dfad4210aa72d2c72bbb5267f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae88c065305a602f05cd639106fec77ad90518828f24868e72e94f2b868a91db`  
		Last Modified: Thu, 30 May 2024 00:11:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38dc35f57533fe117dfe52d1ac36d9db0f5f48559d72644ab74f02e59872070`  
		Last Modified: Thu, 30 May 2024 00:11:48 GMT  
		Size: 101.5 MB (101522125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182dff1affda7ce47a96f6302ef714a6841c43a7a7cf068f253b6d813864f135`  
		Last Modified: Thu, 30 May 2024 00:11:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad21572ec7bf2d83908901c9ce4c8108dd6dd246c8e42f2945798c30a4d886b3`  
		Last Modified: Thu, 30 May 2024 00:12:21 GMT  
		Size: 20.8 MB (20844671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c763612fd821600a7f3952d29d7a19ee189d1649ab897c061ed895c9be082d0`  
		Last Modified: Thu, 30 May 2024 00:12:15 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e616ae3bf0703a783c551b7e011d0a16c7666823ce2c35591953fe3947e5ea7`  
		Last Modified: Thu, 30 May 2024 00:12:15 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c9dbc5af4ded235d88a733f07f6d0edd9aff4eafc1945fcc36ab7730ecb71`  
		Last Modified: Thu, 06 Jun 2024 06:32:51 GMT  
		Size: 12.8 MB (12789587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd6422933a4d61e566907ed280b856c875580b545d0a0f340bb3c2132b915cb`  
		Last Modified: Thu, 06 Jun 2024 06:32:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfcf9376dbb7f4bcbe35a70562691f09b0ebbf0da2a6842815436bfec72907`  
		Last Modified: Thu, 06 Jun 2024 06:32:52 GMT  
		Size: 11.9 MB (11864254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c43df960752428d94fcd0f366ee42f68a527819502dbe298fd6f054763a7a8`  
		Last Modified: Thu, 06 Jun 2024 06:32:48 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd124a8a25e462356972d39c51bf2af857b939211f2b9c48a2e9eeee4e5b071`  
		Last Modified: Thu, 06 Jun 2024 06:32:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b974c65d5cfe629de3bd538d0f18869e7aafaf86cb5469062a5a3f6789e8d0`  
		Last Modified: Thu, 06 Jun 2024 06:32:48 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487f0ceb4e424f951d181d55f126e94ccc69b978487ad796d68585092eb1d900`  
		Last Modified: Thu, 06 Jun 2024 08:02:02 GMT  
		Size: 26.7 MB (26702917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4161a6732464c6f97f14c067c387faf02a3acbc28a7c9ada0104ebe24ba7fde1`  
		Last Modified: Thu, 06 Jun 2024 08:02:01 GMT  
		Size: 11.4 MB (11432023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b2ac31e632d37f8f5fef2d105c3c1552bd72cb232ba0c85e2ace70a7dad893`  
		Last Modified: Thu, 06 Jun 2024 08:02:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4172eb489d069399645277fdc7f48bff485d8ccac392699ecf57a41605e1254`  
		Last Modified: Thu, 06 Jun 2024 08:02:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdcce6528d3405e62d64def221cc717e0e95d78a911cc5600e70bc564bd816e`  
		Last Modified: Thu, 06 Jun 2024 08:02:02 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168eba4d67a3d1e82e0a4ad52515244a843d3a9b185216669d73103f00b2db45`  
		Last Modified: Thu, 06 Jun 2024 08:02:03 GMT  
		Size: 24.5 MB (24528080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7983b0db4f90f7b88337bc3e129a8fc639817cde3058e2af8d9157e18448db`  
		Last Modified: Thu, 06 Jun 2024 08:02:02 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3a3b583068db8d9f18e784af38013cce563ba2818bf43f0af2b24edd2da94a`  
		Last Modified: Thu, 06 Jun 2024 08:02:03 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:b5f3d55743d372bb1a11c53d5a863e10cd5aca718518ddee60761f01ac077290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7996388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06246c133ba58a600a89575a7bfbba01c952ff97459ba8986cf6a87f2bc4f45b`

```dockerfile
```

-	Layers:
	-	`sha256:dcfbc1048513997f7008bdbcfe8d1b3b778dccaede1e4fa9a250046d79916b8b`  
		Last Modified: Thu, 06 Jun 2024 08:02:01 GMT  
		Size: 7.9 MB (7936841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9bf5b6c82316ef73eebc2ad0125b8dc5ffc0d62e1b0a081a04897a269f1bb05`  
		Last Modified: Thu, 06 Jun 2024 08:02:00 GMT  
		Size: 59.5 KB (59547 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:089158a33c7e316a0ecb2c4bfd35072ca697099e8beeeabe9e5317486ff03c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213022882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f29747a993e3fefc49f10d29b118eeb4a87f3eea988903a5a94a433c47db983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2e1c698171a97617ed0fd85993b1c4fbfb0c77e43dc91441d64f571cd45fb0`  
		Last Modified: Thu, 30 May 2024 00:25:38 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b3ea3309903857564f87a2748d9f8332469a1129a83cde0ac7a2cd108b3ae9`  
		Last Modified: Thu, 30 May 2024 00:26:37 GMT  
		Size: 80.5 MB (80475201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8673e122189a654ce946d41d5d58cdf9d0c1bf699e30b6e9b0d0162169f84b`  
		Last Modified: Thu, 30 May 2024 00:25:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc809c826b43228c86d396ad8ad5b9ec5424e91ba1174f54debe1599ea9ee22`  
		Last Modified: Thu, 30 May 2024 00:27:23 GMT  
		Size: 20.1 MB (20064271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d1c6d59c55f8793e0e772f71962ab816d08c0300c1f6d04fc908d27d9e7a0`  
		Last Modified: Thu, 30 May 2024 00:27:10 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af1543d07c15c36e0d49a31f64ab30ea5b0a33269623e48f1adbeea3ed0c310`  
		Last Modified: Thu, 30 May 2024 00:27:10 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc99eff8702856926a02f3520408344788f2acb5a6783be10036307c604798b`  
		Last Modified: Thu, 06 Jun 2024 09:26:55 GMT  
		Size: 12.6 MB (12582243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33c86abc7501298df3f7ff47b06cabeefb9ce10681bc14460e56c4807fc54e`  
		Last Modified: Thu, 06 Jun 2024 09:26:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c21805665f1c5020285de9a6dddb4bc89d76c9bc3ea0a398f93733d64e5577e`  
		Last Modified: Thu, 06 Jun 2024 09:26:59 GMT  
		Size: 10.7 MB (10709503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796b9908d540d4e40c33e4ff6ceb3bfc22067cd2e107354ddff2f792b1f77e72`  
		Last Modified: Thu, 06 Jun 2024 09:26:49 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b13afe02d77e2192edefd03540258847373207ba27b0fb8cd9a3afb28cad72`  
		Last Modified: Thu, 06 Jun 2024 09:26:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338b726a86a2a4698587e8a0035709fc61e5612c813074fc500610f188ff5873`  
		Last Modified: Thu, 06 Jun 2024 09:26:49 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb765868925e3bedd7053d2e1ea5c3060ae7e0dd7ece8e949dea56f6f91ba95`  
		Last Modified: Thu, 06 Jun 2024 17:54:15 GMT  
		Size: 26.0 MB (26021437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6013e3a85f0a63239de9f673030af54726eaf93cd9d051d5425947385f722d4`  
		Last Modified: Thu, 06 Jun 2024 17:54:14 GMT  
		Size: 9.5 MB (9468949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b142b8e88e70ee0ac4492041abe1c4b09113d3c1a7d72d17fcf560599d818`  
		Last Modified: Thu, 06 Jun 2024 17:54:12 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f197360ea15e63ac702fd240eccefc02ffb461f46f03d9b7cdde6031895e809`  
		Last Modified: Thu, 06 Jun 2024 17:54:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6f4050ddcae817466111159fb4373422f2e3c447ab91b274ec76e53d95a21c`  
		Last Modified: Thu, 06 Jun 2024 17:54:14 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6937d60ce7a406e236b97d8a10ff1441e943fcd991389fc8085da2326bfe666`  
		Last Modified: Thu, 06 Jun 2024 17:54:17 GMT  
		Size: 24.5 MB (24528088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894a2a432ae5c5d172e257710bf9c902afa93f25ed08de25cf25449bdcc4804b`  
		Last Modified: Thu, 06 Jun 2024 17:54:15 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12bf857e7f5f17a130a90c5f14173bdf23022ae9ba4c68688da0bc8318f3888`  
		Last Modified: Thu, 06 Jun 2024 17:54:15 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:172c998c832aeba2536d12d620f2e0c4c392823c1485383248bcee211f8377a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 KB (59479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a899b0a03b026601fa4e78757bbd8b780867675e8bb526d3c42cc727655efa`

```dockerfile
```

-	Layers:
	-	`sha256:964509318fca3631e9b2a2c7b9802aadcd7cc9471d53d6185cadb8a1ff2ae1e9`  
		Last Modified: Thu, 06 Jun 2024 17:54:09 GMT  
		Size: 59.5 KB (59479 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:b60fad889d7146e66ba829ef241147fbb2ecf4c679b8fa5ade58f92edbb3fc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245977637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3151d438ea0ac52a6d15553d6050eb1afb901a58ce373fcbb3e006d569f37e60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da3e260369cebf4c4f8ff3a322a8189ac84c811c2f0730eaf0e889033b35193`  
		Last Modified: Wed, 29 May 2024 23:47:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0b39fd81bebe81729ed8bac9fef9066c71d11a146b0ad366372e4e50686280`  
		Last Modified: Wed, 29 May 2024 23:47:54 GMT  
		Size: 103.3 MB (103316970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49947ee01e2a48415fc10d7c62c69ef77995b6b859d8014feffcbcdb074b7ef4`  
		Last Modified: Wed, 29 May 2024 23:47:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec2faaf21a842044a8d6e4301b734258ecb3a523d8748755faf087658b3d621`  
		Last Modified: Wed, 29 May 2024 23:48:27 GMT  
		Size: 21.5 MB (21512810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d65db55eb143ce0f149568f61c15912dc0f69df7af638be67560dc9082f473`  
		Last Modified: Wed, 29 May 2024 23:48:22 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe70f18edcf83d47326432ec689384b527abc011bc877d447b85d2e5fa0c1f4`  
		Last Modified: Wed, 29 May 2024 23:48:22 GMT  
		Size: 516.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb91090efa1e7b2957bc3dff011097c935ff3dbabfadc8f32cc3ccafeced9c2`  
		Last Modified: Thu, 06 Jun 2024 03:10:41 GMT  
		Size: 12.8 MB (12789820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df55626997522062cf484edaf50f4cc12618b774e84d1e03b730328e94eac8ff`  
		Last Modified: Thu, 06 Jun 2024 03:10:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381d3a776058b0847285b8dd938221403fd0c3fcbdba533ac20f845c5c057c0d`  
		Last Modified: Thu, 06 Jun 2024 03:10:41 GMT  
		Size: 12.1 MB (12054477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e16da7fddb826b196c3ba6b8fcb875dddb7878d607d63a3b7c75ac2c3403437`  
		Last Modified: Thu, 06 Jun 2024 03:10:38 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7813930895efd876baa2e9b518080b15a535038741c4e41c77124eada0c2cdd8`  
		Last Modified: Thu, 06 Jun 2024 03:10:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2698f653d975fe6ed72f40dad256cd81e301da9b5543f2ddf3def55427896784`  
		Last Modified: Thu, 06 Jun 2024 03:10:38 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb9697e91cc9f7a9fbfe707ca7b2bc5a4640e82b54aaf55a0bb5207b7ec90bd`  
		Last Modified: Thu, 06 Jun 2024 08:47:23 GMT  
		Size: 27.3 MB (27346945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15dd45b92b9720120ec3b471dfc389708f2e8814f9467503cdc4cf92c1dbc32`  
		Last Modified: Thu, 06 Jun 2024 08:47:23 GMT  
		Size: 11.3 MB (11257802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737cd00ffd1c817de68a4bc513c11ecec54128b9edc381c35230f9f849b94d1`  
		Last Modified: Thu, 06 Jun 2024 08:47:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015a68df73d0765afb74768581526a6b5e99aa20d18c2c41e001222643fa48e0`  
		Last Modified: Thu, 06 Jun 2024 08:47:22 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b526a4d9421122a24a35751d775eff0cda6324731ec0ce9acd399497506323`  
		Last Modified: Thu, 06 Jun 2024 08:47:23 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361e1daa554c4c1d1249dcbbfdd83d59478d87c56b0943c9dad2264244a44f49`  
		Last Modified: Thu, 06 Jun 2024 08:47:24 GMT  
		Size: 24.5 MB (24528080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f43b1c4b785e359a0df6d919c91cd1b49edc017e02c55fd7f57ba6b85a987`  
		Last Modified: Thu, 06 Jun 2024 08:47:24 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e572ad69869600a69d49b737b5d079de2b36056d83c46593ecff7eaaeb854b2`  
		Last Modified: Thu, 06 Jun 2024 08:47:24 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:346ff77749f714c0511c55332f93cdb243b4708b61b5838eb53857b92e26ffa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7995226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd633cd2e997757e0932bfc07026519d28345e8a969ffb4cbdd4d160585427ef`

```dockerfile
```

-	Layers:
	-	`sha256:b2f83dafcb594b6d40bf8d5272764120fc4e4bbf32ee5b4691c443d6093749c4`  
		Last Modified: Thu, 06 Jun 2024 08:47:22 GMT  
		Size: 7.9 MB (7935548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8856ee35da55cdb01ddb5584a21ba139382b6ff0cd0c5fc86b030b6066f243`  
		Last Modified: Thu, 06 Jun 2024 08:47:22 GMT  
		Size: 59.7 KB (59678 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:0e6546d3c92082d213001452cd0534d17ea733501ad003e7c1e9026815bdd57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212006571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb2c90e989d6eb10f677ec86ec0a26d401c80059690e675d867fbf31a3d1db1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 07 May 2024 19:09:31 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 07 May 2024 19:09:31 GMT
CMD ["bash"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 May 2024 19:09:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 07 May 2024 19:09:31 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 May 2024 19:09:31 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_VERSION=8.3.7
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.7.tar.xz.asc
# Tue, 07 May 2024 19:09:31 GMT
ENV PHP_SHA256=d53433c1ca6b2c8741afa7c524272e6806c1e895e5912a058494fea89988570a
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 07 May 2024 19:09:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 07 May 2024 19:09:31 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
RUN docker-php-ext-enable sodium
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 May 2024 19:09:31 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 May 2024 19:09:31 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 07 May 2024 19:09:31 GMT
WORKDIR /var/www/html
# Tue, 07 May 2024 19:09:31 GMT
EXPOSE 80
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 May 2024 19:09:31 GMT
RUN set -eux; 	version='6.5.3'; 	sha1='8e4950d39990a2c200a7745d44d32b176baa5ac5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 May 2024 19:09:31 GMT
VOLUME [/var/www/html]
# Tue, 07 May 2024 19:09:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 19:09:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c7c5236d1c8356fc773b8cce2bf09dec8f54b44c3223f36d6d3e7bf823d87`  
		Last Modified: Wed, 29 May 2024 22:42:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b095dac692581d3ab7d8d35382ada1f35fc014fb3b708c2c5a0228b973e596`  
		Last Modified: Wed, 29 May 2024 22:42:34 GMT  
		Size: 80.8 MB (80814039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781911421736c891768da7f2a43ef63663f6978a1e21555583dd6d6a8d630912`  
		Last Modified: Wed, 29 May 2024 22:42:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f84b1c9ba60018b057e6e9e5740924f9f5c94430bb82f53c4eca0d8a89ec31`  
		Last Modified: Wed, 29 May 2024 22:42:54 GMT  
		Size: 20.1 MB (20103096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d2b02ccc810f3339cc769a486bad144f61ece7cc63225721c8fac6410032f6`  
		Last Modified: Wed, 29 May 2024 22:42:51 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a612a68842b3a372d4b3680878a17c293c13430d7268f0043ce37d765edf851`  
		Last Modified: Wed, 29 May 2024 22:42:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f384838f20c054e513e795db2785ab13052b989a569686ae69575d50e3350cb`  
		Last Modified: Thu, 06 Jun 2024 03:32:48 GMT  
		Size: 12.8 MB (12788866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17be4e857900232269539d08eb068b93c291efb5b91bad148439f4e3fd88cdbd`  
		Last Modified: Thu, 06 Jun 2024 03:32:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8843000ef87cceb95ce8ec70037ee99b8aae7887af65ecf5b63eacd30f280570`  
		Last Modified: Thu, 06 Jun 2024 03:32:49 GMT  
		Size: 10.9 MB (10855471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d514526773c612a8556389847c88175c05dfd30893236de5c10ad711cb4e5e0`  
		Last Modified: Thu, 06 Jun 2024 03:32:45 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3429f5b5e8dd15a0c0ac1dd74b1b6d4b2e033ce70f5131d478d490bcff710ce3`  
		Last Modified: Thu, 06 Jun 2024 03:32:45 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7556058637bda4fd3c949e5e7714fdcac8e48cba2abe5add5fc562f15b1d11d2`  
		Last Modified: Thu, 06 Jun 2024 03:32:45 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e330ff2c410c02fa16345d8c673857e5238c19dda6d7c27b8ef694c0feb201ff`  
		Last Modified: Thu, 06 Jun 2024 06:53:29 GMT  
		Size: 25.9 MB (25900952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8f0af7fd08cce19322935f6e3fead5e195350fc95757568d614ba9468884a`  
		Last Modified: Thu, 06 Jun 2024 06:53:29 GMT  
		Size: 9.5 MB (9474110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977a5b429a1c33375d8e79008dc770f1ca99c5e2daa3a2f4892716c78906baa6`  
		Last Modified: Thu, 06 Jun 2024 06:53:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856adfc29cd9e27eb4b1a9e4ea1a37beb5d0b758e610ba93f3afb900908ee184`  
		Last Modified: Thu, 06 Jun 2024 06:53:29 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d802144982fbd2b61c1366fe7b62f5c266eecdc7637bc681a0e993ae1171f69`  
		Last Modified: Thu, 06 Jun 2024 06:53:30 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87520aaaa4e0a60b830198e676c4ab808fd9221d399e88a42ef403fb99bfa45`  
		Last Modified: Thu, 06 Jun 2024 06:53:30 GMT  
		Size: 24.5 MB (24528089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e7135d15bf64f89ce3a9d9fd892a91f2e379df98ccfbfc873826ad85fb1cc1`  
		Last Modified: Thu, 06 Jun 2024 06:53:30 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bae7564fbf08c6e404a9b54b6558fcff5c51d38110c4ed9c518ea77957de7`  
		Last Modified: Thu, 06 Jun 2024 06:53:30 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:f5b1f18af88041f0c23479fddc15ae0ebbed68f7d810ba3b593b0f101a3185a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7848237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c5c33d626756765107bcca36101cafe04a24467dac8cf49ef397f486466e23`

```dockerfile
```

-	Layers:
	-	`sha256:22d3b300d165124af515957e10a6b068270a378f09b47b7986854d6389f5a9c5`  
		Last Modified: Thu, 06 Jun 2024 06:53:28 GMT  
		Size: 7.8 MB (7788647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a2c8040d9ea436a5bb777eeed03ca335c6f6db148a87e8b46adf338577e3f5`  
		Last Modified: Thu, 06 Jun 2024 06:53:28 GMT  
		Size: 59.6 KB (59590 bytes)  
		MIME: application/vnd.in-toto+json
