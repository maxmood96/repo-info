## `wordpress:beta-6.7-php8.1-apache`

```console
$ docker pull wordpress@sha256:f4abc2afb8d533edb853b1701de24eab85c4b28c829a72e6e31d1536e8d3f5d7
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

### `wordpress:beta-6.7-php8.1-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:e378a05ce3f480a775dc0b569ca7b2a95bcaa4878cee928b90eab1e889b6b56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253106752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c4bb8c6f345b06299643934f7a526c86acf46fe6a285ba35eb31aa962fc505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923881530ea76e6dee80efe753a158b8fa3ddeaa62f085da06c86d3d595fe`  
		Last Modified: Mon, 28 Oct 2024 22:12:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb36fbb9aaa0103623e9e157481c7527b37b2ed084006fddccf8a78e0ca6f1`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 104.3 MB (104344820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ce8114bd056ed702ab3918154808f17fc19709880d196ad4178bcb7f6a577a`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e019fcbe1b2248fff82029424ef93e4c1fda2fb2179b338cc5eb78de89e5a`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 20.1 MB (20123782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29cbf15823a2f985e291d9f2ca3d8013df1394ad63ddba1b195c6ab01404c`  
		Last Modified: Mon, 28 Oct 2024 22:12:42 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346805f9cf697be14cb6fea107cbd0301bbaf185f38edf77953f559f3072b854`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea11a31f10c9875f39a0da4f660929e04cd9c7c9a478ed232a3043e605608a5`  
		Last Modified: Mon, 28 Oct 2024 22:12:43 GMT  
		Size: 12.0 MB (11978954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ed1285cc1d4329225e99b6a1fc351cfd4011313a07aa43bc9b3d73bafae0a6`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ce22ed84dbc98de9a995b57c0e96095c1e37feb6dd820f2163355a63e4db9`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 11.2 MB (11154705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ed6b150803e69bf91d0f403db49a9fce8d600bece18ead61f2e72bb6c1578`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1088a6234d4b0065d944e2b2f9fcfa29d34eea126f9b7abc77fb54777d977da3`  
		Last Modified: Mon, 28 Oct 2024 22:12:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d8f1f8c16c47833769853a3d20f881c2107fb8109e50c0879b861d912186c`  
		Last Modified: Mon, 28 Oct 2024 22:12:45 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e2ad9cea0dd3d88998d882fdc237693d6f2939826a8831040612935cce4a3d`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 26.3 MB (26255168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5332b01bb96b574aff513bde562dca9e84c6355aeb0a29228ac4235247561c9`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 17.4 MB (17441544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050b449c168627ef55dc34d8fd5bfeec3c3e20aa9e9d103f133fc0205f1cd12f`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761c575cefcb5c55b9b712685eec03f58a25e592d8a1c483e9e4371adc97773`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f3cccc87f3baf7ca80436586e28234092d25608a17d2803549cf339934544a`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 19.1 KB (19140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7543f07f7750b7ba11167ff42816ccd143b33b0d4e11cc7778fc49f50c880`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 32.7 MB (32651977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf68383bdd6ee8f0399d93302c3d0d970ef51438d5c94936d1bea91021d61ea6`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18459f90960b6470d71ee08fb19b2df98c826781f79ffb5ab892510108bab4db`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:e8f72d999468407f87c37dc2fe88b482ec99b6a0f8cc91b22550b3be4d09fbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8183963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1e8c17c3686667fd98398a9521f1b12a142ea0833d18fbab709c44777c7c16`

```dockerfile
```

-	Layers:
	-	`sha256:717408efee3ccf0bef0a9d5daf6ab16fc1fc742ae6a7872b86144080c8a35bcf`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 8.1 MB (8123174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5658776ef0e3fb6c7be9fb7ebf1ad0e0c321b526c166b8cea49919a49301760f`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 60.8 KB (60789 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:946b5a2f19e1a7d990118109783f2b67b8f813127ea19511a7a2df725ed92bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (222000560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a67e10b2b3c9e58131cd46ce26230a50c0597cdf508dc3173cafc4d24e3421`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cbfa5cbebed9fd7c8f34077debdb42c371f3e9ff0874a76eeecaeea391fff`  
		Last Modified: Mon, 28 Oct 2024 22:06:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d7de8ee38de821e7a2d49fddb538f63c035fac91b992f00ac7bf6b39d25964`  
		Last Modified: Mon, 28 Oct 2024 22:06:33 GMT  
		Size: 82.0 MB (81993591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b072383a75b21caa7c43d077f84a4e9c721b6f8b19ab0e9df353f53ab84ca`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e85e77875bb273fe263ad3f33329ff4aec330e79ddf1f8063eaa30810787f5`  
		Last Modified: Mon, 28 Oct 2024 22:12:37 GMT  
		Size: 19.4 MB (19418870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4c981efad954cf32a3908ca82953214cd6071fec1c979b34181c63546ebf8`  
		Last Modified: Mon, 28 Oct 2024 22:12:36 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9718dbae37263d9bc8d722584725ce8dcc3e716cb937ff6b85801f56374c88`  
		Last Modified: Mon, 28 Oct 2024 22:12:37 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f1eb021609c2011c7c3d1f78db55abd7e61011b231cdf9028d8eaaf43dad5b`  
		Last Modified: Mon, 28 Oct 2024 23:20:10 GMT  
		Size: 12.0 MB (11977220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7805cb0c12233e2d1a71b757f7ba90dadbba1b2479b0a3e04bf5e87b97c70c`  
		Last Modified: Mon, 28 Oct 2024 23:20:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b58f2f5f8157d68c8ba05cea218184777666cc466030a7c5fa5cbb531bcf9c`  
		Last Modified: Mon, 28 Oct 2024 23:20:11 GMT  
		Size: 10.1 MB (10117689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cf2d92ec8b4f39f6b8d53f4190be829b67b4eb86034fc4f308f00e8c5e1d4d`  
		Last Modified: Mon, 28 Oct 2024 23:20:09 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ecdc3eb94e1099702c07da2469214b6a63d29892cbeb2718aa7d90766d9848`  
		Last Modified: Mon, 28 Oct 2024 23:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262eb88c4df0fb31a8951d99af70add8fb9abeb35cc74f301f68dd1678470a0d`  
		Last Modified: Mon, 28 Oct 2024 23:20:10 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db161fdf6d455819cc61260ae7fa53a7171c07ac7d4cd9eba1cba21335f37791`  
		Last Modified: Tue, 29 Oct 2024 01:08:20 GMT  
		Size: 25.7 MB (25705163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897859de2ccf95f670ebe781a9786f77da489176334f1aa98a1c0aef54824434`  
		Last Modified: Tue, 29 Oct 2024 01:08:20 GMT  
		Size: 13.2 MB (13219211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19f67a2a63334a6aa1e4dd53a48ba06e8eb24f14bf7639a8fd27511cff39b8`  
		Last Modified: Tue, 29 Oct 2024 01:08:19 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015a6c6202205c09a545ce554355a0d55dca381780986147435af263ab5d2f7f`  
		Last Modified: Tue, 29 Oct 2024 01:08:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56f378752555b3d2b7bf6d23efe4e5b8b4e4ee4f04c8dc5acf2392ea8db63b3`  
		Last Modified: Tue, 29 Oct 2024 01:08:20 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b51519a4257c49d7363fefae2b552d3fce307fec7c2e9f0672554ad6d9f74f`  
		Last Modified: Tue, 05 Nov 2024 20:59:14 GMT  
		Size: 32.7 MB (32651951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ef1f32f7bdd853632cc4555ad1571049ed3fb7b9b97558b0956ee85cb72ee4`  
		Last Modified: Tue, 05 Nov 2024 20:59:13 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf754659f9ab315004e7fb4cf8cafa7236ba7e14b94d1e43bc7b8c5dfce0e8c4`  
		Last Modified: Tue, 05 Nov 2024 20:59:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:20b62c85c8767085122a879d6fd32e38b0f7e00765ee28cb7f54ecccc4f4cff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7990063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f730d71af9115f08b01610dbd183b68cffc0751f253dac30df1b5b9483c92ed4`

```dockerfile
```

-	Layers:
	-	`sha256:c8a6410aa39e4ab8182855691959fcc46b804393d72b5d47986d2d79e4f6afe1`  
		Last Modified: Tue, 05 Nov 2024 20:59:12 GMT  
		Size: 7.9 MB (7929056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd15d7ca73a71e5b914dfad1c9a8a588fdceffeb5d98027c2e7c25de7457e6a`  
		Last Modified: Tue, 05 Nov 2024 20:59:12 GMT  
		Size: 61.0 KB (61007 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:baf3e2b47d4bb086b1e873ce6daf933f5f429c840c737ce7b50ec71cb6d69d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211043965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeecb163df5f3056b4daec087033f64f61e4727c1c57018b621f9b1a136402e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcfcb380cfbd1992d2f15637ef37999cbc4f9934874d34a17b217098fa8c2f4`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63df587ed65ffaf4f0e56a3ade450a0c2f4bd0ec52cb90e0193d9ec9a394a939`  
		Last Modified: Mon, 28 Oct 2024 22:06:06 GMT  
		Size: 76.2 MB (76163014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f4e906cd29de73704abed83d01761162847c368f1a7c597dc584fd985a75c2`  
		Last Modified: Mon, 28 Oct 2024 22:06:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b42cf4a791cfd52dd382314b8b0f4cbf7a46e61d6c6c664a4299bfc5656b5a8`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 18.9 MB (18857494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bf1529cc0e5c50582fc58382ef311e785b9a8a182db98e8831efef019fe199`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fca32620845d0574b19199a5b046dcb2260722f191ef3f55c582ed51287e788`  
		Last Modified: Mon, 28 Oct 2024 22:11:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93530a363a64403a01b9825b51f5e405c644ed5d8d0bb5653f2af475bd6f40d5`  
		Last Modified: Tue, 29 Oct 2024 01:13:20 GMT  
		Size: 12.0 MB (11977253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8912826933d9b32a480082646f4b758bb776541bf7ea3cde4ee4441221148ee7`  
		Last Modified: Tue, 29 Oct 2024 01:13:19 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1faab983e083533a0f5a0b7e249a62fd90f61430747a2f4a3524326e0bea12`  
		Last Modified: Tue, 29 Oct 2024 01:13:19 GMT  
		Size: 9.6 MB (9582240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ed5229a5c4d11dbba8c957218fd7222f48d92725fe963f269b454c9d3cf6b`  
		Last Modified: Tue, 29 Oct 2024 01:13:19 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e8a723c28ecb3fb2f0d307ca1edd9957cfeb37292bac5fa8c90c4bcd3fa11`  
		Last Modified: Tue, 29 Oct 2024 01:13:20 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612b86b0a4e8dd11b15ad28cb8c28a4287283344b6f9744771634386b7fff036`  
		Last Modified: Tue, 29 Oct 2024 01:13:20 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7d2a0f4449eca338ccf44a25a22977c9734a2de20ef1c24e8ca462b980d142`  
		Last Modified: Tue, 29 Oct 2024 02:01:04 GMT  
		Size: 25.1 MB (25075369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e21af52f6480c57832105f1226d7667ec960381bb764804ea59ef989ea664e`  
		Last Modified: Tue, 29 Oct 2024 02:01:03 GMT  
		Size: 12.0 MB (11988897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e8760d6370803a3b031fc7b26e4bfeda9f2e8fd005aa0a91a05f19ae7bd88a`  
		Last Modified: Tue, 29 Oct 2024 02:01:02 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c12b559f1ec80041b0692b18756ee5cb7bab499e2bf6afd9b0bc7f1cbe108b`  
		Last Modified: Tue, 29 Oct 2024 02:01:02 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47543deadf18567e21694cac9547269c692c9f00d1efbf1bfa353907fce0e00`  
		Last Modified: Tue, 29 Oct 2024 02:01:04 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744ecdb1f108deb1434faf3d35a2b8436a8243387947395822bc34218a40b43`  
		Last Modified: Tue, 05 Nov 2024 21:00:01 GMT  
		Size: 32.7 MB (32651963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae626a8beeccfa777d1b8ef731afe2d6ea2d4ae36977e7941c69dadc8d6f32`  
		Last Modified: Tue, 05 Nov 2024 21:00:00 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcffb013f1291b25f7ced2bf4e9ef5871e46accca83c8028434577e0b1ec7c4`  
		Last Modified: Tue, 05 Nov 2024 21:00:00 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:51e29f381d77fb1ac984fc0ac02b2a7821f306ea70e4e1f2edd9197091f9c4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7994747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b25f3b97e8e42b514f1d0dcae5e9721ad714109f21fae0d9dab7ca643818529`

```dockerfile
```

-	Layers:
	-	`sha256:d7ed728dc66dea4422e8ff2369afc22c828dcb03c4e7e382a7c1946c9960ad5f`  
		Last Modified: Tue, 05 Nov 2024 21:00:00 GMT  
		Size: 7.9 MB (7933750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8790da42f2eb03c5548f30d2e4b84220f04ce2f1ad2c64d9ea1eacdce8b735cf`  
		Last Modified: Tue, 05 Nov 2024 20:59:59 GMT  
		Size: 61.0 KB (60997 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:d033e99d0e23fe8b2c0ad49a13b8c68b44bf29e99664a57b9139886658dd15b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243140505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1865a289f6fae0e1ce192c811c7bc3314513d95b8bf31645cadd5912755cc4eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77074644eeb7cdf46475293fba2c88bbb04a0d4639f8fe1072fb11d7a6434fb4`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844b6c933ada1472f6f12b5dab5dbb974ff7c8299bc6ba9312586feada41bf1`  
		Last Modified: Mon, 28 Oct 2024 22:03:23 GMT  
		Size: 98.1 MB (98130054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d350ecad63f801fc61e8fb71f1da4b5052fb1caae60ea46e1ab87d2c3cd4ae7`  
		Last Modified: Mon, 28 Oct 2024 22:03:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b420f8be6082fd2562efa3ab5c5be52021e75fc1ad60aad50264cc70250ea8e6`  
		Last Modified: Mon, 28 Oct 2024 22:07:10 GMT  
		Size: 20.1 MB (20120934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bb8443b199e35f18d67d4df1195046c90b460eafe7450bdddc9b0b0b45531b`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65caf96ff18c89bce6dd79217c16e38c511df6d517eb60ca2ec174387a81a432`  
		Last Modified: Mon, 28 Oct 2024 22:07:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fccbee601c8894cef1c71383d3e29026744a9a3fe84d8ee877668ccffb0e1b`  
		Last Modified: Tue, 29 Oct 2024 00:58:13 GMT  
		Size: 12.0 MB (11978755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f60723cfb8a235f2d1e63ba1ab37cc61e9532ac15b1a7d536c7119ccd7468a4`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279d698131d95552fe612a37c7941088a2a36098e0a54fe01abfe11cb3698f9`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 11.2 MB (11153034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2f09b87dcac0c7aa48e318a18fdd05992a2a89ec73aa28aa6ee6c869ce3fe`  
		Last Modified: Tue, 29 Oct 2024 00:58:09 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9347b89a99e60c15df6c60a694040ed17c83585ef527999e88bb0dc21f874d`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e40c72036285abc3b2a1a229c0acee4f102448b62aa3e9f3b76e89f4079feb`  
		Last Modified: Tue, 29 Oct 2024 00:58:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badc046cfa95a53bec39c6e554d82f1e7eb7e0f6790204401579783ef7ad194`  
		Last Modified: Tue, 29 Oct 2024 02:03:19 GMT  
		Size: 26.2 MB (26171631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db7dd76db851e60ae5cbcfa37111b77e743fbf61c4d314d867205599004b621`  
		Last Modified: Tue, 29 Oct 2024 02:03:19 GMT  
		Size: 13.7 MB (13748255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e180d1d135f563fe336aa42cfeabf9e939dc78309e926d5f327964c7d994049`  
		Last Modified: Tue, 29 Oct 2024 02:03:19 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f7132a9527220ae407ac7ee41a6d4c0a283e8a2c7d88c86a1323bcd148e987`  
		Last Modified: Tue, 29 Oct 2024 02:03:18 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a75dcc683ab0ac4c0b7203e0f16e0a2cfd30379a3452ec422d68c76bad9b3`  
		Last Modified: Tue, 05 Nov 2024 20:24:33 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d92792c831b283b73df2a05ed2c4f2ad0b56e8b36413398711e375c4093a14`  
		Last Modified: Tue, 05 Nov 2024 20:24:35 GMT  
		Size: 32.7 MB (32651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbd3df5160cdb4945ee7249a7d17b521776d1243a026a99466e4665948c4d14`  
		Last Modified: Tue, 05 Nov 2024 20:24:33 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b013113aaed270582c126a34b8d1deee071527609e86d8cdfbe952871e83c1`  
		Last Modified: Tue, 05 Nov 2024 20:24:33 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:38069d7920fc551122a7e44558a9cae5fc25cc51b27a3a4320bb031d6bd04c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8213082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cce8643ff39e708aa61626d8630305ba55bd75b34d4927d00d3d01f0542d6c6`

```dockerfile
```

-	Layers:
	-	`sha256:bb3a863fe74d1de6e55e29a920e9fcfafb4898f8d8b76d2f85906ccda9560fa6`  
		Last Modified: Tue, 05 Nov 2024 20:24:33 GMT  
		Size: 8.2 MB (8152021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8757387a165d9a59332a4e026981709df6242e7260ce87412f1861b9ea60f859`  
		Last Modified: Tue, 05 Nov 2024 20:24:33 GMT  
		Size: 61.1 KB (61061 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; 386

```console
$ docker pull wordpress@sha256:885679ecfa7cddbc786612530fa5d59317df81cd79c08810116f0e9fd56e3476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248486708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b2b6abd00a0ecbc0031f1778f00d5f3860402a617c110ad770c987741baaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d3ded189eed4a2a77e9de8dd7e7a30dd9405f4ecdf99b6039190148637a5ff`  
		Last Modified: Mon, 28 Oct 2024 22:12:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0373dda4b3ace680f5389fe3ace602930d66a226f20d909db1e61e4c2c9e7b38`  
		Last Modified: Mon, 28 Oct 2024 22:13:20 GMT  
		Size: 101.5 MB (101516504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5c4916b97a37fd597339021043b9a8b3297fcd02493d3f7b9a2ea6b35fd0e9`  
		Last Modified: Mon, 28 Oct 2024 22:13:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b33f5105b4acd5412597cb57b9d5913bfbc4ccd1e781bfeaaf016ca044bcec`  
		Last Modified: Mon, 28 Oct 2024 22:13:18 GMT  
		Size: 20.6 MB (20638469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f710080f7e3e0ed8aa77bf3e6cda79cdbe38c4467cc5330273ad2552a41202`  
		Last Modified: Mon, 28 Oct 2024 22:13:17 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6151a407f6a0884f0bbb2e29c82e17aae7b9fb7e726d88c02ac955392a464e3`  
		Last Modified: Mon, 28 Oct 2024 22:13:17 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e528f939f25c06ab29ef43f0f450b3eb048b86343f8b20cf2b786ef1b750d91`  
		Last Modified: Mon, 28 Oct 2024 22:13:20 GMT  
		Size: 12.0 MB (11978127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcdc6049d05996d12c4ffa7d7db30fe8362a2506d1700e89a321fae1d10c8d0`  
		Last Modified: Mon, 28 Oct 2024 22:13:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eebabe4f60d28cb43facc023ab04a16cd87890ae7fb5bf9c7a4f09123ebf03`  
		Last Modified: Mon, 28 Oct 2024 22:13:19 GMT  
		Size: 11.4 MB (11378393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3048b7367770fb07c5cf0d395161f06a7b893eb6410093a9fed70c9073a08d`  
		Last Modified: Mon, 28 Oct 2024 22:13:19 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60573c7e6c9612fef3bcf9a351bfebbe80ebbf34167e11dbe7424ce68e0e94dd`  
		Last Modified: Mon, 28 Oct 2024 22:13:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f976d7a218d3240cf072d0cd9197a735d5715d422cd9faf4d6614cfc614a4bec`  
		Last Modified: Mon, 28 Oct 2024 22:13:21 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3fec1562e0212c45800514e9c8b9b00c6136cd9f278569ef779592400b33fd`  
		Last Modified: Tue, 05 Nov 2024 20:37:47 GMT  
		Size: 26.7 MB (26696359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014cbeecc50d206da8f136f1dfd82b117a60747a14ef737efe7b4b0a19c36836`  
		Last Modified: Tue, 05 Nov 2024 20:37:47 GMT  
		Size: 13.5 MB (13453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e48e4e2ccfd361858c28be177474f44c618d3a5394d5699f9f74c043202590`  
		Last Modified: Tue, 05 Nov 2024 20:37:46 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fb57e078a2bd763a84df36374ee2c5ce38b84141fe2ea02219869f65023372`  
		Last Modified: Tue, 05 Nov 2024 20:37:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fc19cb2fa2bd6644519ce0cd8efa93144580ad42eb030a140691415000271c`  
		Last Modified: Tue, 05 Nov 2024 20:37:47 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1054914545dae91029c5bd13c46b75124550b361449c1534491139f2e912b1`  
		Last Modified: Tue, 05 Nov 2024 20:37:48 GMT  
		Size: 32.7 MB (32651967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73b5511444aa28bafcfb72ce885903fa1ebd2ac462543365fbab262ce01a972`  
		Last Modified: Tue, 05 Nov 2024 20:37:48 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220464e86c8fe71f32195d1cf3cea237e5752f6f141a09cd1c89871641eb8df4`  
		Last Modified: Tue, 05 Nov 2024 20:37:48 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:85eb3f15a65c396d364040997a51a8ca8b780ad514f4d7a50c8bfabf67619cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8157111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78b55a880fde8b8a34823daa1eb243366c083723c62983a04fe68eac86e3c62`

```dockerfile
```

-	Layers:
	-	`sha256:95791fd302dc773496ddddad69edd8bc3428f691996a00ab5810d1ea02c5132e`  
		Last Modified: Tue, 05 Nov 2024 20:37:46 GMT  
		Size: 8.1 MB (8096384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ab253af43dea69a91310767b9f217bcd118822dc24e56b25b21480e47a2fdc`  
		Last Modified: Tue, 05 Nov 2024 20:37:46 GMT  
		Size: 60.7 KB (60727 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; mips64le

```console
$ docker pull wordpress@sha256:84ada9f5e4657e560f6a01979d9fa01313788bc91d2d1055bea5f6f5d06e89cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223698026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed97bc903c352eebddc2486c1434f9e6489a409c201bf51955f6bd9188bf306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75971b85139441fe144cb93dcb63eda60c20b8b82bcc4cc161a345662be6e248`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae54a087649536e7da942bb23de64ede6ba55259b78328b804de7695cf731369`  
		Last Modified: Mon, 28 Oct 2024 22:20:39 GMT  
		Size: 80.7 MB (80666666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9d1ae69be6bff3b5f486ce83dc2a01329491bc64c77e183361743695495d62`  
		Last Modified: Mon, 28 Oct 2024 22:20:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9805e4def2c522f97a948ff0a106d6753819d71887cabeca9b1ab8355a0ec3f5`  
		Last Modified: Mon, 28 Oct 2024 22:40:31 GMT  
		Size: 20.1 MB (20069130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f108a36b91c4b30f45222f94048f45b028abb9cbd4872f312cc17b7ebdf9e0a`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc8de30d0eaabcca7399faec8b52772f4a699389c0f6ee67d901929b205efb`  
		Last Modified: Mon, 28 Oct 2024 22:40:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d173d9375fe48afa1e08e17ebc7160066a7f97bbfcbc26f4a6922ee4e9630f`  
		Last Modified: Tue, 29 Oct 2024 02:08:23 GMT  
		Size: 12.0 MB (11976921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a871f1956e7037793e6f02e951c18f65ebcf31c08a14d5e100c035a72d11411b`  
		Last Modified: Tue, 29 Oct 2024 02:08:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56598c5fcbd37330de3c7f19775a1203d99e3164611507a11c82b07236389d8f`  
		Last Modified: Tue, 29 Oct 2024 02:08:23 GMT  
		Size: 10.2 MB (10227613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e9d3df2a81a84b04177aecbc3eb032000772ae7c6ac8b20cb8a2a0cef9ef08`  
		Last Modified: Tue, 29 Oct 2024 02:08:21 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bf543d131f34c67f0f8b70019970ff9f7308b16607f7e85a71cd379ef90d06`  
		Last Modified: Tue, 29 Oct 2024 02:08:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae9da65b60447c6f1dd0554dd524078f8bacad3339e61eb9d27b413edfd4ef6`  
		Last Modified: Tue, 29 Oct 2024 02:08:23 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bac3b538d605da8d2cb80fc5c8581efb1473efa05d4e2d2c26cd09025710c16`  
		Last Modified: Tue, 29 Oct 2024 07:47:31 GMT  
		Size: 26.0 MB (26025540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc857397490b64c582c2478004123d90cdb49f3340a6916667c9d3d4f35b57a8`  
		Last Modified: Tue, 29 Oct 2024 07:47:29 GMT  
		Size: 12.9 MB (12925846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a506c1d8f707b3e4057b77bfe921a6d18c4cbb1ddd1e00d119b09ab473c2869`  
		Last Modified: Tue, 29 Oct 2024 07:47:28 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8d2d0bff10a1c376ee863b72d685ef573f28d3bb8c320165daa0b8c9039af`  
		Last Modified: Tue, 29 Oct 2024 07:47:28 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6d717c71267a34c698f08c4fbcc0c67c7a3a13bbc18ecb235fd380fa0c030`  
		Last Modified: Tue, 29 Oct 2024 07:47:29 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0bb609ac45da0d9ac6b3ae0538ae7c5c0a66e2c6c2e84326d2d524bf23f7ce`  
		Last Modified: Tue, 05 Nov 2024 20:38:19 GMT  
		Size: 32.7 MB (32651963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e98a444eeb7a3b7b2cb82b94c74650a383eed01403d4eeebf200e472304c9db`  
		Last Modified: Tue, 05 Nov 2024 20:38:15 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd9385b7a60dee8bfc3786d61ff76e7b4f4d7012a992633d345f21da99b82e8`  
		Last Modified: Tue, 05 Nov 2024 20:38:15 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:5c5111f370ae0d9e868b2759b70872d7c740cab6cc23c10ecb9b083922b53572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 KB (60736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae70e7d40879485e6bb20e56f80b04822192e7a8078a8061d645b567de3e1858`

```dockerfile
```

-	Layers:
	-	`sha256:4000e593db3a38e7379d49258a962a383c30e4fd5ae9b03390794e6293f5abe3`  
		Last Modified: Tue, 05 Nov 2024 20:38:14 GMT  
		Size: 60.7 KB (60736 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:1da014275c2c698f8600007d368ae481656c2b1a307df30fc6d940dd85fdf45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256868690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad594b16a507dd07668df58564cb8673e01f1a9c0b7cffa44489769e3be4a4d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aae56eb39d7a6f0865b2b2c1e759158f7f32cb38431cf0b9f4a53e75069829a`  
		Last Modified: Mon, 28 Oct 2024 22:03:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc191720824d9a8274cc0a9d7a4e17b74deb924b9ba62a638fcfe329b1cb843a`  
		Last Modified: Mon, 28 Oct 2024 22:03:58 GMT  
		Size: 103.3 MB (103321639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e65ebf34f6eed8b3368c7c37216f302c7b19e10d99d1c5ebd90d00bbf57cd63`  
		Last Modified: Mon, 28 Oct 2024 22:03:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ca7c4e1c934a05195ae2806efa08495b749078e5060a107b69954c9e8831f3`  
		Last Modified: Mon, 28 Oct 2024 22:09:18 GMT  
		Size: 21.3 MB (21308341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afeb891a5f261be3057466eac9022a1bd1afa1a3773815828cd1caeb277139c`  
		Last Modified: Mon, 28 Oct 2024 22:09:17 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6afdb35491d58f7d16d1d4ace112bba4fb8ba8a1702dbad4ec8737e9e449f6`  
		Last Modified: Mon, 28 Oct 2024 22:09:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83c7c47c6f2edfa7f965ca13d062c0f4bbb568b982a5acaf25e4a327761be7`  
		Last Modified: Mon, 28 Oct 2024 23:51:00 GMT  
		Size: 12.0 MB (11978495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f35da74d22ad109ddfcdc5d1a1c6cd8f29e5fbb1734fb3cc9d7caaacbe9aea`  
		Last Modified: Mon, 28 Oct 2024 23:50:59 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94b706f507fd488bdf55121b9e7a4c74a81d876f5c9f6f8c94c31bfb2df33b0`  
		Last Modified: Mon, 28 Oct 2024 23:51:00 GMT  
		Size: 11.5 MB (11524913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01fd051df1e81b514d109be0a324bb2a37431176e1d3320ccce4bed4dad0da5`  
		Last Modified: Mon, 28 Oct 2024 23:50:59 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0df75971aabf67ea8f94e114fa36971e93086145b654261dbab2add1cb9419`  
		Last Modified: Mon, 28 Oct 2024 23:51:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a1620692ae795e4f797e78aabf2fa7ea2c8b98779e921b9eb0f49db2971a59`  
		Last Modified: Mon, 28 Oct 2024 23:51:00 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75a6de7f408d952d554fc10c10f479bb95ca3e74706fb192391db29b277ffc7`  
		Last Modified: Tue, 29 Oct 2024 06:22:23 GMT  
		Size: 27.3 MB (27336785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c183db6f118a61085aa9df02f123c147307b45f32b4796631cacc2036820f9`  
		Last Modified: Tue, 29 Oct 2024 06:22:24 GMT  
		Size: 15.6 MB (15594820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974ff4f2161fddd4f04bf4b735b703463dfdc8b6b35029c4e0956974cfc218f7`  
		Last Modified: Tue, 29 Oct 2024 06:22:22 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e52e1beb4332b35fac758128615acdecd61f65371f144f964a4339a2501bbf`  
		Last Modified: Tue, 29 Oct 2024 06:22:22 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3028b86404344980f8e1358d78abd5b1c953d8065af422b1d9aa09fc10ea9a07`  
		Last Modified: Tue, 05 Nov 2024 20:38:16 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc137ef0a40e01706146f50b041b8437de21c80ce5989c87536587d0a98e38a8`  
		Last Modified: Tue, 05 Nov 2024 20:38:17 GMT  
		Size: 32.7 MB (32651963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fcf88bbc7fc386cab093e5235aa663a7bc887ccc3ec40de23f84e49ec010c3`  
		Last Modified: Tue, 05 Nov 2024 20:38:16 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db155b96301547364e3d9622b4e959410ed1cdc5de0777b2503b7b0c3781d054`  
		Last Modified: Tue, 05 Nov 2024 20:38:16 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:9326b1165813604b533cc487a27fa64909d3adec7811aa4f4cfeed75fd4575fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8162929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ddaf707c7effc982f4777f9653cf554379af45978885a08bbb99276187d0f0`

```dockerfile
```

-	Layers:
	-	`sha256:5c534a3b659836fd1e47160b5ee95676f0ed00bcaf881fbb97ca147441e60fd2`  
		Last Modified: Tue, 05 Nov 2024 20:38:16 GMT  
		Size: 8.1 MB (8102009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dee9dca564ceb652295329f1045df27735aeb3a4d2405216877298ec4f44f0f`  
		Last Modified: Tue, 05 Nov 2024 20:38:15 GMT  
		Size: 60.9 KB (60920 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-php8.1-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:4d4154e8fb32826c2271ba7bd13e2eed44d319131198b2b011ad2ec99d03b201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.6 MB (222580868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a66e4b9f63fab79b00fa4deab586acc7cdf4129116961566d803380c2462b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 26 Sep 2024 20:54:05 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 26 Sep 2024 20:54:05 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 26 Sep 2024 20:54:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 20:54:05 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 20:54:05 GMT
STOPSIGNAL SIGWINCH
# Thu, 26 Sep 2024 20:54:05 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 20:54:05 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 20:54:05 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Sep 2024 20:54:05 GMT
CMD ["apache2-foreground"]
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
RUN set -eux; 	version='6.7-RC3'; 	sha1='2e8d6e47cbd593ab60d94c43aeed1becd62cf5ce'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
VOLUME [/var/www/html]
# Tue, 05 Nov 2024 18:57:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 18:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 18:57:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef30fd559c6ef2ac6477f19c70672a7ee15e6df0955b9418d7d99e635fa1bf0`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4284cccc34f4d86bd5b1ffc10f277aa5cc0d4e8e4bf9be585b727389498bc65`  
		Last Modified: Mon, 28 Oct 2024 22:04:13 GMT  
		Size: 80.8 MB (80817298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310b072383a75b21caa7c43d077f84a4e9c721b6f8b19ab0e9df353f53ab84ca`  
		Last Modified: Mon, 28 Oct 2024 22:04:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca23539a560ecbc74c5143d2cafda70db6eb98973a13e443b451e0c9c2995f`  
		Last Modified: Mon, 28 Oct 2024 22:09:43 GMT  
		Size: 19.9 MB (19895121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a45ddf6b46c9a6c7f526ae595797099a5fc579b55abcfd3898676b4d492cd2b`  
		Last Modified: Mon, 28 Oct 2024 22:09:42 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9251a13b927d3a64cfbffb8b90c4c32f8b6e265b8d38173390a57a3b727aad43`  
		Last Modified: Mon, 28 Oct 2024 22:09:43 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0f18997424b0554b7e95c4dd3e85883b0255afd772a4c46f84192afdb92d89`  
		Last Modified: Tue, 29 Oct 2024 01:00:36 GMT  
		Size: 12.0 MB (11977544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21a8defb49268c083d3897e4a6243de171f0bf9e6288c6b2816a45c6fc8fca`  
		Last Modified: Tue, 29 Oct 2024 01:00:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfb9549194eee8bb38184759ddad2b4fd6ce44cfa483dc7be3abed1ddf9484d`  
		Last Modified: Tue, 29 Oct 2024 01:00:36 GMT  
		Size: 10.4 MB (10394212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02fb753a33169a856d873ca6e50fddd501d659c5ee598fa7eed3d5053b66973`  
		Last Modified: Tue, 29 Oct 2024 01:00:36 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4435a48ba0801fc926fa00330d348e765ca278f8147b3ea6cb06006da899ca97`  
		Last Modified: Tue, 29 Oct 2024 01:00:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f031ddc4232bee8dabef71a99b6f953b0f7d46e8ebbc9a9a076c49ec13694dc4`  
		Last Modified: Tue, 29 Oct 2024 01:00:37 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d436e6accbe5c573e37b9bc2443d7236a46ecd9b4018efdcdad4a87bc2457d`  
		Last Modified: Tue, 29 Oct 2024 02:13:40 GMT  
		Size: 25.9 MB (25898785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf550b5e6422d682d874c17eee28c9c513cd28f134f44817f0e6ebe38e7c0ad`  
		Last Modified: Tue, 29 Oct 2024 02:13:40 GMT  
		Size: 13.4 MB (13426287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af1592d2ad724916846c084c1253c508f4a7a66bd2e60e34d20ad57dc3dbef`  
		Last Modified: Tue, 29 Oct 2024 02:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b014e6c4f1cf943ea111d8b9205a7540382031711af3d33cd9f85e1c5623213f`  
		Last Modified: Tue, 29 Oct 2024 02:13:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f4233090535c0c851afbb04d35c540a5f8b72212cf5f79e6bf65ab10083eb4`  
		Last Modified: Tue, 05 Nov 2024 20:39:26 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d3fc2d3987876385c36c1db032a4723b57c6bfcc15343e76562140c3fa7702`  
		Last Modified: Tue, 05 Nov 2024 20:39:27 GMT  
		Size: 32.7 MB (32651968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6680ffa977b1d59205066d79a4019f71b4e207957ea1e98f934605eaef184b17`  
		Last Modified: Tue, 05 Nov 2024 20:39:26 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79514f6cc17e36a8d459ff854f4efad72cd20c4473c3441251ba710e870f1e0f`  
		Last Modified: Tue, 05 Nov 2024 20:39:26 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:52394e5e7a0b7fe36a6801f2ccdb8d8be72a35ccf2051409d6b87f9fa2634eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8013879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51df1058f52eca3a9f1dc21758b683ff3f0e87a2847d274f0a6f8febbe076367`

```dockerfile
```

-	Layers:
	-	`sha256:a21ba3c33de153257dd5c241d10ef759ab511838f16db7b810d33ff2242f7f98`  
		Last Modified: Tue, 05 Nov 2024 20:39:25 GMT  
		Size: 8.0 MB (7953045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15e29320c092399cdfca8f4a004cc4e79e4525bac3b531aa0bd0479272534b2`  
		Last Modified: Tue, 05 Nov 2024 20:39:25 GMT  
		Size: 60.8 KB (60834 bytes)  
		MIME: application/vnd.in-toto+json
