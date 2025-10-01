## `wordpress:php8.1-apache`

```console
$ docker pull wordpress@sha256:eb0c303faba3d1601dcf73a8c6ddd7a7514f06ee861df5140a1ea09880c3a1cd
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

### `wordpress:php8.1-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:76ffc6e5a6d77ff5abf0a5153cfd8381f2d1386fd4b22da30746842849e0157e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262199521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b041fcde4a62ec0c7998e3802ca98ac4e357a52c16ed287da4c3030f77dfba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	version='6.8.3'; 	sha1='fd56bcdc15f1877e45dce67942ea75949ed650e8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
VOLUME [/var/www/html]
# Tue, 30 Sep 2025 18:19:42 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:19:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4ef33f7b1ac07d3a9ba8baa88b77a9c50656f6502978e260811dbad851f37`  
		Last Modified: Mon, 29 Sep 2025 23:53:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df07a1dd591279bca87fd190218995c93972a53dea28672db2cbd1831d4161`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 117.8 MB (117836887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0470c7237e5c936856acbbfe015e0d2066dc239362fdde911e131561a159ea`  
		Last Modified: Mon, 29 Sep 2025 23:54:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd065f60f510c64a620c6eded9f185b798935b07f04b0cf5d4b6cda38cc893a9`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 4.2 MB (4224103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9f805bd9f92a556e50e9c4b06b09a46796df3cb1832a41003f1e46c04a2466`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e00e68947876ce82ae79175ae069263b355ad814ed2e01e2b984059422a8c2`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f000328aacee0bd676fb15d59d1a0a3ae49bb2a8ac67789fd33a8c0f2c4b129d`  
		Last Modified: Mon, 29 Sep 2025 23:54:06 GMT  
		Size: 12.1 MB (12065093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54029becf3866d29fe36c0ee4c23bb734a37e51ec436f8bb62df54aa0995945a`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c45d1cdd95b80d53ac64fb7300c5c881550058af5e25bd56b48180e8d1a671b`  
		Last Modified: Mon, 29 Sep 2025 23:54:06 GMT  
		Size: 11.2 MB (11186035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d4b85a56fe09dc3b6b0b36f0a2a0229a00732fce01a66649d9034e7cebd2a2`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba8254b22d2a69a32a1f8943ef3702b6b00955340942b8b30206d89a40a27ef`  
		Last Modified: Mon, 29 Sep 2025 23:54:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6357eded860ae44c4b1e7a4f485bb1c11049d54563dd310bf7e4fd09db2d661`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da5ee164ee61117cc69a97e10b18bf3b692399bfbae054e058cfe6f8d883a79`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d673066e4e870c50354d93a32ccf9dd909558632a24504a9fca194dac008ed`  
		Last Modified: Tue, 30 Sep 2025 21:13:22 GMT  
		Size: 26.3 MB (26297103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f332fff44bc675987ed0edfe3d3ddb89d3bfc04137ca0e5bb7651d28dce605d8`  
		Last Modified: Tue, 30 Sep 2025 21:13:22 GMT  
		Size: 33.9 MB (33883068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005696debb8c3e17622e5129d4304a2501324a0452943d6cc19e00f6e536665`  
		Last Modified: Tue, 30 Sep 2025 21:13:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220f793214279f7f53ebaba69a6d66d4be721f47c89ce01d9f372093b48bc970`  
		Last Modified: Tue, 30 Sep 2025 21:13:20 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706de7b3adcd17cd55939008d345f49af6877c4092d22f107b7f844f434eb8ed`  
		Last Modified: Tue, 30 Sep 2025 21:13:21 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cc2a2e15f156310eee2ad77af0adf8561966f971b5833bc195aee51c7469fc`  
		Last Modified: Tue, 30 Sep 2025 21:13:22 GMT  
		Size: 26.9 MB (26899838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639b593c2e0571d227520b20dbb4d6de1a3bb35d7bd5400b37a70015e17d6a9`  
		Last Modified: Tue, 30 Sep 2025 21:13:21 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45bc2cc827065bb72b7fe4c146bcac80e7c69d550eee97db2bcb0c2368a217a`  
		Last Modified: Tue, 30 Sep 2025 21:13:21 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1028ff0e6feb48611ea2a9c019afe83d40946f866899f02bee6656852b68451`  
		Last Modified: Tue, 30 Sep 2025 21:13:18 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:cefed97f679e2de3ad762d608ce1be84617b9496b67fe87d74466874e97aff06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8736596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9377ef6e53520b43b10a831763d88947f6268742e96d51c9a64d8392f938c32`

```dockerfile
```

-	Layers:
	-	`sha256:72630129504cabd6dfaa8b25a33f27eed16832ecccc9671ce8110d7ce135ec9a`  
		Last Modified: Wed, 01 Oct 2025 16:17:18 GMT  
		Size: 8.7 MB (8671193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90988c13f598f6985ab9df245385d5d5cc72ba86f1c1c0fe5b458f1b2fab5f3`  
		Last Modified: Wed, 01 Oct 2025 16:17:20 GMT  
		Size: 65.4 KB (65403 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:69d2359dad8a57a5d796141f1b9776f8fa736c387742cb01cfb25a25e02dbdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231676344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7cb935f0fd2a7916654ce7a6f61480095e7a880c585201ad52c7df28922c49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN set -eux; 	version='6.8.3'; 	sha1='fd56bcdc15f1877e45dce67942ea75949ed650e8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
VOLUME [/var/www/html]
# Tue, 30 Sep 2025 18:19:42 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 30 Sep 2025 18:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:19:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05297cb022c102ec4a3ee1892fc4448f2d0b57e79ba5490912165fd17a9d9942`  
		Last Modified: Tue, 30 Sep 2025 00:21:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9db79f3dc42798cf70e869ca309cb9b56e680e4a3f3f5310bd01896ec86d08f`  
		Last Modified: Tue, 30 Sep 2025 00:21:39 GMT  
		Size: 94.9 MB (94874090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a43d1a80a78eaeae1c921f609779c32ffeb2b840382b56197d60075612453e6`  
		Last Modified: Tue, 30 Sep 2025 00:21:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1441eebfd3f54e1687a2d31fa3328125eef1675413eb7146452269550363d6`  
		Last Modified: Tue, 30 Sep 2025 00:21:32 GMT  
		Size: 4.1 MB (4082005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83429d0b8115dc8f13f4586d6b3423d6a05b1a19212ebae3180be4bc1fb63c20`  
		Last Modified: Tue, 30 Sep 2025 00:21:31 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b04c8f76c082655965243647dcb9b259e57c994edc358d04d41a9fd6e821427`  
		Last Modified: Tue, 30 Sep 2025 00:21:32 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7124fc2483ca90e9b21b5f7e0407a48f4defce8d9e7b0f844dbda65e85d1c12`  
		Last Modified: Tue, 30 Sep 2025 00:25:08 GMT  
		Size: 12.1 MB (12062497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb97c53d78f587ec6aa39fb4c07f37f0d6dcda7271cf8cb4f0d15f23c43a2be`  
		Last Modified: Tue, 30 Sep 2025 00:25:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a678be49c316fd05576c3c2bc19174889c5faab32c41f2a535d122b1ee97e02f`  
		Last Modified: Tue, 30 Sep 2025 00:25:12 GMT  
		Size: 10.1 MB (10074337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89dfd418a2a527c648cfb5ce0bfe1e52f7fadf2765b693af5c0cc9a5291396d`  
		Last Modified: Tue, 30 Sep 2025 00:25:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18adababfccd961f2389367fc642d1e7412b32a0822aae809e20cb7f17a52034`  
		Last Modified: Tue, 30 Sep 2025 00:25:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeb9199ab45c992845ff8a8ce79820ab3e3913770cbf23b45460ef6ccb8583`  
		Last Modified: Tue, 30 Sep 2025 00:25:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7fa22a011da72d98d629f4c775b154be544f4143fe149ed24fa69aa075b67b`  
		Last Modified: Tue, 30 Sep 2025 00:25:06 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eda767fc7956f9a42858d1971e87829cf5b3e53c163367cc209307ccabee5ee`  
		Last Modified: Tue, 30 Sep 2025 20:12:18 GMT  
		Size: 25.7 MB (25726392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fdab2c4a89da95dad497701c4e28864f13584603d28196161034f17dfeaa77`  
		Last Modified: Tue, 30 Sep 2025 20:12:14 GMT  
		Size: 30.0 MB (29981404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25900d2148943d9d6d5b013a090b34e75085248f875d74848b8eda98bb357001`  
		Last Modified: Tue, 30 Sep 2025 20:12:10 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c221374e277115cf5276e9e2a4a4bec714bd3631ba1658efcfd56051bed8cb9`  
		Last Modified: Tue, 30 Sep 2025 20:12:10 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0117f59078134a2459686158ac1ce247797652b4079d5c11263ecd72d13bde`  
		Last Modified: Tue, 30 Sep 2025 20:12:10 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6b15507b14a466534275009640c7ca4583346fcdd4e375bc79e3fb67a7cf0f`  
		Last Modified: Tue, 30 Sep 2025 20:12:13 GMT  
		Size: 26.9 MB (26899844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e935749badb65a079376f169e2da30457902ef52c3a54180bf683753f6ce6ef0`  
		Last Modified: Tue, 30 Sep 2025 20:12:11 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d277d9a7d700a757517682a3d5507c4a79b051e30cc6ec77811f6fde7bc0b5d`  
		Last Modified: Tue, 30 Sep 2025 20:12:11 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0f1493efa5b86aab1ac52b72432bbd68ea6f4b51debd0891e86e9c8e58344f`  
		Last Modified: Tue, 30 Sep 2025 20:12:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:de0c1cf4cb3e97d7c15de853e8364f04941446bf56a978d2c4845d000aa67ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8535808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afbdad22d325cc21b1fab3b72463920cfe1a79a047ffba279a22a3b3c33be06`

```dockerfile
```

-	Layers:
	-	`sha256:92ae61b2d264050e98f4aad2eb22fa4e730d919c9876d5e4fec8ec5952c0aac4`  
		Last Modified: Wed, 01 Oct 2025 07:18:30 GMT  
		Size: 8.5 MB (8470226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc28387fe4d3ab402dc1499e3d06105e75057da7be8e822bcc4df61d08dd414`  
		Last Modified: Wed, 01 Oct 2025 07:18:31 GMT  
		Size: 65.6 KB (65582 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:defa9ee26a72d5d6f0c7ff35d14fe11cfc5460c50fc117c9d4ac551aca3e6397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (217975083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f306692c4d78d03207b5d7d66166b8fa71e9eb9a9fd93e7c5b1cfcc9d6479ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2102e8f5e6f94a8ce945c3c6de747895245fe25cb422c38ce417e59b2381ef0`  
		Last Modified: Mon, 08 Sep 2025 22:34:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f71c0f166d88efb066683f6768045682cf2e0e4b66c712b6a235249ec728f8f`  
		Last Modified: Tue, 09 Sep 2025 02:04:37 GMT  
		Size: 86.2 MB (86244623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23902e33c33d860433085e67a2cbc12a06636009e7dd6fcf737d22b07edc148`  
		Last Modified: Mon, 08 Sep 2025 22:34:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbdcb56350fb3896f2da16601562d43d9bc993f5bd90d9af9a0580a86ca6d65`  
		Last Modified: Mon, 08 Sep 2025 22:34:55 GMT  
		Size: 3.8 MB (3751974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22bdf1441b74e6a4ac60e3c52e4ea970a15eb9e243b7a9dd36d7decbc80b2b7`  
		Last Modified: Mon, 08 Sep 2025 22:34:55 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7f9d33d765df04a17dc791d72189a0c203521954b0272167b3a5183a97c62`  
		Last Modified: Mon, 08 Sep 2025 22:34:53 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9babf507c7d336c64f1756ab25069a6d071b2adfeaf2f5c855116a592ac301`  
		Last Modified: Tue, 09 Sep 2025 02:04:40 GMT  
		Size: 12.1 MB (12062599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d8b1ab988bcdbe6585b59a1f44568ed45ca1701a5b19edb6eadcd518a57cc1`  
		Last Modified: Mon, 08 Sep 2025 22:34:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead354e96e3befbc446f1c1a9d9733a4e6487c43b67192b7bf19108154298928`  
		Last Modified: Tue, 09 Sep 2025 01:18:48 GMT  
		Size: 9.6 MB (9574519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af010ced822552aec46e08d2679915d300fd729529763809237a6a258621bd91`  
		Last Modified: Mon, 08 Sep 2025 22:34:56 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693913e24675abd84daa041a8efb6fe89d2f107747bc3c4d090a0b76b5bff75e`  
		Last Modified: Mon, 08 Sep 2025 22:34:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91167faf354cc253bb57564b2fc13ffa64bd473e2cb19ffe65708aa4f42cf76`  
		Last Modified: Mon, 08 Sep 2025 22:34:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fd83f5f228a36692f43be6f3cd5586b748827d5b3c9602e00c401ac66e2e83`  
		Last Modified: Mon, 08 Sep 2025 22:34:53 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9998b26e119480b688c70dc84d973d47b9f7aca796c37a8926e24be8d16bf93b`  
		Last Modified: Tue, 09 Sep 2025 20:19:07 GMT  
		Size: 25.1 MB (25076422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec3a82beb0e96987944be777fbd027b1077ab7211977cada32cff945e0b3da6`  
		Last Modified: Tue, 09 Sep 2025 20:19:07 GMT  
		Size: 28.1 MB (28128889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ba42d9264e55570086d94284ae42eae24c2872dd4435f12b5205b78d732eed`  
		Last Modified: Tue, 09 Sep 2025 03:56:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f313336bce61da6ae006fda4960506639740c7281a73feabf3ce9571c9fc10`  
		Last Modified: Tue, 09 Sep 2025 03:56:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac43c191fa8bf18648d63c5e2e657201f7b191394effe8c57a1c74422f3f200b`  
		Last Modified: Tue, 09 Sep 2025 03:56:42 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b9d47a00e5ced784f3e2f6d5db1d76bfcb3cab0c13551734cae145252cb22`  
		Last Modified: Tue, 09 Sep 2025 20:19:10 GMT  
		Size: 26.9 MB (26898583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2469b441df99a2abd51b31be651eaaf69cb3b4bb1b9b80348c56ee2b0e7c45e`  
		Last Modified: Tue, 09 Sep 2025 03:56:43 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d730a306c97d16b6087b0708a1001377dfd4d73d333331cf93305f736d8501`  
		Last Modified: Tue, 09 Sep 2025 03:56:42 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4731967bb201ba56a97d773e05e4b85a872b9a3689c8e8f340a6b4b88c86f0`  
		Last Modified: Tue, 09 Sep 2025 03:56:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:3f551d15fa1ea1a1a08f5db2db0891525a78f35a5bebd1bcf31824660f48325b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8540436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5c916cae52bdae03ba4fa22c2bbfdeaedf8b739cd31a4608b8f3db23e11e23`

```dockerfile
```

-	Layers:
	-	`sha256:b5ef7b7e8b3cbf04078d447bbdbe27ab9649529b83281da56d440377e2ac318a`  
		Last Modified: Tue, 09 Sep 2025 07:12:55 GMT  
		Size: 8.5 MB (8474938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c63d0349406e6f36c26380093ed50b4877fe5a6d8546a8b49d712ea6e8f92e`  
		Last Modified: Tue, 09 Sep 2025 07:12:56 GMT  
		Size: 65.5 KB (65498 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:caaa99ae55d3b0f3ee7bba81beaa5e1f50500b441b3b7bf70678248214589ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252758608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a603441b350d4b0c70f24b60ca31c9c621aaff411570b93b1ebf9e9bd9d91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f66eca7083384e8b362e8dfa05f874340f2210cd55cc842e8f50da57f87e441`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea142831690601e521bfac113250b9ae0943f845d6cccf2b3a01c69769fd420`  
		Last Modified: Mon, 08 Sep 2025 23:01:35 GMT  
		Size: 110.2 MB (110161693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8382d339faf016d36c0ebd37d3cc9d6a6b2b27f59cd1a00de81e5d2d6c6ed53`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1a2e4f7561ba51c0d40258d23913e0d8d12b43c5b3dcc36c08780681f7f43d`  
		Last Modified: Mon, 08 Sep 2025 23:01:27 GMT  
		Size: 4.3 MB (4302087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc89406611fc9841a20359368a013c3c678e2a7a818540ff616dc3edbccd87`  
		Last Modified: Mon, 08 Sep 2025 22:19:55 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232ad243cdbae57423b06787915b1033abfdc140f9d9f02a85d3e18444f1e5`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a796882b394469b5ceecba551c184340483cdcaf495855519f32ef17e76741e`  
		Last Modified: Mon, 08 Sep 2025 23:01:29 GMT  
		Size: 12.1 MB (12064668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30d43b219d6a5864816c4c809b4635089452897a4b5b7fadba4da2d15f5d6c2`  
		Last Modified: Mon, 08 Sep 2025 22:19:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc8deaf5bfba93cd4d9cc3fec0349b4168830e3ccd4404c04cb31ab36058fa7`  
		Last Modified: Mon, 08 Sep 2025 23:01:30 GMT  
		Size: 11.2 MB (11209217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1abcf56af9d4b68777735bff47b18155c390ef3c37f17337b165afde1c1da23`  
		Last Modified: Mon, 08 Sep 2025 22:19:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d0b9c398ffb0cfb579991919eb919d033b0315c61719fed2df86ea07a6dc4f`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6bb09746a1c0399e56f157034b9c082a71bfa5460784de90c0f5912f4d36b8`  
		Last Modified: Mon, 08 Sep 2025 22:19:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3df73fb2b8098d419804ad3c37c3989cb9804166ff018dd406d9299fea29e4`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8404aa9ecbd1d90a14bc88553d98d81785440fe09a2148ff5ea0847ab8f028c`  
		Last Modified: Tue, 09 Sep 2025 04:17:00 GMT  
		Size: 26.2 MB (26207682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b271c9ea16d9202af6b28c52b2186034d0c8897364bedf74ff6f62f0c5299a1`  
		Last Modified: Tue, 09 Sep 2025 04:17:01 GMT  
		Size: 31.7 MB (31748420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b547d7c0df6a8d05fecd15818ab2e2bf388441de08ea3115a2f2f0a5841b23`  
		Last Modified: Tue, 09 Sep 2025 01:31:02 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b266209138da8655d7235f3a41217ae1e981faef2abb398708d41bad71c17b`  
		Last Modified: Tue, 09 Sep 2025 01:31:06 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7128f9b6af6fa19ef66f4061e965f9fd62f6eb072181684fecef5e2906638921`  
		Last Modified: Tue, 09 Sep 2025 01:31:09 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b782d4ec5a5946b345d6f40f473bad2de340ac2658dadf314312a6ea595d70fd`  
		Last Modified: Tue, 09 Sep 2025 04:17:04 GMT  
		Size: 26.9 MB (26898583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e7f905a0004e5dbf22d2a5bf24f78b1fbd8239c38e0e7b44056edf6d235ec4`  
		Last Modified: Tue, 09 Sep 2025 01:31:12 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1995ae1f2f9056020a2074c2d891f680d94510e1bc6cbf993fe2aaa9420beff5`  
		Last Modified: Tue, 09 Sep 2025 01:31:15 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a97f4b7b1aa23e02cc7567312775d195c522d66156dd5326e51fc95edf65317`  
		Last Modified: Tue, 09 Sep 2025 01:31:20 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:9f224f42c593a07d096395411e33c210ff2ad7749c6dbdce7e50e0d3ef157544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8833162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5b67d65ca4256185843770e1e7a8841323c65ac643c2635e4480f5b8a25b91`

```dockerfile
```

-	Layers:
	-	`sha256:34339a7763ecd19da932b03dab22747ea297846b50336f279cc7e95f81406c57`  
		Last Modified: Tue, 09 Sep 2025 04:13:16 GMT  
		Size: 8.8 MB (8767591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0aa648d4301bbafae71ce50eaded5a109184f12add8e2fdd2344a84aac7100`  
		Last Modified: Tue, 09 Sep 2025 04:13:17 GMT  
		Size: 65.6 KB (65571 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; 386

```console
$ docker pull wordpress@sha256:b5f0b871239f9e32ddaafb1baf76faf51ff0ad99669e1e2ff689cb143bc606f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260797473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b814298b783ee84648ebff3673a0a03ed8414c468e73948da03a98eb2d9cb2d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1310ca781d38ec216c58f42b468e01d7a2f580f69acfc403159bd4b9f03200ca`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2f428ee89fe9ce2d35b987e4ad70371614d6030ac4e509eb10f979b7516ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:49 GMT  
		Size: 116.1 MB (116136824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b724e0afb3a10381117903e4d6dce5542f04401fd7f671f6e1bd0222ee59264`  
		Last Modified: Mon, 08 Sep 2025 21:47:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4da915077b334b31711c05a4b335b5cd7ec4167ff1b6e013e36951da15e6942`  
		Last Modified: Mon, 08 Sep 2025 21:53:35 GMT  
		Size: 4.5 MB (4455403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a80c8505fa74c465d9791cbfb8c5c9d2aade7a0608b45bc0169da7a671d766`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413bbda25d8af6cac40730cd7e20354fe8cea06376c7acb88946a10bc88e82ac`  
		Last Modified: Mon, 08 Sep 2025 21:47:17 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74ca89708fa27d35fdc58d97898069fb0d7aa95b0345456deeec53e398210f0`  
		Last Modified: Mon, 08 Sep 2025 21:53:35 GMT  
		Size: 12.1 MB (12063918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5eefcc0bf5d21b3560358fc3da2d627adeb5d351002bd128083a9c7028fd7`  
		Last Modified: Mon, 08 Sep 2025 21:47:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e445205901893ce7d5548d5d2736bcaf8f865c0c2a62a224b6e04da3a7ee07d3`  
		Last Modified: Mon, 08 Sep 2025 21:53:35 GMT  
		Size: 11.4 MB (11400571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb21ab580a278ecf6753419d20e8f87d882222cf783b5fcde1d45cdb60d4ed11`  
		Last Modified: Mon, 08 Sep 2025 21:47:23 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d701bfbbad0773258f3f2b9fd57f35abc800ad6878e0b81cb8c75f7c0fb5bf`  
		Last Modified: Mon, 08 Sep 2025 21:47:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26960a562ef7130530966ce0d0c4de958e7c2c0d40f87039dd9eb965087ad129`  
		Last Modified: Mon, 08 Sep 2025 21:47:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a6bd197b16766c7060f8ca7b80a6be669d1f3ca6eec9d865af030fcc0f4658`  
		Last Modified: Mon, 08 Sep 2025 21:47:34 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa03b32b93f131ec488b16127c18cf7f89b3bc9c8eb79c03b9bdad391b1cdb1`  
		Last Modified: Tue, 09 Sep 2025 14:31:40 GMT  
		Size: 26.7 MB (26747437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c001d9f5b7ed746e19669a889f838f6a9cf7937d3c196c3f39ddc83c4007138`  
		Last Modified: Tue, 09 Sep 2025 14:31:36 GMT  
		Size: 31.8 MB (31775327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced720fb2154a488fb3fcb72c184d4e2622c35e85cb3b165e477f7848690b094`  
		Last Modified: Mon, 08 Sep 2025 22:39:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c5d43a9e85f0ded74d49a503ff0bace4b8d431995b74b8669b2636a0db4520`  
		Last Modified: Mon, 08 Sep 2025 22:39:47 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd123273204fe6f6f53206ae584cfa5e5bcd85f301c2b04f31fe3f980630352`  
		Last Modified: Mon, 08 Sep 2025 22:39:47 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8343344eebf5cb3543d40c67bc0670fc9350e0414f3b24cfee3cee80ffa3408`  
		Last Modified: Tue, 09 Sep 2025 14:31:29 GMT  
		Size: 26.9 MB (26898587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab8c1110cdc7a333ee6b763ae375fddf406d7f71b11c2f811572f829afb93a5`  
		Last Modified: Mon, 08 Sep 2025 22:39:47 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c37d9674c01942835750e4317182c794a1fa34be556c52ceeaa488047c0380`  
		Last Modified: Mon, 08 Sep 2025 22:39:47 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952a437919fae9459d1310ba9c4cfa91f4d450a5be6c3cf934bf7538c50877c`  
		Last Modified: Mon, 08 Sep 2025 22:39:48 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:963f2829d2adafd3513dfe93f35471f549410f98273e563f2cea7b3a510b8a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8709354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd4564cd34de4ed7e7eca3b23acf5a78dcb46b540c21263d7dc8dcabc3bf538`

```dockerfile
```

-	Layers:
	-	`sha256:c8c73fd9139bea66c1e0120c840c6aaf0032aa100f8e7b54ed779cd76c167860`  
		Last Modified: Tue, 09 Sep 2025 01:13:33 GMT  
		Size: 8.6 MB (8644089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961576242c923451024a4e9013c037c42d583eb6abf82a645aa2a0604fc10d21`  
		Last Modified: Tue, 09 Sep 2025 01:13:35 GMT  
		Size: 65.3 KB (65265 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a851284d013ce7423f9de0c589633ba349c82f6f3a87b2c3d5224c807629464f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258406167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73f388af4653060bb4af002c85064d5016b2b096b9533c266796870f8280448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c5533102d377092f90a64ce96643efc2f90c8132806309f689ef1a0ff55f1`  
		Last Modified: Mon, 08 Sep 2025 22:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c51011b81d61508b6739213b2956df239d3867fbd1b77eade087e74d53486`  
		Last Modified: Mon, 08 Sep 2025 23:13:00 GMT  
		Size: 109.6 MB (109596656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d6bf5057cf9cbf3d82654ad276e19db98dfaca1501852995c56026182bd5a`  
		Last Modified: Mon, 08 Sep 2025 22:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb5a7c2ec964eef33815fc315209dc7259500f176c00afeea12dce7c2622677`  
		Last Modified: Mon, 08 Sep 2025 23:13:09 GMT  
		Size: 4.9 MB (4875556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133daf04d0a4d1719a190dde5b767dcf5cb67060f9891ee35f0f786a618e0699`  
		Last Modified: Mon, 08 Sep 2025 22:47:21 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f8262f8dc896e13cd1eb8cc0b98965b00768f23f0b8b2ca4eb70fd73e0c4d3`  
		Last Modified: Mon, 08 Sep 2025 22:47:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced91204540d06ccc8b13d5d39ef5fd2fc531833980e61b6c6aa874975585f0b`  
		Last Modified: Tue, 09 Sep 2025 02:04:43 GMT  
		Size: 12.1 MB (12064154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2591ce59227d325c1d2774116976b16e1e14eb3ff26ec394e3d9d3f486ee87c3`  
		Last Modified: Tue, 09 Sep 2025 00:52:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e13377781ea0a478eba042784431a856736dc797a58e51a848b3a8991c815`  
		Last Modified: Tue, 09 Sep 2025 02:04:43 GMT  
		Size: 11.5 MB (11526548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dd4d9fc128158c2ab5e48d829869b76790d31bb83ee919fc06ae52cab49940`  
		Last Modified: Tue, 09 Sep 2025 00:52:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d0a8e062e499b2eb70d46c88c9f545d9301dcf3c412b7844119922b689e13c`  
		Last Modified: Tue, 09 Sep 2025 00:52:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc2c0c272b78d4035a84487eae58d73bc4aefdce1a863f8fd8f06e53a1b14f8`  
		Last Modified: Tue, 09 Sep 2025 00:52:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022aa68cab9662832f8c7d509bc4875095553e76faddc7abccb68d4b69c6c18`  
		Last Modified: Tue, 09 Sep 2025 00:52:24 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bb83cf8411e371f5e2e62be2f6ec20a4bedc37ab7357f641399028c469600b`  
		Last Modified: Tue, 09 Sep 2025 14:43:55 GMT  
		Size: 27.4 MB (27368645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bbc0018c3f3031fc8ac4054f3d87902c9eb212aedc14d803274363e19b953b`  
		Last Modified: Tue, 09 Sep 2025 14:43:55 GMT  
		Size: 32.5 MB (32451999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee936d2c43308d407185067ecb18774cf57d175c79f0c1bfd4ee9e9f46c63a84`  
		Last Modified: Tue, 09 Sep 2025 14:43:51 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fe0ef9060e7d2412525569101f6d38a2e978cf88aebaa2156ba25ab5f0575b`  
		Last Modified: Tue, 09 Sep 2025 14:43:50 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e787e4f36f6d458586e1211933ad60bcc744a39540f54ad3b0bb696d948ffc77`  
		Last Modified: Tue, 09 Sep 2025 14:43:50 GMT  
		Size: 18.8 KB (18802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15489adeb02e2bd245d9b4e8aa695662e38382164f6a3daad7ace5b250e916f3`  
		Last Modified: Tue, 09 Sep 2025 14:43:53 GMT  
		Size: 26.9 MB (26898606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4a120d91dcda78658476a8d51e6ae0786f171fe7407605de30e5c90293461`  
		Last Modified: Tue, 09 Sep 2025 14:43:51 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef6f9237c824a15afa82a76da23a23239565b40a7220145884a7727543465a`  
		Last Modified: Tue, 09 Sep 2025 14:43:51 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a80642fc954ade835c9153c0fdb60c76d2e05f3bd6cafc182fa81a3c42c12c`  
		Last Modified: Tue, 09 Sep 2025 14:43:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:61da73bd942e2f56360003fa42208e07f85e63e6ff116d50f97820d47415ffc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8737318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3debdb575b079dc91e51a4ada418c2474660438f2a944181b035f88c12e5d523`

```dockerfile
```

-	Layers:
	-	`sha256:c024195eb0376d38642d673aef816e714c2a5c9fbde70123c77b3bf0592ff87b`  
		Last Modified: Tue, 09 Sep 2025 16:13:11 GMT  
		Size: 8.7 MB (8671910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebdd7d7379043f970d39f3bf60dfb921c1bfebcebee7ca08b79ffe04eb18644`  
		Last Modified: Tue, 09 Sep 2025 16:13:12 GMT  
		Size: 65.4 KB (65408 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; riscv64

```console
$ docker pull wordpress@sha256:a639e23f081ebd2228566e16fd3befa5ce0832714451837eac501e1ebfbf7c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283816022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0283e8e093637264ba8cf8c91cbc02c4d598e2b2cee7296bdba1c74de0d5759d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae3e77da310b8f6abd1c47c2c908b688364ff453788dffc1ea3755bda9a618`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25a2ea3673eda57f8891f3fdc7a2b5bd7baa28ce076ff3427218ba02258d5f`  
		Last Modified: Tue, 09 Sep 2025 20:58:30 GMT  
		Size: 146.6 MB (146579169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fd9eb164bef808ab9cc8b8afd7d2a60572baa81f3ff4c56c34d90a36945fb1`  
		Last Modified: Tue, 09 Sep 2025 18:54:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1d685c22b2a71e0ac90af447b986ccd452c8bf3b3279addf81fabe668d6190`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 4.0 MB (4026102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3b33f48477a8d3d6159781343071903515e9a5e4e3a498f12132dc4e16087`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31a861095607a227987a9645651b2b7a18d0f30647655179a2cb5c863f10929`  
		Last Modified: Tue, 09 Sep 2025 19:57:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764900342fa47df4814fb6a18f607a2b4a60072de65a1810704abbd804049818`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 12.1 MB (12070305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e894e0d478ffcee60c989e35af164ac76ed22b4059aa0a7405f6b1c6e815dd`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d78d6a75c3faa416b199a37010cd39d5a8e65c2ac1aa6c8ab38ff3096738f82`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 10.5 MB (10476602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc2b0c2da9ee27b81b95a53225692e01361f4ffaf61bd024f926619489c50e1`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b6fc24e17ec184b4bcc61bf486e185bfaf30e850cf684d972a90fbed15b71b`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d2242a42597ba83ea513ee7ece0ffd7ee127946d7b41f61fbb7df2f56aa1a1`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8457949a859d7e64afde5efecb7105c7f87f15eab7adbbc7768967f8968fb50`  
		Last Modified: Wed, 10 Sep 2025 10:50:32 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc8d61a2b23925c14a2a7471005c8fcc94badc27130ce7d5d259c4e542af2c6`  
		Last Modified: Thu, 11 Sep 2025 22:06:57 GMT  
		Size: 26.1 MB (26140002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7ebebd8339cd7343ed4d07a6a24c347be3b3909d47671aa86083e23654abee`  
		Last Modified: Thu, 11 Sep 2025 22:06:58 GMT  
		Size: 29.3 MB (29324192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5fa254dc50467dbb2a3d214bbcfe7c0ac79a4946055249c24b97ed0731d9a`  
		Last Modified: Thu, 11 Sep 2025 22:06:54 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76508396f43e2f33f83ddc8eebdd8dd402bfe0c93140b9abac8ace70207d185`  
		Last Modified: Thu, 11 Sep 2025 22:06:54 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ef7e903b08fc2bbef6034cfa99079c7ee931a99a5d855c3b5c6b28ea78ca90`  
		Last Modified: Thu, 11 Sep 2025 22:06:54 GMT  
		Size: 18.8 KB (18819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305de3b0ccb65a6c5fccd06c8e04f1ca71453f3f789c632d0bf33ceea4517add`  
		Last Modified: Thu, 11 Sep 2025 22:06:56 GMT  
		Size: 26.9 MB (26898585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0f0e6c30a1ecf7691649c9a0380065de6c0867ccf1847e6e7e0d8d9508d5e`  
		Last Modified: Thu, 11 Sep 2025 22:06:54 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022ac9b2344b59f8569ea11e53f47e22bd19fedf36b5c1d1aabdcc62fd2ea67e`  
		Last Modified: Thu, 11 Sep 2025 22:06:54 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a21b115e6bbb8e14e7efaf0a65335ac863e6dffeee3cbdfa1a69d46cc31f8bf`  
		Last Modified: Thu, 11 Sep 2025 22:06:54 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:eb25b96211dd472e6f37de3e4e7e5fe228bb7241c83f43ffb4bc4fde4f403389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8807718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b13458373d8439a4e6248706e6a965f3b90f0ae274fb46311e609162ae3a8d`

```dockerfile
```

-	Layers:
	-	`sha256:815af36f6d29a9108cd2a58d51887843c9090ea69c606ca7f488a812678829b9`  
		Last Modified: Thu, 11 Sep 2025 22:13:06 GMT  
		Size: 8.7 MB (8742311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edbed72063f7b3bba18fa081c5ffc9d2eaf3d942275cdc991b5878408ea791d2`  
		Last Modified: Thu, 11 Sep 2025 22:13:06 GMT  
		Size: 65.4 KB (65407 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:f546d946044ee17d8dc13b866484f546aab800bb8891f23f22726d62937abedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233482671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a372ef7cf96d80830e16ad10b3f3196f5b209bd1bb7007517fdcf719c75da39f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 08 Aug 2025 00:02:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.1.33
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.33.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.33.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=9db83bf4590375562bc1a10b353cccbcf9fcfc56c58b7c8fb814e6865bb928d1
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 00:02:22 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["apache2-foreground"]
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	version='6.8.2'; 	sha1='03baad10b8f9a416a3e10b89010d811d9361e468'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
VOLUME [/var/www/html]
# Tue, 12 Aug 2025 18:29:25 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 18:29:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b232e52aa98f49ca19e377e7da8d1acab05ee220da9d68dd81f728babf0c517`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478857e6e1b537f952dd40041dacfe05d27f69962e33a4c06fb4ff6381f540`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 92.6 MB (92562517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa056e798e1e4f9bfdcf75b3f6f5791a4f0e696861934a12a910a510c2ac018d`  
		Last Modified: Mon, 08 Sep 2025 21:55:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12f633efb1bb21ecc579e196bca25f5ab7d52d7c2db3ee2a067ee60f0f9c012`  
		Last Modified: Tue, 09 Sep 2025 00:03:06 GMT  
		Size: 4.3 MB (4320437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c2cf9f6a014fa655f3eb4189a487c63fa210b55a95d802554be23b3bcfe1cf`  
		Last Modified: Mon, 08 Sep 2025 21:55:24 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bab93bff6df540c8c28fd0c65b5629bb7a3784cb5470795e60ecbef3aa18f1`  
		Last Modified: Mon, 08 Sep 2025 21:55:27 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f58d0506d448d6917e4b926598357fe71329c6f764137ba25fa7ffe29d97cf`  
		Last Modified: Tue, 09 Sep 2025 02:04:44 GMT  
		Size: 12.1 MB (12063410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6761845656f422b79dc14745561352e8fc167cce942c5c2a9a677ec0529ed129`  
		Last Modified: Tue, 09 Sep 2025 00:13:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf72c8b7b11c263f6fc57826508c67fbf90db28f379e3ead05b3b84bcd73c1b`  
		Last Modified: Tue, 09 Sep 2025 02:04:45 GMT  
		Size: 11.0 MB (11028193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0324dd047c000d07ba4fc1eeba7eabf63c69b93f1ddff5e335108a5eb9496342`  
		Last Modified: Tue, 09 Sep 2025 00:13:15 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd8baca7adf3c2d0ab47ee4342ec398120ca5240c7182bf6116e1162e603e0`  
		Last Modified: Tue, 09 Sep 2025 00:13:17 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135e1a4e333fd4fe27361c74b53c26d9982c1b283addbc340e6f56dabb24a35`  
		Last Modified: Tue, 09 Sep 2025 00:13:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61725021e3dd11c89a1b2475c2ea5fd6d4e9cde219c5f5d1247ddf9ef7ad97e`  
		Last Modified: Tue, 09 Sep 2025 00:13:15 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ae4ae1141b60ba8e83a1a51201433e4d1b03eac33cdd42f0ff3754c05b25ab`  
		Last Modified: Tue, 09 Sep 2025 11:08:22 GMT  
		Size: 26.5 MB (26480743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f18b01bd484cc6bd9fbb134be499ecf8c2bf1345820cfb11f9d4dcd24efea`  
		Last Modified: Tue, 09 Sep 2025 11:08:22 GMT  
		Size: 30.3 MB (30266228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46347c867b8e1f9661e5b713972a7d12b4f8632a91ff5c121d46bdba417bea4f`  
		Last Modified: Tue, 09 Sep 2025 11:08:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f6623cb9ebc847f44c835cf8f859dcad154d3090e266db67d3ecdc7362bd89`  
		Last Modified: Tue, 09 Sep 2025 11:08:25 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf0c11a46aa728647afc90cfd2c3e894aec432501a05b01d197c34e626c8c38`  
		Last Modified: Tue, 09 Sep 2025 11:08:27 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2035b49017f538f0b04f4a8cba2eed502e9e2f2dab92506ba20c2a66ea22a5c`  
		Last Modified: Tue, 09 Sep 2025 11:08:29 GMT  
		Size: 26.9 MB (26898587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44927b31f4095a1e3edaf872d60279de90d854a8e990ae4ad4f439e822e365cd`  
		Last Modified: Tue, 09 Sep 2025 11:08:18 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5184a761c28c38f18d48216a9cc03ae05315ad82f5bdf62ef2f84d54e63f75ee`  
		Last Modified: Tue, 09 Sep 2025 11:08:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c794a9f7351f99b02bc6a6df24b2cbd503b4d19af08bd7d570699145cd7996`  
		Last Modified: Tue, 09 Sep 2025 11:08:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:fc199ca0b81a2c3c83fe42e5a8e162ca9228998c077702e4d9f0321ac60f6e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8461010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeae3da9a1f7c51358fd14d4416a960a1f0f361584cc71aa6ee6b4775113d8a0`

```dockerfile
```

-	Layers:
	-	`sha256:fa85c3e4f65d8111b9692039fc909cb4de4362151a003c658b7663d047604416`  
		Last Modified: Tue, 09 Sep 2025 13:13:21 GMT  
		Size: 8.4 MB (8395691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:292cce95491f6bde8b135d05826ea0b11fc00ea015ca97ed48573107a1d3f321`  
		Last Modified: Tue, 09 Sep 2025 13:13:22 GMT  
		Size: 65.3 KB (65319 bytes)  
		MIME: application/vnd.in-toto+json
