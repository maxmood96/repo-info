## `wordpress:beta-6.5-RC1-php8.3-apache`

```console
$ docker pull wordpress@sha256:35164dcf1760cacfda5b0f7f926210bed03a59b59e030889a8c5d0cfea1b8698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.5-RC1-php8.3-apache` - linux; arm variant v5

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

### `wordpress:beta-6.5-RC1-php8.3-apache` - unknown; unknown

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

### `wordpress:beta-6.5-RC1-php8.3-apache` - linux; arm variant v7

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

### `wordpress:beta-6.5-RC1-php8.3-apache` - unknown; unknown

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

### `wordpress:beta-6.5-RC1-php8.3-apache` - linux; 386

```console
$ docker pull wordpress@sha256:c219f0b1b83dcb67b6118af4c71954d1e242ea04b11d48c3d0fe3a85b33eb860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257236441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd610f707c507fe033f4fe9799ae4b8ab20c6c44a68c7bb351106bb861f647ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:38:56 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Tue, 13 Feb 2024 00:38:56 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:54:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Feb 2024 04:54:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Feb 2024 04:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:54:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Feb 2024 04:54:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Feb 2024 05:01:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 13 Feb 2024 05:01:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 13 Feb 2024 05:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR"
# Tue, 13 Feb 2024 05:02:09 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork
# Tue, 13 Feb 2024 05:02:10 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php
# Tue, 13 Feb 2024 05:02:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:02:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Feb 2024 05:02:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Feb 2024 05:02:10 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 Feb 2024 20:05:03 GMT
ENV PHP_VERSION=8.3.3
# Fri, 16 Feb 2024 20:05:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.3.tar.xz.asc
# Fri, 16 Feb 2024 20:05:03 GMT
ENV PHP_SHA256=b0a996276fe21fe9ca8f993314c8bc02750f464c7b0343f056fb0894a8dfa9d1
# Fri, 16 Feb 2024 20:05:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 16 Feb 2024 20:05:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:11:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 20:11:55 GMT
COPY multi:e11221d43af7136e4dbad5a74e659bcfa753214a9e615c3daf357f1633d9d3d1 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:11:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 20:11:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 20:11:56 GMT
STOPSIGNAL SIGWINCH
# Fri, 16 Feb 2024 20:11:56 GMT
COPY file:e3123fcb6566efa979f945bfac1c94c854a559d7b82723e42118882a8ac4de66 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:11:56 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 20:11:56 GMT
EXPOSE 80
# Fri, 16 Feb 2024 20:11:56 GMT
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
	-	`sha256:e6c1f7e97d91fbbc4faffa0990be9c7f1f0d5c23f7c0c86a8ff6b1edc7748637`  
		Last Modified: Fri, 16 Feb 2024 23:05:45 GMT  
		Size: 12.8 MB (12796446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ee523da1a93204047e1e555c01a745725dc7e9bb8509f561299cae4c24c04`  
		Last Modified: Fri, 16 Feb 2024 23:05:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2100d69ff3cdb8f0623daabe1860f3ae094a5dcf3595b40ce20554dd0b736e8`  
		Last Modified: Fri, 16 Feb 2024 23:05:45 GMT  
		Size: 11.9 MB (11856728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce4f5ed49d37c46842659e66707a61f41bd782114ccdf1400c03b47d29ef173`  
		Last Modified: Fri, 16 Feb 2024 23:05:42 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db306e78f79d6ada64c3c99b2f08f7cab1c342ca406b8c91db6d70f30ff01f2a`  
		Last Modified: Fri, 16 Feb 2024 23:05:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833711135d5b92868409b915e9f866a3a55040c1f00df20b30ad173c090a4e9`  
		Last Modified: Fri, 16 Feb 2024 23:05:41 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b148bc4e782970fd8e0b43ebacf015522af2edc45275cc3b7464e42c460311fd`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 26.7 MB (26700609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af4fe68d402264111c69d38e86a891ff1e89b38da1edec8ee21cb568f673d1a`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 28.8 MB (28846215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2bb3f866459f477c5867020ebb7785fd1316419e8e3875f880aa8f40dda34`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f777d40b9d006f6f75b7bec5be57c0df727c01d0b1f5751b5820112aa777ec`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29c511caca3b064b0c3eb8467793013b21f138aaa9452b99d962d69337c094`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364b312c78fe47906ea8a7074fe26cb44571a8562e5188a350cbe90f33e85585`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 24.5 MB (24519212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d8192a7d3fc5a7bcf7b54f9ab42188991b18387075e04840a3960151c53126`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18be767b462f4f45dedba4fefc69a973439bf6ebd836ac32ec96c2965601e2f`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-RC1-php8.3-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:9e0cb0ff9d0122ed2cc4e32e61593d3cb0c21bf331deedb8114300edcfdb69e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9004027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650653eea9eed2328ab803b950496d38c5111761bb64190501e00e9aa8602577`

```dockerfile
```

-	Layers:
	-	`sha256:60aed7d2cb4d5ad9c35e8d9bdf05705959fe769a9b29990829400ac8861811cf`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 8.9 MB (8944420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4628c9b3d818a6db87bb73e75038d9e82b770120dcce33b65f654b1ec2099efe`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 59.6 KB (59607 bytes)  
		MIME: application/vnd.in-toto+json
