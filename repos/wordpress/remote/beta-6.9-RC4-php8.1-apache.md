## `wordpress:beta-6.9-RC4-php8.1-apache`

```console
$ docker pull wordpress@sha256:fd3e9e6cf6f7f1fc89a584a0f4cff1ab44040ff43ddc4833f0319297c5b26b1b
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

### `wordpress:beta-6.9-RC4-php8.1-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:a8d4bb2d4c01d597f3784608e924e58a5373d38c9d7a080ba2a2690c84757c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262325619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fc58a472c73b68c60571c0a52ec3808af7ab683b97b4648ec3adc6a3fae72e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:26:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 04:26:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 04:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:26:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 04:26:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 04:26:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 04:26:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 04:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 04:51:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 04:51:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 04:51:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 04:55:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 04:55:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:57:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 04:57:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:57:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 04:57:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 04:57:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 04:57:50 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 04:57:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:57:50 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 04:57:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 04:57:50 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:11:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:15:20 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:15:20 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:20 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:15:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:20 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:15:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:20 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb706d32abb568af187c7338eba0dba44778b2e43031ec985a8aad7cf366b8a`  
		Last Modified: Tue, 18 Nov 2025 04:30:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a19df025b0213db3e8cac08569c68bc7b3436b95774763d3bdd21a192e0d81`  
		Last Modified: Tue, 18 Nov 2025 04:30:26 GMT  
		Size: 117.8 MB (117838105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7872b90dc36f255fe1bc49e35734339efa1718c03f635b42b6faabe8ff4eef08`  
		Last Modified: Tue, 18 Nov 2025 04:30:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53319895a3614d779c67d741f1385ad3cb14cbe2e3f9db5814b35efd2f0c07a`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 4.2 MB (4224517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfedcc0471718eb9a0653883ec626ee076da5ddb9d2220dbf1dfa288e625fe4`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93735e3787d7379b3b85c45bbb8e27bbb6b7470b604ac0bc61ab0354bcb8fd49`  
		Last Modified: Tue, 18 Nov 2025 04:54:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51305ce3beb635c67a1867524853cdd2fdcfc7ecfb5674ec0c570e50b40ada34`  
		Last Modified: Tue, 18 Nov 2025 04:58:10 GMT  
		Size: 12.1 MB (12065191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d781c3262d2adc79571310af37716621a8c21871dd408ff196e460dbe53484d`  
		Last Modified: Tue, 18 Nov 2025 04:58:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14967cdc2e62bee0aa2a47ad6c9874bc21bf49996a9e681d0a0f1ba8bdb22781`  
		Last Modified: Tue, 18 Nov 2025 04:58:10 GMT  
		Size: 11.2 MB (11186188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10525c7eaaa90ed1676670acff652fca98c16aa9ff7aa0e85f32e9048e303fc`  
		Last Modified: Tue, 18 Nov 2025 04:58:09 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb0d72269211f79cf5fbcb7075dc1c84293edf3ee8e62d58f2c3fe0e7b62d9`  
		Last Modified: Tue, 18 Nov 2025 04:58:09 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48431f76aed470d0bdf94d2781a3385c6324490107db98a15bb7e485b0a2c68e`  
		Last Modified: Tue, 18 Nov 2025 04:58:09 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e276a328425b793831e47beb6b0951a9a6259a08aae5777d7c27b585def5fa9e`  
		Last Modified: Tue, 18 Nov 2025 04:58:10 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a5cee13361cca63d56c30edc38d86048ed6084761e5a6982e366422ad9396`  
		Last Modified: Tue, 02 Dec 2025 01:13:21 GMT  
		Size: 26.3 MB (26297308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977e4900a199aeee57b42ba7b53176be63fd94610e1f12ae9b339376e169780d`  
		Last Modified: Tue, 02 Dec 2025 01:13:23 GMT  
		Size: 33.9 MB (33883526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4b3a51cac85b31d92cbfeda7507c231406c3d09ce3171ab6429b3ac69a0ac8`  
		Last Modified: Tue, 02 Dec 2025 01:13:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7905ed33609f15fa0cff0a5a801183eba399ef0d5ed6d10183ed9d67f9ffa7d9`  
		Last Modified: Tue, 02 Dec 2025 01:13:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e460ca65fbb9b0bb5220b8658a3046610105d8f26e1b10485f92e5b17d4ed73`  
		Last Modified: Tue, 02 Dec 2025 01:13:19 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8c654cc1472bf8423ffc3bdfa7e1f5ce2405f9fa5b95500facda5d8fb11f1d`  
		Last Modified: Tue, 02 Dec 2025 01:15:54 GMT  
		Size: 27.0 MB (27024634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0913680172f9bd722768fdee0494bfe667f36fa26bf50f990ac888f33554e0ed`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a176a17e7788958fe575cf5136d9e4be3b52fd47e4873059c5af538882d5a`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80c841d0d28e768dac757f24aba30b3b60e79d493e2ed30ee2d2c90da6b43be`  
		Last Modified: Tue, 02 Dec 2025 01:15:53 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:b59e2fba0c5e6822fdafe268893cc13dc0932ffb58dd5eedb5ba4139b303f486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8737041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1851a69eecf0dcee175d9bff99dac96ceccbac7e1ba7c3ef216dda5ac26bf6`

```dockerfile
```

-	Layers:
	-	`sha256:02003a5ca4d653089d3c66d781779f0c2b8152ed065e2261476af33fdde2dc0c`  
		Last Modified: Tue, 02 Dec 2025 02:25:27 GMT  
		Size: 8.7 MB (8671614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a536211706cb9579f4d4d5cb2807e3c893ca96936f7a4a57cdb0d10d4551a0ea`  
		Last Modified: Tue, 02 Dec 2025 02:25:28 GMT  
		Size: 65.4 KB (65427 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.1-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:0d6af8c9d1f2a95e8ab83bc1e1b07e30cefba2ae0549256d2fd18c41e2a12659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231802117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc83e403e2a772c29f2a1e8f8b72138ea039a6c1be3c62a3a307a33d56434ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:52:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:53:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:53:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:53:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:53:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 02:53:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 02:57:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 02:57:18 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 02:57:18 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 02:57:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:57:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:57:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:57:18 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 02:57:18 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 02:57:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 02:57:18 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 02:57:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:57:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:00:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 03:00:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:00:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 03:00:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 03:00:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 03:00:24 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 03:00:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:00:24 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 03:00:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 03:00:24 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:12:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:14:07 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:14:08 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:14:09 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:14:09 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:14:09 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:14:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:14:09 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:14:09 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa201426d50fb1f122cdb43cc274eb33eeeb453929d345c11b39e5c8414f895`  
		Last Modified: Tue, 18 Nov 2025 02:56:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d9d9a0db5be8ba1f7cb8cb5707f846bd18b7f664b8e638bad9f2a0a4119c4`  
		Last Modified: Tue, 18 Nov 2025 02:56:48 GMT  
		Size: 94.9 MB (94874067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b80eade7ed2881b4317421e054ec9c4e3d9ac08129715e0a0060ad6164a62b7`  
		Last Modified: Tue, 18 Nov 2025 02:56:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d0ec5eb31c7b72368dfb6278ef6510e7b28d1cd2d5537c33fd849d0044ab1b`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 4.1 MB (4082055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efcf9ad600b56f58c33d4e40669cf5632b1d019ff4ff19aaabf14f0ec0ea8c6`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5d5f8f30d59aa20ada86a0da3098b28d730e4d8b784c5a29ee06a04e9daaa6`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9e728b7428ad2569b37fbd95fc378bddb0d82cedecae0a1c7d4942f416874f`  
		Last Modified: Tue, 18 Nov 2025 03:00:45 GMT  
		Size: 12.1 MB (12062605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c625b5fb1fed8305d2f530efc04f271a996f0c4dd494ff891a2641271307cd`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee9328721fca58e167f73b26d9e9b371266640104d1715c5d14647b8a09c069`  
		Last Modified: Tue, 18 Nov 2025 03:00:46 GMT  
		Size: 10.1 MB (10074499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bba95ca70b7e28bb74f96abadff502b76b7a84e27bfcc831a7e85b21017dee5`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037a6886687afba0ec2f4da8e29662a56d8d90b0681256dc012290616c795ecd`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2cee0339ecd733664c0cec1f4b3b1d35b60194ab1e80c26989ca8aa91d38dd`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d1748aff9dce44b18c9bf7d019ff6d986acdeafea254c916990756b30181c9`  
		Last Modified: Tue, 18 Nov 2025 03:00:44 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee3068989bec93b55ba7a25a4c771cfad8aaad5e53ad3a76e99fb194bcbd76`  
		Last Modified: Tue, 02 Dec 2025 01:14:55 GMT  
		Size: 25.7 MB (25728566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfc8464d16785fa55730d609a3d774005ddf6f943a3fe28e75f9a48a1961679`  
		Last Modified: Tue, 02 Dec 2025 01:14:55 GMT  
		Size: 30.0 MB (29981894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213a18e4141b28d86410aee1aa64fb68c6bb1278d108a959bea981c2f5e6ac2`  
		Last Modified: Tue, 02 Dec 2025 01:14:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d02f0e98da5032e70bad11094a291d3a7e4fd674e52d8c0e3dfe9fe79a23c27`  
		Last Modified: Tue, 02 Dec 2025 01:14:52 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b5732b1ac913b66af41622e1729875460b2591607587933d6aa2388660c8fb`  
		Last Modified: Tue, 02 Dec 2025 01:14:52 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f62962256e5ce541e221c0ccb7080654acc7602e9c4b6a9a73cf85e58202f02`  
		Last Modified: Tue, 02 Dec 2025 01:14:55 GMT  
		Size: 27.0 MB (27024618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f2f275df0bd862dcee79da25746ee80af70ee0660e060a216fab74f6c22707`  
		Last Modified: Tue, 02 Dec 2025 01:14:53 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e542e0aa9f904b4c4fc27cfd28bee8a5b0309c28d93a61ee5d5725a4248aacc3`  
		Last Modified: Tue, 02 Dec 2025 01:14:53 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc58aa1824bbfc648fc2bf23aa00e6ee631129329bfed726ad1ced4619a4a`  
		Last Modified: Tue, 02 Dec 2025 01:14:53 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:ec15253c65cf36f93a557ea0a8bd9fc0082322c1a24b6f1970e434c3a4dd6a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8536254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a084b7c5724d256a3a18741e6979fbbb891dce0db6af6e4e822175f4b6731e6`

```dockerfile
```

-	Layers:
	-	`sha256:c512ed6d62815579d12359c07156fdac63a3d2af0c2b3090ec6346f57541c03f`  
		Last Modified: Tue, 02 Dec 2025 02:25:35 GMT  
		Size: 8.5 MB (8470647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:640aec2d96cb0bb470192aa9fc550fb34ae5ebdaee95d2ba884ee4340c01790f`  
		Last Modified: Tue, 02 Dec 2025 02:25:36 GMT  
		Size: 65.6 KB (65607 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.1-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:e7c48e4bdb97cebf64cf3617da9d1190f6c252698061da36da658abc7515f7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218114994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dc1dd6b806e87c77d706bf070d3dadec041a55666aa14fad8cb32702c93443`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:48:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:48:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:48:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:48:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:48:26 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 02:48:26 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 03:07:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 03:07:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 03:07:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 03:07:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 03:07:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 03:07:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 03:07:33 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 03:07:33 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 03:07:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 03:07:33 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 03:07:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 03:07:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:10:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 03:10:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:10:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 03:10:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 03:10:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 03:10:18 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 03:10:18 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:10:18 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 03:10:18 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 03:10:18 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:19:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:19:28 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:19:28 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:19:28 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:19:30 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:19:30 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:19:30 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:19:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:19:30 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:19:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:19:30 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8213fee4dface7d727f3195722400e22bb2336086ec2bfe7227bcc99937c33`  
		Last Modified: Tue, 18 Nov 2025 02:51:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca77d618eb5d43b0f8adc781588b1f2a92000acf08e4825ba6927869866c98`  
		Last Modified: Tue, 18 Nov 2025 02:51:53 GMT  
		Size: 86.2 MB (86246298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab6032c5b4f7ebe290f68602f4611fbf5f84641a32c39750aba507b5f4ab8c`  
		Last Modified: Tue, 18 Nov 2025 02:51:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d779b2cebbc40f0d7843bee6304507095474816f0fdb10d7bb1650a04ab682a2`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 3.8 MB (3759689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efca13c3e80701d02c57399f01790ec727d7d1503e30345a1cdb464c422fabf`  
		Last Modified: Tue, 18 Nov 2025 03:10:37 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c386de75e1ebe1aac03333bd217fa931a7d61fc13401e53326f3c7a8385dff`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1c182847c0e609423f07f9de59b087698b4b11a8b24957faeca8050f0fd1b3`  
		Last Modified: Tue, 18 Nov 2025 03:10:39 GMT  
		Size: 12.1 MB (12062734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f81e50af47f3286d7142683ac384595c2a40dd2a5fe19dd1459084e9fe620e`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c6f073bb0046dfd428fdaacb174b65cd7b63416efe96421a2a4d2d08fc82b2`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 9.6 MB (9574594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30860d9404d1d1d62486f8dfc3113156efc34649da09aca5c6eb9d44ec72d81`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ccf578e869e04a660d75c43f9cd763c9fb2af9cd21ac37d269e3f93dda553c`  
		Last Modified: Tue, 18 Nov 2025 03:10:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445805167e1e3615a50d201a04418856392d541f4c20bbf705c3a27feee5d2f7`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a874e97259c38f815da38e9f940978a3ecf65eeb8d499bb68f1520b1f7e24a`  
		Last Modified: Tue, 18 Nov 2025 03:10:38 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acca03d9d26c0a65c519bb70b885eb90e2c1440633d6bc1eade6e3289f842e08`  
		Last Modified: Tue, 02 Dec 2025 01:19:59 GMT  
		Size: 25.1 MB (25077706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca8c4adda422c27950e6e873770a69e9c9ed61868f681931ed6a831accd0ab0`  
		Last Modified: Tue, 02 Dec 2025 01:19:46 GMT  
		Size: 28.1 MB (28129735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9346818b5e097c777c3a414469456444c320aab7dd96507680f5a7d9d2bdb377`  
		Last Modified: Tue, 02 Dec 2025 01:19:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a7493ea209b2ded303dc671a0416cc867ce543a206f840d20d0dd07cc47b13`  
		Last Modified: Tue, 02 Dec 2025 01:19:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ae36bd337c55f5caf9f57bb50cb60283d034d13e5aff1ad3e0aa7294135ba4`  
		Last Modified: Tue, 02 Dec 2025 01:19:54 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927ea140bdcd1855406a8eb668f99ecca432ace56301a2bd70003e02e82b7093`  
		Last Modified: Tue, 02 Dec 2025 01:19:57 GMT  
		Size: 27.0 MB (27024632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22773f7bf25fe373fae8e6144155b4afe68a23f9998b0387eac707b8cc40d289`  
		Last Modified: Tue, 02 Dec 2025 01:19:54 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16503a8a4bc0bab950f4b3599e84958454620050c3a154cfcb0ce9f91b14e2e0`  
		Last Modified: Tue, 02 Dec 2025 01:19:54 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc5fb917c7e231fdccc57eb54c673d47d6ba01836c21694bdf593545f19cb27`  
		Last Modified: Tue, 02 Dec 2025 01:19:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:e66942718a8540f3f11eea505a5ed1cb462b237b7b7fef3f0802c366b9558665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8541072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f38c19fef6975946e50e82a982215c1547ff0a80144b13f8a91c79eb50ea8d0`

```dockerfile
```

-	Layers:
	-	`sha256:2645238ffc81bca6a8fe634743fccd4bed43f0f245c6da1ea2085b0eddc16e56`  
		Last Modified: Tue, 02 Dec 2025 02:25:45 GMT  
		Size: 8.5 MB (8475475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac453b3c5bd9296e19851d2ea86532501030ca553c2fdad6d676012ba5f263e`  
		Last Modified: Tue, 02 Dec 2025 02:25:46 GMT  
		Size: 65.6 KB (65597 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.1-apache` - linux; 386

```console
$ docker pull wordpress@sha256:192d422fe669f69b09afbb6bac5578f717fcf1ea05c1ffaa9982c50856f6c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260931657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d013e0d3c2cb49ed93cf56b41c9b54bc442b9bc9fd31592fdef2055b1165059`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:25:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:26:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:26:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:26:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:26:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:26:16 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 02:26:16 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 02:37:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 02:37:20 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 02:37:20 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 02:37:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:37:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:37:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:37:20 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Nov 2025 02:37:20 GMT
ENV PHP_VERSION=8.1.33
# Tue, 18 Nov 2025 02:37:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Tue, 18 Nov 2025 02:37:20 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Tue, 18 Nov 2025 02:37:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:37:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:40:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:40:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:40:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:40:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:40:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:40:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 02:40:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:40:11 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:40:11 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:40:11 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:12:28 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:12:29 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:12:29 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:12:29 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:12:29 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:12:29 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dff5d0e5bf05f8998ac18c91f70920cb44cfed58345e8fb3e559b44a9e5924`  
		Last Modified: Tue, 18 Nov 2025 02:29:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef968664bb9049499e8b56e7453252be82177ba44637eeaf49a4cab54695a747`  
		Last Modified: Tue, 18 Nov 2025 02:29:54 GMT  
		Size: 116.1 MB (116138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eeefae2df94ecba2088c70577f86e167257d8e9d8c83bc3f458cc7e7df11e6`  
		Last Modified: Tue, 18 Nov 2025 02:29:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c160d4fe0f51473615da031dfb6e3759577462fde3c0ee880311a55fa12c3ac`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 4.5 MB (4455957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478362bfcd1e0d12c5f50eec5098d3967d45216d3adea8edae5c0d4b3397fe5`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08c595424d4e45b8647f54f703f53767e22ac0ce1f815b9760a3c896286e89`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ab4a70d4223d831452b75ace16d27f863eacb04c7e578d7fb37285998a3481`  
		Last Modified: Tue, 18 Nov 2025 02:40:31 GMT  
		Size: 12.1 MB (12064172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c678dd27efe572403e28d00410bde115be74c3ad72877e388ca2dae2c50d1de`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c60b331668f8db26ace52a30b3705b9b99e6ebc16de110581d192ab99c435f8`  
		Last Modified: Tue, 18 Nov 2025 02:40:31 GMT  
		Size: 11.4 MB (11400827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42466b5c3747afdb934801b3d2dacae6cc08a6a07fa4c1c9e603ca271c47b09`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7e73c2ad2fd0deee3fc717ff6938bea3b9fee9f04156f2b08415e2f88f0e5b`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9cfeab331cbcd2754cb94e978cf9fd7487c7b2cbe72964eb70d1c4dfc9dca`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a0d171a35a8ce015b9250a2e8d7002334236b67195ff0e0b3ef7978cd301a4`  
		Last Modified: Tue, 18 Nov 2025 02:40:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03ccbab8d0272210c594c166ec73e4a9a246b2b6f356c2e1a19507c9b80b2ed`  
		Last Modified: Tue, 02 Dec 2025 01:12:47 GMT  
		Size: 26.7 MB (26747391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1061a840b7f2940a39e3f19af3818f154997ef2680021a7d9f3e76f12cfcfa32`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 31.8 MB (31777322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec5cddaa6890ed845f1ed8cd34574283ef6f16335f2f2a218d76c4baf54f6e3`  
		Last Modified: Tue, 02 Dec 2025 02:19:33 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a90db6864c2f2821f9b225d4b0a22846be5fc6aec95b34bf23ae0dd000190`  
		Last Modified: Tue, 02 Dec 2025 02:19:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7583ff10d747c7441c3f70a894d1ccdf8748903edd74016a1f11cef64496a0`  
		Last Modified: Tue, 02 Dec 2025 02:19:39 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e093bf7e647469d3e40c9d3ca18fddb53ad86fca01cc3a4ed561fe6e7fa22a7`  
		Last Modified: Tue, 02 Dec 2025 01:12:48 GMT  
		Size: 27.0 MB (27024641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9744c6a0a65e71ffad406aa3a977814550e761fbb96b1751bcb01c8cbc1a477`  
		Last Modified: Tue, 02 Dec 2025 02:19:43 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3eecb422b61d146053b3e01758b21511f9cb72129e1fd252588cb8897d09e5`  
		Last Modified: Tue, 02 Dec 2025 02:19:46 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb075329f6cff9a827b5a0b595006cfd7bfdc995f189e3bfc09c71f6ec8b5004`  
		Last Modified: Tue, 02 Dec 2025 02:19:48 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:5eca17ab360e67014f39acf13941c5107ff991a824045851c3d1c8fbef48b734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8709989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7715cb7eee1a7600dc527edeb1ddf5bff37511b71690f5b6d8a87685eeccb766`

```dockerfile
```

-	Layers:
	-	`sha256:f0d02cce01278f3139b5672515ff1c682abe828ef8bcbbdd67f1548380aa25a6`  
		Last Modified: Tue, 02 Dec 2025 02:25:59 GMT  
		Size: 8.6 MB (8644626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d856b289770549924cd43210e4f538b4521171124a5dcb01ef941ca99081419d`  
		Last Modified: Tue, 02 Dec 2025 02:25:59 GMT  
		Size: 65.4 KB (65363 bytes)  
		MIME: application/vnd.in-toto+json
