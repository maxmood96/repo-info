## `wordpress:php8.4-apache`

```console
$ docker pull wordpress@sha256:19ab48c69433df85c1dd1a456924efd7059099a70c768786f465c3e8846731df
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

### `wordpress:php8.4-apache` - linux; amd64

```console
$ docker pull wordpress@sha256:0cb3cae75907dc420eb7eccb3a8ba269c46a1196b5b63795da7c1aeea6c31b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266377736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f68a918a86c5a604783c012d68f3bb90a626e94fb4ed0f21935cae7e9eb686c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
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
	-	`sha256:c9e308cc50b693957306e92ca58a13d5e76fa6062ce1183b80a4d58fbf4813cb`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 13.8 MB (13812111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e087ba3bc8c57515c87d37baddfe40ed81116a0e3cf6a9ee53244cab83fac470`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca534350e7ded62a7c4bff4b7dc033f2e48882ae3886211d33c74bec54278c1c`  
		Last Modified: Tue, 30 Sep 2025 00:00:10 GMT  
		Size: 13.5 MB (13528156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f9354b18f41807e1ffba980c274ba75ddaf2e93ace0be1328a1e41b5a9f70b`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e584db80115d9b76e08cbf59644ff6e1c29774803b273e7e9beb5bb813809d`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6af47d3e303e8b18124958d7bd9a82907c91dcc5f2e6b7ae0ea4e5da7b4ddc`  
		Last Modified: Tue, 30 Sep 2025 00:00:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80f3ae94ca7eca6ab2eb920234e99c99fcb2aa5d46cbe933f6c56728a81e97e`  
		Last Modified: Tue, 30 Sep 2025 00:00:07 GMT  
		Size: 888.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78031a0a9bd73a4c14d8803a6a3168e4159215d918323dfa2d5a3685a4ecfac`  
		Last Modified: Tue, 30 Sep 2025 21:13:20 GMT  
		Size: 26.3 MB (26297073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797956176645263b19874133090c9fe1f56b41fe0c7ec50a75daaf773071043d`  
		Last Modified: Tue, 30 Sep 2025 21:13:21 GMT  
		Size: 34.0 MB (33972195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554ecdfb2c96cfec05a91a18b7000d6fd660e588d6103fd4b7914fa576c5330a`  
		Last Modified: Tue, 30 Sep 2025 21:13:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a330ace67dc44dfa6c57e4632ce050d6d2481ed0384e0da6ef83f2f02d65857`  
		Last Modified: Tue, 30 Sep 2025 21:13:18 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68c8d223f0d0743ecdf7f5871f9e59f2ebd06076b015e4bc2f14060897044c`  
		Last Modified: Tue, 30 Sep 2025 21:13:18 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a78a8e6c35bb2deccc63eae43195ccaf5e2653f985cb8538cc85ccf4983b88`  
		Last Modified: Tue, 30 Sep 2025 21:13:35 GMT  
		Size: 26.9 MB (26899829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe08f40c0f0ccbabee7ded6b3b6622fb6756a620cf97bf5d48733d6a832a357`  
		Last Modified: Tue, 30 Sep 2025 21:13:34 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e96a56ccf088813b57578cc703c7c7964766e4587c4836f563ad779cac76b2a`  
		Last Modified: Tue, 30 Sep 2025 21:13:34 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da5381855ea88edbcf2fed0571e768d018fa7dc4cd6de62b21d8e28523d76bc`  
		Last Modified: Tue, 30 Sep 2025 21:13:34 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:e2fce1770c8c8010048b54bb8bc993fd8dd600a5f52d955d69f05d9ea746f067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8736596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446ff138d4ffdc40a1a28926c2f61095d5fa697c966bdddb8d6a444075f031`

```dockerfile
```

-	Layers:
	-	`sha256:1d4c943e842245158ee428be17a7a52bb995c8b74af240e07a47375a99736d33`  
		Last Modified: Wed, 01 Oct 2025 16:18:16 GMT  
		Size: 8.7 MB (8671193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d87b792eabcf33a6a2fbfa82b8257234f62fed478a9ff3988d8e7666898068a`  
		Last Modified: Wed, 01 Oct 2025 16:18:17 GMT  
		Size: 65.4 KB (65403 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:02e2b04210109552a4366c5821e4ed4444f46ae720a9e854431c128ed789f5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235648704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616923d79446ede0801a662e3df283b89e91aca516c09749f1535d857ef9dbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 18:46:43 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 18:46:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 18:46:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_VERSION=8.4.13
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Thu, 25 Sep 2025 18:46:43 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 18:46:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 18:46:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:46:43 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 18:46:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 18:46:43 GMT
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
	-	`sha256:4454155cd87487bba9a48307903d757a5d949a81cac4ea7181d21c768154709b`  
		Last Modified: Mon, 29 Sep 2025 23:53:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d20120918cfeb5173294cc1c08102ea1383c4e1df5d0e01d5e762648126321`  
		Last Modified: Mon, 29 Sep 2025 23:54:09 GMT  
		Size: 94.9 MB (94874441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02541a4d4fa81df6b424c500c3a4276614553df68e89f9b0165f90e5b56aebb6`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a271e5d70023c4287902016e5804e71024f8dba60c93d744aa28db5149f91bb`  
		Last Modified: Tue, 30 Sep 2025 00:10:15 GMT  
		Size: 4.1 MB (4082030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344cd86f4b68079123149852001ef42deae0ccdeebbd6317a6111a2106d2085`  
		Last Modified: Tue, 30 Sep 2025 00:10:15 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8588ca70d5d36b0643819ee7f13644dfabdb2a58c17f068be8593f4bd22bdb4e`  
		Last Modified: Tue, 30 Sep 2025 00:10:15 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10766c846a7e07f5db51a8f2c2055284c09c57043976684e371fb9c619ee5ad1`  
		Last Modified: Tue, 30 Sep 2025 00:10:17 GMT  
		Size: 13.8 MB (13809487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475f266509bbd7928589204a5257b7b17ee0ef334ad7f3c86b62575aa3001cab`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516f5c6ea7b78380b0d11ec9a9fe08d89bbe1e079a108ee3af74c16e1c017f0b`  
		Last Modified: Tue, 30 Sep 2025 00:10:17 GMT  
		Size: 12.2 MB (12188407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6161b1b27fa761a54dc440483694913cc9acace7d0db28eb54f7b9aad971cd5`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4170549d36c423513600e0da543b4115c1e39dfe21ee022e28497df79313a06d`  
		Last Modified: Tue, 30 Sep 2025 00:10:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c4948c00b8f70d450f273b3f3d120a08b722c37e9998328d192b855f04e3f1`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d5966883bce9f5e1d79b7582657029bc265ee1c0c172b66359cf36c09496d4`  
		Last Modified: Tue, 30 Sep 2025 00:10:16 GMT  
		Size: 887.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b658d99ae9556f5dbad98d6c3a2bbdfa6351fe2301f928c62abf344ccd5b8e22`  
		Last Modified: Tue, 30 Sep 2025 20:38:26 GMT  
		Size: 25.7 MB (25726495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fca155c8b439e0af79ee23e31150c481bbf9aaa78c81dab3b861b945c323fa`  
		Last Modified: Tue, 30 Sep 2025 20:38:25 GMT  
		Size: 30.1 MB (30092241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b802cebad3195cccc08be6eb89902ae37f5080ac3fddb78397ae5ac63413cc`  
		Last Modified: Tue, 30 Sep 2025 20:38:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22df97189462531ad0f8ff45961ad4595dd7b1aeb24927ca5f0341b8b5d7de5`  
		Last Modified: Tue, 30 Sep 2025 20:38:23 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13fdeee74686dc162b3b34549e0da04280cad22145bc19095b28f252210ad5e`  
		Last Modified: Tue, 30 Sep 2025 20:38:23 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11f893b2994d29efeffd0ab75cc1f328a086297182c03f820f49d054fd2461f`  
		Last Modified: Tue, 30 Sep 2025 20:38:26 GMT  
		Size: 26.9 MB (26899839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72caebadf7e5be0b59e4456f6663e68527d2b94a21b38adb54a74e0013ed4a14`  
		Last Modified: Tue, 30 Sep 2025 20:38:23 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a2e84a937e451093318b3ad4fbae1794cb65c04ef9459f36542fc487a92c61`  
		Last Modified: Tue, 30 Sep 2025 20:38:23 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda719de49cdcf349fd694a5a9cba5a21512c28dabe7868f406ec451321d3398`  
		Last Modified: Tue, 30 Sep 2025 20:38:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:7b81af3e973cae78df2e6f774357b3911e2f9a2d4b6b60e685f218a6eaa3200b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8535809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c043dc2ea17a32f281f83a522720f9a0ff329c2974dd32b98112576f7452f7`

```dockerfile
```

-	Layers:
	-	`sha256:47f7dcf3ad52c92f1d721b5b5492b4d971caf722187a8e66f28a8ef0c829151a`  
		Last Modified: Wed, 01 Oct 2025 07:19:20 GMT  
		Size: 8.5 MB (8470226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b744b0a5bfe4442993d4d0945eadc75e940448e00f41265312383db195cdcd`  
		Last Modified: Wed, 01 Oct 2025 07:19:21 GMT  
		Size: 65.6 KB (65583 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:7ea5a0d8d82f60f20a9c942a62ed13949cef8640ebf483bb4b41913fa07eb741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221852585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a8f111acf6b3bd3fb53af8473fd7001101dc73848559bb1c61a8d150649e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.13
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Aug 2025 18:29:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
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
	-	`sha256:b0fea7947b7a81f9270b4216f1e66f4bcf6fbbf05ff9c101aa73830bc96fe5ba`  
		Last Modified: Thu, 25 Sep 2025 21:20:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a88d6aded36addedff947706ab1a2a53e238f592fa79e4f22dcdbb8e8244d89`  
		Last Modified: Thu, 25 Sep 2025 22:13:37 GMT  
		Size: 86.2 MB (86245540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37b3646da3592f98c40979346aaa1292ca2b338b7262add2eb2ed27c2b6540a`  
		Last Modified: Thu, 25 Sep 2025 21:20:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb7903da54721ff582fcfbc4643ce34643f5062b1aed19d9c2289ed96917e81`  
		Last Modified: Thu, 25 Sep 2025 22:13:17 GMT  
		Size: 3.8 MB (3751924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7c3710c409fcb261f5c2813d77f501389a579cbe14093bc65faf518118f7cb`  
		Last Modified: Thu, 25 Sep 2025 22:13:15 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610206b45be14445e2cf1872e39effa3b0b9147ad789896c2f08dd1e501d26ef`  
		Last Modified: Thu, 25 Sep 2025 22:13:14 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5185a3cb9b6bbb1161ab00cff96886fb042108bb29f08e3fc458c9cfd8857de3`  
		Last Modified: Thu, 25 Sep 2025 22:13:16 GMT  
		Size: 13.8 MB (13809587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86b1ff9dd5918031bfea49f66d1cc29fb5815969959e509162e02fb880735a0`  
		Last Modified: Thu, 25 Sep 2025 21:20:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67d3f6c3ae959f986cbb5329391c38766f8cba75cea6b6d1fb8dbe291089ab`  
		Last Modified: Thu, 25 Sep 2025 22:13:17 GMT  
		Size: 11.6 MB (11607950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343bb45f73f16a36a6c48560ef435c95d6212fb4869388202e2918cd99c2c94a`  
		Last Modified: Thu, 25 Sep 2025 22:13:13 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc3c1b1afd8ada070efe71fc1a156e3f12a1fcb805f098a64966773856754ee`  
		Last Modified: Thu, 25 Sep 2025 22:13:13 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e49a6e09be017f93f23903128abfe500f8b38c08237b22b0da358bceb20deb`  
		Last Modified: Thu, 25 Sep 2025 22:13:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc77c45fe9b1ebff354396809d43282ffaa73979f77cd76a953356e8e2d4b45`  
		Last Modified: Thu, 25 Sep 2025 22:13:12 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dc7dde5f6e6d83bbc9a8512d9642ff4eb8268c1ee1ff8d0857f8826a6c7b6f`  
		Last Modified: Thu, 25 Sep 2025 22:16:21 GMT  
		Size: 25.1 MB (25076124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93cc96fb6db77d2c7cfec4ed59ef927a640688ff84846ad8d3af6d22b90c762`  
		Last Modified: Thu, 25 Sep 2025 22:16:21 GMT  
		Size: 28.2 MB (28225383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f222532d114cac42b41294d5a7d5e1045618c3dadba4b47b4d001aad22b8a7`  
		Last Modified: Thu, 25 Sep 2025 22:16:19 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed356f6eda97b9ea8a2fdb402586101ce92914d40d08dfc4d5a9a2b7fed40a0f`  
		Last Modified: Thu, 25 Sep 2025 22:16:19 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ae27481894866357290f67be9eb9008e84667cbd92c9602913d659dd59ffd3`  
		Last Modified: Thu, 25 Sep 2025 22:16:19 GMT  
		Size: 18.8 KB (18794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44761bded431f3478c6fd210a6cec212cc539664e9cb5c39bdf2b8d1ac4c5578`  
		Last Modified: Thu, 25 Sep 2025 22:16:21 GMT  
		Size: 26.9 MB (26898584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2773ff2cb2fbf4e59d3ac2f296a7404e91d08e66f96739fa362f222aee13ba7`  
		Last Modified: Thu, 25 Sep 2025 22:16:19 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781318c677c5cf68f1840d2777a91cb50eee0d15c8a00390a3155da58e0495cf`  
		Last Modified: Thu, 25 Sep 2025 22:16:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c52d69fd4f132890fe41a55f2ea13f1af599dd16e37eb31d80076da038a14`  
		Last Modified: Thu, 25 Sep 2025 22:16:19 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:96241a50d891661f33b0e3dda477deddfbb7808d42e4e833e89b33486207043d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8540483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98daa7983346b32f844ea8d9f93f321f302228cfc97a50d4fb1be213c5adadf7`

```dockerfile
```

-	Layers:
	-	`sha256:b1c27b204a428497e97e75b94cb55dc71d7383eddf9d1042037769aef2144a1c`  
		Last Modified: Fri, 26 Sep 2025 01:13:38 GMT  
		Size: 8.5 MB (8474974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55078c24eea66dde0ddda894082c693b624b52c37a651e51732a75e6e27a9210`  
		Last Modified: Fri, 26 Sep 2025 01:13:39 GMT  
		Size: 65.5 KB (65509 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0dda702ddc94a4613633d2b212465f0011bdfb989c5438b2cb23724bb0613d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256560497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc01ec73de7a474dba0fb0f4bd942742e92a49db0fbc5fa3445b132848874b12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.13
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Aug 2025 18:29:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
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
	-	`sha256:7e5af67e7479c60288fa69c8c8b72ac4482d63bc9118cf3ca877237788fecbbc`  
		Last Modified: Thu, 25 Sep 2025 21:16:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f428f921a6a7a40bacaeb21d53836334f237fa6bbee3f259d1082ad2be5410`  
		Last Modified: Thu, 25 Sep 2025 21:16:24 GMT  
		Size: 110.2 MB (110162970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d08d3425e0c4ab4defcea53441646d5481bc8b6f85447267eb3ecd42067809c`  
		Last Modified: Thu, 25 Sep 2025 21:16:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d49c24c593f4263dd935659ad881cab6c592981b6cc382caa5ad77960decd8`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 4.3 MB (4302105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dea4e68860d8f48e3855ddfb14df55256db6e7ef482060d43469cdcd9681f3`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b9a7ecea6b93169e90887a56de4aa610479d5ea72acc843ade9a0654dc5fb9`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b04132bc5ba095a3fb498a0d4f6f78c566d62891aeaeef791c533650bde9871`  
		Last Modified: Thu, 25 Sep 2025 21:16:11 GMT  
		Size: 13.8 MB (13811697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1488a73fdd43bfede670135173f60421b26fc8aaeb6ef87baa884ffe43374f34`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a70328b2e495b7fe6b050e0e42c8bd31299d0d73d2fe8b79eadca772ba49563`  
		Last Modified: Thu, 25 Sep 2025 21:16:11 GMT  
		Size: 13.2 MB (13179389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fa006798ba541c4b4df9956cd88c54f4f160cd1e7f76ebaceb6a22031adaee`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6477e00312bd9ac1926d108f8b3982e1509bf0465ed9a0760e89687c8eddd004`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339f6aa7b3c11e08936498a934035ca3609e9fc7ee4786ea956152a3c657876`  
		Last Modified: Thu, 25 Sep 2025 21:16:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ecb6962bb77bef69a898ffb056c55947d4f07f50dfa2c40af6cb5470df007e`  
		Last Modified: Thu, 25 Sep 2025 21:16:10 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5909537cdccac7d58487d069da1aad4c465c4d2c53a7a94081857e6c8b577a65`  
		Last Modified: Thu, 25 Sep 2025 22:13:11 GMT  
		Size: 26.2 MB (26207710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d320a7fc59e1d1689efcb6f36e3c0d19439a7b3b13e6815c8610587584ed88b`  
		Last Modified: Thu, 25 Sep 2025 22:13:11 GMT  
		Size: 31.8 MB (31831759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51713f0f9230d9e2e239667b28ceb7a070022d6707913b4d4c6acc323f91442f`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe06f8c43b7ade63266a9136304f2987165bb59e75eab38af83b322bd3d5bc8`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ab58b36b6451b84bab54cbce00046b963dc79628ae36e6bd047c69bbf0ee7f`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9f196f1649aed12a1ac7ec6f3bb3e24f31b8dbc682991c3a6ac7216d5fd837`  
		Last Modified: Thu, 25 Sep 2025 22:13:16 GMT  
		Size: 26.9 MB (26898587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbcceab742edc6b348b65bee32960f5ce7e84ca813304132a8890cd73517fc`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b69779b397f41ff63cf403108e2dca594f8cc91d64e4374793150469b956e08`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1598e18e862a0207a35b33c37b39076931c8217ba6ad7cc2f2ac72df66c9bd8`  
		Last Modified: Thu, 25 Sep 2025 22:13:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:feee494f7c304b85c10f3b1d2024ee1849914f5364ad783f87224523fe5e4dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8833198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaac0a0a46fe8ce751ac9926bc067d64dc61700a4c89f4f127f2de9262b8c27`

```dockerfile
```

-	Layers:
	-	`sha256:9a6862308e5f1285b37a97e3b932c0e2f2eeee98db64c3063f27616d89d36f5a`  
		Last Modified: Fri, 26 Sep 2025 01:13:46 GMT  
		Size: 8.8 MB (8767627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07af0a8bf21172dfe305377b1981680d728e25279cd9130c119827725c8c623d`  
		Last Modified: Fri, 26 Sep 2025 01:13:48 GMT  
		Size: 65.6 KB (65571 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; 386

```console
$ docker pull wordpress@sha256:f7bf07ab0a56999d4713380bd3ea98375f9d507fc60badb1bac38437ff04efad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265055404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7be5faf14b2f6910a657e0a022aec5961f7decbb7d45ff9e92da71e029cdd43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.13
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Aug 2025 18:29:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
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
	-	`sha256:0e1ae0c5627985338504aa5c5a3da5dfa43509e95461eb4dd22ccd6e573a33a1`  
		Last Modified: Thu, 25 Sep 2025 21:18:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27024cf3d8c9d850eba544bf27890ad79da66ba612ee3a1dcb70ac7fbc2f76c6`  
		Last Modified: Thu, 25 Sep 2025 21:18:22 GMT  
		Size: 116.1 MB (116138259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfe0fd8e12d558381681cbb3d70d4941aa96e4c5e0363849da7dee681884940`  
		Last Modified: Thu, 25 Sep 2025 21:18:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77128a2ec4a422959d5663ee1782d4c330a7ea0723e31657e829d07c0726b724`  
		Last Modified: Thu, 25 Sep 2025 21:18:12 GMT  
		Size: 4.5 MB (4455474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e5779bcf8c82f31ef5f87a4251a32402a26f83154c1e0e2cc01e79e2eda90f`  
		Last Modified: Thu, 25 Sep 2025 21:18:12 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1235b198c88237e63a09ba3e883adacc799b5910b5c0695382346f3d029b2c00`  
		Last Modified: Thu, 25 Sep 2025 21:18:12 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0193137f12fd474e50036eeef9604c34f24966b34196f10f405e0ee58eca096c`  
		Last Modified: Thu, 25 Sep 2025 21:18:14 GMT  
		Size: 13.8 MB (13810943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7edefba7e9fc83ef8628e2417ef8671f1991c7e8517dbfc63f71881881560a`  
		Last Modified: Thu, 25 Sep 2025 21:18:12 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd7ab86eacba7df8405343b52f8b0d2e1afea76f9795f1f716c79f281334266`  
		Last Modified: Thu, 25 Sep 2025 21:18:14 GMT  
		Size: 13.8 MB (13822576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa5a516ba1d81eb970c906ef3ea4b5e17a3690deb54f0e6b87d89509ed03530`  
		Last Modified: Thu, 25 Sep 2025 21:18:13 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacb59d0da81989988fb2d98a5044d133a66627f256e25edb7673629bbe61e18`  
		Last Modified: Thu, 25 Sep 2025 21:18:13 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84a1e6bd3568395c67dc4025fb430d914830b80d7dcd175f7082d20f06b0503`  
		Last Modified: Thu, 25 Sep 2025 21:18:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd245cb034fd40956024a775361345be580509a4aa6f1c37716d305446d79020`  
		Last Modified: Thu, 25 Sep 2025 21:18:13 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731bea4e71c1c9a69c3596700047ee4ffb7ea6ee5e442592135ebd185da9860d`  
		Last Modified: Thu, 25 Sep 2025 22:13:23 GMT  
		Size: 26.7 MB (26747629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da74dd394ee0c36ecbd4f0ad2fc83957f9dd4c9b1688da85e295f7c907ac6cf`  
		Last Modified: Thu, 25 Sep 2025 22:13:23 GMT  
		Size: 31.9 MB (31862523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc128b3f8811e6526fc74807796759309a727c3b8e25bef4fbc540684a5dc9c2`  
		Last Modified: Thu, 25 Sep 2025 22:13:20 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b69d2e2a37f2dda54aec252fafb063413511d866e88800dd353ffec79363b9`  
		Last Modified: Thu, 25 Sep 2025 22:13:20 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77658706b8a130521e9a48808aa1ea62a3b19ce32db60f6e1f2aedb84721e29f`  
		Last Modified: Thu, 25 Sep 2025 22:13:20 GMT  
		Size: 18.8 KB (18790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e96aeda8707594dbafd7f79f07316eb857fd96c6fae77fd80832f33bc548758`  
		Last Modified: Thu, 25 Sep 2025 22:13:23 GMT  
		Size: 26.9 MB (26898583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3118f0333e32cb890fbd262d946f44af582d7bf0dd4846b0b05ada4f0383dec6`  
		Last Modified: Thu, 25 Sep 2025 22:13:20 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cb5dc8687b1d0022fd41529b157da067a4c20249576df20393354f4e654be8`  
		Last Modified: Thu, 25 Sep 2025 22:13:20 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f2da71db65d9d5512b924769c8ad087b56a1ec0533057dffa7eee3553df4f4`  
		Last Modified: Thu, 25 Sep 2025 22:13:20 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:5fd64d11c87b3628a9be60a120738dde0e272ceba255841f12d34963f41e7dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8709390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704938a02e781bb63cbde397c42904ede95e15f284dce6a7c43ca3455e89cd0a`

```dockerfile
```

-	Layers:
	-	`sha256:d2ba0fe0af7adc2a971daf4d973c0d43a814852c498ac2637ff809ff652756d2`  
		Last Modified: Fri, 26 Sep 2025 01:13:53 GMT  
		Size: 8.6 MB (8644125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45db5f501282ea0245a20107516f61d120f07d751dceee18d14b369e835bfd18`  
		Last Modified: Fri, 26 Sep 2025 01:13:54 GMT  
		Size: 65.3 KB (65265 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; ppc64le

```console
$ docker pull wordpress@sha256:2b112761a624058aeab3016bbf77a624bab6e2894a802b7337d90a8922ac3274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262653124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bb8170d3d8192253eeb1a588e5a2f0526b30e44f13070dd58dcce4159369af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.13
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Aug 2025 18:29:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
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
	-	`sha256:744cf91bd2cd00883cc6255a7dcd80f4358ad9fe0c46976a42ce620b34cb2a6c`  
		Last Modified: Thu, 25 Sep 2025 21:22:12 GMT  
		Size: 13.8 MB (13826050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71758e3c62adbaf02e3ac52399762c6b80dee547b2e5069216bb05d5c76b70f`  
		Last Modified: Thu, 25 Sep 2025 21:22:12 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b826fde25bea4943bec52a0337e030840f71d662f53869407f056df3c6bdfb13`  
		Last Modified: Thu, 25 Sep 2025 21:22:13 GMT  
		Size: 13.9 MB (13932160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1484b4d26bbdd3099397f26b838c6c5038cd1dc83671bbaa80108af85c6bf1b`  
		Last Modified: Thu, 25 Sep 2025 21:22:12 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e8ef48540876837e6f27474583c1f97a0404aae13890aeccb3f8a0fe135588`  
		Last Modified: Thu, 25 Sep 2025 21:22:13 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519699f53f1d22d5a828464071714bfc1dc7471ec5747c40211fc7f34ae4aa71`  
		Last Modified: Thu, 25 Sep 2025 21:22:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151780a964eda2c7b86d8a36b54fcc05b6f9c7eb89d941d4175a177a924501d`  
		Last Modified: Thu, 25 Sep 2025 21:22:14 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b776aa968f9e98d13b159118f26cbf78bdade7b9c3e2937797d0de5d3cf1e1ae`  
		Last Modified: Thu, 25 Sep 2025 22:16:04 GMT  
		Size: 27.4 MB (27368737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ff19a119bbea1c719c27edbdd16b4c68024b41abea4e70463c88df3ea9b383`  
		Last Modified: Thu, 25 Sep 2025 22:15:59 GMT  
		Size: 32.5 MB (32531351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a538b807174ad5ca0587cb9fa77cd55a5d4a53f321fed26bce2d17d12e45de4`  
		Last Modified: Thu, 25 Sep 2025 22:15:56 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6caea4a3a84227022c1c43b0fc8b19bd0e2b76797a783ce69eee9eaba2c94f9`  
		Last Modified: Thu, 25 Sep 2025 22:15:56 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2ca8b7ad46fe9a76ec829a441f56328a69b5feff51f3cbd995bfeeea28fe1`  
		Last Modified: Thu, 25 Sep 2025 22:15:56 GMT  
		Size: 18.8 KB (18805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bd6321dc26e2594c52f5ef81b8f22635accc272d4134b8b6556bdddcea8dba`  
		Last Modified: Thu, 25 Sep 2025 22:16:01 GMT  
		Size: 26.9 MB (26898592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e4732fd6c219a43db263ffe23943c2b7ab9ed08fc328ff4b420ed93d222524`  
		Last Modified: Thu, 25 Sep 2025 22:15:56 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c2733e0a887fe8d92a3eaa9301eaf825e993dbed3a732be77ca036bcb9516a`  
		Last Modified: Thu, 25 Sep 2025 22:15:56 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60819fb151269d713baf021860955db07a9efa983ea848f0bb31febea918d40a`  
		Last Modified: Thu, 25 Sep 2025 22:15:56 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:dfdcb34f465aadbc5e270e174f5c5a364af0828b526db036cb68a7e3ef78de2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8737355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a33cb0c6047e1274a55665df0c574412724b93c77057828c18047c4aefa3c63`

```dockerfile
```

-	Layers:
	-	`sha256:d90c18f355c8ffcbca60e0a3092d98183713f98dc14f73d2b73d213454d48534`  
		Last Modified: Fri, 26 Sep 2025 01:14:00 GMT  
		Size: 8.7 MB (8671946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df8f65af6217761d3d80189c339f0a44f4f7bcdc1d5edd6893d4f24d4c2fe84`  
		Last Modified: Fri, 26 Sep 2025 01:14:01 GMT  
		Size: 65.4 KB (65409 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; riscv64

```console
$ docker pull wordpress@sha256:dc9ce08d6da73ea612343d0d10a8b9e23f0f5ed006220d9a1b99e8aedd6ab38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288147850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bdcb1b7b9cba6ef246dc29062217315157072e229a737956f77e8428ab2ec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.13
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Aug 2025 18:29:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
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
	-	`sha256:e28384d8f3d3c86e35f4f70dc1dcadf478208c14301f6f982a30dbbadd318fa0`  
		Last Modified: Fri, 26 Sep 2025 04:00:09 GMT  
		Size: 13.8 MB (13826142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4c277fb1ed04b80320f90884a89b809cb5ada35021e363c72ac0f2bdc27d4d`  
		Last Modified: Fri, 26 Sep 2025 04:00:08 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d657f0ae8daac8c63a8f702dbe4f151f46b8afc195742ba577ad222a525ad0`  
		Last Modified: Fri, 26 Sep 2025 04:00:10 GMT  
		Size: 13.0 MB (12963847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdff283939b95f147a630cbd380281ab3cdea4ec1e9268c8a6e47c46cfac0a2d`  
		Last Modified: Fri, 26 Sep 2025 04:00:09 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4751963d449db1446c4869ac1e4f4786dc961f5dd5bedc9d5520d5d01cb08124`  
		Last Modified: Fri, 26 Sep 2025 04:00:09 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c377a86411758dc3139af067ba64731eee106372e5713738b4b40493a0d14cc2`  
		Last Modified: Fri, 26 Sep 2025 04:00:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e029f359b4a8f4f569a1948564120521f6a7e3af73fcba6bd96d4179ae8807`  
		Last Modified: Fri, 26 Sep 2025 04:00:09 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8456df9d63daf0e617c60da4e94797cddf2d3d1ede854ffcf794e46a60d623ca`  
		Last Modified: Fri, 26 Sep 2025 21:30:05 GMT  
		Size: 26.1 MB (26140012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0769b89137ab9314b30b6e8b588de05dc9471b6ecb0b763d7a50bedb39b16a20`  
		Last Modified: Fri, 26 Sep 2025 21:30:07 GMT  
		Size: 29.4 MB (29412923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe180026a5c0a549cdb474c30eb1309872178d0141334ff3dae9439881f477ab`  
		Last Modified: Fri, 26 Sep 2025 21:30:03 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504160bad3e26df29135169edf8a5191ad21c9d2083e2ea9967e24f94be1458d`  
		Last Modified: Fri, 26 Sep 2025 21:30:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e45126047149b3a2ce6e9a1f75668857e9c74eef01f2118a48e6f83e3a4cc27`  
		Last Modified: Fri, 26 Sep 2025 21:30:03 GMT  
		Size: 18.8 KB (18819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28302f14bfb097350b625b6823ae3586eb6018ab5bc1637a2ddef3c472a92e3`  
		Last Modified: Fri, 26 Sep 2025 21:30:06 GMT  
		Size: 26.9 MB (26898594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428be50ab804abd401fe4761fa4fcf0143c644135278f558b022cf2f457d1db`  
		Last Modified: Fri, 26 Sep 2025 21:30:03 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92133f13b8eb9a7dc1677367ae75603b8a7f8029b4181d89e071720940a749ae`  
		Last Modified: Fri, 26 Sep 2025 21:30:04 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2d286f5af6ff304ea4190f5e40d9b3fe8a1c5c63da99efef2efbc39d91066c`  
		Last Modified: Fri, 26 Sep 2025 21:30:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:a47eef2e4f2aecc2d788686449fa4669502d37edfa99765450b70da243d84c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8807720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c74e397a5fdd733b5ceffd68b8f373ba23e7810bcba0fcd1079c08e92af7a2b`

```dockerfile
```

-	Layers:
	-	`sha256:3f52e263150a0850ff790de4d6eaf034d13ba05f542f3eafb34034044614f63e`  
		Last Modified: Fri, 26 Sep 2025 22:13:29 GMT  
		Size: 8.7 MB (8742311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7ac36f3b9f2be21884283cb16690a49d12489421342cfac611ff26534f9daa`  
		Last Modified: Fri, 26 Sep 2025 22:13:30 GMT  
		Size: 65.4 KB (65409 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.4-apache` - linux; s390x

```console
$ docker pull wordpress@sha256:061bea7e6f9a4949de227ce1f53c37042fc1b52d4f4d1556ec3ad65b340d9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237605647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30217ce86774481a0154c29b42dc29154524d16ec49d8053f2cf274445196652`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Tue, 12 Aug 2025 18:29:25 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 12 Aug 2025 18:29:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Aug 2025 18:29:25 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_VERSION=8.4.13
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.13.tar.xz.asc
# Tue, 12 Aug 2025 18:29:25 GMT
ENV PHP_SHA256=b4f27adf30bcf262eacf93c78250dd811980f20f3b90d79a3dc11248681842df
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Aug 2025 18:29:25 GMT
STOPSIGNAL SIGWINCH
# Tue, 12 Aug 2025 18:29:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 18:29:25 GMT
WORKDIR /var/www/html
# Tue, 12 Aug 2025 18:29:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 12 Aug 2025 18:29:25 GMT
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
	-	`sha256:799e49251db06bfa88532180ba72719b8c91dfd20a29cddfc04d8eca70a83db8`  
		Last Modified: Thu, 25 Sep 2025 23:11:45 GMT  
		Size: 13.8 MB (13825382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031820c920619fa1c0626831a68b867f4b928646c3b1305d7716ff9d7daaef2d`  
		Last Modified: Thu, 25 Sep 2025 22:13:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4e00089358ba2af648a1552c76a741712a2f245a864eb21d4f26c7d40a7c52`  
		Last Modified: Thu, 25 Sep 2025 23:11:41 GMT  
		Size: 13.3 MB (13300089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4024b20919a6651140916ae35aac5368a7b56e87a597ed6609195a24a827669e`  
		Last Modified: Thu, 25 Sep 2025 22:13:56 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364274cd6d20ec2b87cf50f77ae48f96a4f9cb753b0c3a6d8f7becc19d371198`  
		Last Modified: Thu, 25 Sep 2025 21:21:57 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09598b55075952b2d3d6a92abf64b8fe0db9ef238ef7859d9a139e3cbfc7edc9`  
		Last Modified: Thu, 25 Sep 2025 21:21:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c660d24fed8874e852ed9165f6b04e6957f4cf0ad9705e3873041c0376501ed`  
		Last Modified: Thu, 25 Sep 2025 21:21:57 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216a502a50cd3ce006cc8d6574de8c494f0d3a102e97fade7a660f097365444d`  
		Last Modified: Thu, 25 Sep 2025 22:14:23 GMT  
		Size: 26.5 MB (26480990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1113d088b7f8913470c7cb2467da595f777855eab1b00d12d655e0971ac932`  
		Last Modified: Thu, 25 Sep 2025 22:14:32 GMT  
		Size: 30.4 MB (30355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a16b3ac2dfdadf74f55a857fb588bbbf781b1aeca1f1b25d3b4b00f7236c5db`  
		Last Modified: Thu, 25 Sep 2025 22:14:22 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390d744015c94f4029e49ee2c727d1bd5997b131aeafb004246caf65de2516f6`  
		Last Modified: Thu, 25 Sep 2025 22:14:23 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2127722af78c0f2033f8c387f50df0aa73c2bb92f66f94d3bc1ae42e110459ec`  
		Last Modified: Thu, 25 Sep 2025 22:14:23 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e64e9f364cd46d380a67b0704b0fe58ab0111fcaf664597e935dcedbb33fe7f`  
		Last Modified: Thu, 25 Sep 2025 22:14:26 GMT  
		Size: 26.9 MB (26898593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1342b966dd0e4657f104682e96184d389ceb92be948bc46b69ea636291a00fd8`  
		Last Modified: Thu, 25 Sep 2025 22:14:25 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc44e368a45fa56207e03d269cefad3bec9e05770fe92602ecd46da73b8c97d2`  
		Last Modified: Thu, 25 Sep 2025 22:14:25 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff6c329be7b8cbde0378cfb6e6a071a8f2069b2427cce6a4ee041f6f2f3a7a8`  
		Last Modified: Thu, 25 Sep 2025 22:14:25 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.4-apache` - unknown; unknown

```console
$ docker pull wordpress@sha256:131ddda1efe5e8b414f6fcb71d4d8b24c744f9075f11c62ab05b524dcfe3e266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8461046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5898a0467bc7d1040139ca497288a49f0b15df19fbe1a9db3c3f6600069041ed`

```dockerfile
```

-	Layers:
	-	`sha256:16853948240262675a7802fc58dfbaa2ace2a066c68e07bd1bb62fb6087c00ab`  
		Last Modified: Fri, 26 Sep 2025 01:14:15 GMT  
		Size: 8.4 MB (8395727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabd4b4e901bb231a23ef0f7332e1458a02433763d5c29de61910e68ed9f4b6e`  
		Last Modified: Fri, 26 Sep 2025 01:14:16 GMT  
		Size: 65.3 KB (65319 bytes)  
		MIME: application/vnd.in-toto+json
