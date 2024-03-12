## `wordpress:beta-6-php8.3-apache`

```console
$ docker pull wordpress@sha256:7362952fef2461d6e890dbbc0e3cdf36b01e45aacbe674765fe45e8b28319371
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

### `wordpress:beta-6-php8.3-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:3816fb8d44385737a2ec0bb6ef05c9d764348fc5e4b0eeeeca7594a72e0f2e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257988564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5317db27a124160b698731996845c8d5a700023bf35b2c1e0d565cfcbed19b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Mar 2024 23:23:48 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 11 Mar 2024 23:23:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 11 Mar 2024 23:23:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.3
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
EXPOSE 80
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["apache2-foreground"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de14226e1706b621fe796af63b375db247a2490752558ed4f5ea40648234129`  
		Last Modified: Tue, 12 Mar 2024 05:25:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aaf617d1d2bc41efbec77e9f05370e6f35d8f4363fb26fa04883ec538b7d66`  
		Last Modified: Tue, 12 Mar 2024 05:25:37 GMT  
		Size: 104.4 MB (104355586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba065e262ff15c57d91609cae32d80920edac1e9b0826e0d8cf5f0f3c60107`  
		Last Modified: Tue, 12 Mar 2024 05:25:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ecae067f5d5cbf3c2a3cf42d5677472bc8cc633b8ccea33d011749bb84661`  
		Last Modified: Tue, 12 Mar 2024 05:26:03 GMT  
		Size: 20.3 MB (20303886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f1b407f7499799755557f8769bbeb98d0573d6092913d5303cf951acdace0b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1b2cfb806df514ad4cf5cffa00c66aaa6322c1ef8f3b1c597592771925569b`  
		Last Modified: Tue, 12 Mar 2024 05:26:00 GMT  
		Size: 512.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfb5bfbb419b0c504a2d6ea61c7799a089a88f25d18c9719bd1c82689e9a46b`  
		Last Modified: Tue, 12 Mar 2024 05:28:47 GMT  
		Size: 12.8 MB (12797394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63270db9abcfe9136a948a2e80ba993666529fa0e5e53650f2af8541e486021`  
		Last Modified: Tue, 12 Mar 2024 05:28:44 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daf799111e1cacd5653596647f1a29996d0d2e048a5ee9ccbf3e705b6d97d6c`  
		Last Modified: Tue, 12 Mar 2024 05:28:46 GMT  
		Size: 11.6 MB (11634643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fcab20224c2e037b0af205548670b497c0e5e3b076af1ed5d62181c7b492d`  
		Last Modified: Tue, 12 Mar 2024 05:28:44 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c1c039414eab873829924352e257a6d7fe52e8960b2d6cdd9be0ee0d85e4d7`  
		Last Modified: Tue, 12 Mar 2024 05:28:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd458eb15c3de4d7a72a067265ba33f837efebc69d9e4e0f9a8a52907efec76`  
		Last Modified: Tue, 12 Mar 2024 05:28:44 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67a7e5e6933217166150322217e3bd214ac20bef4e2a9a3925e1e0febc5d70a`  
		Last Modified: Tue, 12 Mar 2024 06:59:08 GMT  
		Size: 26.3 MB (26254048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc5c2c2e84a7c56b52187d5b83d18137785afea7d2f7dddc10cd6e89f6b0702`  
		Last Modified: Tue, 12 Mar 2024 06:59:08 GMT  
		Size: 29.0 MB (28970063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df759f67fafe151cc0c7f8b0c489e67cef1e6cbf5aa6b2b7bc0c3654406f3d6`  
		Last Modified: Tue, 12 Mar 2024 06:59:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea744f136f8e18d417094e8358ff867bb67173b566b49e856aa6521ae4c219a`  
		Last Modified: Tue, 12 Mar 2024 06:59:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706ca504036d02b1c73a28bdb38c775a95cf48be7bedb894ae5e060c46ac1e5f`  
		Last Modified: Tue, 12 Mar 2024 06:59:08 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc3b4ba32bd9b5d7a23bcdc200b4f2b29d6ea63428856fd06ed76cc9b142bb`  
		Last Modified: Tue, 12 Mar 2024 06:59:09 GMT  
		Size: 24.5 MB (24519207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59207f3a3a1e3b9fb9e48746aa52977e9e5fddc133f77f7180f8be50a40214`  
		Last Modified: Tue, 12 Mar 2024 06:59:09 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f609e12e28821b6533b153996a7ad55eec21d9182f7ca448c8522d329fdb4`  
		Last Modified: Tue, 12 Mar 2024 06:59:09 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:9ad0d1cc0edd5a37fdff2e222745b90cc2115e3a3ac113fa7fc4aade5909b6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9026213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcf3fad1545c5f39f07ff9a3edca91fa275368807ad4b9f8c96d88669ff94cc`

```dockerfile
```

-	Layers:
	-	`sha256:3961d239fb25a71bc1236da73d6c651e50a86c537956e8b74c3b7e7a96cd9ab1`  
		Last Modified: Tue, 12 Mar 2024 06:59:07 GMT  
		Size: 9.0 MB (8964493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1b048ebc5e6ace1206b05c83971324f032085f975d61c51c2f46a7fee7b425`  
		Last Modified: Tue, 12 Mar 2024 06:59:07 GMT  
		Size: 61.7 KB (61720 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:aeac2a66a90899ddbb92c4770a69a7117a0593acb9cd0323bacd6f7852dc41fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228470525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb29da733bc8ca5f818717f2651254821f6bc8111029575ebae13de9146d22a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 08:07:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 08:07:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 08:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 08:08:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 08:08:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 08:15:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 08:15:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 08:16:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 08:16:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 08:16:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 08:16:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 08:16:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 08:16:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 08:16:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 19:51:50 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 19:51:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 19:51:50 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 19:52:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 19:52:06 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 19:55:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 19:55:58 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 19:55:59 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 19:55:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 19:56:00 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 19:56:01 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 19:56:01 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 19:56:01 GMT
EXPOSE 80
# Fri, 16 Feb 2024 19:56:01 GMT
CMD ["apache2-foreground"]
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Tue, 05 Mar 2024 20:03:11 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 20:03:11 GMT
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
	-	`sha256:4df3c8b8c67c2ba87931facda10b26b5cbdc94ebbd76a7a8a8bd8b93f965037b`  
		Last Modified: Fri, 16 Feb 2024 21:01:35 GMT  
		Size: 12.8 MB (12795582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9c503e752545737e8e8666282f8d1614faca6a7ddcc67028d692a2bc762d0b`  
		Last Modified: Fri, 16 Feb 2024 21:01:32 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7fd62792759153da85da0c4b651b9bdb3f0c7c1f338ee69f1f5993b1f14497`  
		Last Modified: Fri, 16 Feb 2024 21:01:35 GMT  
		Size: 10.6 MB (10604715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd7cd942be0f365c0fc256fe2278732bbdc1ae2ff8e303a94d220b04eb129e5`  
		Last Modified: Fri, 16 Feb 2024 21:01:32 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bbb613cb26e9573f9fd5539c637fefdd41f96c58e12a8dbfc2ea7060b5a26c`  
		Last Modified: Fri, 16 Feb 2024 21:01:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccd84c2a28a4120bef41591aa8a95be3b053334939c30e3222a84f5fd39f07f`  
		Last Modified: Fri, 16 Feb 2024 21:01:32 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4112f4f874ebdf3bbe8d2e3fe00866f986ba72aae6eabb0308117338fe045b67`  
		Last Modified: Sat, 17 Feb 2024 02:06:38 GMT  
		Size: 25.7 MB (25705645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418fcedc10d06b55bfe2340e08d75cd407347cbf92b64f5cd25a2bf4bd2ce210`  
		Last Modified: Sat, 17 Feb 2024 02:06:39 GMT  
		Size: 26.3 MB (26323922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca41a692e54298665d5a45a96b9ed478ba981f7e1f5de08cec76477b959ecc`  
		Last Modified: Sat, 17 Feb 2024 02:06:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b26a6f307dcc3d74b7c64a3532ffe92a169f76c750f20ed3a095244666e98df`  
		Last Modified: Sat, 17 Feb 2024 02:06:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83031ccc0f2cb08469e4f8ec463eb24911c9c3cb4702359f413652cfcdb9967e`  
		Last Modified: Sat, 17 Feb 2024 02:06:39 GMT  
		Size: 19.2 KB (19160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cc0bac20751a3436649daea197133f25f72e4ad16e7be08b87efc3bbe80cd4`  
		Last Modified: Wed, 06 Mar 2024 02:28:12 GMT  
		Size: 24.5 MB (24519208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd870baaffda0691a0c00973bca5e3bfd3ac39c3c7c82346fa02fbeac417138`  
		Last Modified: Wed, 06 Mar 2024 02:28:10 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543ad0f8bae0a37d98fa6c3ae6c21d1c6fa5b9511cdc2158a5dba20377eb92dc`  
		Last Modified: Wed, 06 Mar 2024 02:28:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:ebd50555e09640b7c934e93e2d032371d90b1c8d1b94a97a2743f20526623f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8829791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200efd12473486e15261bc3c27d1aeca1e43831efd6904956d7ce461c6dfe125`

```dockerfile
```

-	Layers:
	-	`sha256:72021548ac25b2a5809cb47843002321ac18e5469a57f7cb8d81a68f6102e7d9`  
		Last Modified: Wed, 06 Mar 2024 02:28:11 GMT  
		Size: 8.8 MB (8772076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b7df2e0a7fb0653b9f503e1b2a3c9d83e886679271d444519f724422c51d76`  
		Last Modified: Wed, 06 Mar 2024 02:28:10 GMT  
		Size: 57.7 KB (57715 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:a59776411c776d94e41b584c35fe86fbed32cd99310bd69c5185b44be8a9f331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217157987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffaedda7eb4525460126a52e0eaf15efd783c892b37a62d287c3639a7647516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 10:01:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 10:01:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 10:02:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 10:02:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 10:02:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 10:10:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 10:10:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 10:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 10:11:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 10:11:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 10:11:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 10:11:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 10:11:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 10:11:03 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 20:09:00 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 20:09:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 20:09:01 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 20:09:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 20:09:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:14:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 20:14:03 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:14:04 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 20:14:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 20:14:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 20:14:04 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:14:04 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 20:14:04 GMT
EXPOSE 80
# Fri, 16 Feb 2024 20:14:04 GMT
CMD ["apache2-foreground"]
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Tue, 05 Mar 2024 20:03:11 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 20:03:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54ec09c321d9443d13d2a1026ff25831b557cfba4d96e69cb04e013c3da80f5`  
		Last Modified: Tue, 13 Feb 2024 14:18:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490d32b608328a311a60472b26afd97528354bc034d70970888f6ee739c420a5`  
		Last Modified: Tue, 13 Feb 2024 14:19:08 GMT  
		Size: 76.2 MB (76170039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d22eae8ae049c93976062baae1ae123e100467b9a9fa3fa3b1f0eec2054f92`  
		Last Modified: Tue, 13 Feb 2024 14:18:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7976c47c921676dbb2f61cab51f861ebe6c1c2fd0256ef4ca602e76284a260`  
		Last Modified: Tue, 13 Feb 2024 14:19:35 GMT  
		Size: 19.0 MB (19045623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b35d2b7a621e2db4c4934c42f654f792902d71ff2b5ef08c61dd51a06157f7`  
		Last Modified: Tue, 13 Feb 2024 14:19:32 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed02b1cf9e045fe41f1be886a34b49a7acc8cefc8c55d4985bf1bf99ea65882`  
		Last Modified: Tue, 13 Feb 2024 14:19:32 GMT  
		Size: 513.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe62b96c8079dbb3d4c43d6062328effb39f117d04f04fc5708d8d3e5de1e3ab`  
		Last Modified: Fri, 16 Feb 2024 21:53:57 GMT  
		Size: 12.8 MB (12795419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e554832d96e98aa3bfb99e13ac293db3e5428f72b0382574ead73dea0a043f`  
		Last Modified: Fri, 16 Feb 2024 21:53:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98de8c442f5516b049cc32303429615d9da4d73bb774e5057d2670678b9e8370`  
		Last Modified: Fri, 16 Feb 2024 21:53:57 GMT  
		Size: 10.0 MB (10029125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9a5735f297eb0b8791e3712d95131aa51af65e0568f1d04c3113c124116ae2`  
		Last Modified: Fri, 16 Feb 2024 21:53:54 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65671fe08736f59b7ee03bc316f438109bc0ef61fb257d1416c8a4152bb4d008`  
		Last Modified: Fri, 16 Feb 2024 21:53:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d112e6772dcfc11c458c1212a383b0e74845705c33b126e04274cd2c15a296`  
		Last Modified: Fri, 16 Feb 2024 21:53:54 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122148cc21bb3c6ba292e6a5dee2aafdb1f7586a7ef6c89fa428e6492bae426d`  
		Last Modified: Wed, 06 Mar 2024 05:49:09 GMT  
		Size: 25.1 MB (25076816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d6b3d8f779d595f496ab1ff426dd200b4003427e804d1c277e8a8f66070dc6`  
		Last Modified: Wed, 06 Mar 2024 05:49:09 GMT  
		Size: 24.8 MB (24775521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eee04ea74bd2660937680e44d75c7c8e0fbdf39c1a2e07b2a9bdab528e6f36`  
		Last Modified: Wed, 06 Mar 2024 05:49:08 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea24854f0498dd7234020e2faf0c3061e0d8a5274df987d39b8d6f69125e2cb`  
		Last Modified: Wed, 06 Mar 2024 05:49:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0495ae86793891857e16732c7d27af502337732d7a5a947f42f9486532d25642`  
		Last Modified: Wed, 06 Mar 2024 05:49:09 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319a18136e58ac0dbe1f6fa808e8a966b707c873d6b89af1099bbd3ed86bc73`  
		Last Modified: Wed, 06 Mar 2024 05:49:11 GMT  
		Size: 24.5 MB (24519218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3728bbc7a4f6bab8dc99af44d40ee45e523b81d8d0d68e5a79e0ba9b75ac354e`  
		Last Modified: Wed, 06 Mar 2024 05:49:10 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb06cab92212d48603c329d757fcf06c7b637f3d5b6b4ed5d409f99c3ef08304`  
		Last Modified: Wed, 06 Mar 2024 05:49:11 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:29b392499be0ddb34fa4fcb909510561bdc23410e1e59eb4d55ea4535f1cb547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8834593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ab72c8e56feb84758e50d506998d333a0c98ef8d34f3a14b04890505bd23de`

```dockerfile
```

-	Layers:
	-	`sha256:acee12ca711d5f6801fe4bf6da61952bfc2ccde1b30c5c03597081415505cf8b`  
		Last Modified: Wed, 06 Mar 2024 05:49:08 GMT  
		Size: 8.8 MB (8776878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:400c1d5c5a6dac83776997f81abcb3ff2703b71d0bc292f79500cc3e81383b28`  
		Last Modified: Wed, 06 Mar 2024 05:49:08 GMT  
		Size: 57.7 KB (57715 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:50a40c6f866aeef8b2f9ba140805b4c5805c8b0771dc2ea5266da2f40eb7e57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249879869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78eb7e7c4c8ef5e4541d3086549cdbcaa590912fc4de7d9fa5f03e1a7a7d2af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:37:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 04:37:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 04:38:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:38:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 04:38:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 04:42:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 04:42:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 04:42:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 04:42:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 04:42:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 04:42:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:42:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:42:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 04:42:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 22:49:28 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 22:49:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 22:49:28 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 22:49:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 22:49:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:53:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 22:53:16 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:53:17 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 22:53:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 22:53:17 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 22:53:17 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:53:17 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 22:53:17 GMT
EXPOSE 80
# Fri, 16 Feb 2024 22:53:18 GMT
CMD ["apache2-foreground"]
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Tue, 05 Mar 2024 20:03:11 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 20:03:11 GMT
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
	-	`sha256:40f607666455f470fde9e32273ab2778c41d3b360b620513863a68f90927b872`  
		Last Modified: Sat, 17 Feb 2024 00:35:37 GMT  
		Size: 12.8 MB (12797040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379c5dc83eed8db6125a3f7e5f5f8e9c82418973a97f571a56008a1556c2689d`  
		Last Modified: Sat, 17 Feb 2024 00:35:35 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f157cb10e23cfbf833cdb545e6f455c5d9bddb0d9d598fbc4dec31cd251f3d`  
		Last Modified: Sat, 17 Feb 2024 00:35:36 GMT  
		Size: 11.6 MB (11628467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab419700b14b9c1e30489718b57535edbf6a928296b5ce98e89a147f47a187c1`  
		Last Modified: Sat, 17 Feb 2024 00:35:35 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3a1da0fdb621b4debe5e52f9065fd555b65e4bc290cda135112be5755a001`  
		Last Modified: Sat, 17 Feb 2024 00:35:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e35afd1db3267bd559a4f42a2e31a3625d785c5fec6fbf8c51c660ca8dbeef1`  
		Last Modified: Sat, 17 Feb 2024 00:35:35 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b63941fe570f5add8d24fff5ed723ae245d54b94c4c2eb336d0dbb27f1621`  
		Last Modified: Wed, 06 Mar 2024 02:58:55 GMT  
		Size: 26.2 MB (26175817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f95e8d788df1ff08d1281103a536e304b3ae2f708aab353ea34c76a4c4c7997`  
		Last Modified: Wed, 06 Mar 2024 02:58:54 GMT  
		Size: 27.1 MB (27142384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef0c8cfa735d6aaf162308a74e4d512fd71d1968b30afd4e5664a797dfc119b`  
		Last Modified: Wed, 06 Mar 2024 02:58:53 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6832abd060d4a7ac3be9aa283490123330151c6e5fc501d4920444f3fb0f65`  
		Last Modified: Wed, 06 Mar 2024 02:58:53 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2d13bbd99abf29036e6b48e3934e2e2b852e79c0f2f46ee2976e4a52d0a66c`  
		Last Modified: Wed, 06 Mar 2024 02:58:54 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c491a2e4326fdce198a6776007bab21c94055348df8d7301e631c379171395`  
		Last Modified: Wed, 06 Mar 2024 02:58:56 GMT  
		Size: 24.5 MB (24519210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366a71a3ddad4969491da657f693530783401ce978731ae637fd26f84064e70f`  
		Last Modified: Wed, 06 Mar 2024 02:58:56 GMT  
		Size: 2.3 KB (2343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292038e2943a0d8f9f42119694d7295f041d7f45322069adf9fb952d43921f2`  
		Last Modified: Wed, 06 Mar 2024 02:58:56 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:c98c44b37b4de52892d2403afd18bb3ebbca24eda15041acfdd38f2ae3862742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9050843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c7d899329df25898e08d117fe4f9d4750afe218a226c8b8b8dcf47c390b01b`

```dockerfile
```

-	Layers:
	-	`sha256:89aec6c6fe02523daa5be72e14ba4072efb2794c50955b0cb0486085005d3312`  
		Last Modified: Wed, 06 Mar 2024 02:58:54 GMT  
		Size: 9.0 MB (8993277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4f8b25e8c62d2ea33e9f2fefa7861c5881e015f9826d9f4fe59b351815afbca`  
		Last Modified: Wed, 06 Mar 2024 02:58:53 GMT  
		Size: 57.6 KB (57566 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:3a158e6405a57823dd007f74023e1d6436f8fc2ed85606a25b19bdce8cfc88b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256731205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205b979c7a4611378265ee3ef890f19aaa1898a8443015510c147a77463e85e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Mar 2024 23:23:48 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 11 Mar 2024 23:23:48 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Mon, 11 Mar 2024 23:23:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 11 Mar 2024 23:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_VERSION=8.3.3
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Mon, 11 Mar 2024 23:23:48 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 11 Mar 2024 23:23:48 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
RUN docker-php-ext-enable sodium
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 11 Mar 2024 23:23:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 11 Mar 2024 23:23:48 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Mon, 11 Mar 2024 23:23:48 GMT
WORKDIR /var/www/html
# Mon, 11 Mar 2024 23:23:48 GMT
EXPOSE 80
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["apache2-foreground"]
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
VOLUME [/var/www/html]
# Mon, 11 Mar 2024 23:23:48 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 Mar 2024 23:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Mar 2024 23:23:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc8b418f2e8ebe03c4a8d60a403099d5bd9956664693b358caef9096763fabd`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f25d2333bd6d54c124fa174175081a9c95780122966ffb6532bd93757a9bd`  
		Last Modified: Tue, 12 Mar 2024 05:53:38 GMT  
		Size: 101.5 MB (101519737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6e71adc002ea9786257601b0d391da402881cf3c46d70b1bf238b5e218a47`  
		Last Modified: Tue, 12 Mar 2024 05:53:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ac2ec3c620e7a371533497b0cfd74ea84db2b079763c0c27f094625f447cf`  
		Last Modified: Tue, 12 Mar 2024 05:54:05 GMT  
		Size: 20.8 MB (20826115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef95ebea38d5ed66df38918c6398211026347c3a649d8cc4c3d081f4e7c6290`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea05f91953dd8b5d5da845bf416fd786a74c12a214cd690ab7a3fe6bc5a5774`  
		Last Modified: Tue, 12 Mar 2024 05:54:01 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fb16b3786c82c21108229bd70b173ca76948b508b50c8fad4f17c42e3758f7`  
		Last Modified: Tue, 12 Mar 2024 05:57:16 GMT  
		Size: 12.8 MB (12796447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91938674c8183065ca7b2e57b77e6fcbb57d4be171ae8bf4c12c34147458fb1`  
		Last Modified: Tue, 12 Mar 2024 05:57:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5248695913cb2840bec89546a6c4a6e16fe23c4a1715b8736a44eae1e50d4090`  
		Last Modified: Tue, 12 Mar 2024 05:57:16 GMT  
		Size: 11.9 MB (11856635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cc458230d23beadf17d01862679abd646fdd66466ce126aaf14c28c8e327d`  
		Last Modified: Tue, 12 Mar 2024 05:57:13 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1457a5616f44f1d381374ef820535ab72097e3e02446b3daccbe76472aa805`  
		Last Modified: Tue, 12 Mar 2024 05:57:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229f7a2878344570c073f6282260893ee1073f30e1c3a67cc1d7797a0a7deea`  
		Last Modified: Tue, 12 Mar 2024 05:57:13 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c31e6ae8558ab93900553ec48f4599f2a43eb70d43e7defe991a1da73caf4e9`  
		Last Modified: Tue, 12 Mar 2024 06:59:10 GMT  
		Size: 26.7 MB (26700621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0f06f9ccf9d7f501cf4e7cdede3c58d47bef508bab5cce326be9463c8d2573`  
		Last Modified: Tue, 12 Mar 2024 06:59:10 GMT  
		Size: 28.3 MB (28341013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fed6d5fdb072521bf7a61d4e670a69d266cb082375448ef161494bf768e4cf`  
		Last Modified: Tue, 12 Mar 2024 06:59:10 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef43cf4a31fca7aeb1819733d89e2db1ea44f236ca8425680b1d789a93a0b3a4`  
		Last Modified: Tue, 12 Mar 2024 06:59:10 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a376519f47342f11b53ca988aca5d45fc413204af393a12a9c03ab73f39a591f`  
		Last Modified: Tue, 12 Mar 2024 06:59:11 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390cbfaa9d5dac78f2bbb7ae1f0e546da9821b99a8ae92408929dd85ee07f8ef`  
		Last Modified: Tue, 12 Mar 2024 06:59:12 GMT  
		Size: 24.5 MB (24519207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f5597cd4b68ed74bf6c7676765a55fae192996e64ecc1b7d39b0c02c854af`  
		Last Modified: Tue, 12 Mar 2024 06:59:12 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ee8c2a6d1e252f8e18475d42d72389b763bde5ebd53353d89b4943fa93fdb`  
		Last Modified: Tue, 12 Mar 2024 06:59:12 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:380ccc853a7492ae5b753ca9038b6d5339d571ba8e4a6423da9698004e794d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9006081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c20284c58449b63b8d9fb832bfbf593567ab33855491a370a953f96197feef`

```dockerfile
```

-	Layers:
	-	`sha256:f402e0bd73096c4a40257db63ef16845347948f712f8c99275458db40248b198`  
		Last Modified: Tue, 12 Mar 2024 06:59:10 GMT  
		Size: 8.9 MB (8944420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1697c059c9ea0fbf13b726d42bb8cc3a540b60b638611327a3c431df2613389b`  
		Last Modified: Tue, 12 Mar 2024 06:59:10 GMT  
		Size: 61.7 KB (61661 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:b7354fadb0b02d1df690fa32bfdce002d0364be7507626ff6d6b83dc63ead587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264158018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe5c188c9523e1d7b5d5f9ec3609a1f5f7ae2517627619563e96ecaa57ee6a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:19:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 04:19:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 04:20:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:20:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 04:20:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 04:24:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 04:24:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 04:25:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 04:25:11 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 04:25:12 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 04:25:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:25:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 04:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 04:25:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 20:30:09 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 20:30:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 20:30:09 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 20:30:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 20:30:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:33:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 20:33:54 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:33:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 20:33:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 20:33:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 20:33:57 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:33:58 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 20:33:59 GMT
EXPOSE 80
# Fri, 16 Feb 2024 20:33:59 GMT
CMD ["apache2-foreground"]
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Tue, 05 Mar 2024 20:03:11 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 20:03:11 GMT
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
	-	`sha256:d811005a1c56712aa83d2f1fee1370b5fc577362fcf7de761198c51728102eb4`  
		Last Modified: Fri, 16 Feb 2024 22:02:31 GMT  
		Size: 12.8 MB (12796981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c0bf1497a6839cd7a22105f9244f79758b1fd3d90f142fef8308e0f794213`  
		Last Modified: Fri, 16 Feb 2024 22:02:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61e96322ee1bca995c95a448d619e5e8f36974adde759cd329d5e9d429ef697`  
		Last Modified: Fri, 16 Feb 2024 22:02:30 GMT  
		Size: 12.1 MB (12050119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c081f0f4917b3800c86b4a98df763aca2807c9be04f1732c432a698d0ac977`  
		Last Modified: Fri, 16 Feb 2024 22:02:27 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2e84c9daa2db8ac526be250bb180c8f972c1b52114d6d8df844df9b9d421f2`  
		Last Modified: Fri, 16 Feb 2024 22:02:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af85815d0d99a7347ebd6a83bb3bf3c528d8d91547e8320bf868588a1d0fd216`  
		Last Modified: Fri, 16 Feb 2024 22:02:27 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08ade63754669519d6dbb24df70aa24aac696a16c2113846d3b1f9062f55ee`  
		Last Modified: Wed, 06 Mar 2024 10:14:37 GMT  
		Size: 27.3 MB (27340409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466d677aec8cad8d5f82f5466d8fec73c98521dbe44053989e0476ac2fbcbb4d`  
		Last Modified: Wed, 06 Mar 2024 10:14:37 GMT  
		Size: 29.5 MB (29500171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc91bd56e16dbb58e0ff2f7db2bbf85d0e7396ea3659a7250708bde5f9cf565`  
		Last Modified: Wed, 06 Mar 2024 10:14:36 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a387053e32b7306fda7d76ebdaa7fbb4a9685264c48348ad30c7a339c433347`  
		Last Modified: Wed, 06 Mar 2024 10:14:36 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40afc87d874a130f9e1dcc98dd09f99a795dd367fa7b89518ff21473ffe417d`  
		Last Modified: Wed, 06 Mar 2024 10:14:37 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d410277f3f876b4b66a4f9393b76eca66c30407277f7de2bbd9cb31f8054b04`  
		Last Modified: Wed, 06 Mar 2024 10:14:38 GMT  
		Size: 24.5 MB (24519214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c73ea3ed063a9f5bdd360d3c6c45cbf4046dc9084c1cfc878ff9c3c6b4d15`  
		Last Modified: Wed, 06 Mar 2024 10:14:38 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a49fd778be5d5c1cd978b290b3a1bf298b0b7f308fc14c19621dfd2ec23456`  
		Last Modified: Wed, 06 Mar 2024 10:14:38 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:b11a7bb81f3ec9525329e1f2e015234d1aac8a96b0b581008c950b1f9b69e3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9001443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21ce25c3fd41fea36985853d84853a943c6f56d008f3a6d8ac13760df7bc629`

```dockerfile
```

-	Layers:
	-	`sha256:819e38105a845d40a3f1ff080da18a439fb4723bde51c1a5bd7a7f6bdb0bea94`  
		Last Modified: Wed, 06 Mar 2024 10:14:36 GMT  
		Size: 8.9 MB (8943815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1476c1ca695cacb12e56f70783ba0fe3af8e683125b307d1a57c447ad999cf2`  
		Last Modified: Wed, 06 Mar 2024 10:14:35 GMT  
		Size: 57.6 KB (57628 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.3-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:fa51451775764d3e0fba6a5707a725b1178bd383b7cfabd3492ed2c9351bd165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228562416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef6bfb13f29362cf518d56000a81aa4caa61eb518b5c5274bd8f309f944764`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 01:02:37 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 13 Feb 2024 01:02:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 05:08:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 05:08:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 05:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 05:09:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 05:09:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 05:12:59 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 05:12:59 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 05:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 05:13:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 05:13:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 05:13:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:13:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:13:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 05:13:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 21:16:31 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 21:16:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 21:16:31 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 21:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 21:16:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:19:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 21:19:24 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:19:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 21:19:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 21:19:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 21:19:25 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:19:25 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 21:19:25 GMT
EXPOSE 80
# Fri, 16 Feb 2024 21:19:25 GMT
CMD ["apache2-foreground"]
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
RUN set -eux; 	version='6.5-RC1'; 	sha1='5008d9f73b247670e8c848bc309f932f546ca79d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
VOLUME [/var/www/html]
# Tue, 05 Mar 2024 20:03:11 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 20:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 20:03:11 GMT
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
	-	`sha256:e9658ee931ef1197379ded67e8548b7870ae9df8b656bf6732eec8d70051e12d`  
		Last Modified: Fri, 16 Feb 2024 23:18:24 GMT  
		Size: 12.8 MB (12795814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d39ad7f3bef861b9e0ca21588c4578ca3ca4d949c5a350eed59bd54e1185ed6`  
		Last Modified: Fri, 16 Feb 2024 23:18:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b1c52f1447dc1f55231a9a790d8fa0d4939759065c9824d20ad5d7f6634f8`  
		Last Modified: Fri, 16 Feb 2024 23:18:24 GMT  
		Size: 10.7 MB (10664364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456c987b49f376eb66b485cf37e091bb5741e744df9014aed4c64dd385da3f04`  
		Last Modified: Fri, 16 Feb 2024 23:18:23 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4036f86498c04d8216a169e68cc5f028be211551387f42a59aaf1609e46f3611`  
		Last Modified: Fri, 16 Feb 2024 23:18:23 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c45b9d3f7a8b12de431d25d1e81277bc49888f1d6683458a867ee8607da2d15`  
		Last Modified: Fri, 16 Feb 2024 23:18:23 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f4d0837f5f773307920f58e87a7875eeb622fcef80fa19c3f2b8209c571ed3`  
		Last Modified: Wed, 06 Mar 2024 15:40:46 GMT  
		Size: 25.9 MB (25899755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b56b1517385fb7d00915ce2cd637cbc7c99c6c0f377415f09504a635378f6c`  
		Last Modified: Wed, 06 Mar 2024 15:40:45 GMT  
		Size: 26.3 MB (26273483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38041d46e07b9c81f6674308b9079a28fe7c64f9bcb1fc4d357adda7c7c0a91`  
		Last Modified: Wed, 06 Mar 2024 15:40:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8760f6ca7e5d55cf61b14f8c67de5e6647f85a7b8791ec72300ca6ae20ae900`  
		Last Modified: Wed, 06 Mar 2024 15:40:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb511bbf9f1b6641c216e3a260cb3a071304cee48601e7168b1295698030c49`  
		Last Modified: Wed, 06 Mar 2024 15:40:46 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c355a2eddbadd201415c632373ffe6004a3e23e59b0731caf9d0c6161751b907`  
		Last Modified: Wed, 06 Mar 2024 15:40:46 GMT  
		Size: 24.5 MB (24519213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37138ff5a820cc7cd88d6be80197733b77e8529f63df805b8d71f9102b56426a`  
		Last Modified: Wed, 06 Mar 2024 15:40:46 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8361d822a02f7c65509a63f27f670ef1b0cc62552a94abeaf8fa1716fe8221e3`  
		Last Modified: Wed, 06 Mar 2024 15:40:46 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:56d5f9601227bdd159e9d0d0fdb9fe7918b3842f58ea2c216eca5b71a0d7051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8853886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07e01d0136e5762c86051fd7e75204f7f31e997e63b2705786ce198add55cf3`

```dockerfile
```

-	Layers:
	-	`sha256:6b3e48ab9f7ef9d00892e508ddd1acf04e7cfc0e03a2d81735ba98093f1089ae`  
		Last Modified: Wed, 06 Mar 2024 15:40:45 GMT  
		Size: 8.8 MB (8796338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:127a1e86a00c874eb1384acd28394bd66a385e9065cd215f95af87580e7edf2a`  
		Last Modified: Wed, 06 Mar 2024 15:40:44 GMT  
		Size: 57.5 KB (57548 bytes)  
		MIME: application/vnd.in-toto+json
