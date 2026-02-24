## `joomla:6-php8.3-apache`

```console
$ docker pull joomla@sha256:f076b0f4b65335e0fe0ab6e214ca70007025e2847be2a9e347e5cf2f7c28d824
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

### `joomla:6-php8.3-apache` - linux; amd64

```console
$ docker pull joomla@sha256:f9a146e274700aa6dcde539a2eedfe07047815529d07839d590bea6e37bee596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275077982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fb0f24ecbd9a13c611f5517d65d5daeee1dfeced45341a89d41a608e1e45aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:05:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:06:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:06:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:06:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:06:11 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:06:11 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:06:11 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:09:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:09:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:09:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:09:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:09:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 24 Feb 2026 19:09:29 GMT
ENV PHP_VERSION=8.3.30
# Tue, 24 Feb 2026 19:09:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 24 Feb 2026 19:09:29 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 24 Feb 2026 19:09:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:12:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:12:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:12:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:12:14 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:12:14 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:14 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:12:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:12:14 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 20:08:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 24 Feb 2026 20:08:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 24 Feb 2026 20:08:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:10:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 24 Feb 2026 20:10:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:10:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 24 Feb 2026 20:10:40 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 24 Feb 2026 20:10:40 GMT
VOLUME [/var/www/html]
# Tue, 24 Feb 2026 20:10:40 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 24 Feb 2026 20:10:40 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 24 Feb 2026 20:10:42 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 24 Feb 2026 20:10:42 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:10:42 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 24 Feb 2026 20:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:10:42 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d966da89514aeb6d7666fdca4df0cd99ad75f161929d7cbc15826c02fcc35373`  
		Last Modified: Tue, 24 Feb 2026 19:09:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b6b15c3457a8569197ab6c992509ef2dd3f1ab8aededb4b8e8c9d116ccb4df`  
		Last Modified: Tue, 24 Feb 2026 19:09:17 GMT  
		Size: 117.8 MB (117841801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e74fa77754e47de793d3a4fc8660d2a376d2269668776d42efce6900f2c0d6`  
		Last Modified: Tue, 24 Feb 2026 19:09:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9a88b46c717f754acf02ed6830c329b4f4d276870e634b22be9f105774fbf9`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 4.2 MB (4226864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb68688d83719e647806fca2b0356d064f1f75ab63839954a8e70c38da2117`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dd0a7d60555f5999aaf4fce5ff8c9821cadd79d8862b9a6005348d9c20d869`  
		Last Modified: Tue, 24 Feb 2026 19:12:24 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f40ee734f4a27b7b6b1a86a5cf0ff75011b7b1c52c87e21ea6c067783d2acb`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 12.8 MB (12774699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f1b0890dbe87cd4de1159070879fe86c66e595b4db7cceb8502e3b223878e0`  
		Last Modified: Tue, 24 Feb 2026 19:12:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27442454b736d435aa833e821f9e8859b21037c94aff514c8f3b4a14fd028f40`  
		Last Modified: Tue, 24 Feb 2026 19:12:26 GMT  
		Size: 11.7 MB (11714140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f532b20dce6d81fcd16d3d16b8e3780d99addb335fd9d3b2efb8dff27cc47dc`  
		Last Modified: Tue, 24 Feb 2026 19:12:26 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6480a7139c3d9bc67c77380c129faa3bd0e97234510ac25df7cbe0099c9ba6`  
		Last Modified: Tue, 24 Feb 2026 19:12:26 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197481443d563e4de23a7998a620c6c1747ae9752cff4954da32dbcdba07fdb`  
		Last Modified: Tue, 24 Feb 2026 19:12:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735e906fddd9e869318cc88bbac37d13da8917774ef58cc45950af43c96a69e7`  
		Last Modified: Tue, 24 Feb 2026 19:12:27 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1452fb1a325fc48db7827c839ff07958deedd4c48b21a1f668ac769bae352b1c`  
		Last Modified: Tue, 24 Feb 2026 20:10:53 GMT  
		Size: 27.3 MB (27273501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f425141d48bfb3ed6d0f1e0e81ac58566d2aa57e477b3e34cda2aa374acf477f`  
		Last Modified: Tue, 24 Feb 2026 20:10:55 GMT  
		Size: 45.0 MB (45010148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73817f4d2683276917b02ecb03970b83502ed244b7e9818f92cd7e330c9d31f`  
		Last Modified: Tue, 24 Feb 2026 20:10:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86af417bea98c0563ab8f458ff3244e96c869c2be043105bfd7edf98b3fd9da`  
		Last Modified: Tue, 24 Feb 2026 20:10:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eaf80a67de0f49c1f007a711b317d7b2131c46694a9c22dc36c2d45c544c12`  
		Last Modified: Tue, 24 Feb 2026 20:10:53 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dc3dc10adefb7353fb08bf9bef46adcd2b81b6bfe958811a3731204052c6e3`  
		Last Modified: Tue, 24 Feb 2026 20:10:55 GMT  
		Size: 26.4 MB (26428224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4b8184215ba57bd306db7a46c9cc9b21c693313b62a5cc91ef0e2d33b732a2`  
		Last Modified: Tue, 24 Feb 2026 20:10:54 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbfe753ed6db428f53f21d073e1e2f131fd48ffc556e41a6ae7270edc94e654`  
		Last Modified: Tue, 24 Feb 2026 20:10:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:521d7361aab09991e8fff4d5fed192b9b36f85edcee6a78754f3839a1ad38e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 KB (57781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7caa8b1ffc73887730b30329ef54c74bf2eb74ca7094d69ee6b7125ae5cf19`

```dockerfile
```

-	Layers:
	-	`sha256:2526e6f91a5c8adbd6bf73e0896bc3bec5643a3b3347cc344b4e17a54e6e2c71`  
		Last Modified: Tue, 24 Feb 2026 20:10:51 GMT  
		Size: 57.8 KB (57781 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; arm variant v5

```console
$ docker pull joomla@sha256:275a4166a7647352442303b0792b5a00831f93b2d8a4fed988704e6868685fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246237992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d545470714f3a1456e8e5afd4ac595de6f827f6f8c05ba1a5f492e571be7b5ea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:32:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:33:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:33:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:33:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:33:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:33:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:33:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:43:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:43:41 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:43:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:43:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:43:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:43:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:43:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:43:42 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:43:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:43:42 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:43:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:43:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:46:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:46:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:46:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:46:55 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 02:46:55 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:55 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:46:55 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 02:46:55 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:45:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:48:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:48:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:48:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:48:29 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:48:29 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:48:29 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:48:29 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:48:31 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:48:31 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:48:31 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:48:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:48:31 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3469a6f7e7af0ece3eb959807f097cfac2fcf3d8c0d94eced1d162ba490b1d`  
		Last Modified: Tue, 03 Feb 2026 02:36:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5732d3819fdb18427561fefe1696521d9d8449e56f8b248dc6d5a3cc26505500`  
		Last Modified: Tue, 03 Feb 2026 02:36:54 GMT  
		Size: 94.9 MB (94876516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129f4d4d08b10c75a45b4cf46d7ca700f61d4c7d287da21ab98faa80889ea4e6`  
		Last Modified: Tue, 03 Feb 2026 02:36:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcab8853e1f021748a3ecea5f1a8f06b3e1748945f2b8d7091d6a4264b36fa`  
		Last Modified: Tue, 03 Feb 2026 02:47:06 GMT  
		Size: 4.1 MB (4088944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a18a3cb92696d399d2a6c93e5c889753866d5e5e1e021d1046b69682e946446`  
		Last Modified: Tue, 03 Feb 2026 02:47:05 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910e116f2a276ed55ee5d15562f12cd612f32dce57a82865bca14a38eef018ae`  
		Last Modified: Tue, 03 Feb 2026 02:47:05 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d57791b0c9ed06b3296bc04de6be67e2068035db05dcde4cab707dd2995279`  
		Last Modified: Tue, 03 Feb 2026 02:47:06 GMT  
		Size: 12.8 MB (12772213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b8cd13b6e5cd4f69c4f86a3276aa17b2a794dec2a19501b1c6870d47a0344`  
		Last Modified: Tue, 03 Feb 2026 02:47:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781276a1024dc516dc9e10776164aa91ac113c5e9b613060d43eb4b90145425b`  
		Last Modified: Tue, 03 Feb 2026 02:47:07 GMT  
		Size: 10.6 MB (10600781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a3aa9f42994a48d33727bd9f190a75ec773efb12223d1d52fd3ebd87fb4800`  
		Last Modified: Tue, 03 Feb 2026 02:47:07 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b87f1c788fe0a572fd0024e256aa1d66ed7b85b17be451b47a2607f5fec94cf`  
		Last Modified: Tue, 03 Feb 2026 02:47:07 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a820f2af3222caaac89494605695bb6b261a15840d27796e73cfc116928728`  
		Last Modified: Tue, 03 Feb 2026 02:47:07 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef40db451294a28ce4e59acb4ea54af73c576c964dba2f665271e4b2bb69c20`  
		Last Modified: Tue, 03 Feb 2026 02:47:08 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf28366ca71af4a66cbdfad8feec8b2eea606e5317d1c073f7b49f76bcd389a6`  
		Last Modified: Tue, 17 Feb 2026 21:48:41 GMT  
		Size: 26.7 MB (26706209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd18f17dc96d388b6ffde75d264d8431f2294ada562e5b7941c16dfb98ad200`  
		Last Modified: Tue, 17 Feb 2026 21:48:42 GMT  
		Size: 42.8 MB (42787597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550fd3bce3b50bf5e80f4ab63df58544c48a8ffd4f9a34aba5082c85445f9ba1`  
		Last Modified: Tue, 17 Feb 2026 21:48:40 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b76d2f2885e14bb4f2f09478642ebc5203a1693c03f56425dff6faa98bcf07`  
		Last Modified: Tue, 17 Feb 2026 21:48:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f62508f4e158a8efd961980ddbd5858405707ce97f8630a536a22f730acf73`  
		Last Modified: Tue, 17 Feb 2026 21:48:42 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63ad5cd7ec47f8f15c198a1cfd9014a9c266765f57002f5ed7d21eca45adc04`  
		Last Modified: Tue, 17 Feb 2026 21:48:42 GMT  
		Size: 26.4 MB (26428203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9419726bac6dca1ab79e0acb97f3bb3b07a850921f6dcf30b6bc82b3228ce79f`  
		Last Modified: Tue, 17 Feb 2026 21:48:43 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4799be1864c8cfa67313617f725eae6726ab7b22ab0614e39c032ed103605fd`  
		Last Modified: Tue, 17 Feb 2026 21:48:43 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:59c48fcd60f50d06f5bcee5863a6d63873dd007b6deb43b8d26a07a466f1f3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 KB (57917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cf180ec78f166a115b67cf53b2f3aeda6441fc33fe52af20dc80591ae0e351`

```dockerfile
```

-	Layers:
	-	`sha256:2be626f34f8b1aa49948ed73402e1f5f0b39ed563b951e60fe097cdb438d45e4`  
		Last Modified: Tue, 17 Feb 2026 21:48:40 GMT  
		Size: 57.9 KB (57917 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; arm variant v7

```console
$ docker pull joomla@sha256:ef26ca2ae1f3ce0e11435327a25a3fb2fc73f4eed6d50bc64d99bc05774207bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232667460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9a5d76dc41444f3756a6d4e2474d432d9c49fb449ef9af702e7258166046cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:47:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:47:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:47:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:47:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:47:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:47:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:47:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:47:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:47:47 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:47:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:47:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:47:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:47:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:47:47 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:47:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:47:47 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:47:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:47:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 02:50:39 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 02:50:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:50:39 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 02:50:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 02:50:39 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:48:22 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:48:22 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:48:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:51:13 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:51:13 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:51:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:51:14 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:51:14 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:51:14 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:51:14 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:51:15 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:51:15 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:51:15 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:51:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:51:15 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c53cf40cfa3886cbac0bc230c216e03c8ac64000f77d7ea45738e22d62a962`  
		Last Modified: Tue, 03 Feb 2026 02:50:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d4c21244042087a79690dc6f9cf23337d31f382f8463dbb078081fb5b5b452`  
		Last Modified: Tue, 03 Feb 2026 02:50:59 GMT  
		Size: 86.2 MB (86244734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6f8201d1427d63892435e218f96fae71e7106c1703a1adefe636dc2495c1a0`  
		Last Modified: Tue, 03 Feb 2026 02:50:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aec42d91782302900b9a04b78afdf3302af59874ea775116d061b737d0dfad`  
		Last Modified: Tue, 03 Feb 2026 02:50:56 GMT  
		Size: 3.8 MB (3757582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1455de9446a5ecfeb925a315b3fcf01d95aac69ca79f1fd54fa26489bcd7a217`  
		Last Modified: Tue, 03 Feb 2026 02:50:57 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1701fafedf1a21621b44ff2d6f3d58a66612a39b3ef61d07925be67f6acb26da`  
		Last Modified: Tue, 03 Feb 2026 02:50:58 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0496492fbe08601ca13c49e554f3ab33afce58d34bdb4b8e4a8feb8648390`  
		Last Modified: Tue, 03 Feb 2026 02:50:58 GMT  
		Size: 12.8 MB (12772348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef5e5fb1c6105c09542a36af5352c4bb96c1c93db70430400faabc96931af1c`  
		Last Modified: Tue, 03 Feb 2026 02:50:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a2ee553923dc8f5409d6b48af843fce34939245216f5025a9e3d1c7fcfc668`  
		Last Modified: Tue, 03 Feb 2026 02:50:59 GMT  
		Size: 10.1 MB (10073021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75bcfe401293c8efa196cc0a2cc9cac1409f8a9a3e2f45a3d21f73667fe4555`  
		Last Modified: Tue, 03 Feb 2026 02:50:59 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3c228f960f595a42c4af9505a3a4cebdb112d874131ed36f3526a6245105a2`  
		Last Modified: Tue, 03 Feb 2026 02:51:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed433bf5097c12900e96610beebd71c246e57449d45833972c61e1737e120dd6`  
		Last Modified: Tue, 03 Feb 2026 02:51:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be3dfdce01c82ed949189814cae1ca191bb57dd1e77d544a9204d10756513a`  
		Last Modified: Tue, 03 Feb 2026 02:51:00 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fac048bc40973b44de806edf4b1d4a8c61354a2ae9c094276725daffe7b7599`  
		Last Modified: Tue, 17 Feb 2026 21:51:24 GMT  
		Size: 25.9 MB (25925790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c185424478796d97f5699123aeeee6ea581420f1af7f2e3762e5c7090a7adc`  
		Last Modified: Tue, 17 Feb 2026 21:51:25 GMT  
		Size: 41.2 MB (41222060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b12817313220152d4a86786640a65616b6b81352ceca5221eb30954aad82f`  
		Last Modified: Tue, 17 Feb 2026 21:51:23 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4936926f1c1bc2e1235a0a5366b5b2f7317c1fcb3220a940280385c429345d50`  
		Last Modified: Tue, 17 Feb 2026 21:51:23 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d759c6b6ef7c1936a7d62e3b6a2bdf4ceed59e24fa9da73babc0bf112830ba`  
		Last Modified: Tue, 17 Feb 2026 21:51:24 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a755ba28b50f462ff205ba08f3e56365277c8943235baed6b6657a313169470`  
		Last Modified: Tue, 17 Feb 2026 21:51:25 GMT  
		Size: 26.4 MB (26428213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ddb457f41d98d8ad05aadbcb115a4805674024d1521908ffeda2beaca1b7f1`  
		Last Modified: Tue, 17 Feb 2026 21:51:25 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24fd36b833590c06f7d6aab1a8edc7b444778245f781b3a7d93b9a6a2e5cdf8`  
		Last Modified: Tue, 17 Feb 2026 21:51:26 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:20e9d1e8fc4f7646a9dbbca70a170bcf4bd7a63d76caf5c1f53b902b9e28a7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 KB (57917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dcf2b5cdc8a1ef46d650445b15655e1ec79a91285e6f734ba4fef928b342f71`

```dockerfile
```

-	Layers:
	-	`sha256:957348cf6edb7b5a0a295a0d476e91c0e7c07a7e36703353fa9eb9f9d6b0702f`  
		Last Modified: Tue, 17 Feb 2026 21:51:23 GMT  
		Size: 57.9 KB (57917 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:93acad9e5ac8514ecab1ec3504ab940fbed3a6d4b868575c7258ea8853c9491b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266592960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58cee178bf12041c8d89aa37826402625fc0d017b5b2fa3786ab066e931e31b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:09:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:09:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:22 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:09:22 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:13:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:13:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:13:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 24 Feb 2026 19:13:07 GMT
ENV PHP_VERSION=8.3.30
# Tue, 24 Feb 2026 19:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 24 Feb 2026 19:13:07 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 24 Feb 2026 19:13:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:13:16 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:17:10 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:17:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:17:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:17:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:17:11 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:17:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:17:11 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:17:11 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:17:11 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 20:19:09 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 24 Feb 2026 20:19:09 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 24 Feb 2026 20:19:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:21:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 24 Feb 2026 20:21:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:21:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 24 Feb 2026 20:21:52 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 24 Feb 2026 20:21:52 GMT
VOLUME [/var/www/html]
# Tue, 24 Feb 2026 20:21:52 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 24 Feb 2026 20:21:52 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 24 Feb 2026 20:21:53 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 24 Feb 2026 20:21:53 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:21:53 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 24 Feb 2026 20:21:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:21:53 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ad5734082a82505fdc07a9a3d1f809491aa3f8ecfbb12367a73db36a563f4a`  
		Last Modified: Tue, 24 Feb 2026 19:12:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d335fe715d847e45f7d78922d27f3ca59412f105cf983c004d9163804c51ae9`  
		Last Modified: Tue, 24 Feb 2026 19:12:53 GMT  
		Size: 110.2 MB (110163243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59815db09cb1ca6507343edc11941c4650f455f93b70c3985bd9e1c43f3fb0fa`  
		Last Modified: Tue, 24 Feb 2026 19:12:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0049a8a24a7454a0d92831e14bac5651497b50361519e45d50683b6e538ddaf`  
		Last Modified: Tue, 24 Feb 2026 19:17:22 GMT  
		Size: 4.3 MB (4304880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440e52a2fcb90aabae3101785ded07c19a82911f599db98f20cab5bb29b39bfc`  
		Last Modified: Tue, 24 Feb 2026 19:17:22 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4606afd4e20accf98575b0e1946846ad8b349ba99cd702123d72379787088e1c`  
		Last Modified: Tue, 24 Feb 2026 19:17:22 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16adb7ff87b49008a37b047f49a8935fe538a9481c574b5b3e6bab999f5180`  
		Last Modified: Tue, 24 Feb 2026 19:17:22 GMT  
		Size: 12.8 MB (12774002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108d7fec58c451298a2fa1b1655ae774419d916f08903bc7dfc1dc56bb525e03`  
		Last Modified: Tue, 24 Feb 2026 19:17:23 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc36f20612d6436200dc4ed9f5a5816c25e9d79f1b4ef2c3b6d8a0cb1fa1cad`  
		Last Modified: Tue, 24 Feb 2026 19:17:23 GMT  
		Size: 11.7 MB (11732757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7f6f956bf472cb306409c0843685221f395b4fd12cb56bb221624100639941`  
		Last Modified: Tue, 24 Feb 2026 19:17:23 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d8cf8276257a51db054871267dc15aae7dc4e734f4be3eea82523d032b7447`  
		Last Modified: Tue, 24 Feb 2026 19:17:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6225eff16eb05c2ee20e7610ee3e19469d067259fa3a0782239c305283d7ef`  
		Last Modified: Tue, 24 Feb 2026 19:17:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d7ba8d7e581d6f371b629e0bce6e816045fc6c8734b0b0353a3bee7a9946fe`  
		Last Modified: Tue, 24 Feb 2026 19:17:24 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8fc5d8f322e4de5130cdff5793c977d2d196946674861f183b06faf8991f42`  
		Last Modified: Tue, 24 Feb 2026 20:22:03 GMT  
		Size: 27.1 MB (27100088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc225d216dd121e3b6fd3c77377d0f2c3cca18b5a2011bdd82b6ae078daeb4f2`  
		Last Modified: Tue, 24 Feb 2026 20:22:03 GMT  
		Size: 43.9 MB (43919700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e35893456be58d343555a12d01765e417d17a7e237b4dc761e6baa0d468d9`  
		Last Modified: Tue, 24 Feb 2026 20:22:02 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a91dea3cd0d15a25f85492aee2de0a14bd4523ca5f20e833510ad94f273ab3`  
		Last Modified: Tue, 24 Feb 2026 20:22:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f378c18aefa20569fd1b220e15ff8525974f5d5f97c4d139307c3b56b34acf`  
		Last Modified: Tue, 24 Feb 2026 20:22:03 GMT  
		Size: 18.8 KB (18798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee4976f490ee104bcd5bd298b1a530aa0c3830cd366ac3703bbb639cd461c84`  
		Last Modified: Tue, 24 Feb 2026 20:22:04 GMT  
		Size: 26.4 MB (26428227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b071d4cc619eaba6fcc04723a9663bba77a5a22a361c76fbb8da88033b93912`  
		Last Modified: Tue, 24 Feb 2026 20:22:04 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d67b65ef8d0750e804c7f2345b77d3c45018e5fbf91893de33974eed3ba8a`  
		Last Modified: Tue, 24 Feb 2026 20:22:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:13621f401baf0e15821aedbfcfc07045ec38a274eba8660b158b9c11461e71ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.0 KB (57959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1c98208f768908a869ea225a2479ec77e5ec5726c3336edbe9172dfae41087`

```dockerfile
```

-	Layers:
	-	`sha256:6e29d581242c735ed37f97f20666401ae1c1a9d04b4dcae7457490ac5691474b`  
		Last Modified: Tue, 24 Feb 2026 20:22:01 GMT  
		Size: 58.0 KB (57959 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; 386

```console
$ docker pull joomla@sha256:3e30732fa022645f6ed2eff7ca62c6b4bec749dd90f65c03b60b291106e0feba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275997764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c733e738face534fd06fe9965ee39f4b78de97caecd87527e2d92c10790e3e22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:36 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:06:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:06:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:06:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:06:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:06:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:06:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:07:01 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:07:02 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:07:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:07:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:07:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:07:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 24 Feb 2026 19:07:02 GMT
ENV PHP_VERSION=8.3.30
# Tue, 24 Feb 2026 19:07:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 24 Feb 2026 19:07:02 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 24 Feb 2026 19:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:07:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:10:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:07 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 19:10:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:10:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:10:07 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:10:07 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:10:07 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:10:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:10:07 GMT
CMD ["apache2-foreground"]
# Tue, 24 Feb 2026 20:01:32 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 24 Feb 2026 20:01:32 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 24 Feb 2026 20:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 24 Feb 2026 20:03:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 24 Feb 2026 20:03:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 24 Feb 2026 20:03:57 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 24 Feb 2026 20:03:57 GMT
VOLUME [/var/www/html]
# Tue, 24 Feb 2026 20:03:57 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 24 Feb 2026 20:03:57 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 24 Feb 2026 20:03:59 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 24 Feb 2026 20:03:59 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:03:59 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 24 Feb 2026 20:03:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:03:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ef93648aea785872a8cb172b5b4af034f97df51bf8b7b13e1f511b0eb98867`  
		Last Modified: Tue, 24 Feb 2026 19:10:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af13035895ca46934b09799e4b0cb4293aa0b063a1ea76cebe277b975906b4`  
		Last Modified: Tue, 24 Feb 2026 19:10:32 GMT  
		Size: 116.1 MB (116144732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a599a67270ab8124cdbf9a141da8ee8a158cdebb9e79ef779ebbc681a1fdac94`  
		Last Modified: Tue, 24 Feb 2026 19:10:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2f77f58a165a3cecd9d06440240d851ae287bc72735e0a6b5953ba0a3e528`  
		Last Modified: Tue, 24 Feb 2026 19:10:28 GMT  
		Size: 4.5 MB (4458313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595d47e4f26fb67e0553b785fb67267d5406a283abcbcc5f56309e5a0e16e6e5`  
		Last Modified: Tue, 24 Feb 2026 19:10:29 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d46f5746b62672bfa32ebf6d971737a1cb12dc4a0185c7ab45f45c26b689f18`  
		Last Modified: Tue, 24 Feb 2026 19:10:29 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85471c26395209c41a65b8df0861cf962465f5f7fa11ebdde4cfa8c1ac41f17b`  
		Last Modified: Tue, 24 Feb 2026 19:10:30 GMT  
		Size: 12.8 MB (12773445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637ce7955a1bfb4fe4728a06c28403513ea3ab420a8b4299f99debf6e972726`  
		Last Modified: Tue, 24 Feb 2026 19:10:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1f0dd47e1ff0a0080ca339fd0edd8caa89777414982f85274cb69b29640efb`  
		Last Modified: Tue, 24 Feb 2026 19:10:31 GMT  
		Size: 11.9 MB (11924259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e0216a651cc36c27e50a7c1cb83755a2dcf19bad9d52486af64d9b22ffc144`  
		Last Modified: Tue, 24 Feb 2026 19:10:31 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120639016940bf575ede416f324583162229c9f9133b6b84bc181c0fdd4de157`  
		Last Modified: Tue, 24 Feb 2026 19:10:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb8e34dc1e8d14221479008b6a64b421fc5285d31007fffbaab16e6b15065b5`  
		Last Modified: Tue, 24 Feb 2026 19:10:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bf3ff02d12a4f43984c0752a0e3772f8b5d7b21810a29d09a108ef80d2bcc9`  
		Last Modified: Tue, 24 Feb 2026 19:10:33 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa4285548f7d07ecb3f42ec6877d36ddcfc5ac4d902745807315e102b19f34`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 27.7 MB (27715776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ebf9547436f1135870b1c0d26023c2e00673efb11a66c221b7db9d204b8287`  
		Last Modified: Tue, 24 Feb 2026 20:04:10 GMT  
		Size: 45.2 MB (45229109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d7e119111c8088f6672be5ce34ffbdea5984c5d5ee6c9ea94477a4dc2c5808`  
		Last Modified: Tue, 24 Feb 2026 20:04:08 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd6a0ab47e84994de5578f0ac0a8247880489fa943731d1b4414b051fe215cb`  
		Last Modified: Tue, 24 Feb 2026 20:04:08 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3bd5521a5e7eb862b6f641b1c0ef3cd402760cead4f9afbecc73cbb9a1339d`  
		Last Modified: Tue, 24 Feb 2026 20:04:09 GMT  
		Size: 18.8 KB (18817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35278c15d7afbd6726782c39d92a27c82af5159b46b6d4fb05142359e17cf3db`  
		Last Modified: Tue, 24 Feb 2026 20:04:10 GMT  
		Size: 26.4 MB (26428225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a35e6043da4f5ebff95a285100aa19d4a6f271d6b46bc45fb2217244a58284`  
		Last Modified: Tue, 24 Feb 2026 20:04:10 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc940d1cfd403c408944b4b702e2d9316887a1e6a0633bcfac00f3d0b576c0c3`  
		Last Modified: Tue, 24 Feb 2026 20:04:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:9990c3ca70aec58fbf53118e045176e7681d41f6a2684653c5bc1848f72e34cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 KB (57739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c365d6ce006fad91a540bc7fbd10171e8626cdde71f1863bb12119a16983f55d`

```dockerfile
```

-	Layers:
	-	`sha256:728b57c427202de6c2e104813c5724661fa7e9d684f2ebf658d46c783ca9886c`  
		Last Modified: Tue, 24 Feb 2026 20:04:07 GMT  
		Size: 57.7 KB (57739 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; ppc64le

```console
$ docker pull joomla@sha256:2dfe10e31cda56dbcbfaff892bd7f5d6ecbfa62402c50f4004fac29050e94ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274635409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627beb7439901f8e409b47a8e5c9fe94d01766bd566f20238c22799f92a36f9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:47:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:47:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:47:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:47:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:48:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:48:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 04:20:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 04:20:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:25:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 04:25:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:25:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 04:25:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 04:25:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 04:25:32 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 04:25:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 04:25:34 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 04:25:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 04:25:34 GMT
CMD ["apache2-foreground"]
# Wed, 18 Feb 2026 00:22:21 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 18 Feb 2026 00:22:21 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 18 Feb 2026 00:22:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 00:28:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 18 Feb 2026 00:28:19 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Feb 2026 00:28:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 18 Feb 2026 00:28:21 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 18 Feb 2026 00:28:21 GMT
VOLUME [/var/www/html]
# Wed, 18 Feb 2026 00:28:21 GMT
ENV JOOMLA_VERSION=6.0.3
# Wed, 18 Feb 2026 00:28:21 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Wed, 18 Feb 2026 00:28:25 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 18 Feb 2026 00:28:26 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Feb 2026 00:28:27 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 18 Feb 2026 00:28:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Feb 2026 00:28:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5aef540a1dbd10111c40eb7d9fc2480005c3fd8d164979371878603dac2854`  
		Last Modified: Tue, 03 Feb 2026 02:53:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282dc5cdeff5e017f78b0496f224050268f625b87ef7cefd7cdd16e6abf1d723`  
		Last Modified: Tue, 03 Feb 2026 02:53:17 GMT  
		Size: 109.6 MB (109597358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f41d4ecbf32a9e015fc638210e66283419cedac7dd29494bd26c767c870b92`  
		Last Modified: Tue, 03 Feb 2026 02:53:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b9ee345db4a78acffafdd3238a5dca1e196b0a4b0820239c3b77306dfc411`  
		Last Modified: Tue, 03 Feb 2026 02:54:27 GMT  
		Size: 4.9 MB (4881260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214b31dd46127f293476e70fcf6aebc429b886d623edf3762ae804c6607a6c5`  
		Last Modified: Tue, 03 Feb 2026 02:54:27 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a1e19e97031950f9a8cb1af296b4ff35ee053b50f2f569235ee2442575edd8`  
		Last Modified: Tue, 03 Feb 2026 02:54:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35607e9aeb01590002e2fa6b014f49ace7a2fd3d123fabaf82f0bee53de4e187`  
		Last Modified: Tue, 03 Feb 2026 04:26:00 GMT  
		Size: 12.8 MB (12782739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e1592126c72c855a94ddb28d5a1afae8e207bc559a84fb37d658a3f6ef9e84`  
		Last Modified: Tue, 03 Feb 2026 04:25:59 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67bd3662b3752fef6abea85e0ba903da5c8248d684f8c5e5e23f8b14cd22066`  
		Last Modified: Tue, 03 Feb 2026 04:26:00 GMT  
		Size: 12.1 MB (12122038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a01e4a8943bee1e08c8899bf7334b3848e0e2fea70bce00e3ee106319f98d9b`  
		Last Modified: Tue, 03 Feb 2026 04:25:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa86ecbf974cc40e97a3d1052e0389db8879f9d40f3431757687619bc7d8c4f`  
		Last Modified: Tue, 03 Feb 2026 04:26:00 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da322673a33d71eddc4353b49614423427693bd937ef9c04684dd26273a1242b`  
		Last Modified: Tue, 03 Feb 2026 04:26:00 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44de9263b994115c104bb97c66f994655d5690fdf1a7a9d376f00050c321d4c6`  
		Last Modified: Tue, 03 Feb 2026 04:26:01 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d516bf6446bd8a7804f0286e32bc343c30daad979df659e9d17e733ec5f0d69a`  
		Last Modified: Wed, 18 Feb 2026 00:28:48 GMT  
		Size: 28.4 MB (28418799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6a7a7973a8a6ed2a2e834d14f4c75388a14f01c36a0083158055d3c0f0ab9`  
		Last Modified: Wed, 18 Feb 2026 00:28:48 GMT  
		Size: 46.8 MB (46774769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127d3bc8eb7f577a775a3054d40bd1e9173ea9bfef3ae0c934050d7d42545031`  
		Last Modified: Wed, 18 Feb 2026 00:28:47 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c324a4af370685176f65ed9c44c81e0cd8e7f68590031985c49c9cefe7a785`  
		Last Modified: Wed, 18 Feb 2026 00:28:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf5ac4bade5d0e33bd97fd50603f8f4b96e36fbe2a96bd1701138ef44c5db05`  
		Last Modified: Wed, 18 Feb 2026 00:28:48 GMT  
		Size: 18.8 KB (18810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4009fe214e549b932322a89d64ef016c98f90c4a5dc3b86ef0a8a1f6c6da7a34`  
		Last Modified: Wed, 18 Feb 2026 00:28:49 GMT  
		Size: 26.4 MB (26428261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2108891c9a75fb05bb9f080df2d313b93c09de7224d74a1ca8b538f28486f302`  
		Last Modified: Wed, 18 Feb 2026 00:28:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba3cd36f393e16d38b94f776f7e8989de09cea8310bf8f901057635dd48cb99`  
		Last Modified: Wed, 18 Feb 2026 00:28:49 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:4a798eb8ebccae562aa4e5097be6c9020500bfc591cc7592ad31b820c0430a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 KB (57835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c603e824e33f80fe97bcccc2e8852bec122cd723914c8225871030b51d90949`

```dockerfile
```

-	Layers:
	-	`sha256:64e33df049ba1af3a730dc400c60be7e651798daec7b53a64b98deb2141a0069`  
		Last Modified: Wed, 18 Feb 2026 00:28:46 GMT  
		Size: 57.8 KB (57835 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; riscv64

```console
$ docker pull joomla@sha256:5a1c55c697758a0b53339ece67d75aaaa3cafd93ea3f3d56aff22f0b3f36b42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309282802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c44c088545d3adc3697d89c2c1eef0acff21b35b63c8f65bd9891dd2196a91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 17:08:39 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 17:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 17:10:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 17:10:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 17:10:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 17:10:42 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 17:10:42 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 18:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 18:15:47 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 18:15:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 18:15:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 04 Feb 2026 10:13:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 04 Feb 2026 10:13:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 04 Feb 2026 11:04:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 04 Feb 2026 11:04:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 04 Feb 2026 11:04:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 04 Feb 2026 11:04:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 04 Feb 2026 11:04:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Feb 2026 11:04:10 GMT
STOPSIGNAL SIGWINCH
# Wed, 04 Feb 2026 11:04:10 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 04 Feb 2026 11:04:11 GMT
WORKDIR /var/www/html
# Wed, 04 Feb 2026 11:04:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 04 Feb 2026 11:04:11 GMT
CMD ["apache2-foreground"]
# Wed, 18 Feb 2026 00:35:58 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 18 Feb 2026 00:35:58 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 18 Feb 2026 00:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 01:02:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 18 Feb 2026 01:02:45 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 18 Feb 2026 01:02:45 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 18 Feb 2026 01:02:46 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 18 Feb 2026 01:02:46 GMT
VOLUME [/var/www/html]
# Wed, 18 Feb 2026 01:02:46 GMT
ENV JOOMLA_VERSION=6.0.3
# Wed, 18 Feb 2026 01:02:46 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Wed, 18 Feb 2026 01:02:58 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 18 Feb 2026 01:02:59 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Feb 2026 01:02:59 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 18 Feb 2026 01:02:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Feb 2026 01:02:59 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a0c7bf9985f7aa3278051e22de8b2e25e48b9247e1f8ee94b0580a41f8dbf`  
		Last Modified: Tue, 03 Feb 2026 18:13:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c308411999737082a164f0c80e801b9bba1f870be1efa26fb715f1dd002ad6b0`  
		Last Modified: Tue, 03 Feb 2026 18:14:01 GMT  
		Size: 146.6 MB (146578579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8ed6ff919b7995bbffcb5df8a9d82dfddafe0ad63dc244974287839a83ee2`  
		Last Modified: Tue, 03 Feb 2026 18:13:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c39a123fee7384a8e42dd0131ab0dec5b9cbf76fa8ed14a529fbebc60ac424`  
		Last Modified: Tue, 03 Feb 2026 19:16:24 GMT  
		Size: 4.0 MB (4031154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c78bb3209b3345dbe74ef17fe714509c869fb02bc4a3474afe127ff1263cb7`  
		Last Modified: Tue, 03 Feb 2026 19:16:22 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad8722119dcebc8afef8a1229503e5323ae32e648b97a65ea37d1bb92e48eee`  
		Last Modified: Tue, 03 Feb 2026 19:16:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf881cd41273eb490614e51515b852663dda8e63b11a0f22d98f819918408171`  
		Last Modified: Wed, 04 Feb 2026 11:07:19 GMT  
		Size: 12.8 MB (12789155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1d5ceac248cdbce8c18148ed0fe47ba659ca9c498372a91d7b8b31de1682f`  
		Last Modified: Wed, 04 Feb 2026 11:07:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe7d74cb5b2648a451622ac9ee355d95430d9f726acb671c9bba9462ffa24d`  
		Last Modified: Wed, 04 Feb 2026 11:07:19 GMT  
		Size: 11.3 MB (11253021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38432fcb9f0d32a84eef24df7e6cc00c15a83538e7ca178ecb3916e985688f6f`  
		Last Modified: Wed, 04 Feb 2026 11:07:15 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0d76941894159fd8818f14ea6cea822e79ac148586f81a18d02dcede6123fe`  
		Last Modified: Wed, 04 Feb 2026 11:07:17 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f9f5ece76783630acb1ed061a2e10a58cb2d013d2706ddf6f57678ff84c96d`  
		Last Modified: Wed, 04 Feb 2026 11:07:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f18dd00d5e59db69b7f22fde8eb0361fd76b6942e15d4cf802ca85d3bbd83f`  
		Last Modified: Wed, 04 Feb 2026 11:07:19 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9107666fc33e107fcbee2118cb8a2fbc235ce1c945b65bdffebb06bb1790392`  
		Last Modified: Wed, 18 Feb 2026 01:05:21 GMT  
		Size: 27.2 MB (27208974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90a4cc29654976a1881e067a1c87218a6ade3c2226f0a2777fce1fee2dc03b2`  
		Last Modified: Wed, 18 Feb 2026 01:05:26 GMT  
		Size: 52.7 MB (52687308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55066743d9af8e4749533b85efc59dad9bcca96e82f72c88944b5cfd2403f765`  
		Last Modified: Wed, 18 Feb 2026 01:05:09 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df997d7db337612cda847b4f7a978cbcde6d2341e842e3d5909658696f64e1e7`  
		Last Modified: Wed, 18 Feb 2026 01:05:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bf2cde24897c366aeaea87013c8f89245f81156f6c983c1ec976c8c9aefa3b`  
		Last Modified: Wed, 18 Feb 2026 01:05:11 GMT  
		Size: 18.8 KB (18810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff5acedaed46626a07bba7dfe530d574afe613acba52c059b76d920ca51145`  
		Last Modified: Wed, 18 Feb 2026 01:05:22 GMT  
		Size: 26.4 MB (26428213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23b40c776e2188b6c2ad8df5676bd9e7a3c0985ca9c4abc8cf2bbcce8b641b`  
		Last Modified: Wed, 18 Feb 2026 01:05:14 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3410c2931e6413af62eb121af4e81be7b248b23c3848acbd152acbc7a98df32b`  
		Last Modified: Wed, 18 Feb 2026 01:05:17 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:e48f637cb6bef8c51df88d464946fc5c413ef14c1be5f8a01031d2cbb96ef1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 KB (57835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d130bc8d4a31632013ec6248591666a08020619548ceb583a9f244d210952574`

```dockerfile
```

-	Layers:
	-	`sha256:75d80ed0914158325459309cd3ab3649a7fd776f2c3837dc113d5d13d619f4a0`  
		Last Modified: Wed, 18 Feb 2026 01:05:09 GMT  
		Size: 57.8 KB (57835 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-apache` - linux; s390x

```console
$ docker pull joomla@sha256:c8ea42ddd21000a533e79db2988193596fe1f0a3218a002d15a6be79856f0b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249631910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896d51ae8496cec1e2c819453469e0c87824bd8031cba2e82c25e3f6a1c2be96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:26:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:26:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:26:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:26:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:26:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:26:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 03 Feb 2026 02:43:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 03 Feb 2026 02:43:34 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 03 Feb 2026 02:43:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 03 Feb 2026 02:43:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_VERSION=8.3.30
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Tue, 03 Feb 2026 02:57:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 03 Feb 2026 02:57:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:00:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 03 Feb 2026 03:00:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:00:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 03 Feb 2026 03:00:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 03 Feb 2026 03:00:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 03 Feb 2026 03:00:02 GMT
STOPSIGNAL SIGWINCH
# Tue, 03 Feb 2026 03:00:02 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:00:02 GMT
WORKDIR /var/www/html
# Tue, 03 Feb 2026 03:00:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 03 Feb 2026 03:00:02 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 22:22:42 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 22:22:42 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 22:22:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:28:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.27; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 22:28:04 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 22:28:05 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 22:28:06 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 22:28:06 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 22:28:06 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 22:28:06 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 22:28:10 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 22:28:11 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:28:11 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 22:28:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 22:28:11 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549210c719d320a22b8bf177acb816a6d0a7f20e7093e59116bfeb44e7274e77`  
		Last Modified: Tue, 03 Feb 2026 02:29:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4813f2bd608dbd0dbe552bceb021d2482736af40cc9da0ca38931df91ac57db`  
		Last Modified: Tue, 03 Feb 2026 02:29:44 GMT  
		Size: 92.6 MB (92567360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda8f1dea52189d07742c4c8d84b6cf3d696d06f26442e2c14c0f3086587f6fb`  
		Last Modified: Tue, 03 Feb 2026 02:29:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baec2b933c384a809885e8b3077c0420df3bbadca2b7beb36d95bdf00206a0c5`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 4.3 MB (4329021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e241fc83a7431cffad00a35fc2c23374748fe912e3e887aa2757fc5555e14`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755e5d79ba50ae9db70a3b883777ee7d316750ea9f046a741f7f5a162f4f59d`  
		Last Modified: Tue, 03 Feb 2026 02:46:40 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffc99e984b97479815798ccb37bbe99214a55e73f503403a08384eec46c0540`  
		Last Modified: Tue, 03 Feb 2026 03:00:22 GMT  
		Size: 12.8 MB (12781812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dabd7b7f341e59320b95add1c014128e70d71c34458332de2b9c2dda92835a`  
		Last Modified: Tue, 03 Feb 2026 03:00:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3cf4eefc706c13c002dcff31a2597e61e95f13c3e0a71afa8f61d081a3e058`  
		Last Modified: Tue, 03 Feb 2026 03:00:22 GMT  
		Size: 11.6 MB (11571452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809424feb6c744c32372d3d7a0127a078272b750fb5534292d58370dc463d05`  
		Last Modified: Tue, 03 Feb 2026 03:00:22 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a8cb2a9282668b5432fd61333c2940501f535b80188f5b78810d3ee64c0021`  
		Last Modified: Tue, 03 Feb 2026 03:00:23 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a4418de2ea91021b1cc344cf0a6d304cf9b7ed1ca36d667ba3ad7841c2410d`  
		Last Modified: Tue, 03 Feb 2026 03:00:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fabf6e95d4d4368c80109af0c1be26cc51a3398fade8f232a03996b54d105`  
		Last Modified: Tue, 03 Feb 2026 03:00:24 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52657e8de1658319ac1e81f72fee7f6996baec028473b0ac58227e0c2c687f78`  
		Last Modified: Tue, 17 Feb 2026 22:28:30 GMT  
		Size: 27.6 MB (27551902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f3ac244471450b69d2caef1138ed23542e995e6b9aba7ce05df3ccdf6feda2`  
		Last Modified: Tue, 17 Feb 2026 22:28:31 GMT  
		Size: 44.5 MB (44534013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212c5abbf25018c10d991cbd85e984792e4ef513d5e1ec23f7d53ea5cf234505`  
		Last Modified: Tue, 17 Feb 2026 22:28:29 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5112dffbcd57c11eab66424f869563283606fe0ec894bfc7a3a9d7c87b69cec6`  
		Last Modified: Tue, 17 Feb 2026 22:28:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e44948ceb35a636b6c6699b9c40e8c98cda2c6b32b11c8523d12ae2510f674a`  
		Last Modified: Tue, 17 Feb 2026 22:28:30 GMT  
		Size: 18.8 KB (18806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735a05d3244123a39cb6ba001dbc0c8aa65ccc847742f3c37c549cc33e0e6367`  
		Last Modified: Tue, 17 Feb 2026 22:28:31 GMT  
		Size: 26.4 MB (26428203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaabdde3113d17c44155a1cabc503aa8a12a3f599d46deea9f48e470a175bde`  
		Last Modified: Tue, 17 Feb 2026 22:28:31 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d5254bc5f26e2bf8d32e675c28c1cbb93bcd68328b747bf4dd9d681f2142e`  
		Last Modified: Tue, 17 Feb 2026 22:28:32 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-apache` - unknown; unknown

```console
$ docker pull joomla@sha256:1bb812c313b529792e8001e7bffab4711573299bdcc4365e5332f61ade584956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 KB (57772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01b3a73a28ca6ae51f40deec5d4ac1a36310bad9979dd17e933e68a0443fc91`

```dockerfile
```

-	Layers:
	-	`sha256:b731a53510ae3f10ac1a76d336980e5f5ea7bdb3d8bf41295701ee0fbb099e90`  
		Last Modified: Tue, 17 Feb 2026 22:28:28 GMT  
		Size: 57.8 KB (57772 bytes)  
		MIME: application/vnd.in-toto+json
