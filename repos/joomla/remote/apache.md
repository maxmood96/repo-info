## `joomla:apache`

```console
$ docker pull joomla@sha256:67ae6e51960c39cb726a5a153a26cf18799acf1fb4cf7be859c5481137660f9c
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

### `joomla:apache` - linux; amd64

```console
$ docker pull joomla@sha256:57b923a912cb5c6bc6c8fa79991c53ea6d32785322c075f41b89099d83ea3ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278184333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2252b7214594d3eabc92632bb79ff60b7d70a1cf03be2e75823e71b9be88a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24403a1f6855abf71a2a5a1dba8cddf2ea0349dc7034854674eea92699c9d272`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf44d6017a42f5a269318657b7ccbfa56d2604edb26e2eb83f3e602fae3a46`  
		Last Modified: Mon, 29 Sep 2025 23:53:11 GMT  
		Size: 117.8 MB (117836896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489d5e860a704a01205fd1d8785abf1ddf0ce491019435d356dcfb46b0e6fbf`  
		Last Modified: Mon, 29 Sep 2025 23:53:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0248257cbd514fef0ff8dd24148b2bb02026c71d7e556c4303d1b9d24659c56a`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 4.2 MB (4224110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53cf9bf4cf654eb4dd19cf9d43b64ce91656ad39fa8097466095a4f498895d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a139c2f3234a943642d68ca70d513b82aa048c112b042d982dc2e85c56aff14b`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571cfdbe5b25fe605b4725d978af9e7b1e4b3496f859a70d16c882ffe4ee239`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 12.7 MB (12746820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83c968ca9ac96d45154026ae5416c8cb5fd322fda68633488cb4a8d0ee540d`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddb92e888a7073c3bd33d4705beabb1f431e26cf3c0a4e92df38ed3984e036e`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 11.7 MB (11710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b92ea0995b308cac40d1390270e721f26cd786d06a7c0c66774f5c51e23b4`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eed3454c20c841bbe5ca7c5c9c49af8f575ee8c68ed9bcc0dabce47e592d31f`  
		Last Modified: Tue, 30 Sep 2025 00:02:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef78e422f0ecd898f732d929fd9c2c639ec3a4df76cda28e610d73148ec871`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004f06ab2f6c33344882daa271ee4e935f9a3230090bfea11b234bcbcefac444`  
		Last Modified: Tue, 30 Sep 2025 00:02:35 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769dc3eab893dfbb7d9d5b4a6fe8e7b41e319e144defcfa9446840f2edf82996`  
		Last Modified: Tue, 14 Oct 2025 17:55:22 GMT  
		Size: 27.3 MB (27272284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4747c8e3e01984c616128f7d7af6dce88db26b4ac30f4732dd2455b0701e607`  
		Last Modified: Tue, 14 Oct 2025 17:55:25 GMT  
		Size: 48.6 MB (48628195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfd046a9f728653ddf6933f42976533e3795dc6fedf9765081d3debde07fdc2`  
		Last Modified: Tue, 14 Oct 2025 17:55:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c049e8011e0c9d2ee46cd8555c43fb7d1e912a6c600970b0b215fce2008df93d`  
		Last Modified: Tue, 14 Oct 2025 17:55:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cda5602a6c96c039bc24ca4f9c776eb79b583ad644dd8991c7bb631e387ddba`  
		Last Modified: Tue, 14 Oct 2025 17:55:20 GMT  
		Size: 18.8 KB (18802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46042273e0c25dcb9ea753687f618a7efb69847fd303d3ce2ce2ec3aca0f557e`  
		Last Modified: Tue, 14 Oct 2025 17:55:23 GMT  
		Size: 26.0 MB (25957948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17fef7a743311733b59e102cdd77db69d8049df211f6f66b3656f2ec5fda090`  
		Last Modified: Tue, 14 Oct 2025 17:55:20 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2d2bde7b0b54b4e823a43256950acfa801228c703e115b42adbf5c4efca782`  
		Last Modified: Tue, 14 Oct 2025 17:55:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:148329e091880a572d4feaad0da4999e3169267f24107f56f30eb3c18eccf646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76de18aa5fbc4b68d9c4edad898da6da5cba51ca231010f0d61615b1337ded3f`

```dockerfile
```

-	Layers:
	-	`sha256:3e5c0673a769ab1b7a3d37b281e48bb2b5074586ebb69329e75e62b38ab8f73b`  
		Last Modified: Tue, 14 Oct 2025 19:48:31 GMT  
		Size: 61.4 KB (61430 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:137d6344b4ef99280404e07b263cb3b5c5dc7a955c12cec28f5d11154559be2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248736754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c12988da69e9647e1b0326b23cea6d3b81079cb6ff6db2013e91ea6f30fac3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b007bddf6b8df6f16650adcffe0dacb1fee59c744660556edf359b780192847`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec9f6720c7db6210c9d3b519807d2563820d21df82dfc565b3372ea1a03f61e`  
		Last Modified: Tue, 30 Sep 2025 02:14:17 GMT  
		Size: 94.9 MB (94874060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00daafd9b9ccaf8c1e75baacdf7da67d49b411e9cad365bc72976b3923d0287`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cf6a13c90b29503c40921b44fee481f4908ff62c1e04cfcac5e3bf647b1b60`  
		Last Modified: Tue, 30 Sep 2025 02:14:18 GMT  
		Size: 4.1 MB (4082004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15942a0743635d309f04baecca177b081a5e5d9ebe10bb8fe45a62cb8eab7ea`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25c7d84a1b4978754571d6ab5d6d6094c1c94fd14c1ef3135fe73b15d27960`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e686865f0e335c575c8d11f9d1ca90b1a62fe3feacfb65489ed8e675f880dc93`  
		Last Modified: Tue, 30 Sep 2025 02:14:18 GMT  
		Size: 12.7 MB (12744168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4301516f99e0d67bc04ae7a2ed6757d50e1dcf88b63fbfb055f9af8ba3f3060`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fdda99f167dd263c2d6c98893afe00ef998d7e5a121ee771796a0fc00422cb`  
		Last Modified: Tue, 30 Sep 2025 02:14:18 GMT  
		Size: 10.6 MB (10591692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10d609ba2aadf9efb22d675e38a5396acfd0230df487d1163b9cf508c8e4f16`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408963a86c34aa9abcbf45f7c00a3b246c9e6293104aeed1186ba4614d93dd6c`  
		Last Modified: Tue, 30 Sep 2025 01:06:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c98decf8188290ef713653d29db563f34a629d4dd3135361503821507d7eb`  
		Last Modified: Tue, 30 Sep 2025 01:06:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f52ed47faaa6a14ab8e30cfbb5f0e7e7e8a4a72ad00313a9bb5015be5752bd`  
		Last Modified: Tue, 30 Sep 2025 01:06:10 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ef109f94bbc5d06034f67b3875096d18ec89b34e0406addab089177219974c`  
		Last Modified: Tue, 14 Oct 2025 17:59:12 GMT  
		Size: 26.7 MB (26704862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ffecaa80c269203073d3fbe49dd4b57f1d60c99f5d1d0ba82ecdad85526b19`  
		Last Modified: Tue, 14 Oct 2025 17:59:15 GMT  
		Size: 45.8 MB (45805929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6524feff5aba886817583fa2ced4b8efa9d8e7627bd06819676c151908414b`  
		Last Modified: Tue, 14 Oct 2025 17:59:09 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5369341666326cb5fa83e8f1cc6dca5844d5ed72d3d86e950117de1a5418227b`  
		Last Modified: Tue, 14 Oct 2025 17:59:09 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420d6a77540dfdce69733d32317f975c7ebc57fa64325e19db8890f59f577e88`  
		Last Modified: Tue, 14 Oct 2025 17:59:11 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414875afdc753f702ed5e46f254b9a3b0d46b193ef81276df3d7ae0728a1c49e`  
		Last Modified: Tue, 14 Oct 2025 17:59:13 GMT  
		Size: 26.0 MB (25957947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab72fc92599383573e89b57cc4aa4693f7325b13ae3ea7d52576b2fb09a01b9`  
		Last Modified: Tue, 14 Oct 2025 17:59:09 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a47aa1750ce46186fbe7d589b53e431976d07a2ddb0b3cb20d23bd03940a67`  
		Last Modified: Tue, 14 Oct 2025 17:59:09 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:4c1aa9789c08adf647b587286bb37c8df3003b258574cc75c50e55360970d4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 KB (61661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4478dbd0f9d495fab629d0135ceef0696b8a5262a7c45daf69f7fd1e55f80af1`

```dockerfile
```

-	Layers:
	-	`sha256:2f140532d9dbbf71f8614f27c927944f01d1dd900907b09ecb76597848acfa94`  
		Last Modified: Tue, 14 Oct 2025 19:48:34 GMT  
		Size: 61.7 KB (61661 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:2f507cebb76ec4a0f9ef1526ea1b0cfe78f1b22a476c98ea110c6c4f9333b5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234945269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2806fbcddc02fa47943a348c623bbfd3e0b2394e2cf92172ff4e4ade480ea2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce819c84fdcc6e61bb091589a0b208d02d460713f8dbe4d17ff7e33a36f900d9`  
		Last Modified: Tue, 30 Sep 2025 00:06:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f2a554c44d6e229aa4e66a678289311feba8e355071ceb877bbebeddfc4bf9`  
		Last Modified: Tue, 30 Sep 2025 00:06:29 GMT  
		Size: 86.2 MB (86245392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8c1c85f1cb509addb65cfaa888cc0ee1cc9464030eed921f79f86b26ae2612`  
		Last Modified: Tue, 30 Sep 2025 00:06:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fed3ef3e48e7f4952008092af4d10c443bbb5272361bd071535c4f5a289d955`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 3.8 MB (3752006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8b2a3b75024af9d062e6d0fc7eb4d0d02310f1e625b06eb5d3dede683d6518`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99235e87a669e6d891f9f1b299fe4d372a22ceb8d3580bcd8db9b751897b7c6c`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99c8a4b51961d491c0388bcee9534cc4f9fb3e5b48bdf0164ca427bf3b6dc9d`  
		Last Modified: Tue, 30 Sep 2025 00:17:26 GMT  
		Size: 12.7 MB (12744364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da3b510312fdd1495f4f325dcc9d60b71710735c9d1b16ec6046105cc2afcf0`  
		Last Modified: Tue, 30 Sep 2025 00:17:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615652fa79960d0a851d122ed8d0dacecc33ea955d26a2763f9c735aadf30ab7`  
		Last Modified: Tue, 30 Sep 2025 00:17:27 GMT  
		Size: 10.1 MB (10064437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede3576e182c2759883e5d781b08b94eef40e79d722f48e51742d2c6ea3fa1c1`  
		Last Modified: Tue, 30 Sep 2025 00:17:20 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371235052af5ee8f742744b99ee6b4665c8cccde64df8694cc4d1ebec1037038`  
		Last Modified: Tue, 30 Sep 2025 00:17:21 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875d4eaf0bebe7a1fc26cf60b4073d4f97ad5a7aaeadb18e7ee1a851ffd7ce02`  
		Last Modified: Tue, 30 Sep 2025 00:17:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd50e3c95c94cc549fe2c9eaedfd9eda8f83864681d58e09edebd1fbb54ce9b`  
		Last Modified: Tue, 30 Sep 2025 00:17:21 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ea2888a29029150a6f0d7305062838de9f30147a4973981442b961c7a015e7`  
		Last Modified: Tue, 14 Oct 2025 17:57:19 GMT  
		Size: 25.9 MB (25925149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaa187833947b562d521ab1f509586468e6b64498019a45ca7100c335ec68`  
		Last Modified: Tue, 14 Oct 2025 17:57:21 GMT  
		Size: 44.0 MB (44013260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472f37d58d8e7edab02d33a089151c73346a6a1670494bcf350a08f9a87445a2`  
		Last Modified: Tue, 14 Oct 2025 17:57:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00583a3ae7da86cbe432dd40116a5145dbecdcb7da1a13ccf03f90bd888ec86a`  
		Last Modified: Tue, 14 Oct 2025 17:57:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f5ed9af1dafcf15a2b2a36146ec3585b926fb2be1ce5a43891b63c2d8a9bdb`  
		Last Modified: Tue, 14 Oct 2025 17:57:16 GMT  
		Size: 18.8 KB (18799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91e8f20f68e4d108f3ac001ec7c1eb4d6d540997e0dd97e59002e687d096da6`  
		Last Modified: Tue, 14 Oct 2025 17:57:18 GMT  
		Size: 26.0 MB (25957928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef110e3a42b7d5bc764be18b35969743c0e3659fd1e85c10974bfc2299dee902`  
		Last Modified: Tue, 14 Oct 2025 17:57:16 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce10bca697796a1bf35e43b6805530c49968b63be8e2fddbe112913f61d0060a`  
		Last Modified: Tue, 14 Oct 2025 17:57:17 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:bf8e0166338111b274f3ce3218412f1c98280bb5d6d95f71a683100ce38b748e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 KB (61662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de178e60c5ca0f15835369bb10179627b2a241744a668e1bcd04f3d36aaf9a69`

```dockerfile
```

-	Layers:
	-	`sha256:e670e37d0bf6c6f68a0af09cb180416bb62c25d0846fbef354caf06978bc4eb6`  
		Last Modified: Tue, 14 Oct 2025 19:48:40 GMT  
		Size: 61.7 KB (61662 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:a08320f304021f5bd70d34dc152054d0fa9d12cda03e5382028394adac310210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (270035333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2615a835971d16bc91374967a5e7ae742bfb2139efe7aba3858df4498235f89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851973b6a343ab0077a39222fbb197f330af3f3baac41cf4c16e540e0bacc2b`  
		Last Modified: Mon, 29 Sep 2025 23:54:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3e15c58d5a46159d7e7db6ad2dc4fc2c2d448fb83068b448ae4567dab5d9`  
		Last Modified: Mon, 29 Sep 2025 23:54:22 GMT  
		Size: 110.2 MB (110162969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34601830e48af2f62bbcdcac4b07fe37309d94b87f21647126fde17f2ef7587d`  
		Last Modified: Mon, 29 Sep 2025 23:54:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4463658cd639a4198ef13046b43c8b4f4f6b0952cd3a468603e073fe815e52e7`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 4.3 MB (4302065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811c6a6bd7477dace4f70b43011c6371ff86c85fc8c6cf5e0b0edc0df132b9a6`  
		Last Modified: Mon, 29 Sep 2025 23:54:11 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153fdd814bd19b51d736112b47c8d06f22a03e6651aa1ca105e50be69a79587`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6709149993ea5025ee8e0c901dfde1721e77d7c5f7116effc2fe6d97c759d7f`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 12.7 MB (12746428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec54ae0c85d5751887d5b01090b9d4fa4f976f93a85722923b2e3af6d9a008a`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1f27ddd28e39c10f67537e15cde5db0d0d340597422db5164a0de0f73aad4`  
		Last Modified: Mon, 29 Sep 2025 23:54:21 GMT  
		Size: 11.7 MB (11731854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276953c91a2025905ddadb2e06f50f4399da3b6a26b11f1af1d249b405967e62`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b344022137ce53b94f3a09b62a7c181ba64aac768e61cbaf478d5369859e410`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e0a7a670ccb673247f247b6443a1b09a689b77e074097a11608ff7d2c8a212`  
		Last Modified: Mon, 29 Sep 2025 23:54:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf6fb46394fb7c32b3e5e79acf9a6be56e25a4c171e43ab6a7c1941e4c9e379`  
		Last Modified: Mon, 29 Sep 2025 23:54:15 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f582570db714b3dd9e0f5b79ecbaeba42c0fcf6f3ebd7d860b9f5084d8968b86`  
		Last Modified: Tue, 14 Oct 2025 17:57:25 GMT  
		Size: 27.1 MB (27097276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fe9fc48867c79e72e349180688ca1297f148b180f9344a1839db0e06ec5885`  
		Last Modified: Tue, 14 Oct 2025 17:57:27 GMT  
		Size: 47.9 MB (47866024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7303c768028f25d822d25594e11bd3e4dc5fddee00124a04edeba48fd53ec70`  
		Last Modified: Tue, 14 Oct 2025 17:57:22 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501276f89e2b10fc43c61a4f2aa5bc0d6e0d119842e126d63960948649cc588`  
		Last Modified: Tue, 14 Oct 2025 17:57:24 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33432a2b5e4c82d8a7a56ef7ff2e7eab3a936f30e3ed3da4026460b04a6f00d`  
		Last Modified: Tue, 14 Oct 2025 17:57:22 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29679cadacdc6cb0237d3a65d2a368be51b00016ea832d9bba93df77fbeb9355`  
		Last Modified: Tue, 14 Oct 2025 17:57:25 GMT  
		Size: 26.0 MB (25957928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddab1cdb513640604343238d35a4069eb0a9ded2caf6e4df970176e31c3deac`  
		Last Modified: Tue, 14 Oct 2025 17:58:50 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d4538ea3bb06089e48cfe5429cb48f5f5276ba4157672cadb92c54c2ea6719`  
		Last Modified: Tue, 14 Oct 2025 17:58:56 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:1a10cd41efe62981100c26e192827bd45c42c2b4b73387105aebcb6b45203a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 KB (61753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64dc5d6eb77ce336d5297fba280fe7ab340088f2b0f96f7c4d5137d7c80789f`

```dockerfile
```

-	Layers:
	-	`sha256:b7aa83b76952d125afd508511a757a0469474694c9f7adefc0f98e230d37c9f0`  
		Last Modified: Tue, 14 Oct 2025 19:48:42 GMT  
		Size: 61.8 KB (61753 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; 386

```console
$ docker pull joomla@sha256:19e3449d531ac1d2b3892c960d45a9df1851e5c8c4500f8845029dcfbc8a6cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (279025492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44dba5cb3246c51030c090eb1ef3a8388a5909bf1da3e66ed5785de7f2872ec7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9461ff14037e9e86052111a11f5d19afebb2bde96140c152cd47a51979184a55`  
		Last Modified: Mon, 29 Sep 2025 23:59:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e047cbcbd0717bb1b9fdee77e059658d262320e1825b77027d09be649095e242`  
		Last Modified: Mon, 29 Sep 2025 23:59:34 GMT  
		Size: 116.1 MB (116138188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408c02c3bb09142f028ad0ace874d7d7c54e899cb939a467ec76886730f8f27`  
		Last Modified: Mon, 29 Sep 2025 23:59:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a606c239cf33fabf307f998a4e2fc9480a0d231edf41ad4dd748ded819b895dc`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 4.5 MB (4455463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2639cfa6bfdb3e681f4583b1b86d72d112539e52cb432ccc0499c3177a23c7f`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eaf83312b44093e6ea71d00412083eb1143122878954ef3e552c8d643d0c8e`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc0fb7e819ad24f48de136ffaafd38d0355c58414351fad1bdc9b2811a3e828`  
		Last Modified: Tue, 30 Sep 2025 00:03:02 GMT  
		Size: 12.7 MB (12745631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b136f66c4fa025bcb6a67e4a7aefe412b00b8a1ddebafb965f2e63a86f83c7`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e82924a158381d19f6dc867fb0196ce0b10b8d977d7d10575a1306920be159`  
		Last Modified: Tue, 30 Sep 2025 00:03:03 GMT  
		Size: 11.9 MB (11917023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ab55cd62bb1fba68c5ee47e142cc1fac4ded15c96cce866cc62cdf6517864d`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd311e28774a48264de7a45fcc2871b00c681707f06033156062f33f820238`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917849e8458de58339fc3ae90b713cad4f232b8eddc1521015aad80863f7ff77`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf5cf0346847a23eb573c07f9243fa8c3570c7c3a4c172734de39e9ffa9778`  
		Last Modified: Tue, 30 Sep 2025 00:03:01 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0696b9f6530541785c3e5eeaeb3b84c90a49bae8ff846d3570e7d659169078`  
		Last Modified: Tue, 14 Oct 2025 17:57:14 GMT  
		Size: 27.7 MB (27713921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0597cd0221e1a9577485240393d86ab07af2ea8c7a95826a9ad76259367323e9`  
		Last Modified: Tue, 14 Oct 2025 17:57:16 GMT  
		Size: 48.8 MB (48772808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ddc4de8d2382d1ef15d99f4835887195bf17055eee76406b85a7e551579364`  
		Last Modified: Tue, 14 Oct 2025 17:57:11 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d0c1604cfbb4178273ccb1a97b92672f8cbe743580076c1fbf5988465bbc28`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75272c835b3267aab8d44f97d6aa2f00318c8f73a8322da92de92a38327ba3c5`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f719e4d5815a774856792cf2271fde807785dbf263acdf63ef8ddda58ef859`  
		Last Modified: Tue, 14 Oct 2025 17:57:15 GMT  
		Size: 26.0 MB (25957962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4acb77c72bbabf7bc08bd04833e04531b4b2200417afca9476f74b62ed1c77`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a628de3cd03a245a40c9c8e0e513c658dd3e7d5d04bab553a8479a36142e95`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:f5ac1b4798957a443a5d7c7cbc684a8fe6071eb9a3f7d70cf97eef09f937958e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a28dd6858182a65e84ed26faebb8a95b88d5a10251e2be16a63f3f68f43934`

```dockerfile
```

-	Layers:
	-	`sha256:72871a2ed82bef893812e70bbd16499ea3a51ab826c2d5d62cbcd8d5891d30ac`  
		Last Modified: Tue, 14 Oct 2025 19:48:45 GMT  
		Size: 61.3 KB (61327 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:2cab3822f937a2b34185187bf57644193ee9cc4f22e9a181ec64b36ac8ddf793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278009053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79554c60b0989d0a22c545a2f957d4e26d1e52f0a960011b3742c0220e8960c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d8f05f06dc824d87111df6e83c98b44d4b30120744017674fa115b47c2dbe6`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75015a3f4b08f0357c989a4c27950c8a6de956a67874e0df0e8876482f1c6285`  
		Last Modified: Tue, 30 Sep 2025 07:16:10 GMT  
		Size: 109.6 MB (109597733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbf93152fe00ebb17d96bb0b9dce5763e9ee0f645695274ef06bcf783421bd`  
		Last Modified: Tue, 30 Sep 2025 07:16:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cdaf3986afeff98ab8e26d5054958a0fddcd91c28e37dfca6c9bd1937c38c1`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 4.9 MB (4875653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd3405d5eef9a007a25174bf4a788fce2a6cb8f4d2a07d35b2433b2d1d52fb3`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0d88f08b4ee89f9ccb3d82e7e8a74e3a33d00089433c4500c8c0bf24c522e9`  
		Last Modified: Tue, 30 Sep 2025 07:21:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77edc343c916403763589f847c954cb7307d1ce3a5ddd81949086c26a528303`  
		Last Modified: Tue, 30 Sep 2025 07:58:17 GMT  
		Size: 12.7 MB (12745895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e900f713a9f47d326b39e139b7d0e403be4974d90260ca685f97fd170c0318`  
		Last Modified: Tue, 30 Sep 2025 07:58:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b873839233b2b57c86a027faf3ceb57b066bd95e5ecdd25e85ae6ed114089cf`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 12.1 MB (12116907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055d60b33f5e4a67049ceb0ec372674ade80bd1fcaa40a4d1cba22e7328173a`  
		Last Modified: Tue, 30 Sep 2025 07:58:15 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5520a113744694808a200592d73e60ac4e0b161e0574d6e20ced25649fffcf`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9265b962f01c977332d57f7f8969ae776bda0156ff44343163bef8a1327019a`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cca64b19960a3ef677a3543ffed63c42782da3b2b81b0594e8c8c286911710`  
		Last Modified: Tue, 30 Sep 2025 07:58:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad41ca95256e19bce8e0fc4e9fc043bd467ca450cb6739254194d33afa4b05c`  
		Last Modified: Tue, 14 Oct 2025 18:00:54 GMT  
		Size: 28.4 MB (28417569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1a0f1a33931a91d9f53242838f9fa0bcaa01677cc921ae67d1e333c266d45c`  
		Last Modified: Tue, 14 Oct 2025 18:00:52 GMT  
		Size: 50.7 MB (50668915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d81fe044fd25eeda66a434dfc1bbb37f271848a551b51d20bf261f94fe4fd8`  
		Last Modified: Tue, 14 Oct 2025 18:00:54 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5588664ab0304de145cce5d50d3541ca044a5f5d2367fe0e4abffd1e96f588`  
		Last Modified: Tue, 14 Oct 2025 18:00:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f710fd91c9a96cbef117b4f5ca91e3d6f34fc86c3bf087f2d556c24e662a81`  
		Last Modified: Tue, 14 Oct 2025 18:00:56 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9365b078517ea4f129d2248bca10ce5150f461369221e4bb8ffe7fc09bd2c5`  
		Last Modified: Tue, 14 Oct 2025 18:00:51 GMT  
		Size: 26.0 MB (25957958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f58e86bac8198d37bc46956c5161aa570f015c9810d6313278bf683443bcd2d`  
		Last Modified: Tue, 14 Oct 2025 18:00:46 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2281d57eb1b2b83f86a10de8c845ad20fc72dd90608f53ac095580cd9347aadb`  
		Last Modified: Tue, 14 Oct 2025 18:00:50 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:9b267d0e216d4615765d2eccaeb0a91666d34648170e6e43ad5c5f41a4647338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e92fa3f30feb457463580ab6dafc1395ea3f250648d6c3e02dc4bf2d16d118d`

```dockerfile
```

-	Layers:
	-	`sha256:8cfe28681d67919b43de31ce2c6a1daa0fb116ac2c89bf4715b1e967e7cd7f92`  
		Last Modified: Tue, 14 Oct 2025 19:48:48 GMT  
		Size: 61.6 KB (61554 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; riscv64

```console
$ docker pull joomla@sha256:457a49d27376caf8203652e9807c76ca8a8dc6d5cd65fc376b0f182b1f98f9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (311976474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d207bef6a7f41d6fd9bbd425bcd69a46505d303ec4ae973a0124e348209f8797`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e10c25f1d43bda19fe1addca79e55bd60680b6683c485853db1be0763dd7e2`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03438fb8247e71c15afcd0508b678af32b8a41a4cd64dda788e8224b32557902`  
		Last Modified: Tue, 30 Sep 2025 15:10:17 GMT  
		Size: 146.6 MB (146579364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df117f051d654fe662d0af341155be2d955517920079566410cd20daddb0a237`  
		Last Modified: Tue, 30 Sep 2025 05:07:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5820c12643e6a3e49d793483aa7a8f0fc043801a3e3d7085a78a2243ac2efa0b`  
		Last Modified: Tue, 30 Sep 2025 06:10:09 GMT  
		Size: 4.0 MB (4026042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13195b106bcebf839d7af0f2269c2a442a10e9e41e345d562397fa27f3d35f90`  
		Last Modified: Tue, 30 Sep 2025 06:10:08 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627b6eeabd2d7dec5e31e065537160dea1d3126b8ca00665c8bbb2aaace9b070`  
		Last Modified: Tue, 30 Sep 2025 06:10:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fe47ae8b684f5caeb83d9cd67cf89fdf0fc2383d69dbbac08c501112421d9d`  
		Last Modified: Tue, 30 Sep 2025 13:56:17 GMT  
		Size: 12.8 MB (12760793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9facf10beb33f09907f6b28f68613d3c5682c3f7151f216c385f6b0cedb93bb`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80438ff315a32555c89c6a436108b19441c75de91f63e5823891962a8f82816`  
		Last Modified: Tue, 30 Sep 2025 13:56:17 GMT  
		Size: 11.2 MB (11247976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f213298c7495f6f0834e5d36e2cedbe5ad94734747b1198e341a8662caeeea`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ff4b32a0686b241a5f4d73f6b49f274047ec58fbce1293bb869c960995bf5e`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c424c4b576c259db3f48b1e583c6c162559f9c547b2455e798a14f97ec49586`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8768d29dbe1389096ac1264e963a24cda78ed7f1a04ded93bcf27ba00553da07`  
		Last Modified: Tue, 30 Sep 2025 13:56:16 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d4d21955e49dc4a8d7a0c4da4debf0038b7e4e1fad881087545df3a19d728`  
		Last Modified: Wed, 15 Oct 2025 08:15:34 GMT  
		Size: 27.2 MB (27206422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062d85cf451df1977a0faeac0c99e037e1d0a408e2fe21ad41d14effa5d31894`  
		Last Modified: Wed, 15 Oct 2025 08:15:37 GMT  
		Size: 55.9 MB (55892362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620ec0db517a094e303e174b6e521927ed7d7666482bc4fc2194161a5047270c`  
		Last Modified: Wed, 15 Oct 2025 08:15:30 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065835a589ca14a2e976e79e38201d5ef2764a13bfd615b468677b4365d74da2`  
		Last Modified: Wed, 15 Oct 2025 08:15:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e911fd4c03745b336e8ebd4a85c2e65e985695459419c20e17341a39b4ec381`  
		Last Modified: Wed, 15 Oct 2025 08:15:30 GMT  
		Size: 18.8 KB (18811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd390a1a4b1771e6c76f88419bf2c6c594f5c94bf9343e1c031c62a2c0f39244`  
		Last Modified: Wed, 15 Oct 2025 08:15:31 GMT  
		Size: 26.0 MB (25957997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898c74472e7515706c903692805f379b51e6169cc16e24f601a1ceee83b48955`  
		Last Modified: Wed, 15 Oct 2025 08:15:29 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3aa90dfd386b262c9c32a429362d369a2bbcd630f3dbdd98ed399f0e14c38`  
		Last Modified: Wed, 15 Oct 2025 08:15:30 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:345938b55fc23b596704b7dec5e140a4c5877a27a99b27d557703df1dc4ea64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef41e1b6a0d4b912d24123ac5b782a8dc158cdb0476138a1af8f2b11505678c`

```dockerfile
```

-	Layers:
	-	`sha256:75a4e4a477360948cf7c4116a6c9368e9feb91607eb6c46b5308b39a158c03cf`  
		Last Modified: Wed, 15 Oct 2025 10:44:15 GMT  
		Size: 61.6 KB (61556 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:apache` - linux; s390x

```console
$ docker pull joomla@sha256:6bbc820558a3d7eea6ba951fccad313f67cd293ac8fdfc6a407208eda8060b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252366765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c434c9b1f7caf220e20cb05ed43d1b4b6217acfede5f45d8a47e75a29a00ae2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 25 Sep 2025 23:53:24 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGWINCH
# Thu, 25 Sep 2025 23:53:24 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[80/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["apache2-foreground"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9ee178226f7ea0f482af09b7dc3ba5fca7c07de96e60ad828b1737709e6b19`  
		Last Modified: Tue, 30 Sep 2025 06:40:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b8c6f589e7cb0b9aff90a6df6a7cccfae60ed23d9fc4328b15d0c44aa0266e`  
		Last Modified: Tue, 30 Sep 2025 06:40:25 GMT  
		Size: 92.6 MB (92564454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674ff7c7e8a7de8708af6056d40b56dffeb3ae246f618226bf482e0f207ff014`  
		Last Modified: Tue, 30 Sep 2025 06:40:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a4110d360212ee6e0ff8a1ea6d731b2aaff510a71163b8a748a26aa60e590`  
		Last Modified: Tue, 30 Sep 2025 06:44:29 GMT  
		Size: 4.3 MB (4320480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763509a8474369ab3c7c1528f033ff966ec368402debfbc88d137b2f4ab19403`  
		Last Modified: Tue, 30 Sep 2025 06:44:30 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d5e9b63e43b1a0a70264c4610e6f5dd857a8d5245e08b172e026ecb396e1a`  
		Last Modified: Tue, 30 Sep 2025 06:44:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b259324a65e330e9f681f2e5950782f713b110e2c10f3e934bc47fba2ea0547`  
		Last Modified: Tue, 30 Sep 2025 07:17:16 GMT  
		Size: 12.7 MB (12745179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5834b2d85fe4a101cfbaae2ec80c35f43d1e594bc2293aed80a7db76d728c6f`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c9b48987db0e93fe5b9be24c82dbc5be2514ebe7a66969ee6803bafe88c25e`  
		Last Modified: Tue, 30 Sep 2025 07:17:17 GMT  
		Size: 11.6 MB (11562688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73636a81b76033d489c97758e9dc4c95e764ed93efef24e9b994f4cea791bbf`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b82e61548fe1c152e7c3145740867ca12096eb1ee3e589a8e098707eea008d9`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4577b80535eb680a848be96af4451818cedcad81c4842724f7b7ae3f13179453`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410955c39f3e9374ffd55640d3f06a79d6408368f4bab4423a5f6630d5adde5a`  
		Last Modified: Tue, 30 Sep 2025 07:17:15 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0673608f0839c1a867192ae64e095cf4a564dc85cef98ae1997a450cd8361a9`  
		Last Modified: Tue, 14 Oct 2025 17:56:29 GMT  
		Size: 27.6 MB (27551472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829455fe0d2d517051bcd64ec754dd1ba26fde41699f2a154852b96d95ee99ad`  
		Last Modified: Tue, 14 Oct 2025 17:56:28 GMT  
		Size: 47.8 MB (47797355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60feb6c7fd1f5048886078bcbd2fcd4f39f821ff0db24d356d4161b48d7a98ff`  
		Last Modified: Tue, 14 Oct 2025 17:56:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b624e0e105ae1396faeff06608dae932aabe31f30e400921bba76af8cf1296fa`  
		Last Modified: Tue, 14 Oct 2025 17:56:23 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b642bc15868794ff3ab066f1d5943bf372581a31fa883db276951ca3d7763ba2`  
		Last Modified: Tue, 14 Oct 2025 17:56:23 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7949ca521bbe258133a7fe072945d886a5b513be3b4aefaf8dd56d1a488218a8`  
		Last Modified: Tue, 14 Oct 2025 17:56:26 GMT  
		Size: 26.0 MB (25957949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f756556e4f74df1ed06abe0574b605bf010f05c32c97258ea848cb3db77ae62`  
		Last Modified: Tue, 14 Oct 2025 17:56:23 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37a6b7b4f1478583c37337887b3ee19eb23fd47a84a0069a790ebc0f9106c02`  
		Last Modified: Tue, 14 Oct 2025 17:56:23 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:apache` - unknown; unknown

```console
$ docker pull joomla@sha256:fd5c77632184b4881be7a746c4bd0597479f1a53b30eb704a95fa5a8ac3b132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fef635e6ccf3382dae89aa270ba03b47d4f075bdc7e5d99dded53dc19ca0f7`

```dockerfile
```

-	Layers:
	-	`sha256:c31696c88f7b80f21e9a8e9ff7ccc57207f74b2c3e1dad1506a74309c67b8ca8`  
		Last Modified: Tue, 14 Oct 2025 19:48:52 GMT  
		Size: 61.4 KB (61420 bytes)  
		MIME: application/vnd.in-toto+json
