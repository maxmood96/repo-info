## `wordpress:beta-7.0-php8.4`

```console
$ docker pull wordpress@sha256:290109f3b64c492793be381ecbbfd6711ed273851d6e8c9e80390f8e4bd9eb5b
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

### `wordpress:beta-7.0-php8.4` - linux; amd64

```console
$ docker pull wordpress@sha256:ffc580af07fe5000aaa59c54c0f72f19fa4d077b92610f545f6fe3fbc64a4748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271629921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572145d50096436148367c6f7c35a6bdf33742255e033d574b5e4163f3a8a054`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:25:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:26:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:26:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:26:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:26:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:26:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:26:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:26:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:26:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:26:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:26:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:26:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:26:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:26:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 16 Mar 2026 22:26:07 GMT
ENV PHP_VERSION=8.4.19
# Mon, 16 Mar 2026 22:26:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Mon, 16 Mar 2026 22:26:07 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Mon, 16 Mar 2026 22:26:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:26:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:28:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:28:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:28:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 16 Mar 2026 22:28:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:28:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:28:52 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:28:52 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:28:52 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:28:52 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:28:52 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 17:56:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:58:11 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:58:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:58:11 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 17:58:13 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:58:13 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:58:13 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:58:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:58:13 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:58:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceb58543f0f93458c9f20c0c91c2f936b1955ec87a41fcedcf51007bca04aed`  
		Last Modified: Mon, 16 Mar 2026 22:29:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609f20b19c60b26392cfc424cff13a0977b37ba0930946af6ff62f4876489194`  
		Last Modified: Mon, 16 Mar 2026 22:29:16 GMT  
		Size: 117.8 MB (117843410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa4bc0b49bebf7b563b19647efc8d0a4a1e82a3f3716336b222c0537650a606`  
		Last Modified: Mon, 16 Mar 2026 22:29:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dd2477210e9928cda9a59f210e4bca2d060f401652c074304a265e1e4fd0a1`  
		Last Modified: Mon, 16 Mar 2026 22:29:13 GMT  
		Size: 4.2 MB (4226955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c3c1b02bee71270c50c6ac9628b2ee5b5a99130d56a54263f3dd2cf233d058`  
		Last Modified: Mon, 16 Mar 2026 22:29:14 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8909101519147d95c930ad13b45e3d969f33ecda1d804f0701e13d24c3b0e8`  
		Last Modified: Mon, 16 Mar 2026 22:29:14 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4e2414384c7c95899cc461d14ac47d43e988b841f5cb43f4ba9607ff0d6dc1`  
		Last Modified: Mon, 16 Mar 2026 22:29:15 GMT  
		Size: 13.9 MB (13851142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0632ce6011d1cb99266711e5d9c127b98babfa9aa70c39dc45e079758f5e34`  
		Last Modified: Mon, 16 Mar 2026 22:29:15 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d709ded6fd6396ad98fde9a014f82606ee2e2baf3b8f4c3f2af367a1ea660ef1`  
		Last Modified: Mon, 16 Mar 2026 22:29:15 GMT  
		Size: 13.6 MB (13553645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c126c9681145d230e3f3b4851d8cb65027cf7538a23ff4be50578fcd5d5d0`  
		Last Modified: Mon, 16 Mar 2026 22:29:16 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a7ff29c43663046c1302f635d4b69f3bf797632885623f9ca0b539a2891a96`  
		Last Modified: Mon, 16 Mar 2026 22:29:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de099736a113317780ce6410f243907e5a5ec0bf4ec99f3406c3bb9d92868f3`  
		Last Modified: Mon, 16 Mar 2026 22:29:17 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b846626fbcb1bf54d575e375b7a000a5f9a188cec6b0a5db504df231f731f96`  
		Last Modified: Mon, 16 Mar 2026 22:29:17 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0462b5a2ab35a16db22b88e703ffa5748f261cc298fc77f5b898e7c33f97cf75`  
		Last Modified: Mon, 23 Mar 2026 17:58:30 GMT  
		Size: 33.0 MB (32953344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef546cb0a2795af9bb886a392f526d135aaee2faf3b6f7f6a021a1e0d3c0160`  
		Last Modified: Mon, 23 Mar 2026 17:58:30 GMT  
		Size: 30.0 MB (29974045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868b1f4b4eb4b47f2f789c59f0682158f214d7681fa1e95cfbfe8d03edc4fdd5`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a54620baff767338e93061cf4d48d71a2a6917541521acf28b17b727968ab0`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8357683dac64753b1b8202484fa08eaadf6831dbfc09a5aa6637ea3acaaf1d1`  
		Last Modified: Mon, 23 Mar 2026 17:58:30 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414492b2447b6d4c596a82b7d2554ea4919e2575a721e0a4dbd66eb33da29a94`  
		Last Modified: Mon, 23 Mar 2026 17:58:31 GMT  
		Size: 29.4 MB (29422248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a48555d5e0769a1e7f6f026cefbc524516bc31dd961df2b6be88f511f82606`  
		Last Modified: Mon, 23 Mar 2026 17:58:31 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20444f369643d112306ff238cf434d4b776be2acfe40a3757779f6929afa983e`  
		Last Modified: Mon, 23 Mar 2026 17:58:32 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b121c34a998618ebe1929f88e6d9e377fc7f82c3485cd6e84987ff16c87a811`  
		Last Modified: Mon, 23 Mar 2026 17:58:32 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:6d2794a52d968b922d492d4cf1a6c85803ab6b99b177c65a16cc7081b55cd604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8759579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3929b7ac0b980546876c5ec5d4194d8f9d5342945e5db92b725cdba6fcef49`

```dockerfile
```

-	Layers:
	-	`sha256:942ce21b46fcfcda49dbc832fc825fa958feea9fd696f242a1c596c1e17e6246`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 8.7 MB (8693700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93dbfe1019768782bb2b3d46448475796f84323022530c582153ff793703338c`  
		Last Modified: Mon, 23 Mar 2026 17:58:29 GMT  
		Size: 65.9 KB (65879 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:06730d07c1646b1afb4f2cdd5ac5b10d8a354e0bc8a3c9c89e8bdaa76f30f11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239903983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84661086b773bd67a38be15780f97fb4c688c1398ac157050789e0624e892a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:21:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:21:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:21:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:21:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:29:00 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:29:01 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:29:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:29:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:29:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:29:01 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 16 Mar 2026 22:29:01 GMT
ENV PHP_VERSION=8.4.19
# Mon, 16 Mar 2026 22:29:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Mon, 16 Mar 2026 22:29:01 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Mon, 16 Mar 2026 22:29:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:32:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:32:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:32:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 16 Mar 2026 22:32:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:32:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:32:23 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:32:23 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:32:23 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:32:23 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:32:23 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 17:56:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:58:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:58:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:58:19 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 17:58:21 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:58:21 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:58:21 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:58:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:58:21 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:58:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:58:21 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67109b30418fade3cc247e45c3ed938e25be0887dc5b7ec9711757e13eb729f6`  
		Last Modified: Mon, 16 Mar 2026 22:25:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a3c18230f4eb7ef08a545aad6852c10d8471e14a4d66cfdea78863ade20f5c`  
		Last Modified: Mon, 16 Mar 2026 22:25:05 GMT  
		Size: 94.9 MB (94883918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f024949353510a8bb767480fa0e00918e2116ae0cbcd9ef7117e3f35ca10f`  
		Last Modified: Mon, 16 Mar 2026 22:25:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95918568d6a043fdeb21fe4caab0d5d4e6383b1233d89cc8a720a82d90197e6`  
		Last Modified: Mon, 16 Mar 2026 22:32:34 GMT  
		Size: 4.1 MB (4089375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccff2a11f3e16df4d07a3d5b2e8584315bbfc529d08f19a9acdbbc253879078`  
		Last Modified: Mon, 16 Mar 2026 22:32:33 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e709747290ba4771fb01f6a957f6342888ddfe71a7aee53369b52cb60b285b02`  
		Last Modified: Mon, 16 Mar 2026 22:32:33 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecf4f06bc3fd23c727fc80713468e52fd317bdef8d1eb4d4b3b26d0ea4d8df9`  
		Last Modified: Mon, 16 Mar 2026 22:32:34 GMT  
		Size: 13.8 MB (13848561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbf18c8904c334000d47568babbcfc5879a8b2ef96a203857d59105baf4099d`  
		Last Modified: Mon, 16 Mar 2026 22:32:35 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3371846b4e5a4766532de414d41bc16d848080e847eb6e83206784533646c`  
		Last Modified: Mon, 16 Mar 2026 22:32:35 GMT  
		Size: 12.2 MB (12200248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e547ac1ecfb3e2dcfb73c9226425506ac8bbce3003d2cffb9125dc256f73aca5`  
		Last Modified: Mon, 16 Mar 2026 22:32:35 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a90199b7ffb31284df8a9c06be7f4d882b915148a667ed9ebb7e385304bd94`  
		Last Modified: Mon, 16 Mar 2026 22:32:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6751ae3fa6ec3236a857f260457f6ccb77ec34da3e4c107a6c180ba57db683`  
		Last Modified: Mon, 16 Mar 2026 22:32:36 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e072ff14618f007129f185c50f1e84f0fec039f9bb76853ed9ff4638c62e848`  
		Last Modified: Mon, 16 Mar 2026 22:32:36 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a400718dac78e1eb7b3541d5648642fd26776d4420ac16c3113a4ba1252f05`  
		Last Modified: Mon, 23 Mar 2026 17:58:38 GMT  
		Size: 30.1 MB (30142089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693015e3e407c7e154d95c4a291251986a5033d656695d9e29422cb697c46404`  
		Last Modified: Mon, 23 Mar 2026 17:58:38 GMT  
		Size: 27.3 MB (27344251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2264ed2dd3e3e7fed6bba5efe18f182f88d293f9ef7595aadb683a52a992e726`  
		Last Modified: Mon, 23 Mar 2026 17:58:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d49c67129353f6a88aa4c423439eb3df847efad3f73fbcffbd4b9e3ba3a3ace`  
		Last Modified: Mon, 23 Mar 2026 17:58:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f34080d8c48618a76672148a14fa76fbc05827376b547d0e986ca5118a0d255`  
		Last Modified: Mon, 23 Mar 2026 17:58:39 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd7b17f8276cdfd0fba410a81143d1da497582c335b5ca1133968f2c81622cd`  
		Last Modified: Mon, 23 Mar 2026 17:58:40 GMT  
		Size: 29.4 MB (29422255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4167f99c427bb18cc95defbe64f4e1e54e4d30eca9b47b6f1369173cd2e27aa`  
		Last Modified: Mon, 23 Mar 2026 17:58:40 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61cccf10f6af76ee106a204a2cd93efaaae49f8a6c06230276d624a79aeaa81`  
		Last Modified: Mon, 23 Mar 2026 17:58:40 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939df22dc1c3eaf31863af73ddf192489d534aea95f5e580f74c8409b70d0bc8`  
		Last Modified: Mon, 23 Mar 2026 17:58:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:60869a5a526e2545218effb6fe427cc868639485e2cb6c0dbc47c6696fb92bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8553318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c03e318fd1274fbd2b7b7f7ef6a49d2b1be97206e1e3b978d4934e72b7eaeec`

```dockerfile
```

-	Layers:
	-	`sha256:9faf2451234d61157ae93c16cdc2b8179371fdf90be1b260dc30599dbca41179`  
		Last Modified: Mon, 23 Mar 2026 17:58:37 GMT  
		Size: 8.5 MB (8487259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428095c9bdba1e873d6d59d8a742a553f4d214a5cc6a1e45ca5d518379e653dc`  
		Last Modified: Mon, 23 Mar 2026 17:58:37 GMT  
		Size: 66.1 KB (66059 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:de6789c274ccda27263ce156250b008b407ea557ab9911226e590ba65cb599fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225942339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717e14b49ad363998151fa5c58d391bf05d2b59643277deaa1dddc0cafb73491`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:32:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:32:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:32:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:32:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:32:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:32:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:32:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:32:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:32:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:32:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:32:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:32:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:32:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 16 Mar 2026 22:32:24 GMT
ENV PHP_VERSION=8.4.19
# Mon, 16 Mar 2026 22:32:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Mon, 16 Mar 2026 22:32:24 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Mon, 16 Mar 2026 22:32:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:32:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:35:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:35:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:35:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 16 Mar 2026 22:35:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:35:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:35:19 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:35:20 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:35:20 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:35:20 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:35:20 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 17:58:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:00:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 18:00:23 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 18:00:23 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 18:00:24 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 18:00:26 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 18:00:26 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 18:00:26 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 18:00:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 18:00:26 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 18:00:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:00:26 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52005a9b7be6f589fd8a6a8aa9880d48924b60fe8d9ef395edcbcd9b0397dffa`  
		Last Modified: Mon, 16 Mar 2026 22:35:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c5a91705e7e760197d1ecb55be0d30a57ad739ffd71ff515a3f27ba601daa3`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 86.2 MB (86248108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae2b2926da00edae0ca01087d28b41170d58dc99d4ce424d3f71db975d7d64d`  
		Last Modified: Mon, 16 Mar 2026 22:35:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dbbcdb587070615a3759ea035718cc8bc3234dcba36c051448a8c8d866b8ae`  
		Last Modified: Mon, 16 Mar 2026 22:35:37 GMT  
		Size: 3.8 MB (3757213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2037c32d0b818fd59bd3e3d857074fef8aad99e66ec8e760270e69a38ccb70`  
		Last Modified: Mon, 16 Mar 2026 22:35:38 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b855a8a85b2b89f33d4181e304c2ca42130dfc63ba856b007a10dc1a3fff0d8`  
		Last Modified: Mon, 16 Mar 2026 22:35:38 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f644f3e8126cd81f56240b878e8f500a3f3cf2c2575a2ce383243c98bcea604e`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 13.8 MB (13848642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7b756fa4b2e79e65661d8179ddb14495968d4e7b7915c6d85b022836ca325`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df8e6aff2f7a9cd1e21ce99df17969326187c959f17fad45e10f52083d3317`  
		Last Modified: Mon, 16 Mar 2026 22:35:39 GMT  
		Size: 11.6 MB (11614704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b9b917af65be91de013ac1543218fea4bb29b418c3ffea35feb5315f6f34c5`  
		Last Modified: Mon, 16 Mar 2026 22:35:40 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93755a3b843601dcebedad67406d2222e40bb9cba80aef289bb569d4e5b0ad64`  
		Last Modified: Mon, 16 Mar 2026 22:35:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0876ca161556988c73763d4ad0d8c9acf27efeb2265b42e54a3928336002c685`  
		Last Modified: Mon, 16 Mar 2026 22:35:41 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b073eb23e4e5fca812d8c6308d0e5243a9586d72c39cb2102157289236dfa3`  
		Last Modified: Mon, 16 Mar 2026 22:35:40 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee768fcc757d3e0727cd26994896e81ffa542c54c4625bf8d420edee48d6b85`  
		Last Modified: Mon, 23 Mar 2026 18:00:45 GMT  
		Size: 29.0 MB (29040684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eeb2ac50a03707613cec27c1dce5ce530737134d8f1147d6e82c66bd821913`  
		Last Modified: Mon, 23 Mar 2026 18:00:44 GMT  
		Size: 25.8 MB (25771609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9b84aac56cf3f27601dfdc1735d6ee96c3269b1257bb9cd6634334ba32fb30`  
		Last Modified: Mon, 23 Mar 2026 18:00:44 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd82640d2bcfc63702873d455e4d0e483ff5098738bb9029d0eb7ea8be6eb0c`  
		Last Modified: Mon, 23 Mar 2026 18:00:45 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbad4bbe3c2d6396a216092beea04e4cc86a3620c40111aa17ca988bc3f4568`  
		Last Modified: Mon, 23 Mar 2026 18:00:46 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d84e46c830014ea07dfeaa87d725f70c38ff83255f3f72652a263952cb4e0e6`  
		Last Modified: Mon, 23 Mar 2026 18:00:48 GMT  
		Size: 29.4 MB (29422236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee48d8dd066e317e02f3c61e2df12e0a6f891f98a068950648a0048b58c4972`  
		Last Modified: Mon, 23 Mar 2026 18:00:47 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3358dfff1b9603f0ea5afc2ddb60c00f6a3c5d6987fe42d8317d1108afa373`  
		Last Modified: Mon, 23 Mar 2026 18:00:48 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e77f4f4a00a72740d4a281e79cb5a1f222d38ec7be79eadab1505a9ce8a4741`  
		Last Modified: Mon, 23 Mar 2026 18:00:49 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:b7903eae49bbc550953678d665cf9910cf6bd4a1056a424ed22feb7d82872675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8558152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75941c7d7de96b363d02f9b8d03be953a657beb4fea35f693946f96be898a80e`

```dockerfile
```

-	Layers:
	-	`sha256:0f450d358a5b46bbc42400a226015ca9566358320c7ba4bd0447ec674314e67f`  
		Last Modified: Mon, 23 Mar 2026 18:00:43 GMT  
		Size: 8.5 MB (8492093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b0cc9e22ac0ef7e472f13d91b9de86f5706d39021bc1a4c0d9d751f307376a`  
		Last Modified: Mon, 23 Mar 2026 18:00:43 GMT  
		Size: 66.1 KB (66059 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:f4681a33d39f1f61f738bcbf13aa251669082b6969873f81badfa3ef3a1bbae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263866277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c618ebb938c73b08e0274905cdc3e23b6e2803a7c64ef653a1da5651e6b332c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:25:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:25:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:25:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:25:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:25:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:25:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:25:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:25:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:25:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:25:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 16 Mar 2026 22:25:59 GMT
ENV PHP_VERSION=8.4.19
# Mon, 16 Mar 2026 22:25:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Mon, 16 Mar 2026 22:25:59 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Mon, 16 Mar 2026 22:26:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:26:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:29:14 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:29:14 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:14 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:29:14 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:29:14 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 17:56:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:57:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:57:54 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:57:54 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:57:54 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 17:57:56 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:57:56 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:57:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:57:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:57:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:57:56 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66e667464959ab0c9b7fbabbcbf67c02e35a304ee9f7fa8ca9af8e9623e8ad2`  
		Last Modified: Mon, 16 Mar 2026 22:29:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09e0ab81291b28d74d4722bc0394dddc1ce58d184b7a9bb77e0e3e0618fc3f`  
		Last Modified: Mon, 16 Mar 2026 22:29:37 GMT  
		Size: 110.2 MB (110165056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81d9d9f9376ba4cead5c5f2d8a08e6df915677e5342b5f85842f2c507386610`  
		Last Modified: Mon, 16 Mar 2026 22:29:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47bf0f83120b779e9a904bc201f08730bfbc41fc08fa42311453ae7180547fd`  
		Last Modified: Mon, 16 Mar 2026 22:29:35 GMT  
		Size: 4.3 MB (4305420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe981650dcca02e84c53e1eb33188c342a7e5b9406e1b1a0502eb96539128bf7`  
		Last Modified: Mon, 16 Mar 2026 22:29:35 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e1cbcf8104accef6b5769a0425e32a42f7d2b748a90b20863c09e34675bccc`  
		Last Modified: Mon, 16 Mar 2026 22:29:35 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628ec4f46c2487ae39112d174c2b63961c352bf300f50c8921075e2624c96d2f`  
		Last Modified: Mon, 16 Mar 2026 22:29:37 GMT  
		Size: 13.9 MB (13850766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4b24d45afe1dc38b25497443beebe44ceec1801e5bb819e0dabee9c5a73397`  
		Last Modified: Mon, 16 Mar 2026 22:29:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c455c44443cc16510daca6277d180dafe45082dc1f6ea2e72a58448b6c371`  
		Last Modified: Mon, 16 Mar 2026 22:29:37 GMT  
		Size: 13.2 MB (13197638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6898c33a6062611c3eedd025ea492db4f215d72c2ac97116ddc9148febd83f8`  
		Last Modified: Mon, 16 Mar 2026 22:29:38 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50595d1980b5e13327746f4af734fe73d4a1dc52efa8292e335cd7805662dd58`  
		Last Modified: Mon, 16 Mar 2026 22:29:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd451cb69f196507aa43def95fc731a21eb5db0ef494acbf7e0e4c6b3c4e82b`  
		Last Modified: Mon, 16 Mar 2026 22:29:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23aea6d22955931764ea31f788a988de28c5ff4cb0c201881ffa1844fe5626fa`  
		Last Modified: Mon, 16 Mar 2026 22:29:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af9197c9de8b77b8b0dd7933c61f51173403d263b53cadd1490bbce4060c274`  
		Last Modified: Mon, 23 Mar 2026 17:58:15 GMT  
		Size: 34.5 MB (34464218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5c5b4ae96a10ac3adb93741ff91c3b5f7a784ad1791c7624bbcab7f92a4025`  
		Last Modified: Mon, 23 Mar 2026 17:58:14 GMT  
		Size: 28.3 MB (28292902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4227a17294f5bd672147c420cc7c95642d723a754fb3a47e9e5669ca2c2d20`  
		Last Modified: Mon, 23 Mar 2026 17:58:13 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ecd147c91301d589c99a6cf5771efa5e39172af031b8063a91a23e05993743`  
		Last Modified: Mon, 23 Mar 2026 17:58:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd80c3e1efa0a50de54ead4bd1b4adb961b6667b7e5a7c6dd394cfb821e6199`  
		Last Modified: Mon, 23 Mar 2026 17:58:14 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0ab82cd96ab60f3aaa9832e8fa85c5047bdd6748f778124b12e00b72f2048e`  
		Last Modified: Mon, 23 Mar 2026 17:58:15 GMT  
		Size: 29.4 MB (29422240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470e2ea8d7711c79ac4e53a3d9a64683e1e3932c59d1a5c2a206252684b51329`  
		Last Modified: Mon, 23 Mar 2026 17:58:16 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e440ec54726eaf74fd38b13bcd9d755aa1d4a8855fa8703ba91b2f00b0821a`  
		Last Modified: Mon, 23 Mar 2026 17:58:16 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756347c01961dfb283964406c9c13dbf1c27c4daab9bac8caa9ceaac4f2e0d00`  
		Last Modified: Mon, 23 Mar 2026 17:58:16 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:3f629f39d6b3d2564a8840a921f35bb1bdb4d55cc7695f783db5737a776cd7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8856339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533457817f1cb39d9763593b711c58a57cff837fc121a86480cb4c814ae4af90`

```dockerfile
```

-	Layers:
	-	`sha256:ebab6b4b11b4dcedf4c107291d9075f3a7546242564a72104f02a76f6d15a450`  
		Last Modified: Mon, 23 Mar 2026 17:58:14 GMT  
		Size: 8.8 MB (8790218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194ddebe70af1c486324031840d2fef725d489b771b7a89ddbaa501c52ac5b27`  
		Last Modified: Mon, 23 Mar 2026 17:58:13 GMT  
		Size: 66.1 KB (66121 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; 386

```console
$ docker pull wordpress@sha256:dfe583262706911e1ef5fa457134fe2538a80e3a0999c61a946444b4de32b25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269484499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92450ddfb3a0ae40f97115dcedc7cb63e9b33de1c37eb3d7cf7d0d998083ee21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:19:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:19:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:19:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:19:36 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:23:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:23:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:23:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:08 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 16 Mar 2026 22:23:08 GMT
ENV PHP_VERSION=8.4.19
# Mon, 16 Mar 2026 22:23:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Mon, 16 Mar 2026 22:23:08 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Mon, 16 Mar 2026 22:23:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:25:59 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:25:59 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:59 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:25:59 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:25:59 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 17:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:55:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:55:01 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:55:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:55:01 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 17:55:03 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:55:03 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:55:03 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:55:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:55:03 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:55:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:55:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff18cd405b0077f8c0cc220744ee2fd3352b9a92a1ec478206127eeeaedf01`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6834162b03896936de217cd3bc496c3a3bbc10417cad5f4f6f4c703fc07e4c`  
		Last Modified: Mon, 16 Mar 2026 22:22:54 GMT  
		Size: 116.1 MB (116144065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aa4986b735ced1046b1a93e12899e1fc9147484cbe2cf1d6e2ff6e99e61ed8`  
		Last Modified: Mon, 16 Mar 2026 22:22:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdae570efb63aa57a6c3546f494610cee0681f3cb5b63cb24ac816061cffbff`  
		Last Modified: Mon, 16 Mar 2026 22:26:09 GMT  
		Size: 4.5 MB (4458352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92beef1c97f015cc7959f33f2ad777c9b54ba4e3f09f9866b0c8ba8c371c5926`  
		Last Modified: Mon, 16 Mar 2026 22:26:09 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8755df3603ba77d219f16f8073b5726580cc701da578699d0fed873b7709bbc`  
		Last Modified: Mon, 16 Mar 2026 22:26:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a46a9c83629f1573d06722f55d9a12018823b0a3d35062204f5cd07ddef6c44`  
		Last Modified: Mon, 16 Mar 2026 22:26:10 GMT  
		Size: 13.9 MB (13850159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ee681db10faadf038e120c78c250617e33deee1464845d3d26c7772432d8ee`  
		Last Modified: Mon, 16 Mar 2026 22:26:10 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49502917b604d4c17995e1d4b56b9620a7db42a4544cf085035d6df4ae1f2ccb`  
		Last Modified: Mon, 16 Mar 2026 22:26:10 GMT  
		Size: 13.8 MB (13849319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48be00ed3f6de888b4c1e814ccf56e8d54196b66d4f9347572faf21708e1cc5e`  
		Last Modified: Mon, 16 Mar 2026 22:26:11 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd1e1a91daceb2a537a2440bd633ea34e3067b88bc6b0622c60c8b925d3bd23`  
		Last Modified: Mon, 16 Mar 2026 22:26:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f1acc1a24b7377f67146709c518d224829aea9e12cc77b88811dc5d3b54992`  
		Last Modified: Mon, 16 Mar 2026 22:26:11 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29992c3ca7e44083b9ab7da772833c13fa8628a452436b14ae5b40996ed1ce`  
		Last Modified: Mon, 16 Mar 2026 22:26:12 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d8e351128d9fca955ac5bd9eb69c97fe4914f7b7fe5a8d9d536ec39c270c6d`  
		Last Modified: Mon, 23 Mar 2026 17:55:20 GMT  
		Size: 32.4 MB (32406078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ca19d5f48300c3b2fe23de5fb557e7cc8fe1fd35da790df306e02abe374ca`  
		Last Modified: Mon, 23 Mar 2026 17:55:20 GMT  
		Size: 28.0 MB (28033516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197751982a0f3deb40293cbf71342beb170a66b8c4db30d8d2c9e30c35792e8`  
		Last Modified: Mon, 23 Mar 2026 17:55:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec20535612561a8503e71f94f45569b9235ed14960cba05b30fb805c6d41dc0e`  
		Last Modified: Mon, 23 Mar 2026 17:55:19 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554a1ed19204c85b717b1758d36a7886cb5dfdaf27e010ffc65886f3fd075792`  
		Last Modified: Mon, 23 Mar 2026 17:55:20 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14874243f0085ba14195b14c8e26c499a27cba6ef01920e625c3cee46a80ee8`  
		Last Modified: Mon, 23 Mar 2026 17:55:21 GMT  
		Size: 29.4 MB (29422240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4588e10872c116ce3c48bc494242ccd3195284eb05e3633bec0751c9f6c823`  
		Last Modified: Mon, 23 Mar 2026 17:55:21 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51aacf17d0d22db9af4883ea27b2861995d2b1088c296e5dc89c7017ace8229`  
		Last Modified: Mon, 23 Mar 2026 17:55:21 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ba4fa2d038084d9280f560bc20509eecd851b6f5ee3e5fbb26880b6872d221`  
		Last Modified: Mon, 23 Mar 2026 17:55:21 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:a0aa4d66ae36e53e96e35b7d0ab309272456c4f1164707be97577f5a390c0ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8732519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d98ae52c80334c27eac937d9209614dff8025599d4eac0ab3f39d7c2bdeb39e`

```dockerfile
```

-	Layers:
	-	`sha256:a3ca1a80248bacaec17af212bcf155e6514a942f09f695b5d47dc38feddf971f`  
		Last Modified: Mon, 23 Mar 2026 17:55:19 GMT  
		Size: 8.7 MB (8666704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd43a3771f9b881df28764a304efe210fde3bc50b9a0c0721014a13e1cd9b64`  
		Last Modified: Mon, 23 Mar 2026 17:55:18 GMT  
		Size: 65.8 KB (65815 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a7ce556488a9442a2d9280b2a0846fa020b5fb3f45448366e669db9d0f37c697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267557268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02d0b7a2ff4f562161b352848898dec7a1d5f27954d354efb0bd3ab292a175c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:08:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 17 Mar 2026 00:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:09:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 17 Mar 2026 00:09:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 17 Mar 2026 00:09:29 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 17 Mar 2026 00:09:29 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 17 Mar 2026 00:11:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 17 Mar 2026 00:11:05 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 17 Mar 2026 00:11:06 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 17 Mar 2026 00:11:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 00:11:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 17 Mar 2026 00:11:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 17 Mar 2026 00:11:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 17 Mar 2026 00:11:06 GMT
ENV PHP_VERSION=8.4.19
# Tue, 17 Mar 2026 00:11:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Tue, 17 Mar 2026 00:11:06 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Tue, 17 Mar 2026 00:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 17 Mar 2026 00:32:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 00:36:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 17 Mar 2026 00:36:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 00:36:30 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 17 Mar 2026 00:36:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 17 Mar 2026 00:36:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 17 Mar 2026 00:36:30 GMT
STOPSIGNAL SIGWINCH
# Tue, 17 Mar 2026 00:36:30 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 00:36:30 GMT
WORKDIR /var/www/html
# Tue, 17 Mar 2026 00:36:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Mar 2026 00:36:30 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 18:07:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 18:11:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 18:11:01 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 18:11:01 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 18:11:02 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 18:11:05 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 18:11:06 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 18:11:06 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 18:11:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 18:11:06 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 18:11:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:11:06 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb03c46c4e3a31e2b4f495c9335dc55280c3ab8757fca7a09e34292dd392624`  
		Last Modified: Tue, 17 Mar 2026 00:14:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b32d1fdb741701192f7fb2aa3e0f0fe279555c73025c4d8e2bfe3afe82dca7`  
		Last Modified: Tue, 17 Mar 2026 00:14:55 GMT  
		Size: 109.6 MB (109598843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c8e58deeac398c483ddeffcafbfedcad200b501b9842a4972a58d96d41f222`  
		Last Modified: Tue, 17 Mar 2026 00:14:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e261ceb10fb32d685090be589edc24a83b5557f329d79556d0b8346b7187d6cc`  
		Last Modified: Tue, 17 Mar 2026 00:16:22 GMT  
		Size: 4.9 MB (4881621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862c893c3f07d7fe517bea23637fab1afa886194ed1740237422df29eb804f60`  
		Last Modified: Tue, 17 Mar 2026 00:16:22 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d224818cbc48d66a7f29df7a539e01878a7c8432906bf8cfeae409bca082d`  
		Last Modified: Tue, 17 Mar 2026 00:16:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e612bea27a90d9fb904c0a9bb3b607d73397e105f4c436d4978823f25a99fc8`  
		Last Modified: Tue, 17 Mar 2026 00:36:54 GMT  
		Size: 13.9 MB (13850281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16e00e39d09d1fcc34147b03aac47c5f39271dfd1579328f6dfa81df59dd55f`  
		Last Modified: Tue, 17 Mar 2026 00:36:54 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3d067bfcb7e9bc15dcf0cb1f390c324fff4063026551f507237cbd5e668fcc`  
		Last Modified: Tue, 17 Mar 2026 00:36:54 GMT  
		Size: 13.9 MB (13949023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1b86b1839703299deab64eaf66f77d9cd75e99838eeae77d0c95106199cb06`  
		Last Modified: Tue, 17 Mar 2026 00:36:54 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf28a0780600a76a2aca881567115f2e6caf3762a1fcbdae421cb41833f03d4`  
		Last Modified: Tue, 17 Mar 2026 00:36:55 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c45a5908d114a4baa498378f7339466c3161ae49446b515f73a121cc3a886b8`  
		Last Modified: Tue, 17 Mar 2026 00:36:55 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832b5f29c60d612acc385327225fc406ff9190e61763c21f330a9a3c9c5f2d8f`  
		Last Modified: Tue, 17 Mar 2026 00:36:56 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c20681fc424a8539c53f71fc979ac65255baf87cae0aaf1611dc6d09a766783`  
		Last Modified: Mon, 23 Mar 2026 18:11:45 GMT  
		Size: 33.0 MB (32951584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5269c041e9e91f866cc030ef6d86ed6df19b6c24a95d36a8394a3c50159f5`  
		Last Modified: Mon, 23 Mar 2026 18:11:44 GMT  
		Size: 29.3 MB (29281185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8a26a99278b7e6b195adedc856b230c71370bb1199a0eb42324e0fd00211d7`  
		Last Modified: Mon, 23 Mar 2026 18:11:43 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95944d2f9a905ef62e4e6d64862dceed52c0a2a0d1d99bfa5204bda58391a83b`  
		Last Modified: Mon, 23 Mar 2026 18:11:43 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dde4a9ca2b588373cf8989f4960bc0501a4f905df4e4be51f2b7677210b1093`  
		Last Modified: Mon, 23 Mar 2026 18:11:44 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0765e7410b1773b0f738a147f0194f7d35d025e3dd17716666140f97bdc52c5c`  
		Last Modified: Mon, 23 Mar 2026 18:11:45 GMT  
		Size: 29.4 MB (29422244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0b5bdceab6149c66851e51e66450dbb2d944821f49e5c34cb92f6c543a681e`  
		Last Modified: Mon, 23 Mar 2026 18:11:45 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2493508e2a393713a5f6ca74785d8606f274849f9434d5ee87e6de1a5a8bef54`  
		Last Modified: Mon, 23 Mar 2026 18:11:46 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf084d2559d85cef0c76851edd19c391f7877ba0dbed1438bc6975d911b8f627`  
		Last Modified: Mon, 23 Mar 2026 18:11:47 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:603ef1c9b3c12ff3adb440966d3aeeb47dd187539e3626d32675a791321bdd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8760526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aec5ea1716b7179216c32aaeeeceb5dd70ee34fc36e10df61a854a3b6066ef`

```dockerfile
```

-	Layers:
	-	`sha256:452f1f9ac39a6539fc07731ce8027e22efae08a7f04567f917d0818ad2cca357`  
		Last Modified: Mon, 23 Mar 2026 18:11:43 GMT  
		Size: 8.7 MB (8694569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12c7249cf0b51a8d6e5793b4acf521f0a4eb362ae4a57e391ef2cdad63e3f24b`  
		Last Modified: Mon, 23 Mar 2026 18:11:42 GMT  
		Size: 66.0 KB (65957 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; riscv64

```console
$ docker pull wordpress@sha256:4f897b82470e643f2c21405f462611783be1a447e02449aac7d31a2b6584a47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304785065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c2e18b0689fa1bd3525434e9896beddedecbe30fb19c58185010da4b74ae80`
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
# Fri, 20 Mar 2026 23:12:36 GMT
RUN set -eux; 	version='7.0-beta5'; 	sha1='ba5b170b627cae0a73939bc1b03978a738906b82'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 20 Mar 2026 23:12:36 GMT
VOLUME [/var/www/html]
# Fri, 20 Mar 2026 23:12:36 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 20 Mar 2026 23:12:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 23:12:37 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 20 Mar 2026 23:12:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Mar 2026 23:12:37 GMT
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
	-	`sha256:d873c8b07daf720d828927963223dfde942c676c509d3717b7164a9b57c94370`  
		Last Modified: Fri, 20 Mar 2026 23:17:26 GMT  
		Size: 41.8 MB (41754257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89a05e55474d5775aa8d300400feeabbf1ad46ef5211b7018e2bc260e03ecf0`  
		Last Modified: Fri, 20 Mar 2026 23:17:19 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b58dd6274d4a5358a76028d17eaca99efac342beeebab7da6d9c4269910755`  
		Last Modified: Fri, 20 Mar 2026 23:17:19 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d7daa372121d227c7d00138cdae705a55f14afa02ec916355c11f890bc9b74`  
		Last Modified: Fri, 20 Mar 2026 23:17:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:e524b67f59c6f88d79bc5b903beb6ab3f5d023dbd3b8f8c396ebc473fba42c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8840683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f4850ccb3026a312603ae0f01da170467c426de380d95784f95f42ec75345b`

```dockerfile
```

-	Layers:
	-	`sha256:a5403f04dfc54221c731f68f3e64893be4cd5ac2f6698060127827d3fc410ac2`  
		Last Modified: Fri, 20 Mar 2026 23:17:20 GMT  
		Size: 8.8 MB (8774724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21a19d2d8cded9188ca5616c5d1bfa20016b3148f51a6636ec637ff2129a544`  
		Last Modified: Fri, 20 Mar 2026 23:17:18 GMT  
		Size: 66.0 KB (65959 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.4` - linux; s390x

```console
$ docker pull wordpress@sha256:69c3427b3ee9142e2fb49b3b58c26f3dd8c0759ebbd318627f647313177f6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242085580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2008f9d1cd3db3185e4d2e692b819b513acf3cf30307550782c95dcb8e828611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 16 Mar 2026 22:23:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 16 Mar 2026 22:34:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 16 Mar 2026 22:34:06 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 16 Mar 2026 22:34:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 16 Mar 2026 22:34:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:34:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:34:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 16 Mar 2026 22:34:07 GMT
ENV PHP_VERSION=8.4.19
# Mon, 16 Mar 2026 22:34:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Mon, 16 Mar 2026 22:34:07 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Mon, 16 Mar 2026 22:34:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:34:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:39:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:39:11 GMT
STOPSIGNAL SIGWINCH
# Mon, 16 Mar 2026 22:39:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
WORKDIR /var/www/html
# Mon, 16 Mar 2026 22:39:11 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:39:11 GMT
CMD ["apache2-foreground"]
# Mon, 23 Mar 2026 17:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		libheif-plugin-aomenc 		libheif-plugin-x265 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:55:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:55:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:55:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:55:16 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Mon, 23 Mar 2026 17:55:18 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:55:18 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:55:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:55:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:55:19 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:55:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:55:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e46e1620cd3c7b7f036b3a3391ed3db0eed8e0946fff1e1c7a8addcb819cdd`  
		Last Modified: Mon, 16 Mar 2026 22:28:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868826499ca4d1a10f9f3e2de04ae7b4901b5b977edec1a6ab8f3e89e3e34448`  
		Last Modified: Mon, 16 Mar 2026 22:28:09 GMT  
		Size: 92.6 MB (92572934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e80ff3c161d147a6f738605c2420c1c12dfb5085d94b0bd3c6c19c7f6225ebf`  
		Last Modified: Mon, 16 Mar 2026 22:28:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd87d619e696958fc84e28893f9807b231d9081ed01290732519c736130a6d`  
		Last Modified: Mon, 16 Mar 2026 22:39:31 GMT  
		Size: 4.3 MB (4329340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c66152edfdfb05fd73241d87656199967990c1c84bb4984ae567f2c4bdae28`  
		Last Modified: Mon, 16 Mar 2026 22:39:31 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91c5dffa786619db4e8937e2a194302544585af6deb969098f96aac07ee6daf`  
		Last Modified: Mon, 16 Mar 2026 22:39:31 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a633c8e8bd1cfbf2ed6e03955973567a58dd853a3cac1621ef016c5e28c482`  
		Last Modified: Mon, 16 Mar 2026 22:39:31 GMT  
		Size: 13.8 MB (13849514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cd20d23d5e46a16a98fb5aeb0d84afde1f4071b82d1bfd7fc57cdce5d0538c`  
		Last Modified: Mon, 16 Mar 2026 22:39:32 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff25dd3e6ff02ab3462b933141da2bc5ed828055d88c886e441218f9a4c15489`  
		Last Modified: Mon, 16 Mar 2026 22:39:32 GMT  
		Size: 13.3 MB (13307161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32223f796db3f3102a882e27c59705d3beda103ee48d7b2c6d45aa4762218d9f`  
		Last Modified: Mon, 16 Mar 2026 22:39:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98fc687cc812eb85979a62e16f5655d24adf9112b050007a280735b7b96814`  
		Last Modified: Mon, 16 Mar 2026 22:39:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5513a9f769bd647e99532ccd3935b7b8ceb31d02928259495830b7b4fcc4b0`  
		Last Modified: Mon, 16 Mar 2026 22:39:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57921c4de9c84a08c74d8f1465a42387b00604a21959326626632b0f3c083b0`  
		Last Modified: Mon, 16 Mar 2026 22:39:33 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8d0c8d474939ded15b6f4418c86b20f30e9c33f0a1dfc7921423469a8ee6e7`  
		Last Modified: Mon, 23 Mar 2026 17:55:44 GMT  
		Size: 31.4 MB (31396147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448f33ca0cc6e9aafee5474ba94d4c8b178ec41ad5a205de6d52dbf006dcff5b`  
		Last Modified: Mon, 23 Mar 2026 17:55:44 GMT  
		Size: 27.3 MB (27343354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a52715f335973f890dae3e49cfbf35c68062f840bef26f3ba2e88fc00bdc9a5`  
		Last Modified: Mon, 23 Mar 2026 17:55:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6650c2add4d3da5733da080038a82024046339d1765036dbeefec64949dac`  
		Last Modified: Mon, 23 Mar 2026 17:55:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59be9cea66e23d1c9226133abafa0d7aa22dcf2622913fc25d8422130e06052e`  
		Last Modified: Mon, 23 Mar 2026 17:55:45 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9c18c45a317c41d2abc66782bfe45fad7ea507566d287fa486ef7112754f38`  
		Last Modified: Mon, 23 Mar 2026 17:55:45 GMT  
		Size: 29.4 MB (29422228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3789cc8d9169c034322be3572fff5bc327b05abbbb049f3338247cbacdcc9d38`  
		Last Modified: Mon, 23 Mar 2026 17:55:46 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f06346e1f80f30fb4076684583d39efed273dbf26da167068a6fd946dcfb25`  
		Last Modified: Mon, 23 Mar 2026 17:55:46 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa821fbac577ad3afea4cea1f16242a803c6a87705ac2d44e31d8b230f404cc`  
		Last Modified: Mon, 23 Mar 2026 17:55:46 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.4` - unknown; unknown

```console
$ docker pull wordpress@sha256:7cea26582b2d768d300458dff22b5e58a8126ee2dcab1a9be8f8dc7c0677d106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8478703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45911f2f1fc0b7dfc945114aa56a9c5a54cfac134296dae416ed1cc5d0605fe8`

```dockerfile
```

-	Layers:
	-	`sha256:35dfdc67cf16cbf1d8306f0039425c9ed085688fda2befad4388eb177d48560f`  
		Last Modified: Mon, 23 Mar 2026 17:55:44 GMT  
		Size: 8.4 MB (8412834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d36d487beed5961867f8ace4cbff14103e54ca7f49ae5459a53fd1ed5cdc9e8`  
		Last Modified: Mon, 23 Mar 2026 17:55:43 GMT  
		Size: 65.9 KB (65869 bytes)  
		MIME: application/vnd.in-toto+json
