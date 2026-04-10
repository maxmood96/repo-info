## `wordpress:beta-php8.4`

```console
$ docker pull wordpress@sha256:4698315f94bc5eb7a69af6bcf261020f0f5df962766f009b662f2e29f158ba98
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

### `wordpress:beta-php8.4` - linux; amd64

```console
$ docker pull wordpress@sha256:c727826c870583754be95b3652b33141a9398ba7f7c107108ceb95fd198e707a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274493228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dfdd607cf133991500927bb29db977350ba80590c375576fdcad7935f8ae5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:15:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:16:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:16:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:16:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:16:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:16:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:16:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:16:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:16:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:16:17 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:16:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:16:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:18:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:18:54 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:18:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:18:54 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:18:54 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:18:54 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:13:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:13:46 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:13:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:13:46 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 09 Apr 2026 23:13:48 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:13:48 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:13:48 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:13:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:13:48 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:13:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffb7e1d7f94860f5b3a9e2df478da8a2661498b38db3222d9490e0e63fd1e07`  
		Last Modified: Thu, 09 Apr 2026 22:19:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd73acf43b8d72c9dce9d17f01a9fc96884e893fc0702b8be4ba1e9b39945ca4`  
		Last Modified: Thu, 09 Apr 2026 22:19:17 GMT  
		Size: 120.8 MB (120798321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e27b2414675d618ef8d63b7faf256eda9fb801f17c768ca2b063c97843fa451`  
		Last Modified: Thu, 09 Apr 2026 22:19:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc31bb8e9d4fc68dce9e7c72545b026b8586fcc7b7d99976a216777b9b33fe`  
		Last Modified: Thu, 09 Apr 2026 22:19:14 GMT  
		Size: 4.2 MB (4227183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c95eebb2f652d3f8bc58d02c8f368f5be63a1f67390fe9de93e6baba1956a99`  
		Last Modified: Thu, 09 Apr 2026 22:19:15 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf8294cbce8072b8bef494170ec4e214049a03390ca4d566e00156e38f30e18`  
		Last Modified: Thu, 09 Apr 2026 22:19:15 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c151ee09453b87c82f5735f7018d15ed5d30c6041dc559bc10bb7d30f0d7afe`  
		Last Modified: Thu, 09 Apr 2026 22:19:16 GMT  
		Size: 13.9 MB (13852862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f6373c27c3d7dd9b7e77fed7edc59b8be02efab451f8d8ba326a7490553753`  
		Last Modified: Thu, 09 Apr 2026 22:19:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9737d96107ee92514e5d96eeb1a70a902de902fd2ed8001a3805160ec1d84f5d`  
		Last Modified: Thu, 09 Apr 2026 22:19:17 GMT  
		Size: 13.6 MB (13557848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48126b155e192ea24076e34fbca93a8b1c6291af2f36f25d9a0cf5fc5aee768`  
		Last Modified: Thu, 09 Apr 2026 22:19:18 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2952872e255d2257f7578c14704e67ae49e1be9cf71b56b1ee7dd00650fcb77`  
		Last Modified: Thu, 09 Apr 2026 22:19:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e305ee441fb9d0e7a2339b25d3413b213db2965089b29aee05d045863217b97`  
		Last Modified: Thu, 09 Apr 2026 22:19:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e170750ef23969459ae184cc5b350c055501327c889084b0d23dc8c77ab3c`  
		Last Modified: Thu, 09 Apr 2026 22:19:19 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b5703e783cccf22831a148d97835dbcbd3c87f22c76c7308f37681bbd0b313`  
		Last Modified: Thu, 09 Apr 2026 23:14:05 GMT  
		Size: 33.0 MB (32954002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5a89c85e7e74931a4b621eefc9753b4e6653fb7c399f277ac7e50c3c307935`  
		Last Modified: Thu, 09 Apr 2026 23:14:05 GMT  
		Size: 30.0 MB (29974267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c0bcd1532adea7824fe866cce6602cf2274d59884381d0bd622a1d590ed142`  
		Last Modified: Thu, 09 Apr 2026 23:14:04 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010a90cdc6ed438c482c48e91b89f28cc42e592d7ff1378fb193b9a14d166877`  
		Last Modified: Thu, 09 Apr 2026 23:14:04 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5675511bac1c5adee6abd7951ce9b1951edad37058022212213b7eeb9e11eb3`  
		Last Modified: Thu, 09 Apr 2026 23:14:05 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8618b6a34c15e462aa5149e51fcfd07443b53f3977fb046f411e7cc18ba17350`  
		Last Modified: Thu, 09 Apr 2026 23:14:06 GMT  
		Size: 29.3 MB (29323469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9558e1492c02f5f3e1e90ce0da5fed352a7ff836b9af37535914bdc89d930cc`  
		Last Modified: Thu, 09 Apr 2026 23:14:06 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25ecd544c6016722d36f07892de3ef2895626871104309e608d11004b2323d7`  
		Last Modified: Thu, 09 Apr 2026 23:14:07 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155a05d753f0ae8eaaafa45c064f23df7c24fc8e7a01a523781d40de4124d84d`  
		Last Modified: Thu, 09 Apr 2026 23:14:07 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:56b97dcdd509bc96bd7f989ef74c6faaad64e8ea2df5ee4ab456a689bf2b2c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8759560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c6c9a1d2c1a1d0ebd4eefd032af35a66fc968d70fb201f045b4ff01ba9d069`

```dockerfile
```

-	Layers:
	-	`sha256:697764656df032472624b426526581be872dde12b113b2321579aff0bc0b1b30`  
		Last Modified: Thu, 09 Apr 2026 23:14:04 GMT  
		Size: 8.7 MB (8693692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1fb9ae0b43962ec10f586abd34cbe601bcfd2113f65cb483a361f0dbad9387`  
		Last Modified: Thu, 09 Apr 2026 23:14:03 GMT  
		Size: 65.9 KB (65868 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:f0d363b8e8f59928934a6372f924083d0bd3109aebd69866220e0c46dde73448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242182564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf39718d83f5b54b220b4938893baa971486b256f587448bcce19c79d8417e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:23:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:24:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:24:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:24:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:24:19 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:24:19 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:24:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:24:28 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:24:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:24:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:24:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:24:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:24:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:24:29 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:24:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:24:29 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:24:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:24:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:28:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:28:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:28:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:28:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:28:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:28:00 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:28:00 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:28:00 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:28:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:28:00 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:17:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:19:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:19:52 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:19:52 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:19:52 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 09 Apr 2026 23:19:54 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:19:54 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:19:54 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:19:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:19:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:19:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:19:55 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780be59d96728ad47535e05525d1220285e788aec1caf59d3077fbc651ad598d`  
		Last Modified: Thu, 09 Apr 2026 22:28:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b0c982be7a49fb5f03b96a624fbc9d81045cfc3e4e3b5769cd4d9498cfdc9`  
		Last Modified: Thu, 09 Apr 2026 22:28:22 GMT  
		Size: 97.3 MB (97253012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ac65776d6d5b6e37aadb3440eef508e59c333a8c670a8763aa689862b50703`  
		Last Modified: Thu, 09 Apr 2026 22:28:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1571d55ad280be8f1eb504ed3664dbc3a29611d19571c95b3f8b58fbf4dab444`  
		Last Modified: Thu, 09 Apr 2026 22:28:20 GMT  
		Size: 4.1 MB (4089530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad6236c2f611ce01667c1a4410c43450ba4317baf11a0ea2cdc76360fddce18`  
		Last Modified: Thu, 09 Apr 2026 22:28:21 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90608dee01995f03f67ad383bf9875c74745cafb90220ab90646e6798d12e5ad`  
		Last Modified: Thu, 09 Apr 2026 22:28:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1dd59fb63293555263be1b569c46a2b4b1b0f77c6f476cd632602f40840899`  
		Last Modified: Thu, 09 Apr 2026 22:28:22 GMT  
		Size: 13.9 MB (13850229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c0096909d5235e93c52e529083d8a37c6a074f815dfb8e6e3f3a42276b0c1e`  
		Last Modified: Thu, 09 Apr 2026 22:28:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa429e336e671b13554b0d8a39ff32af6dc0a100a908a934299c4bd60ac120e`  
		Last Modified: Thu, 09 Apr 2026 22:28:23 GMT  
		Size: 12.2 MB (12206435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff306b0c979dc5bbffd63ad7d40394edd13c46d16e61ddecb8c86d843313781`  
		Last Modified: Thu, 09 Apr 2026 22:28:23 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1392c03353241016914ea00bb7d7f397cc1bf9e080c6be9babcb60d517dc8fbd`  
		Last Modified: Thu, 09 Apr 2026 22:28:23 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d48238172b0090a21b0356513adc85400ba21b991ef5c64450f1d438d9d21b`  
		Last Modified: Thu, 09 Apr 2026 22:28:24 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2854efed5ef145bf58facd57b13c9f7d9f33bde912f3755c7f7a2a8e78c3de6`  
		Last Modified: Thu, 09 Apr 2026 22:28:24 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74975155d63b661b6ab82cb847c3f91c96ec133cdfeb205246fffccfdf7ff4c`  
		Last Modified: Thu, 09 Apr 2026 23:20:12 GMT  
		Size: 30.1 MB (30142018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824de612bb5e4a664f15ba8579766cf0506bd4a4d565c3be33640314552a16df`  
		Last Modified: Thu, 09 Apr 2026 23:20:12 GMT  
		Size: 27.3 MB (27344429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acc0df449ae55ee3f4713fb4dd1b34cb53beaa4757adb97d87a0dd338e5b99b`  
		Last Modified: Thu, 09 Apr 2026 23:20:11 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e99ad96384cd54d70caf3b3cdb38ec3336a213f48bfa8d3191ee79426aa1680`  
		Last Modified: Thu, 09 Apr 2026 23:20:11 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259368ef5eb1aefb603beb3dac91f2b9b94a856192f0f6d254f59d596019c0b3`  
		Last Modified: Thu, 09 Apr 2026 23:20:12 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e1876f40bc46a76df92e0c2ae9a8ea720fe022e03f9c8c3cc469685fb429b`  
		Last Modified: Thu, 09 Apr 2026 23:20:13 GMT  
		Size: 29.3 MB (29323461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855c0972a7b62d10a3898ced5fe8a01c75dd1596479a91ef5df32b266dacefb3`  
		Last Modified: Thu, 09 Apr 2026 23:20:13 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0627981a612799d872d25ec8ef2d8fb0bde3a71f365ac7bc3b3ba66cefde196f`  
		Last Modified: Thu, 09 Apr 2026 23:20:13 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bb3c9cca96c2cc0c116d05ce3521f3d586cf21b679618d86097a2ef69a0f22`  
		Last Modified: Thu, 09 Apr 2026 23:20:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:4b1ba5342b43857c12990d20d3c90636e7437ff6fa1da444665927366074e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8553299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bc689fe55d40bb41628f198616d91277f0d29629b5d8b206d77ba81a0b3ae0`

```dockerfile
```

-	Layers:
	-	`sha256:4d6c2855ba48ce363086c9c1ce3f878231e5de1c6ce526f4574354848838b651`  
		Last Modified: Thu, 09 Apr 2026 23:20:11 GMT  
		Size: 8.5 MB (8487251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b8705a07ebf0ed2adefcb0201ae418c6d9b5c43cbcf32006b8165e5fafddc0`  
		Last Modified: Thu, 09 Apr 2026 23:20:10 GMT  
		Size: 66.0 KB (66048 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:433aa9bd8b745b6512693ae6b341b6687237f98a9bca68d771c069669bc0033c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228064407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a48e1c1d50f2c81a06eb37172abd99bc34ed5eb0221ade795b9108c2911019d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:23:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:24:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:24:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:24:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:24:13 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:24:13 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:24:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:24:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:24:23 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:24:23 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:24:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:24:34 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:27:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:25 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:27:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:27:25 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:20:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:21:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:21:54 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:21:54 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:21:54 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 09 Apr 2026 23:21:56 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:21:56 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:21:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:21:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:21:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:21:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0128c6517e22ae07a90d2d53d482b1ccf7b914707f39c4b40d9e304ae6ec4cb5`  
		Last Modified: Thu, 09 Apr 2026 22:27:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d854cffdaee5fd297d469b8963aebb247498d83a49a7c5deb26d68f1ca7c1e`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 88.5 MB (88463301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd78e7b03a1506505ff4e2357beba6c4855c1e762463f1262aeaaba547d4b`  
		Last Modified: Thu, 09 Apr 2026 22:27:42 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fd66de35fc4b6b762abfe39a9442a2d4efa944581b0a7eb7033c21ac84d157`  
		Last Modified: Thu, 09 Apr 2026 22:27:42 GMT  
		Size: 3.8 MB (3757405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260c13ed7dc08209d20d334187f9a51c2cefd9a568d2519f095e1dc912a853a0`  
		Last Modified: Thu, 09 Apr 2026 22:27:44 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd003c675d84dba2ce06cc80ceeb1992de569cc5d18f6d7f551f1feb3a2bcc`  
		Last Modified: Thu, 09 Apr 2026 22:27:44 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac37e47d191b62e7f6e43458346d6f3355a25b461964bd0ed801a4ba679dcac`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 13.9 MB (13850372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cb6d95e03404421d8eb92e7a8a2fc508d5c9e783e0d209d20108f234083c2e`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e11293b6092bafa94f6c635f63a063f53445de6c79c42486e077a8a7b331bb`  
		Last Modified: Thu, 09 Apr 2026 22:27:45 GMT  
		Size: 11.6 MB (11617794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d8282280582efe36635d2dcbcc9d09807c4d617ea798fdaf20a672500ff66`  
		Last Modified: Thu, 09 Apr 2026 22:27:46 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1925ff69bb29d6cea799781584b619aee1df1ebfbb7d0358d5edfb3c5829e43`  
		Last Modified: Thu, 09 Apr 2026 22:27:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcefb6170cb2f4cc0af2a8f801e8b2bc784e377dcf4066936c1899fde82f17e`  
		Last Modified: Thu, 09 Apr 2026 22:27:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6453786394b4d850905bf56d93207bd709039503ce5b4dd85574e3b10ad46833`  
		Last Modified: Thu, 09 Apr 2026 22:27:47 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69176cebfb22527c30612e5b8aa99f3669e4e632cb49773ad78804eb35b3e54`  
		Last Modified: Thu, 09 Apr 2026 23:22:12 GMT  
		Size: 29.0 MB (29041043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705ce064dcdaddad6878de76ef578e007c6b78e3eac0c94527e5a74679d44e17`  
		Last Modified: Thu, 09 Apr 2026 23:22:12 GMT  
		Size: 25.8 MB (25771723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6dc563de7aeb2384551e8109618f2bcc95607355e2243ee99b575f848538bb`  
		Last Modified: Thu, 09 Apr 2026 23:22:11 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb2b15121cb63d8456f07cc86ffd20bbb720b7f395ead3073c18e714a8a137e`  
		Last Modified: Thu, 09 Apr 2026 23:22:12 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4d17a63dedad8c6a69ca54f21ed314649a680002eb020921fb8a1783bd66af`  
		Last Modified: Thu, 09 Apr 2026 23:22:13 GMT  
		Size: 18.8 KB (18793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29955b7e629f8551441a8585b1d9770ee9f657d85225949089f716ca098ac43a`  
		Last Modified: Thu, 09 Apr 2026 23:22:14 GMT  
		Size: 29.3 MB (29323471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bfbc4f5757abcd8b45536b7d445ac36f9bb0702f389510bfd7e2a0713b65b5`  
		Last Modified: Thu, 09 Apr 2026 23:22:14 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36c1e1d35c7df73be0ac9a9d80fd4d0c6ee8872931f82e0cb43d8cd6259698b`  
		Last Modified: Thu, 09 Apr 2026 23:22:14 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e4862e53d70e195c7e4b579da8284aab4536b23a410276d24ea870c25b9276`  
		Last Modified: Thu, 09 Apr 2026 23:22:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:d85be9a2ba92e91ac81a7f2a20ec4d4ce3588c23927bf6a95fcdd46068763873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8558134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efad5726814690d858db56e526f706a3e49c09fd094e6cea5133b438dcea466d`

```dockerfile
```

-	Layers:
	-	`sha256:a7fa89fa0aabf53019451353c434697b52bc1ca716f3cefbf9af51d8cb38ea2a`  
		Last Modified: Thu, 09 Apr 2026 23:22:12 GMT  
		Size: 8.5 MB (8492085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e834845f3fbe7e5d0e74d9e622dca22d6631abaee0d1fd6639696280507014`  
		Last Modified: Thu, 09 Apr 2026 23:22:11 GMT  
		Size: 66.0 KB (66049 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0fccb46ea22f8e75d280f3895d4ba06d907e6e20368dfe2e4d0868ee7c98898b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267122327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4890a713c0641a6ca01771b6d8867b9b55fff7b2a992f47f9475a576583808e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 22:16:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 09 Apr 2026 22:16:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 09 Apr 2026 22:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 22:16:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 09 Apr 2026 22:16:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 09 Apr 2026 22:16:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 09 Apr 2026 22:16:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:16:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:16:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:16:45 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:16:45 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:16:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:16:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:20:01 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:20:01 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:20:01 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:20:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:20:01 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:12:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:14:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:14:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:14:17 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:14:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 09 Apr 2026 23:14:19 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:14:19 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:14:19 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:14:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:14:19 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:14:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338ea32ccb6710f9a682185fd06ae9ec4f900b61387416169639d8ea6c2cc0b`  
		Last Modified: Thu, 09 Apr 2026 22:20:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc88cb1f79996d45df348bb492317d64532bd42f62297aa7bea02d90003a9be`  
		Last Modified: Thu, 09 Apr 2026 22:20:26 GMT  
		Size: 113.5 MB (113507428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fed35923d21dc60ad69bc693d326331e0a0c7073e561b4a44d5ba25504166c`  
		Last Modified: Thu, 09 Apr 2026 22:20:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a06a2c5945814b4e74d4f46092aeecf8c2de9e39a6ab51d0e25c3f569f24f4`  
		Last Modified: Thu, 09 Apr 2026 22:20:23 GMT  
		Size: 4.3 MB (4305799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4ec882417cf6b7335d4f14a8abdb39fac07521db952fddacf1ef75e9d16ceb`  
		Last Modified: Thu, 09 Apr 2026 22:20:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731768ee0f6fb461e3600410b457fbc6bbe938ebaf5275067ba9912aabeb1f3`  
		Last Modified: Thu, 09 Apr 2026 22:20:24 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8881a242eb81a0565a768bdcc648a7147149c032b758e29cc4039b5914b295`  
		Last Modified: Thu, 09 Apr 2026 22:20:25 GMT  
		Size: 13.9 MB (13852382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fccd83ca47a53cb0d9f8e783cef04bd25f0506ea44ee9dfcdd1717eb9f5aaa1`  
		Last Modified: Thu, 09 Apr 2026 22:20:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ea7ac474f047296270655a2dd8c8175c85ebfc9d7d983c0737933d479ee6b2`  
		Last Modified: Thu, 09 Apr 2026 22:20:25 GMT  
		Size: 13.2 MB (13206297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d31a0f1b8754c4d349dbfeda5eb674bb6939768c0036f19ae26c4a19e042549`  
		Last Modified: Thu, 09 Apr 2026 22:20:26 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7266fa89a433a670a82c0e0744a4bdf11227ce5865a30269c8a41353ac6d2d09`  
		Last Modified: Thu, 09 Apr 2026 22:20:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c46f206b133b93ea1e49cfa9e70c50747d808b8938b0dc73ba86015fae98c`  
		Last Modified: Thu, 09 Apr 2026 22:20:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edcfc2b7d3dbe1ff7618369da15633d8e17cbd51e7fce9a81d6f9d622e63bb9`  
		Last Modified: Thu, 09 Apr 2026 22:20:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e1e149ed0ee64f79528e060906d45c7e0867c6269656add9ae8cbe05e01fad`  
		Last Modified: Thu, 09 Apr 2026 23:14:37 GMT  
		Size: 34.5 MB (34465712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8336ac829f5cc7673490def50c9ee7ed40e82ead7d518d4e4c7beba82d835f`  
		Last Modified: Thu, 09 Apr 2026 23:14:37 GMT  
		Size: 28.3 MB (28293065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03231478fab83afc84f815cbd9ed3b05506709e327b5c2ad0e7cd3fabf78a119`  
		Last Modified: Thu, 09 Apr 2026 23:14:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6cf0519a55c492b1a77455f969f6ed13bf71ad24b1e877ac012d608f420fd6`  
		Last Modified: Thu, 09 Apr 2026 23:14:36 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71282390bc37b5b820dacdc48366894c2e2342e61cf5b6686231134e9610747d`  
		Last Modified: Thu, 09 Apr 2026 23:14:37 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb8c4ca91abb49066d32c2fc64c79a62b044ea7e09f76e8b4963919b2401eeb`  
		Last Modified: Thu, 09 Apr 2026 23:14:38 GMT  
		Size: 29.3 MB (29323451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3cbcd1880df2607b41a35d0151bc360726bc56997fab2320e99700624adf24`  
		Last Modified: Thu, 09 Apr 2026 23:14:38 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d910ee12be3bf4c14fe9c0eca59906d33c9915796a0a089006be6f3a1a4f68`  
		Last Modified: Thu, 09 Apr 2026 23:14:39 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7926c1b22e8b6522ddba7540f4d73073bac82e38e0e26eb46646134653f259`  
		Last Modified: Thu, 09 Apr 2026 23:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:f0316c7db28f242ba077f0e0b2f6342a6886a1eaee29a19bb7cf20a66df6e25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8856320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d92e1d1ba0695474d8f5557019e0d2ebd980209656eb7bdb337df65b592bb1`

```dockerfile
```

-	Layers:
	-	`sha256:74ec3a1fa81d868d0a4d288ea8ac342347cb9d4cbaa42e6b4547bd4022bbcccb`  
		Last Modified: Thu, 09 Apr 2026 23:14:36 GMT  
		Size: 8.8 MB (8790210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1837b071e4a9e360487f080ee88077e4fddbe7c5c19a9d68896856d9918a4fd0`  
		Last Modified: Thu, 09 Apr 2026 23:14:35 GMT  
		Size: 66.1 KB (66110 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; 386

```console
$ docker pull wordpress@sha256:dd852e631acfa37118cb7cb65546aa12bbdf4103d68e5b179f79760dd7a2211e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269386158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8025a8a4e456df6ea3920aabb246437c1121b177fbcd4a9e84ef0f1f6173060`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:27:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:27:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:27:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:27:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:27:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:27:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 01:27:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 01:27:58 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 01:27:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 01:27:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:27:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 01:27:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 01:27:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 01:27:59 GMT
ENV PHP_VERSION=8.4.19
# Tue, 07 Apr 2026 01:27:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Tue, 07 Apr 2026 01:27:59 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Tue, 07 Apr 2026 01:28:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 07 Apr 2026 01:28:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:31:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 07 Apr 2026 01:31:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:31:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 07 Apr 2026 01:31:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 07 Apr 2026 01:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 07 Apr 2026 01:31:15 GMT
STOPSIGNAL SIGWINCH
# Tue, 07 Apr 2026 01:31:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:31:16 GMT
WORKDIR /var/www/html
# Tue, 07 Apr 2026 01:31:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 07 Apr 2026 01:31:16 GMT
CMD ["apache2-foreground"]
# Tue, 07 Apr 2026 02:40:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:41:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 07 Apr 2026 02:41:40 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 07 Apr 2026 02:41:40 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 07 Apr 2026 02:41:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 07 Apr 2026 02:41:42 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 07 Apr 2026 02:41:42 GMT
VOLUME [/var/www/html]
# Tue, 07 Apr 2026 02:41:42 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 07 Apr 2026 02:41:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:41:42 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 07 Apr 2026 02:41:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:41:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd659f813539fb29912a91838eea294834d8e78ab2e636ce173cb8ab112bc8`  
		Last Modified: Tue, 07 Apr 2026 01:31:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d527f2f67c7814caf2ca551adf495ffe1af459f505df0978e2f5711eac2c55`  
		Last Modified: Tue, 07 Apr 2026 01:31:39 GMT  
		Size: 116.1 MB (116144404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fd97cc6dd90402ec0db9c710495c4abed18d5b5a13ab301d6ead05d822526f`  
		Last Modified: Tue, 07 Apr 2026 01:31:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd6da33ccd19e26f74338a1391c6a9682fe37a0c2a42599bbefab5930677100`  
		Last Modified: Tue, 07 Apr 2026 01:31:36 GMT  
		Size: 4.5 MB (4458422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dbc919bef71284cc2c904e6cbf12eda8e94a76a580d023582faf5d99b3b182`  
		Last Modified: Tue, 07 Apr 2026 01:31:37 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b531f466e6e6a44499621fa799dbf807712dd22d75ad0d419585c07b3b7211c5`  
		Last Modified: Tue, 07 Apr 2026 01:31:37 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8d0f103f9aa39d5c722001b950cd208c2eb65ff4c5597609e0b38447ded5c0`  
		Last Modified: Tue, 07 Apr 2026 01:31:38 GMT  
		Size: 13.9 MB (13850171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffffcc5755e52b54f6dea3164f89fac3002ea61d4b8267765d0ad05389e4fac`  
		Last Modified: Tue, 07 Apr 2026 01:31:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72d0ab9bef61259441fbb89df707bc03087ebf2f0666f9f83d01dd26b43a196`  
		Last Modified: Tue, 07 Apr 2026 01:31:39 GMT  
		Size: 13.8 MB (13849409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92fab02706b487144b1c252a183229ab8874ef77f8a4e9d18e801facfd77ac`  
		Last Modified: Tue, 07 Apr 2026 01:31:39 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005cb3cae76f4c8fee2c50de8e62b4fadc3ac7dd268693cc8202db5e8f60e2fa`  
		Last Modified: Tue, 07 Apr 2026 01:31:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc6382616ed910d5540075c3b5ea0591ef2c8e055785e366c91fc61ffaf57c`  
		Last Modified: Tue, 07 Apr 2026 01:31:41 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb2ac1e31ae82b1d5f23f4eefb6111b5a2c2675659c90c8fa5c1571ff2a1317`  
		Last Modified: Tue, 07 Apr 2026 01:31:41 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3712e2e1dcd220cfdbc7077e65a41c054940b66ed269f1b91eed0de6bd47e6ea`  
		Last Modified: Tue, 07 Apr 2026 02:41:58 GMT  
		Size: 32.4 MB (32406016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701d62f7d27855d070d1e382784211ed53b978d0ab87dd67144e869060932ded`  
		Last Modified: Tue, 07 Apr 2026 02:41:58 GMT  
		Size: 28.0 MB (28033391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b29a9cb8bcaa59cac7ebb18cf34863e9c6f762e5e3af2e72f8eaf87c875af1`  
		Last Modified: Tue, 07 Apr 2026 02:41:57 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8702c35b01caf8115f0111f46d1bc87a205fa1ef8710d9d42e9c0252e70b5b16`  
		Last Modified: Tue, 07 Apr 2026 02:41:57 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc523ef08ec31997a3758a544ed6e7af38ffa5797e36b89236d390b340618445`  
		Last Modified: Tue, 07 Apr 2026 02:41:58 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77cb459ae380ed0690a1d1dbe68c32fb16f6d37229881fae8395358662aada3`  
		Last Modified: Tue, 07 Apr 2026 02:41:59 GMT  
		Size: 29.3 MB (29323472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bc694c6fb4fe3d17856eb8d8b1c802e7cb9ef1b48f96cfdea8c23c023d9ca5`  
		Last Modified: Tue, 07 Apr 2026 02:41:59 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869fd448e610594f80e20797be426723707a89c1bc83082840a2b00e1d61c4e8`  
		Last Modified: Tue, 07 Apr 2026 02:42:00 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99047d6126901b4b9f756b2690cffff6b333c0bd731aaec9dbac2460224e48`  
		Last Modified: Tue, 07 Apr 2026 02:42:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:f42f38cb06d77d12526943528e02ae802406026422c7258573d49c7799add240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8732501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d21bab221f9024335ee20e1144650e06c7853a89801d365d477aa85e0d6414b`

```dockerfile
```

-	Layers:
	-	`sha256:bc4a2c66920ae28944359409d3f3293f0222c704e836f9c20409d2a750be01d2`  
		Last Modified: Tue, 07 Apr 2026 02:41:57 GMT  
		Size: 8.7 MB (8666696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f97022c6de13d91c6ef7ab965a14b04c3c7314818b12646274495e1e09075b88`  
		Last Modified: Tue, 07 Apr 2026 02:41:57 GMT  
		Size: 65.8 KB (65805 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; ppc64le

```console
$ docker pull wordpress@sha256:4ffc60f277383f2bba82a96db242ea733dcfd790bd9aee857977ea0d7b92301c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271155753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63c9f4d142cae1ce4ada1a42ab2a7fb63c1495ce6a90c0f31761d00b5f5e43a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:52:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:53:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:53:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:53:06 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 07 Apr 2026 02:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 07 Apr 2026 02:15:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 07 Apr 2026 02:15:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_VERSION=8.4.20
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Tue, 07 Apr 2026 02:15:48 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:50:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:55:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:55:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:55:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:55:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:55:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:55:37 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:55:37 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:55:37 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:55:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:55:37 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:54:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:54:38 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:54:39 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:54:39 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Fri, 10 Apr 2026 00:12:58 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 10 Apr 2026 00:12:58 GMT
VOLUME [/var/www/html]
# Fri, 10 Apr 2026 00:12:58 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 10 Apr 2026 00:12:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 00:12:59 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 10 Apr 2026 00:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Apr 2026 00:12:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9146bf73c8a452f415773cc4d7b28152e6a0132b4872c062036e93ceda4a1`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f4a0e07fb6454284581cfcdd933b1a8aeaf834a24a8768bd1bdee7fe76ac43`  
		Last Modified: Tue, 07 Apr 2026 01:58:49 GMT  
		Size: 109.6 MB (109599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79e4f5187124bd689202e1c0b532dcdbfed0adfcf45354b5dcc246a80a88c8e`  
		Last Modified: Tue, 07 Apr 2026 01:58:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c2826d5bd7597d2bc055cec74a30953477482f418eb99bc191b54a5657bea0`  
		Last Modified: Tue, 07 Apr 2026 02:22:07 GMT  
		Size: 4.9 MB (4881630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4711f0a1e700d515af14d521ed74bc330dbff10a897db0c88f1da3017c82e`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ea076c7d43b09b2edeb333274a93e4615a067914cc9eb5a71e39816735581b`  
		Last Modified: Tue, 07 Apr 2026 02:22:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dec351a1ea0e9f8260db0fe7f5d544d413ead98aa6f93faf52f5156bb42d56`  
		Last Modified: Thu, 09 Apr 2026 22:56:06 GMT  
		Size: 13.9 MB (13866829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f754301576436903c98219c1253480fba798fa000796d9db4f6011448f5160`  
		Last Modified: Thu, 09 Apr 2026 22:56:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b357d4da30965de24a959c63bc4844d6f6f5beb41154aab5e98cb072cd32d1ca`  
		Last Modified: Thu, 09 Apr 2026 22:56:07 GMT  
		Size: 17.6 MB (17628234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17fe5d72f918a62b30ed32340ee8d5cbbd95d30d46fd2d9f868466d9e98dfa2`  
		Last Modified: Thu, 09 Apr 2026 22:56:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd59e22820a87e6bdc0facc2a3223bc3c80db8152bfef03f17ea6d6137c1be3`  
		Last Modified: Thu, 09 Apr 2026 22:56:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8543dcddba6ccd9c73c4c19848d0c9fccd12afdd8e85a282bf1cd6198558483f`  
		Last Modified: Thu, 09 Apr 2026 22:56:07 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1582253340f81d8245e092973d69ddd30341420233cde15f2aa9bc04b2d52f7`  
		Last Modified: Thu, 09 Apr 2026 22:56:08 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28fb2433252e40e497ea6ab1b85dcc40ba505b7e4b7631f250c3fe248be0aec`  
		Last Modified: Thu, 09 Apr 2026 23:55:40 GMT  
		Size: 33.0 MB (32952436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812edf3ef6deb2f6813aab6caba4a575a9678da8eca77e1ab6e50eb0b876ba84`  
		Last Modified: Thu, 09 Apr 2026 23:55:40 GMT  
		Size: 29.3 MB (29281404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cca9b47d0f15049d08ee54cbbd221b83bb5e678ca3a04cf2e76fc008a3174c`  
		Last Modified: Thu, 09 Apr 2026 23:55:39 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fce3e3bbbc499336b50e55299caabb20569d54bf2e5a4667f1b0098d87e9ad`  
		Last Modified: Thu, 09 Apr 2026 23:55:39 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cec611a08cf777b9669c35b1c28525ff1e38d42eb5912d37b28becb48b4c5fc`  
		Last Modified: Thu, 09 Apr 2026 23:55:40 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90e99263e381ca49c7ea2444087779bbbb40d56371bcc47f205680788a13e84`  
		Last Modified: Fri, 10 Apr 2026 00:13:46 GMT  
		Size: 29.3 MB (29323467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a647260df00e997dc47af7ad24e89643e8e2df887333cf7ebc2850127e86d`  
		Last Modified: Fri, 10 Apr 2026 00:13:45 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace33f4fb3d756c3b5aa8a231f034585aa905b58eb03e4449575e6c627a24da6`  
		Last Modified: Fri, 10 Apr 2026 00:13:45 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a3ef0dc913788ea6864a8c48764566571de881fee8e97041db52211ee4a16b`  
		Last Modified: Fri, 10 Apr 2026 00:13:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:8120081f00cfc32c7498750d55ea589b108da34ab39c1025bd9978fb75891f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8760510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff014b47b77d14bdd7287f005ff6feeae90b1ec660efe4c9d86c6e4ee3f77eb`

```dockerfile
```

-	Layers:
	-	`sha256:71d3dc1a50610973822cb8c1abc736b3eb92849304450c998bdea9df25d731e3`  
		Last Modified: Fri, 10 Apr 2026 00:13:45 GMT  
		Size: 8.7 MB (8694561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bfcb5b2a3a01a5999f2d9c012576577ab6395273842c7acf395780c4ca78b54`  
		Last Modified: Fri, 10 Apr 2026 00:13:44 GMT  
		Size: 65.9 KB (65949 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; riscv64

```console
$ docker pull wordpress@sha256:791c2d1efeefa41fc84dc02f64b5c36a95e7c52dad6f93afbd29b896505928c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292354287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0b524fb2decee608076658e6bbbbb0a386a3e01681b8bcebdeb320f9e55c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 06:49:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 17 Mar 2026 06:51:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Mar 2026 06:51:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:51:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Mar 2026 06:51:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 17 Mar 2026 06:51:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Mar 2026 06:51:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Mar 2026 07:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 07:56:14 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 17 Mar 2026 07:56:14 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Mar 2026 07:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_VERSION=8.4.19
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Tue, 17 Mar 2026 07:56:14 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Tue, 17 Mar 2026 09:59:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 17 Mar 2026 09:59:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Mar 2026 00:05:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Mar 2026 00:05:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Mar 2026 00:05:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 19 Mar 2026 00:05:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Mar 2026 00:05:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Mar 2026 00:05:25 GMT
STOPSIGNAL SIGWINCH
# Thu, 19 Mar 2026 00:05:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 19 Mar 2026 00:05:25 GMT
WORKDIR /var/www/html
# Thu, 19 Mar 2026 00:05:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 00:05:25 GMT
CMD ["apache2-foreground"]
# Fri, 20 Mar 2026 21:51:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Mar 2026 22:09:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 20 Mar 2026 22:09:55 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 20 Mar 2026 22:09:56 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 20 Mar 2026 22:09:57 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Sat, 28 Mar 2026 05:37:33 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 28 Mar 2026 05:37:33 GMT
VOLUME [/var/www/html]
# Sat, 28 Mar 2026 05:37:33 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 28 Mar 2026 05:37:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 28 Mar 2026 05:37:34 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 28 Mar 2026 05:37:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Mar 2026 05:37:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052ed4f02aa31c663fadd7dcbdf7d48cff60f65277fca52fb6bc071ae3231c16`  
		Last Modified: Tue, 17 Mar 2026 07:54:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162d9824bd9e3774ef91ecc16979a3f4b3a7fbeaa59ac22d99b7357247d2682f`  
		Last Modified: Tue, 17 Mar 2026 07:54:37 GMT  
		Size: 146.6 MB (146577811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb554c2db715df402d78477452cfa9b3584aef39b30723b2ef10d4426fa35b`  
		Last Modified: Tue, 17 Mar 2026 07:54:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f12fc09529fe17ee50bb7b7c7dddad29d860b052519ad501c69557bdf9de64`  
		Last Modified: Tue, 17 Mar 2026 08:56:47 GMT  
		Size: 4.0 MB (4031214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b81af5a2dba9cbadede6c5ef9d497dd3628c5428646e32b3ffb77268532ec22`  
		Last Modified: Tue, 17 Mar 2026 08:56:46 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acc95446d3d3d6fbaf3750592e294e1995ef308b8b6b6cc25ff89f374bdd686`  
		Last Modified: Tue, 17 Mar 2026 08:56:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d0cadf636f6c80b80b682e020206005d94cf4583bee81c7a25085315d8c08`  
		Last Modified: Thu, 19 Mar 2026 00:08:35 GMT  
		Size: 13.9 MB (13857571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2488572a5c62e6137883453ebd4cd3c022dc06b7618d95a0008eb082f05632`  
		Last Modified: Thu, 19 Mar 2026 00:08:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd510606594e17787980c25ab3f4734f1b22610a2e8704544dd70062dc1ae33`  
		Last Modified: Thu, 19 Mar 2026 00:08:35 GMT  
		Size: 13.0 MB (12997031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b066a09dbbaa71d06e526ba9194088f5447ad2a2472cd9e5a8ef1a4b1b4844ff`  
		Last Modified: Thu, 19 Mar 2026 00:08:30 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763f8a4fa0ec43be7497f28fc96ef01dbadb749e5c1f17a1964b57d133bd098`  
		Last Modified: Thu, 19 Mar 2026 00:08:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5267a39661aa748297b2427bf5db4c68bbf18224e54aae1ef0dfaa54328c30`  
		Last Modified: Thu, 19 Mar 2026 00:08:32 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a226a3ed0d9f37ebddcc10e464089758052bb71aa68c071546a74b885df3ba4a`  
		Last Modified: Thu, 19 Mar 2026 00:08:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770739452b87a593a5f0aa334e3a83e39c604a9250f6c39b9f75c4135f47206e`  
		Last Modified: Fri, 20 Mar 2026 22:14:45 GMT  
		Size: 30.5 MB (30538476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b396b7bc20f182dbdd072af457d2fcfcdd81783db26085a7882bcfedc8ffdd0`  
		Last Modified: Fri, 20 Mar 2026 22:14:44 GMT  
		Size: 26.7 MB (26723379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df59578458bb709965b0d10cba57fc530fcca7b86e4f05e34fab0c8a3c5f0b82`  
		Last Modified: Fri, 20 Mar 2026 22:14:33 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8ad8e7086b4dbe9b9cfae5c8b6aea98da9a30b04468802634ec23994b3de80`  
		Last Modified: Fri, 20 Mar 2026 22:14:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcf07f5f140396ac8f28570e908fbd72ce95e0cffded474aafd3cfb6be9654e`  
		Last Modified: Fri, 20 Mar 2026 22:14:35 GMT  
		Size: 18.8 KB (18819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec59e9f90b85ba25d66d904127390b44997a0767dce40dd7125588437d338ac`  
		Last Modified: Sat, 28 Mar 2026 05:42:11 GMT  
		Size: 29.3 MB (29323474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cc132d8fe8d0595a24ec76253de33055eb9556443c368cda60a40c679dc0c6`  
		Last Modified: Sat, 28 Mar 2026 05:42:06 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e60a3aa0934e2ca154b0aa31c1202a8bb1872abfb050795e61a39d6ca2e73fd`  
		Last Modified: Sat, 28 Mar 2026 05:42:06 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c90bd0b2077c8cb121ce073663649618c07dbf75f435d63047f59d8bc6b4c1a`  
		Last Modified: Sat, 28 Mar 2026 05:42:06 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:d832d2afd6e75517c1989d67368ff8be71c901fb34e7c4af739fe94faeb2a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8825377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76990d5b371bdce2ffb2ccae8946bd92efacd0b662e2bac976528b67bc93ded1`

```dockerfile
```

-	Layers:
	-	`sha256:593470d10cdebb915722bde83856fd86156bd3611ce42c87bc697cce9efd27c9`  
		Last Modified: Sat, 28 Mar 2026 05:42:07 GMT  
		Size: 8.8 MB (8759428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b985acc160f4368a818aaff543277e273cba7b2a77976595cfa4fc2a02b207`  
		Last Modified: Sat, 28 Mar 2026 05:42:05 GMT  
		Size: 65.9 KB (65949 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4` - linux; s390x

```console
$ docker pull wordpress@sha256:dce9d4b4d91f0a2809d7975fee81aa0e680213801a112de813d641c74a6309cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245078192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8ca4d49e36fbd2c8c4a5b411c5b0aacb0a9619eb4441aee806842e940ad59a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:26:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 07 Apr 2026 01:26:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 07 Apr 2026 01:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:26:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 07 Apr 2026 01:26:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 07 Apr 2026 01:26:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 07 Apr 2026 01:26:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 09 Apr 2026 22:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 09 Apr 2026 22:28:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 09 Apr 2026 22:28:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 09 Apr 2026 22:28:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_VERSION=8.4.20
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Thu, 09 Apr 2026 22:28:01 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Thu, 09 Apr 2026 22:28:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 09 Apr 2026 22:28:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:32:31 GMT
STOPSIGNAL SIGWINCH
# Thu, 09 Apr 2026 22:32:31 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:32:31 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:32:31 GMT
EXPOSE map[80/tcp:{}]
# Thu, 09 Apr 2026 22:32:31 GMT
CMD ["apache2-foreground"]
# Thu, 09 Apr 2026 23:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 23:16:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:16:35 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:16:36 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:16:36 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Thu, 09 Apr 2026 23:16:37 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:16:37 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:16:37 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:16:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:16:37 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:16:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:16:37 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba7c97d634db0bf7b04319d896d93eb13e70bc5e2a5daf23b3c4b5710f3acc`  
		Last Modified: Tue, 07 Apr 2026 01:29:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f5aba2e62a8aff95377ba1541ebda00e243f039e8a96124c4029b535783f4`  
		Last Modified: Tue, 07 Apr 2026 01:31:18 GMT  
		Size: 92.6 MB (92573092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1830f35178a510aae66fa242c825ad8540d4f3add9ceb7ccacf66e1bb9da043f`  
		Last Modified: Tue, 07 Apr 2026 01:31:16 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b301ccb75c77960806c0ea37e92e1b99243e9a8d687bfc6db319970ac91f9c`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 4.3 MB (4344650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf23a194a95511e11697de8599bd15c2e7d23e82439849817ff4ee0545a6810`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f2358fea68d2f11fcbcec43f2eb9742f1eadd4a93ce25b7e68f23cfb85aa8c`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991dd16132fc94a6d52d5107f9776c86dcf8caae024f764f06bc885d575cee`  
		Last Modified: Thu, 09 Apr 2026 22:32:49 GMT  
		Size: 13.9 MB (13851076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87d5a1b93460e311218f5ac3e87631522b4433142da175d424f6bd320df4e94`  
		Last Modified: Thu, 09 Apr 2026 22:32:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb95cde67f1742edb7cccfde71f78bbbe935107625ddb21ba1724d38435a99a`  
		Last Modified: Thu, 09 Apr 2026 22:32:50 GMT  
		Size: 16.4 MB (16380506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97d4a74df6527bcd960fce4094c8e1c27291528451064ea3faa896ac2c1c1b0`  
		Last Modified: Thu, 09 Apr 2026 22:32:50 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefc446184137fe33299c034d9cf46ba3572475c9efe360f211417e8e418bb9c`  
		Last Modified: Thu, 09 Apr 2026 22:32:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724e29eb6c04410dbb77ffce8a97ab6d3df5233bc2227d951d39d5f0a9c94cfe`  
		Last Modified: Thu, 09 Apr 2026 22:32:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885828dad5e6c28eee98a5b07f7316a15c2969bd0a4c4e961e0ddd32c0ff6aad`  
		Last Modified: Thu, 09 Apr 2026 22:32:51 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e06dfcf2e3ac577778729ec4f3e8cc02538cc4d1a45a3459455d0b106106a4`  
		Last Modified: Thu, 09 Apr 2026 23:17:03 GMT  
		Size: 31.4 MB (31396564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a936d0bc7f6aed6533561c9dee6e7d75af48586cf98c609a090486bad358d150`  
		Last Modified: Thu, 09 Apr 2026 23:17:03 GMT  
		Size: 27.3 MB (27343765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3f31f592a2af14774103dbad900bb1f9d5d9bdc74944ad2461f7ea6e89f85a`  
		Last Modified: Thu, 09 Apr 2026 23:17:02 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce1b1e6715ccb5c443693f0f70c5281b53ef602e561953b4d3adbef8975b84f`  
		Last Modified: Thu, 09 Apr 2026 23:17:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f464b86f6cb3e9c8faa6f33257f6a40f2a5e2e4f29ccf59580d0048437d0ed44`  
		Last Modified: Thu, 09 Apr 2026 23:17:03 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fc3020f24ece32c22bd873743ebc1ca7cdbdb1b063716f78588ce372f8674c`  
		Last Modified: Thu, 09 Apr 2026 23:17:04 GMT  
		Size: 29.3 MB (29323473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09f5325d9899f2fe27ddd229bcca14205a1f5010cc5a6f9373fdc085d178b67`  
		Last Modified: Thu, 09 Apr 2026 23:17:04 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a895bc30face2c2567832de36eac6fd9b5feee30baf4458be1120057d283d1f`  
		Last Modified: Thu, 09 Apr 2026 23:17:05 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22366101946dc3bd5c17db8259947ef5be44c57f74938964bf364804705691`  
		Last Modified: Thu, 09 Apr 2026 23:17:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:cab662d8f90fdafebf1f44870d6a59c8d4ea994b98c1be01f1539e76582fba5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8478685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44355c13e6f579321482ce234c176e4daeffb0392be88f8282080c367472552`

```dockerfile
```

-	Layers:
	-	`sha256:dfae3b5635910cc9a4ea5198ca7ded56c4ba056a3ffe6a09e25d1943030acdc3`  
		Last Modified: Thu, 09 Apr 2026 23:17:02 GMT  
		Size: 8.4 MB (8412826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f149b88871075dc8145b8b18962858ee9c86275eb64743286b734b6b8da01f4e`  
		Last Modified: Thu, 09 Apr 2026 23:17:02 GMT  
		Size: 65.9 KB (65859 bytes)  
		MIME: application/vnd.in-toto+json
