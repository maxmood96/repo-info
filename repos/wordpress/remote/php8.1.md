## `wordpress:php8.1`

```console
$ docker pull wordpress@sha256:98e2135bcf134cedd59660a2a32fdbbba584c134244e58ce4eb0df0afda9c6db
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

### `wordpress:php8.1` - linux; amd64

```console
$ docker pull wordpress@sha256:5b687da30ad59f14dc658926ca152f666d8a5ab57c72a1ac7e443578f66bc4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240190309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4381e57b281b8c11e3704b14534fe2cac612abcf007b0b6f28bcb4908ed8a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:39:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 06:39:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 06:39:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:39:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 06:39:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 06:43:10 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 06:43:10 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 06:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 06:43:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 06:43:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 06:43:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 06:43:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 06:43:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 09:08:43 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 23 Jul 2024 09:08:43 GMT
ENV PHP_VERSION=8.1.29
# Tue, 23 Jul 2024 09:08:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 23 Jul 2024 09:08:43 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 23 Jul 2024 09:08:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 09:08:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 09:12:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 09:12:27 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 09:12:27 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 09:12:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 09:12:28 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 09:12:28 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 09:12:28 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 09:12:28 GMT
EXPOSE 80
# Tue, 23 Jul 2024 09:12:28 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	version='6.6.1'; 	sha1='cd5544c85824e3cd8105018c63ccdba31883d881'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 19:30:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 19:30:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a83fa76a2b6c79f2ceb6a3ac1d705844e9f1b13544b372353738d852317d8a`  
		Last Modified: Tue, 23 Jul 2024 09:35:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3cd9e6b429af5419fe7f9a9d1ebd1b80eec307fb1eb50d85e9ce901775300`  
		Last Modified: Tue, 23 Jul 2024 09:35:51 GMT  
		Size: 104.3 MB (104349191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41714dd6e6a02a12b553a69607d296b4acfe06ebfd34170e47f89ce43f2fd09`  
		Last Modified: Tue, 23 Jul 2024 09:35:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e362d14d0b88a76a0df065fd31bfc25b16f4f2afc88ecb30273c08bd21d1ab60`  
		Last Modified: Tue, 23 Jul 2024 09:36:16 GMT  
		Size: 20.3 MB (20327898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b475c73fa4cd4c57941308b5448392792620bdb6654ebde07c1856ea462830`  
		Last Modified: Tue, 23 Jul 2024 09:36:12 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1c872d3db8284d29f89158d5ecb0ff14ebbc08e78834d499468496a1232bd9`  
		Last Modified: Tue, 23 Jul 2024 09:36:12 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779aa4c257b37678504b4b45883431bcb72c96c581602376ac5cb54b96bdd763`  
		Last Modified: Tue, 23 Jul 2024 09:48:28 GMT  
		Size: 12.2 MB (12159375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3ef6f77923fa8abe1781df9028c8562854fd897e0f31d27a44613ecfb847ec`  
		Last Modified: Tue, 23 Jul 2024 09:48:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c7ac1aa6e2247bf6ac2e6cb8ae6d3adf514082075c7bfa21e37685da7d8c16`  
		Last Modified: Tue, 23 Jul 2024 09:48:27 GMT  
		Size: 11.2 MB (11155840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acfa523b99da95ea5fdbc701fcf32e7bb7df0abf096c63c67fad4db97b5ac96`  
		Last Modified: Tue, 23 Jul 2024 09:48:25 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eca0a80d1a5344c54a8ca12f4adf72e00bf5d8ea0f649f67b495b2e166263e9`  
		Last Modified: Tue, 23 Jul 2024 09:48:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfbfa103fe53d07038fd5ba6606292a29930ea456fd9765ab652b6b1a226cb1`  
		Last Modified: Tue, 23 Jul 2024 09:48:25 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787709266f750255a2db83edb7044f852dc90fd56448304a91fe71d45eddeda3`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 26.3 MB (26254215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b464d6cf2726c2a09e77d9a11d712b9755a9b7befa1d14b8432bab52f5d6b491`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 12.3 MB (12325763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbcd3bfa4626c0140cbf5e2ff3ab0cbe440019e7c3c134ee8eb88300540b4cc`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5244814b6eedb6f1614c04649ae129f65ad4beef6349bc9c094cb47ec4b707`  
		Last Modified: Wed, 24 Jul 2024 01:10:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37dc0a17168b1b4b9f4f6927d596a42c601207afa11e5cd72d0b598b106683`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807db851ce8321dff377c300acdd6abe30971868a9691bc59f2b17ce047e2ca1`  
		Last Modified: Wed, 24 Jul 2024 01:10:19 GMT  
		Size: 24.5 MB (24462286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e5d0c18fb826cb14641bef2bd8609b5659d7b1cdba3c9c143e51e3d66d158a`  
		Last Modified: Wed, 24 Jul 2024 01:10:19 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1162198e279ef72417441d11f482542636c5ea27f2d1adf5a5549c96a356ad25`  
		Last Modified: Wed, 24 Jul 2024 01:10:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:f77693044f162a737ce9b668d7b2ff6b8cd880af9f6d3e064c9c9dff95f29bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8067147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42dd47d50f436bccef95894ba935e9660c741f02ff44b74b5b3ecf30e4b6de0d`

```dockerfile
```

-	Layers:
	-	`sha256:ba538c6d3cca369825cb30901945cdee3f45cec2f071972b5872e3f624991dd3`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 8.0 MB (8007523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4f101cfab21fe32b3c4ff7108644163259e66bbf22eb9716ed0540aa4facd9`  
		Last Modified: Wed, 24 Jul 2024 01:10:17 GMT  
		Size: 59.6 KB (59624 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:7a4b60c02f90749926b6e798c8bb7de3d824d78b2abbd046aa39a581ca0e976c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210881006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a03000e7b38e49609c9823e241e5f996d905e1e37298d4516194107b3ffa64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:01 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Mon, 22 Jul 2024 23:57:01 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:27:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 00:27:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 00:27:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:27:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 00:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 00:33:03 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 00:33:04 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 00:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 00:33:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 00:33:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 00:33:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 00:33:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 00:33:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 02:49:31 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 23 Jul 2024 02:49:31 GMT
ENV PHP_VERSION=8.1.29
# Tue, 23 Jul 2024 02:49:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 23 Jul 2024 02:49:31 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 23 Jul 2024 02:49:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 02:49:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:52:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 02:52:41 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:52:41 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 02:52:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 02:52:42 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 02:52:42 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:52:42 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:52:42 GMT
EXPOSE 80
# Tue, 23 Jul 2024 02:52:42 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	version='6.6.1'; 	sha1='cd5544c85824e3cd8105018c63ccdba31883d881'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 19:30:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 19:30:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1060bd7a17f68edf46abfd7f2bbe196a13150748c143722804f62e6decb61a4`  
		Last Modified: Tue, 23 Jul 2024 03:19:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abab82a130067dcceb069a9535c56733df616e1c839b216cd8148a9b312c91e9`  
		Last Modified: Tue, 23 Jul 2024 03:20:22 GMT  
		Size: 82.0 MB (81997235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e53f141e71951b20be7495d56543c4bfd6d8429bca31b80d3401fee7f306b3`  
		Last Modified: Tue, 23 Jul 2024 03:19:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c60a3731902b294c49dd82a016f333a1ed13a06bb5d76e6cfd1c61bec0eef6e`  
		Last Modified: Tue, 23 Jul 2024 03:20:52 GMT  
		Size: 19.6 MB (19627696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd6afb49323fe743b6982ce9411e316d8907dff9f77b5cef2f2c4a1492f9e8b`  
		Last Modified: Tue, 23 Jul 2024 03:20:46 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffeadfa956a312fbd3125874d59e26df75ae32e29f973101bfa17f48c84c886`  
		Last Modified: Tue, 23 Jul 2024 03:20:46 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645e64502db15dbe6ba62a5eb8047389d3f12d32931c2a5b5ffda778dc2f651f`  
		Last Modified: Tue, 23 Jul 2024 03:34:53 GMT  
		Size: 12.2 MB (12157580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92adcd38e31adaa6e3157f9d078638fefd39ab19ef091c90909f0c4a51808a45`  
		Last Modified: Tue, 23 Jul 2024 03:34:50 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6411a50cd7667abd16e25993bb2ec4237f54068957dbcee2eb986c10e5dc076`  
		Last Modified: Tue, 23 Jul 2024 03:34:54 GMT  
		Size: 10.1 MB (10119227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e92f9cb23e03a8e89ea7cc7ac5b84c9a816d8543f21fdfa3a10ee5a96444aa`  
		Last Modified: Tue, 23 Jul 2024 03:34:50 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d305e808562415aa52eeaf47f707b279579d359f1624e4331a4b04422612114`  
		Last Modified: Tue, 23 Jul 2024 03:34:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6176f8aefb9dd8cc98a2f158aaf77f516945d19831f6f8ed79c96175a72a4`  
		Last Modified: Tue, 23 Jul 2024 03:34:50 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c38823f89161bb47006c10f5dd7dff3b850c142e0eeea9d93fd66276bb6e368`  
		Last Modified: Wed, 24 Jul 2024 02:52:06 GMT  
		Size: 25.7 MB (25705523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24661278e5fa897fb9223c657668f9ba897c3b22a86df083412388806e8041e4`  
		Last Modified: Wed, 24 Jul 2024 02:52:06 GMT  
		Size: 9.9 MB (9894697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435547d3f8e96b23ea6d8e517dd7433394cf17a378b5c7b5814b2fc9845d8a5`  
		Last Modified: Wed, 24 Jul 2024 02:52:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff741acecdbcee2c8d8492ed8c8a45e6db3441d4c63d6c6cd8489db678f7327f`  
		Last Modified: Wed, 24 Jul 2024 02:52:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f607a8627d8439b8d98b3f86b523f8bdb9f2e82875532894501f322f07759`  
		Last Modified: Wed, 24 Jul 2024 02:52:06 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe432737da7537f5ca52f6b2a1c8d9e2a0a1d6b9199b04f0ea22f73391e0b73`  
		Last Modified: Wed, 24 Jul 2024 02:52:07 GMT  
		Size: 24.5 MB (24462295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1abb2e26e016fc5ee5432fde74ad8fdec228e69d071dcc503c11732a7e0324`  
		Last Modified: Wed, 24 Jul 2024 02:52:07 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2db4e197a5d8511ee6b609c9bb2bef1a37a2bfbdd9ee982a886d324f9194b65`  
		Last Modified: Wed, 24 Jul 2024 02:52:07 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:3a0618966887b34dabb8175b76da4f99fddfa16a959128b93b60ba83ecdc24bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7873853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634a4beaa04607d1243ff1e347de69a3d73766f7ab97c8f2f955fe7bf2e987ca`

```dockerfile
```

-	Layers:
	-	`sha256:3777c1db8085ca5e4de519ecd261048de9a58d9dc7ddcaf8c386051f78c68beb`  
		Last Modified: Wed, 24 Jul 2024 02:52:05 GMT  
		Size: 7.8 MB (7814078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1bf48c1b94efcf23f022e568f1b204d79a3f45b269aa9bf177990f2b490cbf`  
		Last Modified: Wed, 24 Jul 2024 02:52:05 GMT  
		Size: 59.8 KB (59775 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:5ebec91df6a603e57e680f1e9207017509349d9ce05c57130d67860814e76ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200177905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7510b425628c719e94cf147171371ed33abc25a96c151d08363b5fa6888da6b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:47:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:47:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:47:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:51:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:51:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:51:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:51:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:51:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:51:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:51:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:36:40 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 03:36:40 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 03:36:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 03:36:41 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 03:36:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 03:36:52 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:40:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:40:22 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:40:22 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:40:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:40:22 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 03:40:23 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:40:23 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:40:23 GMT
EXPOSE 80
# Tue, 02 Jul 2024 03:40:23 GMT
CMD ["apache2-foreground"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98f2ea35903ab22a64a0b9429586e5ebf253d8f30160f658c9a3e91506b6b4f`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed99c1553b06b60dc38f501a723427469be3c7f305f660c2d3f5c4826636db6`  
		Last Modified: Tue, 02 Jul 2024 03:57:17 GMT  
		Size: 76.2 MB (76166316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ff1c809dc06de95648d78a0490826dc9afc53a05c01d001be86b39ec6903ec`  
		Last Modified: Tue, 02 Jul 2024 03:57:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751f0125442586c37682f7ec34b710b4ab71ddc530c91fea2cf2af4901d2a1a4`  
		Last Modified: Tue, 02 Jul 2024 03:57:42 GMT  
		Size: 19.1 MB (19057874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016198828fa6032df9c10ec2e792db92c6a8b19d35a884387328ccb4cb68f19d`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b6f3e158190277e0f0f214b0dc62c26057875ebd2af19ac0a15534c73fb171`  
		Last Modified: Tue, 02 Jul 2024 03:57:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241fb23956f41c1b50b8da5066b8b85ca168f375a16e41c3b8bbd0655cd24f`  
		Last Modified: Tue, 02 Jul 2024 04:08:09 GMT  
		Size: 12.2 MB (12157445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbacdba65a0e937119e6b202eab59efa28e91f73997e2c4f57c91b7e7612369`  
		Last Modified: Tue, 02 Jul 2024 04:08:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff84e9127824cd2d406328d3d1a441669e51e7089549fed924511838a704d09f`  
		Last Modified: Tue, 02 Jul 2024 04:08:09 GMT  
		Size: 9.6 MB (9583279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32e853376894a081a938f581380b88685bbb96366a9a30240ca69f0e854d9f8`  
		Last Modified: Tue, 02 Jul 2024 04:08:06 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c52c89510dfdee86f3a2d6d1ed0376d6ef21e1b620781dc15d21a30c5d0a2f9`  
		Last Modified: Tue, 02 Jul 2024 04:08:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2778b980224191e43011ccccf5283b27c2e0aec9d0ebd3e111846a9c9caecf3`  
		Last Modified: Tue, 02 Jul 2024 04:08:06 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edd799945301264fe2ac3837eb2c1187021b5887dd494ae7c77eb3a5493dcb`  
		Last Modified: Mon, 15 Jul 2024 21:58:23 GMT  
		Size: 25.1 MB (25076696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d971516f5c959bde19f4d0a19238e37cc21b75787da6086685adc27ecaf3b`  
		Last Modified: Mon, 15 Jul 2024 21:58:22 GMT  
		Size: 8.9 MB (8928480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1118266dd3dca9805f951b23caa1f7e221c1793dac32349b99fa136a87b86112`  
		Last Modified: Mon, 15 Jul 2024 21:58:21 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81066da4075035dab1266c05b776214d3cf9ab5e5325c0fed3a08a8ee32f5906`  
		Last Modified: Mon, 15 Jul 2024 21:58:22 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8e5634b32b232c8b8034da1eae2871ea45ecc8555c8ff4bd503dc933e93f58`  
		Last Modified: Mon, 15 Jul 2024 21:58:22 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03abd0b4ed58f561bdf840039f7be219fab5b00c45cb321428b4b45313b7337`  
		Last Modified: Tue, 16 Jul 2024 22:57:29 GMT  
		Size: 24.5 MB (24460189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867f466d15864063946bfc25f1f53bb59a4506c392062022614ddc59ee668ded`  
		Last Modified: Tue, 16 Jul 2024 22:57:28 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b581dd1d23e516cfeafd31f7f1d33bced16c9b501e1eac8429eb866146f5ad`  
		Last Modified: Tue, 16 Jul 2024 22:57:28 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:6908f318eb3891c7f6f5d49f925c3fd9f85063511e21a09a6b163b7f28a810d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7877283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3323f01f05345283f44279c5144f9712ca025e42201d77d03ba3d2b12f99dfd6`

```dockerfile
```

-	Layers:
	-	`sha256:154aaed1e78ff28a47a496c1415633548109c388fa81a61bdfef3b837160720e`  
		Last Modified: Tue, 16 Jul 2024 22:57:28 GMT  
		Size: 7.8 MB (7817524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5000ab7d99fe1226d3867c50f0b93dbbdcfbefbba98a7a7a78e77bb5ccf49826`  
		Last Modified: Tue, 16 Jul 2024 22:57:28 GMT  
		Size: 59.8 KB (59759 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:b130edb4a5706bec8bca92dd66f63438385b21e6b404eb0bfdedcf79a0bcd1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231517418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ea932114a3dbf27dd5a8333132344984e5833f6a7ce708c3184aa879f9ab62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:18:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:18:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:18:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:18:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:22:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:22:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:22:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:22:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:22:39 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:11:58 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 03:11:58 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 03:11:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 03:11:58 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 03:12:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 03:12:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:15:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:15:26 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:15:27 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:15:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:15:27 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 03:15:27 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:15:27 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:15:27 GMT
EXPOSE 80
# Tue, 02 Jul 2024 03:15:27 GMT
CMD ["apache2-foreground"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d168c82669385a88cb2d49927f5d97a9fd361459c5ba221ade1b4833b14530`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be59d5943ae49be3e4ff309c07ef79eacf2bf161b53590db30e1227422f98601`  
		Last Modified: Tue, 02 Jul 2024 03:36:42 GMT  
		Size: 98.1 MB (98131121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702846940aedcd56970bc052b4e64fa8ff21b12b0a6ba8ca8273f4e256aaedc2`  
		Last Modified: Tue, 02 Jul 2024 03:36:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8911daeb05e620d4f86e6e1800ae61553a08eaf29667c22d5a6bdae9461cada3`  
		Last Modified: Tue, 02 Jul 2024 03:37:07 GMT  
		Size: 20.3 MB (20321495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4028ee2076616a6cf681ab5e49658e589a2d0b1918e9213d61a41938d6b4299b`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4d03e54d8a1108c589658f102c0afa22f96cd422f05ace79e1ae3b68741d06`  
		Last Modified: Tue, 02 Jul 2024 03:37:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b9a070da02a47673707526440aef1448352f1e012ed17b79bb64afa70ac94`  
		Last Modified: Tue, 02 Jul 2024 03:46:34 GMT  
		Size: 12.2 MB (12159077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492708d94a8289963d3ceb069db03a9cfa10590f50dffdc7a83fc3813f6ab26`  
		Last Modified: Tue, 02 Jul 2024 03:46:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e160070741ec5c5350bedb20cd8681c3ef08f4d413c7420a978a0ccc16efce`  
		Last Modified: Tue, 02 Jul 2024 03:46:31 GMT  
		Size: 11.2 MB (11154531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf6772dda21f8388088f96f92e8ad6f04dbae950d55849618b1242d58fbd89b`  
		Last Modified: Tue, 02 Jul 2024 03:46:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b45d12f31db4938d3f2760139c3dd593466e5e8db8fc91dec48a46226a2fd73`  
		Last Modified: Tue, 02 Jul 2024 03:46:30 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8aa669209bc8e911af067841cdd6ec92c84a7b80cb9173f2eda9f6b18dca4`  
		Last Modified: Tue, 02 Jul 2024 03:46:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604d351ddafc36e75d09ccc790c30d1d62a2dc51b5af8713ec25a3eea359aa22`  
		Last Modified: Wed, 03 Jul 2024 01:23:13 GMT  
		Size: 26.2 MB (26174071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeb5d4d1fbfaaaab61c5b43c1f8b1ac2e600976169cfefcbb73235f40cb194d`  
		Last Modified: Wed, 03 Jul 2024 01:23:12 GMT  
		Size: 9.9 MB (9930916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673800f1c1a6f84888657b43e26e33e30f6af9a99b4e00057ef06617a761d5f0`  
		Last Modified: Wed, 03 Jul 2024 01:23:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a512e982d313d1f5369169350f261a65db5073580978a4fdc2f5869b94135bf6`  
		Last Modified: Wed, 03 Jul 2024 01:23:12 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28c6642b228e19667cb887d3afa35e75d01b3e69ae4231ff67ea9fc6c60c48`  
		Last Modified: Wed, 03 Jul 2024 01:23:13 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd83306601b4fded4ed6672eb0981e838a32178c2bf10e5efad487eeb9a5014`  
		Last Modified: Tue, 16 Jul 2024 22:56:58 GMT  
		Size: 24.5 MB (24460197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b94b94e45d46f7f250bc49d57abed6808a7d6a482e7585838a46e7f6695579`  
		Last Modified: Tue, 16 Jul 2024 22:56:56 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd4cef906b3ac2febcd71ac759515bf9e1ac528a56372ad2890e666014d5169`  
		Last Modified: Tue, 16 Jul 2024 22:56:56 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:63fac75ef4544f19a303bbc675279ad9fc4c2fa0767a2a152c811e51457fc1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8095144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c39b53477c8f1e1d3d2802d8adaa80b77c18313f3e88ad64930ad41848c493`

```dockerfile
```

-	Layers:
	-	`sha256:5cc09f163b85bc8b5d4a7fae23fbac5b52a8a165f39989caf21b4462223f2414`  
		Last Modified: Tue, 16 Jul 2024 22:56:56 GMT  
		Size: 8.0 MB (8035191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f4662fb6ab9c6f2ce2777a0a510df34071b8bcd2da7ede54ae542c6382c6a1`  
		Last Modified: Tue, 16 Jul 2024 22:56:55 GMT  
		Size: 60.0 KB (59953 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; 386

```console
$ docker pull wordpress@sha256:523ccd7184ed694ebb37059809e5c10757ad0e26f9506854b9c6f8bc2da519e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238631669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c03b8a4b78e2ea6c7fe4660d107e81bff1917a622ac547cbdfe897f7e2bcabe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:13 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Tue, 23 Jul 2024 03:54:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:54:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 04:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 04:54:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:54:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 04:54:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 05:01:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 23 Jul 2024 05:01:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 23 Jul 2024 05:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 23 Jul 2024 05:01:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 23 Jul 2024 05:01:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 23 Jul 2024 05:01:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:01:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:01:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 08:58:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 23 Jul 2024 08:58:07 GMT
ENV PHP_VERSION=8.1.29
# Tue, 23 Jul 2024 08:58:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 23 Jul 2024 08:58:07 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 23 Jul 2024 08:58:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 23 Jul 2024 08:58:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 09:04:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 09:04:21 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 23 Jul 2024 09:04:21 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 09:04:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 09:04:22 GMT
STOPSIGNAL SIGWINCH
# Tue, 23 Jul 2024 09:04:22 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 23 Jul 2024 09:04:22 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 09:04:22 GMT
EXPOSE 80
# Tue, 23 Jul 2024 09:04:22 GMT
CMD ["apache2-foreground"]
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	version='6.6.1'; 	sha1='cd5544c85824e3cd8105018c63ccdba31883d881'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 19:30:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 19:30:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34caeeb2ec9b0a871c2808cc5cad03c85e3775d863522099238ac68eda5e4073`  
		Last Modified: Tue, 23 Jul 2024 09:41:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee053233ee4b919aa7cfb9d47b5f6760be8d3ec7f62e66dd4fe9e6c60e99a7`  
		Last Modified: Tue, 23 Jul 2024 09:41:49 GMT  
		Size: 101.5 MB (101517599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbc19e49f8d18ecebf1bf4f346d396cf87df4d75ee7b99b43a0f051717b7a5a`  
		Last Modified: Tue, 23 Jul 2024 09:41:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fda610fbfb0250b0d7e6b2430595f61c3dad96ed4a2536f3469b9de80d5f57`  
		Last Modified: Tue, 23 Jul 2024 09:42:15 GMT  
		Size: 20.8 MB (20843275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa63e9eb0f2b2ad20ff051c8efa62397470384f5c75a9dbd4d774b6028e8647`  
		Last Modified: Tue, 23 Jul 2024 09:42:11 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1608ceaa879e01156cb06283c35d1871d0cb91db35e47cc469b3da6547a360f`  
		Last Modified: Tue, 23 Jul 2024 09:42:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942ca1d24c43afef545568c277d24c6f789ceee6526fda0672e32a03cc65b7d`  
		Last Modified: Tue, 23 Jul 2024 09:55:48 GMT  
		Size: 12.2 MB (12158524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec13151a0007250d23fe810f52031418c82bf717d82b314f34e463b83c3b5b6`  
		Last Modified: Tue, 23 Jul 2024 09:55:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a136a5587eab6f5b0d36280c248fe149fc863039b614dd518e1f9ee19d51fe66`  
		Last Modified: Tue, 23 Jul 2024 09:55:48 GMT  
		Size: 11.4 MB (11379846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df149573beccf7e84f98990297d6b8d73f7fd81d7ddbec3dfbce7eab0f77641b`  
		Last Modified: Tue, 23 Jul 2024 09:55:45 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8df70acd03fd2240e955d5ebcc546da6556cc0b3c97405d2cf6799d86f683`  
		Last Modified: Tue, 23 Jul 2024 09:55:45 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de5a39b25f836b165a472fe6c35dc80c3e3bf59f26fb290d8fb95d953bcd15`  
		Last Modified: Tue, 23 Jul 2024 09:55:45 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4eb68496889fd36e0be5af66e0f7850ebff283902c672f3ca96b25419368bd`  
		Last Modified: Wed, 24 Jul 2024 01:10:42 GMT  
		Size: 26.7 MB (26699019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a63a6287d7595c0a03671fff5c308da319281db1003ddcaab9b084ad6dba9a`  
		Last Modified: Wed, 24 Jul 2024 01:10:42 GMT  
		Size: 11.4 MB (11397333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a61449248678504536f99a4a580475200d11d12f93bb1c616aec31ea07ca668`  
		Last Modified: Wed, 24 Jul 2024 01:10:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58366383a2ce9a282a7105d1b6df5387c1bb202169d42d1d15173312807ed7d`  
		Last Modified: Wed, 24 Jul 2024 01:10:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0191b4a0b91b0e6c3dfbd299dd09f155e83d88975c2babbdcc5efb1972e19d`  
		Last Modified: Wed, 24 Jul 2024 01:10:42 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75607efd8fb8f22e262ba8ce09e00cd26af4f380cc0f47aeba41128799d27fac`  
		Last Modified: Wed, 24 Jul 2024 01:10:43 GMT  
		Size: 24.5 MB (24462309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf64accdee4a5d339240eb2a3396d2636e61ea0e9a676e8431ee49edf409aed0`  
		Last Modified: Wed, 24 Jul 2024 01:10:43 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2ec3b4e3de3348854eb56d6056650ca141bc46dd5d80f3bd3697b445764dbc`  
		Last Modified: Wed, 24 Jul 2024 01:10:43 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:23b1d25d672db10b261ad942629bd586ddf159802e18512bf035564d116ad8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8046928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e07a99e4aa084321cfe85c5f19128f174a0310358436c83cd0bd0ce2d7816ab`

```dockerfile
```

-	Layers:
	-	`sha256:49ca0f1a01bf0f121c87a7db90b60ed1adab228f33a6f3e8fcb81ab0367bd1b7`  
		Last Modified: Wed, 24 Jul 2024 01:10:41 GMT  
		Size: 8.0 MB (7987363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedfef0c03d1edc948755d66bda14bf1c4e052765eb88a1d456ca8c2b60130c9`  
		Last Modified: Wed, 24 Jul 2024 01:10:41 GMT  
		Size: 59.6 KB (59565 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; mips64le

```console
$ docker pull wordpress@sha256:e1d2c5527b3633910ea9c020006e9a0362972961b2b7684a9ce7c5f40fc0ab4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (211988290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a0740e4e255d9956c564df59382b45679f2aec33bd7fa6c21febd7c6f908b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:50:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:50:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:51:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:51:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:52:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 03:08:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 03:08:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 03:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 03:09:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 03:09:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 03:09:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 03:09:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 03:10:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 11:23:03 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 11:23:07 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 11:23:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 11:23:15 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 11:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 11:24:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 11:39:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 11:39:32 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 11:39:39 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 11:39:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 11:39:47 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 11:39:50 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 11:39:54 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 11:39:58 GMT
EXPOSE 80
# Tue, 02 Jul 2024 11:40:02 GMT
CMD ["apache2-foreground"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed1759dfe41616d659c655029aa5ffee7bc0290fb805344c61d4dd8cc88b56a`  
		Last Modified: Tue, 02 Jul 2024 13:09:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87668ea9f028c1aacf9791f378385bcca4ded07f95e24bea21503a68256c3f79`  
		Last Modified: Tue, 02 Jul 2024 13:10:47 GMT  
		Size: 80.7 MB (80666850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d27f245c61c8b7bad564b06537ec3270b260a1eff129f351336ba7b4ae60b7`  
		Last Modified: Tue, 02 Jul 2024 13:09:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4bd5a82f654c3c60e4b9be2169929baa34b7e44ec8427d9bbaa2d0bb08f199`  
		Last Modified: Tue, 02 Jul 2024 13:11:28 GMT  
		Size: 20.1 MB (20064227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1d530f02878d48a195006e6da16b4131ebc447f824f93d0069f3ceb352f9df`  
		Last Modified: Tue, 02 Jul 2024 13:11:14 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878865a8e5b6fe65287574e259b5e3601bef496c8350af41f65b7d4d365b3cc5`  
		Last Modified: Tue, 02 Jul 2024 13:11:14 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dae9bdd14037e5e8b143d0dac0f12fb7760099484c028bf92a61f5d4013514`  
		Last Modified: Tue, 02 Jul 2024 13:30:13 GMT  
		Size: 12.0 MB (11952477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc49a88b46f31805aa26840eb3efd687ccb5cf1b3a519b71b184e073fae2ff4c`  
		Last Modified: Tue, 02 Jul 2024 13:30:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c461818e823a28fd9dc337067c698c4cc2b2e9c38ccb39734a388158332b72`  
		Last Modified: Tue, 02 Jul 2024 13:30:16 GMT  
		Size: 10.2 MB (10228148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2dba100bd1df52bb484bd472ae5ab5433823d09b6d39971ef618523b0b4c76`  
		Last Modified: Tue, 02 Jul 2024 13:30:08 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dd829e2812a28f27d69fdc580d5be701a4be2dc4906236e5d9c123dc826b5f`  
		Last Modified: Tue, 02 Jul 2024 13:30:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32d5821a1838870374a4aa26c55b5f1a44edd3bca13f7ba734eddf0ac3a98c6`  
		Last Modified: Tue, 02 Jul 2024 13:30:07 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01d2364b8eaa7ee51e9e88a2eb5af1b92d9a1268e4116de6bff1afe31ffd050`  
		Last Modified: Tue, 16 Jul 2024 23:07:22 GMT  
		Size: 26.0 MB (26026161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bcfe700294242aa5daf0ee7cc4e1feeef5ba91cb6d31713710a136fcd6ac7b`  
		Last Modified: Tue, 16 Jul 2024 23:07:20 GMT  
		Size: 9.4 MB (9435815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631a91fb7e43b557dc38443709be89a565bcba88da8f1efe2d80dea1720c9aec`  
		Last Modified: Tue, 16 Jul 2024 23:07:19 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead274f50ecff17a43b3c779e8782d185ed028079fb4233d1e672ab59a67fea6`  
		Last Modified: Tue, 16 Jul 2024 23:07:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fc5a6bd2b487f0dc69b9fa3e3439bcd080f680901037c1768c34839190a566`  
		Last Modified: Tue, 16 Jul 2024 23:07:20 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754644c5b3863749ae56df123c03fb618015b5ad0b5ab3593baa67ab4c3909ba`  
		Last Modified: Tue, 16 Jul 2024 23:07:23 GMT  
		Size: 24.5 MB (24460185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03405ae0577cbf9e53a7d4b9bddf39df74c4849a26ed50d32d21c8758e64f4`  
		Last Modified: Tue, 16 Jul 2024 23:07:21 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87c43e6f909662a8512316d4986968ae78f440cb6a774624e3af90b310053d`  
		Last Modified: Tue, 16 Jul 2024 23:07:21 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:d141085a365b5333e171209a7b78cd885ba1ddedd78b9e2ae40260662c9cd8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 KB (59491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a6d0cd8e9764a6f6a5770ff02a01189709119d058897da950a3c47bff8f6bc`

```dockerfile
```

-	Layers:
	-	`sha256:a0380f45a519df182659c568a15d11925e532c81cc60c953853237aec6a4f566`  
		Last Modified: Tue, 16 Jul 2024 23:07:19 GMT  
		Size: 59.5 KB (59491 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; ppc64le

```console
$ docker pull wordpress@sha256:c5de9c63332d5554017607e37828a0233ce42f2df5e9b10283639162c031b3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244690014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8fcb77d1222ab4413828eea50dfbcff4c455858c53739e088a2caf3a115fd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:35 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 02 Jul 2024 01:17:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:10:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:11:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:11:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:14:35 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 02:14:35 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 02:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 02:14:53 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 02:14:55 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 02:14:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:14:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:14:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:52:19 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 03:52:19 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 03:52:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 03:52:20 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 03:52:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 03:52:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:55:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 03:55:24 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:55:25 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 03:55:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 03:55:26 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 03:55:26 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:55:26 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:55:27 GMT
EXPOSE 80
# Tue, 02 Jul 2024 03:55:27 GMT
CMD ["apache2-foreground"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609eb2596342a8a7f536a9dbbffcfccaaadff4bcd99626d15c588274979eaf2a`  
		Last Modified: Tue, 02 Jul 2024 04:14:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9e2e6a6e6ca971bb68e9cd39a2e7d46e2bacfa5a93def5ea728e84f1553a4`  
		Last Modified: Tue, 02 Jul 2024 04:15:02 GMT  
		Size: 103.3 MB (103317721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8703185de8bbe987d67d7808f74a14a5bcb767eadd604f0096503f998496675`  
		Last Modified: Tue, 02 Jul 2024 04:14:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bfa1030b231350ace419a1b1cb2251a16babac7f828c4850f38366b1a7319a`  
		Last Modified: Tue, 02 Jul 2024 04:15:27 GMT  
		Size: 21.5 MB (21511668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ed004f3d7d188c082021564296cd592b4b41057f3e2a33679c35c3e7bb1a2c`  
		Last Modified: Tue, 02 Jul 2024 04:15:25 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacb72cfc9dd2acb981ca25b9f1f57e62d7bf82694d0a3219b604b104ba52cab`  
		Last Modified: Tue, 02 Jul 2024 04:15:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc086a4349052b5fe54ad5b071f3a5378bfbed770357932b907744b932d8e9`  
		Last Modified: Tue, 02 Jul 2024 04:25:42 GMT  
		Size: 12.2 MB (12158847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31809251e6cb7c50c25ffd27b7a6234e4ef2e2ee6b3eeeb0a54dea562de87f4`  
		Last Modified: Tue, 02 Jul 2024 04:25:39 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aa410991c980308a4eaea061629625202f5752c8113925a4ff8938117f4a56`  
		Last Modified: Tue, 02 Jul 2024 04:25:41 GMT  
		Size: 11.5 MB (11526337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0b5a257048cce617a413f06fd007ae68611216dbca9e5a43e0e5f1968504de`  
		Last Modified: Tue, 02 Jul 2024 04:25:39 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be0867aadefa63f0b90a1c1aee8998850daffacab87b9f979ad4fc06aeefbd7`  
		Last Modified: Tue, 02 Jul 2024 04:25:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4636c2c6dcc7f57991e95613b7b2aec73c3580e21517d3bb7bda7a1089bab570`  
		Last Modified: Tue, 02 Jul 2024 04:25:39 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c33d95cecc2ae25d008baa1ce12ca8b9e0ea86955493de71199c6ce75867e12`  
		Last Modified: Mon, 15 Jul 2024 21:59:35 GMT  
		Size: 27.3 MB (27338928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6db7b420f7f76dcf2529a5b7b38a11c203443910b56ab903b6cf69352eb7b5c`  
		Last Modified: Mon, 15 Jul 2024 21:59:34 GMT  
		Size: 11.2 MB (11224591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4740f8bcf4fde5e1afc5e9f2a20bab5983c64ac972d1374c59bb20f6eb9aa04`  
		Last Modified: Mon, 15 Jul 2024 21:59:34 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af17a2970ab363d8801358599a655e0b71051bc9269f21c34f19f294862e73d0`  
		Last Modified: Mon, 15 Jul 2024 21:59:34 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d110887a8e18f0a53024911359eaf2233a962920e3f6dec4a709fc655a9cd419`  
		Last Modified: Mon, 15 Jul 2024 21:59:35 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f0a3d5845fb821c8f0c3a19ecb80137efb9f3133fe1ede394b93d07a21515`  
		Last Modified: Tue, 16 Jul 2024 22:57:21 GMT  
		Size: 24.5 MB (24460193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ce6be3de32ab7f2ed68d82afdf406305f8e6c063b832e889701986ff061696`  
		Last Modified: Tue, 16 Jul 2024 22:57:19 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb85253d65f40bbabd2d07bff0cd4f8ec32c8e66976604fe84939856c3edcc59`  
		Last Modified: Tue, 16 Jul 2024 22:57:20 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:0f5f511a08029c2fd0ec3f1192cdb0c735219a2c6d81a56db5ca94bef7b060eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8044791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92abb7e741d117f2feec77aced444d19fc74dfbe321278836eeb915644c48f8`

```dockerfile
```

-	Layers:
	-	`sha256:3b47f7297b581facdf45351da2786f54a0b170adae691fe649e3cfef7311a9b4`  
		Last Modified: Tue, 16 Jul 2024 22:57:20 GMT  
		Size: 8.0 MB (7985103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220b19ed10c4b0ea1717bc4a782ad358d8f41753513d635b3af37d7497f4b3ec`  
		Last Modified: Tue, 16 Jul 2024 22:57:19 GMT  
		Size: 59.7 KB (59688 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1` - linux; s390x

```console
$ docker pull wordpress@sha256:31fc139a1be610e935358504e8ff694de28e119e332657202ff54cc69f3bb9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210789053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c690bca999cfd3f481b3c52de164d6fa9e23ff83ea32e1b5422ba902e4b2816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:14:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:14:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:14:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:14:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:17:46 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 02 Jul 2024 01:17:46 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 02 Jul 2024 01:17:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 02 Jul 2024 01:17:54 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 02 Jul 2024 01:17:54 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:17:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:44:26 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 02 Jul 2024 02:44:27 GMT
ENV PHP_VERSION=8.1.29
# Tue, 02 Jul 2024 02:44:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 02 Jul 2024 02:44:27 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 02 Jul 2024 02:44:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 02:44:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:47:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 02:47:04 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:47:05 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 02:47:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 02:47:05 GMT
STOPSIGNAL SIGWINCH
# Tue, 02 Jul 2024 02:47:05 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:47:05 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 02:47:05 GMT
EXPOSE 80
# Tue, 02 Jul 2024 02:47:05 GMT
CMD ["apache2-foreground"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9251ecd224e15bee1af8e5d8ed06b4583727d21c25571b0841308fa40637020`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de732a471a32b9581046aa3735f5891fa36c8dc024c7c7a007087dd77b0bd3a`  
		Last Modified: Tue, 02 Jul 2024 03:05:16 GMT  
		Size: 80.8 MB (80817736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f9b6de1c71adae007cab6934b2b7dfe2155be5d6b7fecfea770f4dca1aa159`  
		Last Modified: Tue, 02 Jul 2024 03:05:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac393ffa46cdbdd309e76835caefc39b9a5f28208a5117719850422e50cd1830`  
		Last Modified: Tue, 02 Jul 2024 03:05:34 GMT  
		Size: 20.1 MB (20101995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b9ac198003d25e1ae488b290fbd759f674d87fea5692596dc85177b0ad0014`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe10d7b17a1f1937efded756698b3791c41a781a95ad1f5b3436f29993e08d6`  
		Last Modified: Tue, 02 Jul 2024 03:05:31 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd98747ef25a50f40748abbb1eeace135d9a238847ee45f980956c5ed9ffd512`  
		Last Modified: Tue, 02 Jul 2024 03:13:21 GMT  
		Size: 12.2 MB (12157833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5785ea0fba3dc10d1fe2270371949b649b28946a95a3a1be59cb810fb1642ba5`  
		Last Modified: Tue, 02 Jul 2024 03:13:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea733bb981aad55666b3281de62cf8dd56b3d89c2a2061253a1f5caf1d2aef5c`  
		Last Modified: Tue, 02 Jul 2024 03:13:21 GMT  
		Size: 10.4 MB (10395875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ec0c5fcacd13fd8a6843984627a8ae3f659c3febe1bd04458ac80a93adc12b`  
		Last Modified: Tue, 02 Jul 2024 03:13:20 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93e1e0dae7ae52d34ab67b856f1d8c23ffb7e595a3456dbc43162b0ed6b2b3d`  
		Last Modified: Tue, 02 Jul 2024 03:13:19 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f393e6d70391580c6587eddc76f3c90a825b5aca6a146015245d24d45f4dd7e7`  
		Last Modified: Tue, 02 Jul 2024 03:13:19 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3396d091b5b737f7a39715b56d1723e9120bb3e74db993cfaad3675551c45f7b`  
		Last Modified: Wed, 03 Jul 2024 22:17:51 GMT  
		Size: 25.9 MB (25899249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88701492404278e7dbbbdda9c6667e5cea850466944d07a4fcd55039bc9c40d`  
		Last Modified: Wed, 03 Jul 2024 22:17:51 GMT  
		Size: 9.4 MB (9436644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc620125c2c9cff8958e0eb5b7c48806ab284e2459d6f41c3e2dc704bdcf3cd0`  
		Last Modified: Wed, 03 Jul 2024 22:17:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a042066700c6cc639d9b1f05706551e90c942335bff95405397bb79c2e5e771a`  
		Last Modified: Wed, 03 Jul 2024 22:17:51 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7734758ebabf94b043530993ece22c04c3765c8244f69d98ddee4431ad72bace`  
		Last Modified: Wed, 03 Jul 2024 22:17:51 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c62b3e59506876325c76aa24914bfa26cdae4567ef8b8aebf2db18174d57edc`  
		Last Modified: Tue, 16 Jul 2024 22:56:59 GMT  
		Size: 24.5 MB (24460192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f25d49caa322eb76c6dc224efccba46e7bcfd0f93769d3ff2ec1c3aba90c082`  
		Last Modified: Tue, 16 Jul 2024 22:56:58 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d254cb6646c5033fdc8e64c81f9440d076673b098c0d892ec2b3c23f9463cea`  
		Last Modified: Tue, 16 Jul 2024 22:56:58 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:8e014ef9a214f63b2094deb37393c039f52095c6d0cc1ac06ea28aa12feb799b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7896803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34135f9bade9b08f93f5464263c888884f50ff1e37aa11044b3af8de8f48f17d`

```dockerfile
```

-	Layers:
	-	`sha256:a2ad82e06c95ad6e1aeb36c38ae7affae559d3f7f5797641af90167a42b9cec9`  
		Last Modified: Tue, 16 Jul 2024 22:56:58 GMT  
		Size: 7.8 MB (7837201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a5aeacfb20ba194e9112134000d517d37bd749ac7e91862816a8b58bbdb29f`  
		Last Modified: Tue, 16 Jul 2024 22:56:58 GMT  
		Size: 59.6 KB (59602 bytes)  
		MIME: application/vnd.in-toto+json
