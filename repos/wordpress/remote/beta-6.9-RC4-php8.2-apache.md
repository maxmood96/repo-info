## `wordpress:beta-6.9-RC4-php8.2-apache`

```console
$ docker pull wordpress@sha256:e67d48e873c03944447e65610087f075ec9aed4e975a196c6d555fc7f5fb4ed5
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

### `wordpress:beta-6.9-RC4-php8.2-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:68152bc295819baff90dfdec671b56f48830024b0b980df25d2cd4a7d076d4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262901422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b73839c9af58826f073d3c2571d688b9c82dfbbc3e82caff4ad67451ccdd9c`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 04:51:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 04:51:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 04:51:30 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:53:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 04:53:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:53:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 04:53:58 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 04:53:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 04:53:58 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 04:53:58 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:53:58 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 04:53:58 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 04:53:58 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:15:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:17:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:23 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:23 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:23 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:17:25 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:25 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:25 GMT
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
	-	`sha256:0d6623ff078a3146bc78cdbaac07278e0425e2b8bb42b7be11801339f60264ff`  
		Last Modified: Tue, 18 Nov 2025 04:54:15 GMT  
		Size: 12.3 MB (12328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c916b917a4e0ba6212aacfcb05d630f118baeb47f560fede2c8a61c893a19a94`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63970d68bc98a9ca87d6f7a9aff1f0ee30ce179e70a3ee61695ad73f99f72b8d`  
		Last Modified: Tue, 18 Nov 2025 04:54:16 GMT  
		Size: 11.5 MB (11455569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a12832db6ede0a569bfb5d7eda765e11fdea0ba4d0f970e6aab9793c3f2fb`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f6cc8a11be27ecf903e58ddc12257f98840c4d438e7cec32e36e144533c1ac`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17826b207b79df9708f94382bee44232e1e77f205f16d9182d1c08217012dff`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed224410a7d7b163790edd1f162a9731925230475aae7d1cbc3053450a4787d6`  
		Last Modified: Tue, 18 Nov 2025 04:54:14 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df09eb598487ee2ada22bbdb2fc54239ecfabd6de60c3065239f20ce2d13667`  
		Last Modified: Tue, 02 Dec 2025 01:18:03 GMT  
		Size: 26.3 MB (26297333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d240c4b79a8e8b4361176f023078b27a31010e6cb2b019f5519ea2a5aaebf`  
		Last Modified: Tue, 02 Dec 2025 01:18:02 GMT  
		Size: 33.9 MB (33926478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296522ec7cdc3c856cab1d99343f6070e221d3d6ff8e614a86da0463def45e14`  
		Last Modified: Tue, 02 Dec 2025 01:18:00 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d70ae072a75ca9f38676fd1d0b362c6b138a23620417081dd5aca732881ccf`  
		Last Modified: Tue, 02 Dec 2025 01:18:00 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba83ec670a725482d446ac25f394f23c991c5cc17dee1894e50d0dc005f58ed7`  
		Last Modified: Tue, 02 Dec 2025 01:18:00 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694d01e4932b76455f56a87b07b8fff61ebc70e467adbee2ee751aa6ac9a07c9`  
		Last Modified: Tue, 02 Dec 2025 01:18:03 GMT  
		Size: 27.0 MB (27024639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c154d25b94020e31cd51f14294c3888bd83b3b8f88d67bd2a2973cb91084bb`  
		Last Modified: Tue, 02 Dec 2025 01:18:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751a4cdee20bb4643606145131887b1a28a1f459193a0c7a50213f2e194e55f6`  
		Last Modified: Tue, 02 Dec 2025 01:18:00 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6309ad962c8600c69797fb13b048abb19c41ec28e3d635d3feda977e808b28`  
		Last Modified: Tue, 02 Dec 2025 01:18:00 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:cca5045c637d6bf0ebefcebe26dedc78f4aed71911806b9d792b9c5355ba720c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8737041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384972a25951afe976e57a70910617379cb60296f2e126c4946ea183917a463f`

```dockerfile
```

-	Layers:
	-	`sha256:35a143b4789beea63623d413ada87ab640b4cf560a58d889f4f6fb1b56fe6254`  
		Last Modified: Tue, 02 Dec 2025 02:26:29 GMT  
		Size: 8.7 MB (8671614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0f0432824a70cf05da78db1f89f1a063bee4c8a832078f285bdf29044d742c`  
		Last Modified: Tue, 02 Dec 2025 02:26:30 GMT  
		Size: 65.4 KB (65427 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.2-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:1744947edbb3f93853da96a59d104efebf91abfb8b3f474a031c3f31d205aa8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232420829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fb654b4ff7448c98878cefb61c88efd7193865e5b7e49b281072aceba909b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:23:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:23:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:23:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:23:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:23:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:23:54 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 02:23:54 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 02:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 02:24:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 02:24:05 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 02:24:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:24:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:24:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:24:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 02:24:05 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 02:24:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 02:24:05 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 02:52:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:52:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:55:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:55:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:55:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:55:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 02:55:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:55:33 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:55:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:55:33 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:15:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:25 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:15:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:15:27 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:15:27 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3dca9efd704ad7c9215b8cfc09aaa2789693d60ff157ac02b098e5f9b6ab79`  
		Last Modified: Tue, 18 Nov 2025 02:28:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dee114141ae8402b7663e86c8de26b48c0620b494a57189fbdfd9dbb86d9f0e`  
		Last Modified: Tue, 18 Nov 2025 02:28:24 GMT  
		Size: 94.9 MB (94874447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20761acf67c6e801ea7bf6fcf60d02627c49b8b1da8221e444e8ef4d03c7a33e`  
		Last Modified: Tue, 18 Nov 2025 02:28:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b372216969f09a26a32175eb5c45e273cec8b3e115d06789b7f2c9696d59e4d`  
		Last Modified: Tue, 18 Nov 2025 02:28:14 GMT  
		Size: 4.1 MB (4082063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538428a45668eee79b0ccdbb00f24332727e0b3b29d727264a3215bde3609f08`  
		Last Modified: Tue, 18 Nov 2025 02:28:13 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670a178e24cab567dd258fe879125d63cf7db881201d3a33ef273dbb1fd043f`  
		Last Modified: Tue, 18 Nov 2025 02:28:13 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da659b6bd318570403e6a82ba19b2515801bd72f124737b7531ed6e25e5a0224`  
		Last Modified: Tue, 18 Nov 2025 02:55:52 GMT  
		Size: 12.3 MB (12326025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fcd59f33c11fe7e68741fd22dcbfe1945043d51651dc97c1b27d62282fc76c`  
		Last Modified: Tue, 18 Nov 2025 02:55:51 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598b2151f3d5b5ba73b7a528f4a9bb895ca2d9b9b159b4963b0c3cbdd2cfc902`  
		Last Modified: Tue, 18 Nov 2025 02:55:51 GMT  
		Size: 10.4 MB (10363035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5709016c8776923a36fb2b66c49e94d9fcc81b866bba77d597773ef43890f8bb`  
		Last Modified: Tue, 18 Nov 2025 02:55:51 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca5b2515479518e60e955a468a61288c391944e2a9039215b56b075605155f`  
		Last Modified: Tue, 18 Nov 2025 02:55:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566f96f0ef6a110ddc24ea13d3500183f7f9f907c1dc150fc1977e47c278af3d`  
		Last Modified: Tue, 18 Nov 2025 02:55:51 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f815263c91c982fd4a2f33801b622178a27fb0a225f03afe844bf5866b303`  
		Last Modified: Tue, 18 Nov 2025 02:55:51 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a33193c1dda40802daf930a4198e3153b72fdd2b42f60e743d20ff83a980943`  
		Last Modified: Tue, 02 Dec 2025 01:16:10 GMT  
		Size: 25.7 MB (25728641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdfea53a406ce3d18c2136737c21ca7b791827a1f14d400a1d77fa2385e4d21`  
		Last Modified: Tue, 02 Dec 2025 01:16:10 GMT  
		Size: 30.0 MB (30048185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126856e362f55c32f3b31cd26c6ce42b29afcaa49506f7ddc97b5fe9a52752c`  
		Last Modified: Tue, 02 Dec 2025 01:16:06 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1752293cab1e5c2a191c0229b6b66651602ebdcdf216727f7dc74eba725ef67`  
		Last Modified: Tue, 02 Dec 2025 01:16:07 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c100addb831765c8d7ec23f33058d9c5f9940be6dc4f397fe855e847048d169`  
		Last Modified: Tue, 02 Dec 2025 01:16:06 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c05360d485b82b6bcc613f7e91d1e09cdb4f750bce0e12269ae87de8509cc`  
		Last Modified: Tue, 02 Dec 2025 01:16:10 GMT  
		Size: 27.0 MB (27024649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d51cfac5bbb55f676dae180f41049c320f30fb55c9978dd36593a78964eb40`  
		Last Modified: Tue, 02 Dec 2025 01:16:07 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dac526a644b2320b3ed99948b30236af532e9c08e934a6fd9f9206485fc5ef`  
		Last Modified: Tue, 02 Dec 2025 01:16:07 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2055527e026b78f3eb0f4983a708188805284d932c4240ea993fdb949abf3f`  
		Last Modified: Tue, 02 Dec 2025 01:16:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:eb91d106cc2e6ac9fd3179781a5542a02a90b1ea12316b98815ae290d6dcc32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8536254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7c83e564ef3dbca85805e81c5780ef1162baea8139ac4928196fe8d2773ebd`

```dockerfile
```

-	Layers:
	-	`sha256:71a36977adc00b57a828c01295ce978f3a65941c99f0c3c836690cb3900150a7`  
		Last Modified: Tue, 02 Dec 2025 02:26:37 GMT  
		Size: 8.5 MB (8470647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849a35db50faf3a3619dc28fee56f89fc747ad7f841b7971e7e7ad3c56c26195`  
		Last Modified: Tue, 02 Dec 2025 02:26:38 GMT  
		Size: 65.6 KB (65607 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.2-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:c19d6e8295cca2bbf7d94a5c94f6f733db3fed9a729cae5069a843c9206141ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218704559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7defdf6998eaeb2760a8e9651223223b2db40ea18336563024c1d9730a467e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:40:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:40:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:40:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:40:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:40:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 02:40:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 02:40:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 02:40:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 02:40:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 02:40:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:40:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:40:32 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 02:40:32 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 02:40:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 02:40:32 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 03:00:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 03:00:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:02:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 03:02:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:02:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 03:02:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 03:02:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 03:02:40 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 03:02:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:02:40 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 03:02:40 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 03:02:40 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:18:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:20:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:20:38 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:20:38 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:20:39 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:20:40 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:20:40 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:20:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:20:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:20:40 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:20:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:20:40 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a69703e2c32b745714173808abeee58567ffdaca50c4c672612f96ec63e19a`  
		Last Modified: Tue, 18 Nov 2025 02:43:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c171ce3d12aac431e58d71357ec9ad2b54d63749ce46941bc40de54b4c318a`  
		Last Modified: Tue, 18 Nov 2025 02:44:04 GMT  
		Size: 86.2 MB (86246239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d7ef7b42bac1181a45a17c56730f3572b187a8673192225264e46a8ccc813a`  
		Last Modified: Tue, 18 Nov 2025 02:43:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944247c2fb356ad8f875e92a406e607f2ef8074ea0de4d89f153cf89b1ea901c`  
		Last Modified: Tue, 18 Nov 2025 02:43:59 GMT  
		Size: 3.8 MB (3752400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3416110200cb84d803c60053ba3b598b603ee6d83ea03be0e3b1e79e6d1730`  
		Last Modified: Tue, 18 Nov 2025 02:43:58 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf621a8142349a85e013864d281acb1aac93d09450df67bc169c401b0702851`  
		Last Modified: Tue, 18 Nov 2025 02:43:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02899cbdcc087c193bd4d10d531d913944f74265a631c60ecf88cc1d38f7dbc3`  
		Last Modified: Tue, 18 Nov 2025 03:02:58 GMT  
		Size: 12.3 MB (12333730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d851ecc2707b97bcedce9f9af63486113fa3e5c1914336fedef4caffc7a4e011`  
		Last Modified: Tue, 18 Nov 2025 03:02:57 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f5293daa445538d44870154989ca262c63a7e1fc45aa5e571541d3bb4d55a3`  
		Last Modified: Tue, 18 Nov 2025 03:02:58 GMT  
		Size: 9.8 MB (9840204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1e46eee1d0722ffe0eeff86396c5c35e7cbbcc7b52411f4690e7cfdf9eb38`  
		Last Modified: Tue, 18 Nov 2025 03:02:57 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bebccde76a7a7675388a9148525bab4cca67f667e16c1910e7efec6571241`  
		Last Modified: Tue, 18 Nov 2025 03:02:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f961c170c75fbcf627936846493a590ae708468587386add78344229ce31adeb`  
		Last Modified: Tue, 18 Nov 2025 03:02:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e83cdb0f2ff64b63524bccdfe80ada8960390a115e70025ad6192966f37190`  
		Last Modified: Tue, 18 Nov 2025 03:02:57 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95415a004b7b96f07cd97cf186b7d6f771bcdd3921955d80b3976f87abe43de3`  
		Last Modified: Tue, 02 Dec 2025 01:21:24 GMT  
		Size: 25.1 MB (25077654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b216b6e456c9bf25bb5edff15ce0afa182bdc277878dfc0f4cf07a23ed7258b`  
		Last Modified: Tue, 02 Dec 2025 01:21:24 GMT  
		Size: 28.2 MB (28190074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80069c86ea5f5a50512d0a545516e82e7085f0eb94bdee5a6b502e3dc7c0b1`  
		Last Modified: Tue, 02 Dec 2025 01:21:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f1edc67fc1c526535f8da666aa6018d256bc9fee647a7694e3c16b189feab4`  
		Last Modified: Tue, 02 Dec 2025 01:21:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca7dc470aa71578232ca0803c2d9ac56ac4e6c78c28880b3ca20408cde459c`  
		Last Modified: Tue, 02 Dec 2025 01:21:21 GMT  
		Size: 18.8 KB (18817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6678f212b6d417c629587872d60702a69aaf9cf78efa169f2229a64cbab355a`  
		Last Modified: Tue, 02 Dec 2025 01:21:24 GMT  
		Size: 27.0 MB (27024630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd54b025d8ddceb9149cf16a769a3a525a1e6fd33dbd127b4a7a32a25841e676`  
		Last Modified: Tue, 02 Dec 2025 01:21:21 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f95715da6f08a5d341df7c9be54d582f1bb2b1305c9ba3388348d1f51672125`  
		Last Modified: Tue, 02 Dec 2025 01:21:22 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ce242c42600a50c966922832a09183f23e716c9e33b43f18768781a7dd0db`  
		Last Modified: Tue, 02 Dec 2025 01:21:22 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:9012b9224caf2ad889cc339c02275d972c43fdcf0eb7260ecee047f535288969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8541072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3cfc8ef3c6ba5fe8a271ab49cb670aed143eecb34282b49db7243f878b666e`

```dockerfile
```

-	Layers:
	-	`sha256:22dec09bca86f7ca9b3648c657f5ba995559b9e38b40982f4a8d5a7864c7f403`  
		Last Modified: Tue, 02 Dec 2025 02:26:45 GMT  
		Size: 8.5 MB (8475475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad3cf7d9b96f8d15f4de74c5cda6f52101af99c3206248a407caf020e794a39`  
		Last Modified: Tue, 02 Dec 2025 02:26:46 GMT  
		Size: 65.6 KB (65597 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.2-apache` - linux; 386

```console
$ docker pull wordpress@sha256:1e0f043c35c94b5d391ae7abca433d7e8cdd5371a6ec2b709da8c4630c97c30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261518364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daf8d95dc9c77baa7e3deed858cccfbfb94714d866cda1c0387cc5ba630de56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:22:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 18 Nov 2025 02:22:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 18 Nov 2025 02:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 02:22:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Nov 2025 02:22:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 18 Nov 2025 02:22:30 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 18 Nov 2025 02:22:30 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 18 Nov 2025 02:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 18 Nov 2025 02:22:37 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 18 Nov 2025 02:22:37 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 18 Nov 2025 02:22:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Nov 2025 02:22:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Nov 2025 02:22:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Nov 2025 02:22:37 GMT
ENV PHP_VERSION=8.2.29
# Tue, 18 Nov 2025 02:22:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Tue, 18 Nov 2025 02:22:37 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Tue, 18 Nov 2025 02:34:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 02:34:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:36:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 18 Nov 2025 02:36:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:36:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 18 Nov 2025 02:36:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 18 Nov 2025 02:36:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Nov 2025 02:36:47 GMT
STOPSIGNAL SIGWINCH
# Tue, 18 Nov 2025 02:36:47 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:36:47 GMT
WORKDIR /var/www/html
# Tue, 18 Nov 2025 02:36:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 18 Nov 2025 02:36:47 GMT
CMD ["apache2-foreground"]
# Tue, 02 Dec 2025 01:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:12:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:12:52 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:12:52 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:12:52 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 02 Dec 2025 01:12:54 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:12:54 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:12:54 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:12:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:12:54 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:12:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:12:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d8d073b37fb300d4cd8f5cda36ca6ac5223e91beb28cf32cbf1bf9f36338eb`  
		Last Modified: Tue, 18 Nov 2025 02:26:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d32d7d5705c6bf0610b96d17cfb6e1bc832b18d9ed440476a4650df99854e`  
		Last Modified: Tue, 18 Nov 2025 02:26:26 GMT  
		Size: 116.1 MB (116138552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075b498ea634e45eb310253ccecd3ac585f1878414ae25419ecef27aa8128dbf`  
		Last Modified: Tue, 18 Nov 2025 02:26:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d87bca2d760fc3ac4598b23fa897de0357c6514742b199e7cd5a03a801a999`  
		Last Modified: Tue, 18 Nov 2025 02:26:10 GMT  
		Size: 4.5 MB (4455893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af0e6014184e19a47f18c3c7739c4c1646e9686799d2586047c2f47f7ef385d`  
		Last Modified: Tue, 18 Nov 2025 02:26:09 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e802dd2461597654a53be679e6f58330518d335dad5e4e426cc30326037086`  
		Last Modified: Tue, 18 Nov 2025 02:26:09 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d487e1274a01d96900d079cb8bb08fabef295e68a2c2e015d19b4fdd5cf6c241`  
		Last Modified: Tue, 18 Nov 2025 02:37:07 GMT  
		Size: 12.3 MB (12327516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e376181b94ed65fff20eb88cf1d3a9d780c282add079cf11a6f07b502f7ad97`  
		Last Modified: Tue, 18 Nov 2025 02:37:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10278e61d0db0049c6d6c6ba8ae79bb994789f806572f4836cfe0acb7b2aa6e`  
		Last Modified: Tue, 18 Nov 2025 02:37:07 GMT  
		Size: 11.7 MB (11679365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932499248953b4b2394e8d2563ea99d135baf27399fc59fe84a6d91fa9605cb`  
		Last Modified: Tue, 18 Nov 2025 02:37:05 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf7e870574e6ebe13d88854b40b7b201e56acadb2c43df39e5107a1aeab81d8`  
		Last Modified: Tue, 18 Nov 2025 02:37:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71b9b76c97a89c8822805b82b80f3b1d917a7ea28e6eac6a9280c02d6e98330`  
		Last Modified: Tue, 18 Nov 2025 02:37:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77eaca90a8b3bb3466422432a802d0a961d2596f6eadd0545c9ba0b2545a7d6`  
		Last Modified: Tue, 18 Nov 2025 02:37:04 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de53db0007035d6d17cf4852d0ed60abcf67f7fa7e2338863f29cba2a0d1c9b4`  
		Last Modified: Tue, 02 Dec 2025 01:13:36 GMT  
		Size: 26.7 MB (26747400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca8f62fcf97a455783dd6cd25f313da3da359a2b92601211df9cc7c72e2497d`  
		Last Modified: Tue, 02 Dec 2025 01:13:36 GMT  
		Size: 31.8 MB (31822301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acec20e1b5789f789f4b1617659701bb1ed2dea613848f01224ebf410f162b8`  
		Last Modified: Tue, 02 Dec 2025 01:13:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f22a88d90a11190866fd6c30c015ff3a3f8faca2c5e590e9bc7c90b56857fc`  
		Last Modified: Tue, 02 Dec 2025 01:13:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f080509e2b42e37e96760e143729bc1626d16b422d85bd4776603a5cda0514`  
		Last Modified: Tue, 02 Dec 2025 01:13:31 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb9e318e1e6ca87f5418483e84cf533f38cc58a8f0ed33569e21ea2a557aaea`  
		Last Modified: Tue, 02 Dec 2025 01:13:34 GMT  
		Size: 27.0 MB (27024621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d38ef06eda4dbf52c6d062102829fd421e8e33b46d8246148702f6f3df4d8`  
		Last Modified: Tue, 02 Dec 2025 01:13:31 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af77ae4bfe38f84c6bc0decfb25d43ba1e7c877b81f1dd5dbe728b0ecc7566`  
		Last Modified: Tue, 02 Dec 2025 01:13:32 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7f96a31ec4e0511a86f5628583abcf9901bdef5c57e1aca695d7db07719cb`  
		Last Modified: Tue, 02 Dec 2025 01:13:32 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.2-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:45cfbe7c3180b7b7ba476d64823749cf33ebebfcd59950104467ac7278aacf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8709989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dbcea98a687da556919dd6e0c25990960033f93ee436f6f14589652974ce0e`

```dockerfile
```

-	Layers:
	-	`sha256:eeb0f483d9856f34d67729479f5f17494eba5210f2a776aa35f257e9c5df1d45`  
		Last Modified: Tue, 02 Dec 2025 02:27:00 GMT  
		Size: 8.6 MB (8644626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1599a76be10bada40e08e0e4282c877e3c702a4cfe6251b26b6ed04b4ad1b6c6`  
		Last Modified: Tue, 02 Dec 2025 02:27:00 GMT  
		Size: 65.4 KB (65363 bytes)  
		MIME: application/vnd.in-toto+json
