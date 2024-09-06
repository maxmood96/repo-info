## `wordpress:beta-6.6-php8.1`

```console
$ docker pull wordpress@sha256:05281815421aa6fdb1d05001a1f25099f2b2b21459e2728096da03264996dbab
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

### `wordpress:beta-6.6-php8.1` - linux; amd64

```console
$ docker pull wordpress@sha256:f4aafd5e0a69a1e9ac82a6bd448bf9d64956f541333e0d6f37b0acb6eac2a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240190263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d7452166b4e0fdf5aa825fe6545a5977b7dbf9ae1a9ada67ea780d49ad85eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c335a1cecf2042cefb300d0412e6cacdaac64e802f084333a622684cb1d64e82`  
		Last Modified: Thu, 05 Sep 2024 01:23:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1356d24f266ec64743f0c51c295266004d42e8335b1038c4f14438de5cd516`  
		Last Modified: Thu, 05 Sep 2024 01:23:59 GMT  
		Size: 104.3 MB (104345555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a67f8d1dfc40864edde3a2f41418653b120eb088d5ffcd3fc1e67832260c4c`  
		Last Modified: Thu, 05 Sep 2024 01:23:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d8e2be6c609f5234e63bf19ce8738505700b3f1f261403385be179e07ea91`  
		Last Modified: Thu, 05 Sep 2024 01:24:23 GMT  
		Size: 20.3 MB (20326804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874a8bbb5229433272e54f3c4b82729caee22bef31d6c358d1c985f774934f9`  
		Last Modified: Thu, 05 Sep 2024 01:24:21 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395851b4c00bb078bf7bdc54b5776fd2926a5002eb8557ea474161621d214e5d`  
		Last Modified: Thu, 05 Sep 2024 01:24:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c856c6370ff6960608a32873390046db94aeda2d9ce90d734d09d2956a61778`  
		Last Modified: Thu, 05 Sep 2024 01:32:08 GMT  
		Size: 12.2 MB (12159409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eff6376384daab6634ff8b0dc5d5697c9611eb027b9c0d836a3537fb3dfefff`  
		Last Modified: Thu, 05 Sep 2024 01:32:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bc116466d6ce79dae7ef7f8eda5a043c8046dbd9b91e50904928a944b4cf77`  
		Last Modified: Thu, 05 Sep 2024 01:32:08 GMT  
		Size: 11.2 MB (11155849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623358c2fc759a87cf013bfb93f446a8ec9c2eb1329eae7be47da2d253227756`  
		Last Modified: Thu, 05 Sep 2024 01:32:06 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce3dd56cf6a33f81f3e545b6fec29dfa5052fadc05e5e78a36e14195ae90d77`  
		Last Modified: Thu, 05 Sep 2024 01:32:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdda0f3dcc8d69efc732c6ffefd5f32cf763fb090e46171268ec7040d17125`  
		Last Modified: Thu, 05 Sep 2024 01:32:06 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64ce150a4699f9c548fc7483964b39b73aa4c4297c9c2c18fbb9a56f0946a10`  
		Last Modified: Fri, 06 Sep 2024 00:04:37 GMT  
		Size: 26.3 MB (26256900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a37b72e78f56c93dd730c0daa91312e5b16bd32d9b0cf2e847de7ac985e62a`  
		Last Modified: Fri, 06 Sep 2024 00:04:37 GMT  
		Size: 12.3 MB (12325262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50fcc2b9affb6f4eff3d3ad650569f371269115ea7b71f1a80312bf451a41d`  
		Last Modified: Fri, 06 Sep 2024 00:04:36 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a0ded6907079431fae560f752062f217d4188daf6b1710ef112b14cfd3178e`  
		Last Modified: Fri, 06 Sep 2024 00:04:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b291d477ab3bc1b4073ad176f2fb8b15f707c7c2185fba6d30dbe8841268830f`  
		Last Modified: Fri, 06 Sep 2024 00:04:37 GMT  
		Size: 19.2 KB (19153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261251a4fef3bdde16b7e4900d2eebe1343b60d380a9d88566c11d43841d6c8c`  
		Last Modified: Fri, 06 Sep 2024 00:04:39 GMT  
		Size: 24.5 MB (24464548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101f89afe44ff21cf6238f0621c3bb8c45ad2bec2b83d468b43735d5ea6ef577`  
		Last Modified: Fri, 06 Sep 2024 00:04:38 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9061210612bf54e2be6b189d87213e2c44fcc1a5a5046274a4850c1a0178e71d`  
		Last Modified: Fri, 06 Sep 2024 00:04:38 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:076f4c4116c7ff56002c8d46b8401b77748ebed5f99aa56806d9dcb796b9bf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8067602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b2631e69869b1d47df73afb731f2335fc07dc4369238e92317b6cc8f4256e5`

```dockerfile
```

-	Layers:
	-	`sha256:c0cdad63e421a1a2718bba0ac3a26be2006fb368175f9001351edf47d0410050`  
		Last Modified: Fri, 06 Sep 2024 00:04:36 GMT  
		Size: 8.0 MB (8007215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695423282deb5b2e799dd655232fae2cec4be0ae7b82a5b141f5f79e0a071707`  
		Last Modified: Fri, 06 Sep 2024 00:04:36 GMT  
		Size: 60.4 KB (60387 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:d8e1797e5cc363d1dea4d0f88b56218f5d792fa139fdcc740cb6899a00ed3bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210879796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb84f12506a77c66b4252a958961f05425bf884f59801309461817469a9677`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf852a9ba86e2887cb6ae81a22fd3cf861010abcf57ae1066ec0b59a523a8a`  
		Last Modified: Thu, 05 Sep 2024 00:04:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc51225fc9b9e1a6df96d433497faacd05a9849b6e148315b9b6ea2063d55e9b`  
		Last Modified: Thu, 05 Sep 2024 00:04:17 GMT  
		Size: 82.0 MB (81995015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ac14ff273c17e96586bdbeac20331d8b9eff59891a0eed04365468f870f6d2`  
		Last Modified: Thu, 05 Sep 2024 00:04:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9f893b68a8981adcc2767d3840423a4802a7813caf48973a2938f928bca3a`  
		Last Modified: Thu, 05 Sep 2024 00:04:43 GMT  
		Size: 19.6 MB (19628100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3e4a76b069f6b8c4241cbc0d1544bf30edc0beee53391fb217fb70cff90839`  
		Last Modified: Thu, 05 Sep 2024 00:04:39 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b60cacfe34030f88f587bddd4f77578f7bfaa6324ad46e45f98319b0642e7`  
		Last Modified: Thu, 05 Sep 2024 00:04:39 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf319c0a207a417048bdbf7c3dba76638bc11a6488f37e71fc5c61e0f939d4a`  
		Last Modified: Thu, 05 Sep 2024 00:12:44 GMT  
		Size: 12.2 MB (12157523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394eb7ce8da5cb9be70af26ac9a9a309969d80bf55ca2cc689e16e55a3f11efd`  
		Last Modified: Thu, 05 Sep 2024 00:12:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd9c9ff3e4b08c8c8d791bfa7015771672e07404e8508a064076149244d2204`  
		Last Modified: Thu, 05 Sep 2024 00:12:44 GMT  
		Size: 10.1 MB (10119203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cd85accbbfd877b74cd335b237eba562098c308d4c1de4b36f59ac5a8625de`  
		Last Modified: Thu, 05 Sep 2024 00:12:41 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641fe0dddd8f765b679d1b5d16d09fac16e7c2924100418fe47f397332ba859`  
		Last Modified: Thu, 05 Sep 2024 00:12:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657f608ea1e2203fb536d2fa9e4dd3fcd850f797f9b9374cef39c0b8d340e6a8`  
		Last Modified: Thu, 05 Sep 2024 00:12:41 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302822488a452d88507295cfb465a50a867cbe4640657a81770fac4af4549c3f`  
		Last Modified: Fri, 06 Sep 2024 03:22:06 GMT  
		Size: 25.7 MB (25705934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af27b3f5be38338bc5c79a3df89d7e421e4fd5da04b6aa2e22e981f31304c4e`  
		Last Modified: Fri, 06 Sep 2024 03:22:06 GMT  
		Size: 9.9 MB (9892638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faeb87677f61e7bc726ce674a8b340e8b2bce74d0d10cb432980db9dd875e43`  
		Last Modified: Fri, 06 Sep 2024 03:22:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c531b276a4311acca5936b0d039495a2e829271a27b7ad777e44029bcb57d5`  
		Last Modified: Fri, 06 Sep 2024 03:22:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6684c675a78dc34c97ba9a2244e98e7544a18f4c41a7d8946874b504e85dc37d`  
		Last Modified: Fri, 06 Sep 2024 03:22:06 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87701f14be531dca8c4cd0cfeb7ac8f10c77b39ccc0537672777b5643d33f25f`  
		Last Modified: Fri, 06 Sep 2024 04:03:43 GMT  
		Size: 24.5 MB (24464526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ce2617e998042e83388bc39ca4bafda542f19d258fbd107f4f68f0e63af1d3`  
		Last Modified: Fri, 06 Sep 2024 04:03:41 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f548a536362ddb909442d2f95cfbc4d5218e5f54309adb7f45307bffb7f7a45a`  
		Last Modified: Fri, 06 Sep 2024 04:03:41 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:1f7d332f77d3ed659de795df201ecd5af0da1a764e7b80122aff14893247205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7874341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027fe166a483de6f792e848270602c73860e1fced343e403aee73da53e1d7d72`

```dockerfile
```

-	Layers:
	-	`sha256:97c3de22ccc31f9faec4abfc33474bdb2b32d52412f573aa5279283a45415590`  
		Last Modified: Fri, 06 Sep 2024 04:03:41 GMT  
		Size: 7.8 MB (7813786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170101ee2cad877765418c4c2f581a8e103d0296e05d565bee4b1378bd79b379`  
		Last Modified: Fri, 06 Sep 2024 04:03:40 GMT  
		Size: 60.6 KB (60555 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:c1559d3459a834882a5d3c4b8f38eb52dfaa3d8802b10d36c40dd2382feb8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200187234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec18736fc4c6b2fd7be7d2180b58ca6e974d899c75b12d174e0774c73c9b6bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52af8d0fa86c9b158af0ab781cb65e065749146b3fe2c329cb4e9d0af8b14067`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ecdfb85b1e01962d1365bfe3926bbbfe42185d9c8b60d0930000a9db914c4f`  
		Last Modified: Thu, 05 Sep 2024 00:26:57 GMT  
		Size: 76.2 MB (76163311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860c94c7af381cee44c718f3a335927de4a439a9ae12847fc214772a3860cd10`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae1097b4dec4fa4f7c19f8af46ce5d5a11f166910ab19a3f03481dcbf2c05d1`  
		Last Modified: Thu, 05 Sep 2024 00:27:21 GMT  
		Size: 19.1 MB (19065552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058c6166ff928aaba746c5eed7f88c59d3291587055d2c72a797d2822575c866`  
		Last Modified: Thu, 05 Sep 2024 00:27:18 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5148041e15e73d623fd28b30026d084e8ab19285799c3ea4739efeabdbb429c4`  
		Last Modified: Thu, 05 Sep 2024 00:27:18 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adba8d6d7fc727ed621c075d07a47ffeb6a440edc4600ec95746f4fbe8dc6ed1`  
		Last Modified: Thu, 05 Sep 2024 00:35:29 GMT  
		Size: 12.2 MB (12157492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8641214d5e3ca4107985d0fcecbb6fec08b75eafc0a7378313d2cdae85826068`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706911532f5f3999ae50050ab1170f8d9e60c86e047e104a5b8d48783d21a066`  
		Last Modified: Thu, 05 Sep 2024 00:35:28 GMT  
		Size: 9.6 MB (9583383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be06055cc9ee4e5949d74d4bf948a8a803155509b724467ca8b903202a272ee`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c749bbef9b21a50ffc2eb805c18284196379886f00696779f4d21ae2662d9a`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946af6261b0a01d4eca0e16ad21696667f1f54b6e322b0b2c3ddf139479852c8`  
		Last Modified: Thu, 05 Sep 2024 00:35:25 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3549c7a4e85d30c6252b1376ff59416a2064bc6a861f1adc19b5153b170a9d6`  
		Last Modified: Fri, 06 Sep 2024 04:17:51 GMT  
		Size: 25.1 MB (25074018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7309119468b365d892e9ff50c9a51c8ae78dabed77604004adae309ec0cdcd8`  
		Last Modified: Fri, 06 Sep 2024 04:17:50 GMT  
		Size: 8.9 MB (8931215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaac1280ac934fc3c05b61b05e0a3a4fd4cbf018b6d97de987689d8727bdcb07`  
		Last Modified: Fri, 06 Sep 2024 04:17:50 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6da4d5c2dd8ce1b5ba504f13dc78d742ed92d1c85862acdb930e785b02bfa4d`  
		Last Modified: Fri, 06 Sep 2024 04:17:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a48632ae13282fd6216b53d8b4865d725b6382dfcb22fe7384ab56b88ace6c8`  
		Last Modified: Fri, 06 Sep 2024 04:17:51 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4931ae50cbe574f73ef540634f69b177ccb46399356387cc56a195eda0c115`  
		Last Modified: Fri, 06 Sep 2024 05:44:00 GMT  
		Size: 24.5 MB (24464542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2935da0f9ec7083ec4b2f904d8e2e1dabb29942fba1f151e0337e9184b41d5`  
		Last Modified: Fri, 06 Sep 2024 05:43:59 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f568e37212c19afac44809cb9bbcec6e02b4701af62931dd76bfd361cf8766db`  
		Last Modified: Fri, 06 Sep 2024 05:44:00 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:1f3d584d8ef88630862dc97064efcada7d9a26ce7e6722dddecd80b3eb60fc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7878887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb4d13033b02ae771714e4ce83246f3c1ce07a27450e244d3b4e69bfbf021fa`

```dockerfile
```

-	Layers:
	-	`sha256:d8d18bef19335a97040d642f14ff2fc3853b1b3d897ba6e723a45d277cee9631`  
		Last Modified: Fri, 06 Sep 2024 05:43:59 GMT  
		Size: 7.8 MB (7818342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6e0ffa36b628253bb9d488a91967f2192ffd615706dc825225041633abcbc34`  
		Last Modified: Fri, 06 Sep 2024 05:43:59 GMT  
		Size: 60.5 KB (60545 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:25589916b766aa5e95726d707af37300fa96144c49668c163653f3e20fd6730e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231527271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c5cf2ededa79a9537a1ecee9d85080a13eb1894622e9e4c1e417ca04d107f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125f50077837c519800d65edc67294c009e30fcc820455fbefc671b63081421`  
		Last Modified: Thu, 05 Sep 2024 00:18:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15c4686903cb5bbd6cabc5447788b26574756d94e02c0952258c66bb2b4379`  
		Last Modified: Thu, 05 Sep 2024 00:18:40 GMT  
		Size: 98.1 MB (98131394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8893eb8a52e8af8365ae670e2549bcff74923def7137abb8dbd4657905297f01`  
		Last Modified: Thu, 05 Sep 2024 00:18:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55da0753dad27fbf674997a6a04397736c543162afcaccd636738da352c108`  
		Last Modified: Thu, 05 Sep 2024 00:19:05 GMT  
		Size: 20.3 MB (20325421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a3e15a12625719622136bcd7ea9d8c614ad174f11b4e5d64ee1a0e103a7c94`  
		Last Modified: Thu, 05 Sep 2024 00:19:02 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70c9882f3f52155ce9e7d769b5539a7fdb5eeab8c65342778b58511aabe9dd3`  
		Last Modified: Thu, 05 Sep 2024 00:19:02 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8bc477c0b4ebcd99bf4025637668563f54849c3309613389f8851f747ccd0`  
		Last Modified: Thu, 05 Sep 2024 00:26:51 GMT  
		Size: 12.2 MB (12159054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71368ad6d04e5375760a94508d5f2bcac930d31ac8ca5e71aae02dcb2b72444f`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b2a521335cd2fa30f5ae615c162522c73dc5d82548de4ca83cdfd3e712d34`  
		Last Modified: Thu, 05 Sep 2024 00:26:50 GMT  
		Size: 11.2 MB (11154472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d7960f72e390a428a0d15529e4724fac767ff7ac0e54b2ead95a52d5e0c2f`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900f27d2e1d2d6483465657a26ef8697582c839d23ae081249cfe389bd9cf7d2`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58049867589abcac9f2348e6c1e8905ab34c66288ee702a23bbee7d62d2a9be3`  
		Last Modified: Thu, 05 Sep 2024 00:26:48 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e31e14a95caad0780d758442c45bad7b13aff6c5f3355ae15a5bf76e29f4f9`  
		Last Modified: Thu, 05 Sep 2024 20:42:12 GMT  
		Size: 26.2 MB (26172518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34326f2dd44db0e15c256f3ea17041c0dfbd737fdefd729c6218b012fe1fa19`  
		Last Modified: Thu, 05 Sep 2024 20:42:12 GMT  
		Size: 9.9 MB (9933878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2d236a5bd75e67ba6fa081d522a82d304632b04b7e5433cfa364de14827918`  
		Last Modified: Thu, 05 Sep 2024 20:42:11 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975c633ffe996ec75c5f06412435b606972dba0929ecfc91095fd50707be2588`  
		Last Modified: Thu, 05 Sep 2024 20:42:11 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6c4bd98c9255447234bd1dd2b2183a1022754a6f1821d7fd63fba6cc4ac7b5`  
		Last Modified: Thu, 05 Sep 2024 20:42:12 GMT  
		Size: 19.2 KB (19159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b147d58b2522e9fc1de951d0b2768e2222a07140f31788b829be05333625f9`  
		Last Modified: Fri, 06 Sep 2024 00:05:57 GMT  
		Size: 24.5 MB (24464544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d005d1ff03debba71c9b8168462b9f4245eb64c24056d7a905daf8db8247542d`  
		Last Modified: Fri, 06 Sep 2024 00:05:56 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a0c904215f5979cccd5f5e7c13523af4f44ba87bf2e5310892d9a91494e92`  
		Last Modified: Fri, 06 Sep 2024 00:05:56 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:d1721e97cc5543cc3b4c2b445db6bd11e9ab6da68e071495a6239dafcc52af3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8096764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfedd0ffa417498d9dc8973e4ababd4f9771b53633ece63f75ed82b9bc81aa49`

```dockerfile
```

-	Layers:
	-	`sha256:b150176dd2d755c151be03af328c5b1a7623d6260090c36432a3ed102644c600`  
		Last Modified: Fri, 06 Sep 2024 00:05:56 GMT  
		Size: 8.0 MB (8036017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5845724ff7a4a42e0a38b50ef904197336a9a5c5a5aaabe31bbd0fcaa58ba8d6`  
		Last Modified: Fri, 06 Sep 2024 00:05:55 GMT  
		Size: 60.7 KB (60747 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; 386

```console
$ docker pull wordpress@sha256:83f555389de2ab32b98b13894e34bd0c6fdf2553038c340ecb86d900c626b5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238631206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a934ed4993eb60f06f9facf6c58de03c9af7d689fa9f7da230e078398568e0d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d31e4426139e19c94ca0942df7023cf26932c267261b263dbd848554444817`  
		Last Modified: Thu, 05 Sep 2024 03:02:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c70cae078252759f892081775f43cfce9b4bca811fa4ee5046fc050063c4cf`  
		Last Modified: Thu, 05 Sep 2024 03:02:34 GMT  
		Size: 101.5 MB (101514423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5066486db10391a0fdfecfd181c1c0ac73eefce83f0210b43e3ba3f66cc2c0`  
		Last Modified: Thu, 05 Sep 2024 03:02:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2676b77310bf32695326d895410b9443408ad96744b377fe197360e0f7d6956`  
		Last Modified: Thu, 05 Sep 2024 03:03:00 GMT  
		Size: 20.8 MB (20843985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912fe8524961caad6c13e9f835014cb80b3fead26e3a772d64634a245f8479b6`  
		Last Modified: Thu, 05 Sep 2024 03:02:56 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e5c9b5f4f66032631cb84b8caa4dd8cdbd247ce2dcb95b2f48718b889832b0`  
		Last Modified: Thu, 05 Sep 2024 03:02:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd5a0e83348f40cf64c382aa41f30106a84fa9b9f8b450272d176cb2b128fc0`  
		Last Modified: Thu, 05 Sep 2024 03:11:45 GMT  
		Size: 12.2 MB (12158494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377060fe6f0fb1a51900a1b6520b2a8828e161b943cf8acad33357107b9b9d62`  
		Last Modified: Thu, 05 Sep 2024 03:11:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca7a1ae4ffa3acea625851b3450adb8375bc75f48740a5eaf4951f641d0ec4d`  
		Last Modified: Thu, 05 Sep 2024 03:11:45 GMT  
		Size: 11.4 MB (11379871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb0a2fe787ec8864d16f570e873dbd4d1d30eefaa98cb763eaae4e4d749a8bd`  
		Last Modified: Thu, 05 Sep 2024 03:11:42 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4687b5463ac8a27641db751567c5f3478f923866ac311d6c3df4a8917641fd`  
		Last Modified: Thu, 05 Sep 2024 03:11:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577f758719e6ad0059cf1848d3d5bbc964ea0cdf0373ac6453b57aeaaed7229d`  
		Last Modified: Thu, 05 Sep 2024 03:11:42 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceeab50b7ef71b1e398e3ed03b9b9634545c8777e835982128a6e57db72bec5`  
		Last Modified: Fri, 06 Sep 2024 00:04:49 GMT  
		Size: 26.7 MB (26695458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a39f2277161707d0392295c3cdee394a76c7b30919c9932dc0434b411a926d`  
		Last Modified: Fri, 06 Sep 2024 00:04:48 GMT  
		Size: 11.4 MB (11400705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c2a983f0e483153af32004396814eff5f728567aad51035a9d034c6497d561`  
		Last Modified: Fri, 06 Sep 2024 00:04:48 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e24798bc99d8915749dba5f1a88d77e3cfe21b6348177899ea924e361f57c6c`  
		Last Modified: Fri, 06 Sep 2024 00:04:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0cbcb3a7bd69d61fea5298e1c108dbad5e492454535b4d80ecbc7811c4a8bc`  
		Last Modified: Fri, 06 Sep 2024 00:04:49 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd26ceffb6d8f87282a24a8f440475aa2b5d8bbce3cb321968588bee365232c`  
		Last Modified: Fri, 06 Sep 2024 00:04:49 GMT  
		Size: 24.5 MB (24464524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f66baf3c176cfdc3dc2f884a838c0045f3b77838987c4a319348a5107f7400`  
		Last Modified: Fri, 06 Sep 2024 00:04:49 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04152344fa3dcc665f9e19b4851404f7985746df5c3a9cc53df792f12dc111e`  
		Last Modified: Fri, 06 Sep 2024 00:04:49 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:7272b7ffd157c2c29cd9d35889166737652b6c65b0973160a0e5e3dd470c952b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8047364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff4c2c9e5695d03d7164683dd08e221bb6724703d88a87dc9df116f51522617`

```dockerfile
```

-	Layers:
	-	`sha256:13ae5e3f6d144d7bc7a9a7b5cdde04ca18948377adc28d4e0ba9a419e3f138dd`  
		Last Modified: Fri, 06 Sep 2024 00:04:48 GMT  
		Size: 8.0 MB (7987045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a518a65468e4992a423ff7d6b2495857cc206872fe1ba0f82832e7395e003b8d`  
		Last Modified: Fri, 06 Sep 2024 00:04:48 GMT  
		Size: 60.3 KB (60319 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; mips64le

```console
$ docker pull wordpress@sha256:7bd7ec00d9ca31e6a7da26f5cc530682e52aa64ba3f619166eaa0e1217ece54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212000006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4136ce27291daf82d0f586d4f41d4ad57209742a4a2261db5471dd4f4036f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd61d7a0bd26fdefd1fc3f6685c32109220be495dcc46fe17919766e554de48`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1187d9c88570478f80b55a3e07d23bb40e2db5e9069089775ddb5d5a54f4af4`  
		Last Modified: Thu, 05 Sep 2024 03:52:27 GMT  
		Size: 80.7 MB (80667470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b165b263f070f18c828e0e5ed25251a1e38f37f96ea4eb4a5727bbc912240e5`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cf2db0d07ff107e570d1ad64e608d226d0998d047f4b4dc832bce52d785789`  
		Last Modified: Thu, 05 Sep 2024 03:53:14 GMT  
		Size: 20.1 MB (20069958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd9315d8d0d2454284a0444c9ce8871c9375f6576538cae76de0a5e2515df52`  
		Last Modified: Thu, 05 Sep 2024 03:53:00 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3803187dbdba9cb9774d484104df9298d89b63ccc059c603dd1baa1e7b0656e3`  
		Last Modified: Thu, 05 Sep 2024 03:53:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4531024b8dcb8e3ec5e01ffe517050974bc71feb14c84cba109e840f492060f3`  
		Last Modified: Thu, 05 Sep 2024 04:02:21 GMT  
		Size: 12.0 MB (11952507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba10a04952439f01dee488052aed46d218de7cb06fbe580f6647c34cb09790`  
		Last Modified: Thu, 05 Sep 2024 04:02:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59259a7d5de1cdac286b8e68d9a7bd37786770ce8bae3a39cd058de3ac6550b`  
		Last Modified: Thu, 05 Sep 2024 04:02:24 GMT  
		Size: 10.2 MB (10228041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b35190c3c9394e4191272f05ac3e7b939bc1715a28d2d00f674867c60f9895b`  
		Last Modified: Thu, 05 Sep 2024 04:02:16 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c3cbe206cade0d43107d968801df4f1c2fd633bbbcae05b18997c16f8a2a30`  
		Last Modified: Thu, 05 Sep 2024 04:02:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a665bd2f074c1b6d26e0ae489edcd69a691776f13650602acfbf5bec7c000139`  
		Last Modified: Thu, 05 Sep 2024 04:02:16 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80d5ca956e21e33a936cb6964a46d949e8c69c304fed0ddb40c9e4b6b77618f`  
		Last Modified: Fri, 06 Sep 2024 06:44:56 GMT  
		Size: 26.0 MB (26026556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9265ed0882e117b1a6582ac8d24ec82b55fe97ee3ef3756775cec05220f368cc`  
		Last Modified: Fri, 06 Sep 2024 06:44:54 GMT  
		Size: 9.4 MB (9436407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596dd0630d412a01199bb02e76c8def474e46d52525b1baa43915dd03f0a3b3a`  
		Last Modified: Fri, 06 Sep 2024 06:44:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895cfc7ca5d4e99bb989f434a42044fd069ca36fa343a3b87f2516103569f26`  
		Last Modified: Fri, 06 Sep 2024 06:44:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134795522bb6efb91d1d45c538e183ebfb7259b661208b778d5f7db28365332`  
		Last Modified: Fri, 06 Sep 2024 06:44:54 GMT  
		Size: 19.2 KB (19177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae469536cb033548bee7dae4baef78fb20edc5ee71f4265a8bef94a1f63c7b8a`  
		Last Modified: Fri, 06 Sep 2024 07:54:29 GMT  
		Size: 24.5 MB (24464521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96137e91e10b7391428f03c5128871c5135f34d493cf746a671eb9ab2b52926`  
		Last Modified: Fri, 06 Sep 2024 07:54:26 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd9f56146ee15e365efff15f5c72ab8ef33cb6a6b0c30cd29af0adef99c64b`  
		Last Modified: Fri, 06 Sep 2024 07:54:26 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:1cc80644f53788eb7fe48fa4d73851a6813567fbecdfc65e8585c35c238175db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 KB (60279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1027ba71305458b98ccc84d5e44dd933dddafbde661a62dea1a49e8f43e0c9f`

```dockerfile
```

-	Layers:
	-	`sha256:a7fbb6aec40b6599055f4014859a581807626c691a4207602f3f03139aeb0e8c`  
		Last Modified: Fri, 06 Sep 2024 07:54:25 GMT  
		Size: 60.3 KB (60279 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d5038e448bbc216f8d2df7847a2d5d1fb45e581b6609d14a1cbbfc51f498b428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244695661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ba25656b83dab926840cf1dcc3cddd1e55c6994835efce7256fd3d82441bf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:03 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 13 Aug 2024 00:22:05 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:39:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Aug 2024 01:39:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Aug 2024 01:40:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:40:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Aug 2024 01:40:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Aug 2024 01:44:02 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Aug 2024 01:44:02 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Aug 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Aug 2024 01:44:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Aug 2024 01:44:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Aug 2024 01:44:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Aug 2024 01:44:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Aug 2024 01:44:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Aug 2024 03:00:36 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Aug 2024 03:00:36 GMT
ENV PHP_VERSION=8.1.29
# Tue, 13 Aug 2024 03:00:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 13 Aug 2024 03:00:37 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 13 Aug 2024 03:00:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Aug 2024 03:00:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Aug 2024 03:03:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Aug 2024 03:03:42 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Tue, 13 Aug 2024 03:03:44 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Aug 2024 03:03:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Aug 2024 03:03:45 GMT
STOPSIGNAL SIGWINCH
# Tue, 13 Aug 2024 03:03:45 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Tue, 13 Aug 2024 03:03:45 GMT
WORKDIR /var/www/html
# Tue, 13 Aug 2024 03:03:46 GMT
EXPOSE 80
# Tue, 13 Aug 2024 03:03:46 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06653ef71f82635296232203a5165c5573c2ead3963166842f72ee2a3b2ef4e`  
		Last Modified: Tue, 13 Aug 2024 03:23:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e565883e2d514a28111a5bb532a2c842a23c71a73d5a88f1d87566e472a04b`  
		Last Modified: Tue, 13 Aug 2024 03:23:39 GMT  
		Size: 103.3 MB (103319337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dd094f1396f39e170f27f825f146fac685f7f6c98e96dc3af4a9675ed1de0f`  
		Last Modified: Tue, 13 Aug 2024 03:23:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa3ca15eb05617f3fb56f26b2011e9c3e3930d65e0fba916ba735a144470e5`  
		Last Modified: Tue, 13 Aug 2024 03:24:04 GMT  
		Size: 21.5 MB (21511456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78475374afd50b36b1d50d7e76b0013a5b44451e299b7322c2a44d1e1142ddd`  
		Last Modified: Tue, 13 Aug 2024 03:24:01 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dbc90c71b4b31ceaaca56bb2014a554dfa1b01129d862cc2c94ed38e3d0c5c`  
		Last Modified: Tue, 13 Aug 2024 03:24:00 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a655fdd09357773699f2285fe25be391b4d3c16d93633179040c6327ba31938`  
		Last Modified: Tue, 13 Aug 2024 03:32:19 GMT  
		Size: 12.2 MB (12158806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f01328a8ccb3a0dc782b05e852944a216092c51254897f9ec28432ba845f549`  
		Last Modified: Tue, 13 Aug 2024 03:32:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f3777154ba77731b7837b6199f772d60e554a59b90d36223d4985fdb21795`  
		Last Modified: Tue, 13 Aug 2024 03:32:19 GMT  
		Size: 11.5 MB (11526437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac40fa160d54ddfce359c61b9308d3b17a0f6f920cf872e3e68bdb9f2d253b8`  
		Last Modified: Tue, 13 Aug 2024 03:32:17 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7911055755a07bb5fec32e5f361b1883894452394b7cf963e0b9b69b0e547709`  
		Last Modified: Tue, 13 Aug 2024 03:32:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c85a67d85bbf68beb3ab134b16e966321c7df65a45fcee9d5f713bcafb3516`  
		Last Modified: Tue, 13 Aug 2024 03:32:16 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddb6535334e929cef5634debb182063135b1045b504881db0e6417efcc28091`  
		Last Modified: Tue, 13 Aug 2024 21:53:36 GMT  
		Size: 27.3 MB (27338693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92b44d5ad9fa16cb7d18ead6cdac63505fdbfeda8581157781eced77fc47993`  
		Last Modified: Tue, 13 Aug 2024 21:53:31 GMT  
		Size: 11.2 MB (11224614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32b6da5bad880b0b405a2211fb89c5c0d4cc9a5d7bbcab2fd47b7bd051af6d5`  
		Last Modified: Fri, 06 Sep 2024 01:15:47 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4f8c091b39c351300107d2c5e1e3b18d5d070037404a6171258d88bc26b6b4`  
		Last Modified: Fri, 06 Sep 2024 01:15:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ffe0246fb00985431360eb3372e52e0efb1e472affd943f8a949b4db4ee0f4`  
		Last Modified: Fri, 06 Sep 2024 01:15:47 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5b699cf8fcf9624163bf7a5164275225f8d1e0aa955da2d975ff4358f6240`  
		Last Modified: Fri, 06 Sep 2024 01:15:48 GMT  
		Size: 24.5 MB (24464550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc78821eca949869020e12bdf4d0dd23b6c3d4160c3607c617214a9aa536d80`  
		Last Modified: Fri, 06 Sep 2024 01:15:48 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba0c12dd8e4836dd6d302b39d4defa665746274ce95b166f0d7d3aecbda402b`  
		Last Modified: Fri, 06 Sep 2024 01:15:48 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:7da2b3090c588d0ae242825fc79423386b0ab04465d574106551deda2652a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (8046349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd3b6d4467f83f64c476408d0e28b964b624d61b6af0a732a72f93873fb8182`

```dockerfile
```

-	Layers:
	-	`sha256:0cac8e418e6855406f017ebeded1a4dd69207a80d48fe2c5d5d26a5a962ee264`  
		Last Modified: Fri, 06 Sep 2024 01:15:47 GMT  
		Size: 8.0 MB (7985877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb963f990f19de3c070ed20936bfef3cd869ab322d0538c4d5ffa3b109380c28`  
		Last Modified: Fri, 06 Sep 2024 01:15:47 GMT  
		Size: 60.5 KB (60472 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1` - linux; s390x

```console
$ docker pull wordpress@sha256:3904138058c89ec1810214d582e3f0e2988419c3d93e610d074d7be217003850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210794643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f462ce8311d6efcf66cf7b5fbae7237ef248492fb747e7215d799cd2bf2df08b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 04 Sep 2024 19:03:11 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 04 Sep 2024 19:03:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Wed, 04 Sep 2024 19:03:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 19:03:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_VERSION=8.1.29
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Wed, 04 Sep 2024 19:03:11 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 19:03:11 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 19:03:11 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Sep 2024 19:03:11 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Wed, 04 Sep 2024 19:03:11 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 19:03:11 GMT
EXPOSE 80
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
RUN set -eux; 	version='6.6.2-RC1'; 	sha1='bd7048a400d418783114485589f16ce8d96b25f2'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
VOLUME [/var/www/html]
# Wed, 04 Sep 2024 19:03:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Sep 2024 19:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Sep 2024 19:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9c3e85da8b09b5b347e0de23df0ba14b87db8c71b84ff72bafeff05ac4c45d`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d162a779ea2f70207f50c43a8ea8a2afc36c812e56c03883aef22591b1fadd`  
		Last Modified: Wed, 04 Sep 2024 23:43:27 GMT  
		Size: 80.8 MB (80817858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d512ffc352f972eede4ede7944fbab31c430f84671da665932f51478717b92e0`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da7cad6f7a39f230d1e8de14363803877b8b1c89328c737be2154969bd6f8c`  
		Last Modified: Wed, 04 Sep 2024 23:43:43 GMT  
		Size: 20.1 MB (20099476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e25d89a6f279f62c6f2c2b233479dea22c0d2c23888634ff212bbda2c33066c`  
		Last Modified: Wed, 04 Sep 2024 23:43:40 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1efd0f24c30aa86b4c75e8ddb0e50a36663b9a80a3d8339de48eded5ecf46ef`  
		Last Modified: Wed, 04 Sep 2024 23:43:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c87aab69585cd731ba0cbce6703da5b0ac03ddd5be5ccbe78cd37a5c8bb229`  
		Last Modified: Wed, 04 Sep 2024 23:49:10 GMT  
		Size: 12.2 MB (12157797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7b3f54beb30faf5b5844577eaf61174138f0a6d39311d094285b609369e51b`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c47e914ec1fa7e0ebed85c893617723034ee4227919c74f66e9bf05ebe94e8a`  
		Last Modified: Wed, 04 Sep 2024 23:49:08 GMT  
		Size: 10.4 MB (10395876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e66f21d2de16ac2e80b9af7ed9e5d206f76263368f5fd892cf48522b2df85a2`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788790c8a59ccddea6a0d80a3afcbd81963ec16c7aaba13406e6836f56250cd7`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70833864b28db30205b966daa9e38c1e16aec9359e003e26b055c947e65ec8d6`  
		Last Modified: Wed, 04 Sep 2024 23:49:06 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f5c4eb8bdc4c0900f278c298a9292329b94f3b9c90e520c1c1277143b3e138`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 25.9 MB (25899075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ad54cad0ed9f2dc7cd1cd69de5a4026d73761014dd6f923e4d61d607763f99`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 9.4 MB (9440246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cc22693466b58bdc0e02c115bdafb519e4fe92e5f5862179b3022f37283903`  
		Last Modified: Fri, 06 Sep 2024 02:33:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d757e919733e7a74096f0fab9ff26c39fba2d9ed021d57eb29db623aa0322ca`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47efd7bb9b1dfaa32f0bd9a96efb45a06283501c2bbd9b690d311a3dbca1ded`  
		Last Modified: Fri, 06 Sep 2024 02:33:07 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4407e2b061ee98ef3895f0dd58e1a5d860d816884958aa6e4b3f5b8d96b021c1`  
		Last Modified: Fri, 06 Sep 2024 03:55:16 GMT  
		Size: 24.5 MB (24464534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8863b3c79ecc443819952860e539020e860b9801bd4297a13480fb331a9a927d`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a3ccf4efaec2286e4cbd58558dc265cc704ff501b17a38c0758fa35880d650`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1` - unknown; unknown

```console
$ docker pull wordpress@sha256:a537846930bd1d4159929ba96fb86586935beb9bdde3976428d632f2a593a912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7898375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045dfd24b52d54111c52f4dffdf035cfb777cba1b81d19c4bf4367dc9a8abe43`

```dockerfile
```

-	Layers:
	-	`sha256:b3bc58eb3c348b514cfb495735ff3e20270e131b6ac7fde17a303c91625020f7`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 7.8 MB (7838003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0815e9c788dd4a23d4e67712926afa306f5dbec8802e954af326e5db9eda055`  
		Last Modified: Fri, 06 Sep 2024 03:55:15 GMT  
		Size: 60.4 KB (60372 bytes)  
		MIME: application/vnd.in-toto+json
